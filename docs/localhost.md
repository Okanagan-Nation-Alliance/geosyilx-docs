# Installing

## Under localhost

### System Requirements
- **Software:**
  - Python 3.8+
  - PostgreSQL 13+
  - PostGIS 2.1+
  - GDAL 1.10+
  - Node.js
- **Hardware:**
  - Minimum 2 GB RAM
  - 2 GHz dual-core CPU
  - 20 GB free disk space

### Installation Steps
**Install Dependencies:**

```
    sudo apt install -y --allow-downgrades build-essential \
    python3-gdal=3.4.1+dfsg-1build4 gdal-bin=3.4.1+dfsg-1build4 libgdal-dev=3.4.1+dfsg-1build4 \
    python3-all-dev python3.10-dev python3.10-venv virtualenvwrapper \
    libxml2 libxml2-dev gettext libmemcached-dev zlib1g-dev \
    libxslt1-dev libjpeg-dev libpng-dev libpq-dev \
    software-properties-common build-essential \
    git unzip gcc zlib1g-dev libgeos-dev libproj-dev \
    sqlite3 spatialite-bin libsqlite3-mod-spatialite libsqlite3-dev
```
    
**Install Openjdk**
```
    sudo apt install openjdk-11-jdk-headless default-jdk-headless -y
```

    **Verify GDAL version**
```
    gdalinfo --version
    $> GDAL 3.4.1, released 2021/12/27
```

    
**Verify versions version**

```
    python3.10 --version
```
$> Python 3.10.4
```
    which python3.10
```
$> /usr/bin/python3.10
```
    java -version
```
$> openjdk version "11.0.16"
```
    sudo apt install -y vim
```
```
    sudo apt update -y; sudo apt autoremove --purge

```


**Setup PostgreSQL Database:**
```sh
    sudo -u postgres createuser -D -A -P geonode
    sudo -u postgres createdb -O geonode geonode
    sudo -u postgres psql -d geonode -c 'CREATE EXTENSION postgis;'
    sudo -u postgres psql -d geonode -c 'GRANT ALL ON geometry_columns TO PUBLIC;'
    sudo -u postgres psql -d geonode -c 'GRANT ALL ON spatial_ref_sys TO PUBLIC;'
    sudo -u postgres psql -d geonode -c 'GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO geonode;'
    sudo -u postgres psql -d geonode -c 'GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA public TO geonode;'

    sudo -u postgres psql -d geonode_data -c 'CREATE EXTENSION postgis;'
    sudo -u postgres psql -d geonode_data -c 'GRANT ALL ON geometry_columns TO PUBLIC;'
    sudo -u postgres psql -d geonode_data -c 'GRANT ALL ON spatial_ref_sys TO PUBLIC;'
    sudo -u postgres psql -d geonode_data -c 'GRANT ALL PRIVILEGES ON ALL TABLES IN SCHEMA public TO geonode;'
    sudo -u postgres psql -d geonode_data -c 'GRANT ALL PRIVILEGES ON ALL SEQUENCES IN SCHEMA public TO geonode;'
```

**Clone the GeoNode Repository:**
```sh
    sudo mkdir -p /opt/geonode/; sudo usermod -a -G www-data $USER; sudo chown -Rf $USER:www-data /opt/geonode/; sudo chmod -Rf 775 /opt/geonode/
    cd /opt; git clone https://github.com/GeoNode/geonode.git -b 4.2.x geonode
```

**Create and Activate a Virtual Environment:**
```sh
    export WORKON_HOME=~/.virtualenvs
    source /usr/share/virtualenvwrapper/virtualenvwrapper.sh
    mkvirtualenv --python=/usr/bin/python3.10 geonode
```

**Install Python Dependencies:**
```sh
    pip install -r requirements.txt
    pip install -e .
```

**Configure GeoNode:**
    Edit the env_local and settings.py files accordingly

**Initialize the Database:**
```sh
    python manage.py makemigrations
    python manage.py migrate
```

**Create a Superuser:**
```sh
    python manage.py createsuperuser
```

**Run the Development Server:**
```sh
    python manage.py runserver
```

