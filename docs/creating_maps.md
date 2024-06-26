# Creating Maps

In this section, we’ll create a Map using some uploaded datasets, combine them with some other datasets from remote web services, and then share the resulting map for public viewing.

In order to create new maps you can use:

    The Create map listed after clicking the Add Resource button on the All Resources list page.

    The New button after clicking the Maps button on the menu bar.

    The Create map link in the Dataset Page (it creates a map using a specific dataset)

The new Map will open in a Map Viewer like the one in the picture below.


Using the Add dataset link, you can add a layer by clicking on one of the layers listed in the catalog. In the upper left corner the TOC button button opens the Table of Contents (TOC) of the Map. It allows to manage all the datasets associated with the map and to add new ones from the Add dataset. The TOC component makes possible to manage datasets overlap on the map by shifting their relative positions in the list (drag and drop them up or down in the list). It also allows to hide/show datasets ( show_button and hide_button ), to zoom to datasets extents ( zoom_to_dataset_extent_button ) and to manage their properties ( dataset_settings_button ). Once the map datasets have been settled it is possible to save the Map by clicking on the Save as under the Resources link in the map toolbar.


Map tools and configuration

In this section, we are going to explore all tools provided on the Map View page. From the list of available maps, you can select the map you are interested in and click View map, the map will look like this.


The Map View (based on MapStore) provides the following tools:

    the Table of Contents (TOC) to manage the map contents;

    the Basemap Switcher to change the basemap ();

    the Search Bar to search by location, name and coordinates ();

    the Other Menu Tools which contains the link to the datasets Catalog;

    the Sidebar which contains, by default, the link to the Print tool and to the Measure tool;

    the Navigation Bar and its tools such as the Zoom tools, the 3D Navigation tool and the Get Features Info tool;

    the Footer Tools to manage the scale of the map, to track the mouse coordinates and change the CRS (Coordinates Reference System).

A map can be configured to use a custom Map Viewer, with which the lsit of tools available in the map can be customized.


Search Bar

The Search Bar of the map viewer allows you to find point of interests (POIs), streets or locations by name.
Lets type the name of some place then select the first record. 


Navigation bar
The Map Viewer makes also available the Navigation bar. It is a navigation panel containing various tools that help you to explore the map such as tools for zooming, changing the extent and querying objects on the map.
By default the Navigation bar shows you the zooming buttons zoom_in_button, zoom_out_button and 3d_button, other options can be explored by clicking on sidebar_expand_button which expands/collapses the toolbar.|


The Navigation bar contains the following tools:

    The Query Objects on map allows you to get feature information through the query_objects_on_map_button button. It allows you to retrieve information about the features of some datasets by clicking them directly on the map.

    When clicking on map a new panel opens. That panel will show you all the information about the clicked features for each active loaded dataset.


Maps Metadata

Maps Metadata can be Edited by clicking the Edit Metadata link from the Map Detail page.

The Map Metadata Edit form will open. Metadata provide essential information for the identification and the comprehension of the map. They also make the map more easily retrievable through the search tools. Those Metadata can be filled out through three-steps in which you have to provide all mandatory information to complete the process. Those three steps are described below.

In the first step the system asks you to insert the following metadata (required fields are highlighted with red outlines):

- Basic Metadata

    Thumbnail of the map (click Edit to change it);

    Title of the map, which should be clear and understandable;

    Abstract; brief narrative summary of the content of the Map

    Creation/Publication/Revision Dates which define the time period that is covered by the map;

    Keywords, which should be chosen within the available list;

    Category which the map belongs to;

    Group which the map is linked to.

- Location and Licenses

The following list shows what kinds of metadata you are required to enter (see also the picture below):

    Language of the layer;

    License of the dataset;

    Regions covered by the layers extent. Proposed extents cover the following scales: global, continental, regional, national;

    Data Quality statement (general explanation of the data producer’s knowledge about the lineage of a dataset);

    Potential Restrictions on layer sharing.

No further mandatory metadata are required in the next step so, once the required fields have been filled out, a green Done button will be visible in the screen. Click Next >> to go to the next step or << Back to go back to the previous step.

- Optional Metadata
    Complementary information are:

        Edition of the map;

        Purpose of the map and its objectives;

        Supplemental information that can provide a better understanding of the map;

        Maintenance frequency of the map;

        Spatial representation type, the method used to represent geographic information in the dataset;

        Users who are Responsible for the layer, its Owner, and the Author of its metadata;

        Related resources to link one or multiple resources to the document. These will be visible inside the Map Information panel

If you miss some mandatory metadata the Completeness bar shows you a red message.





Share Options

In GeoNode the share options management system is indeed more complex. Administrators can choose who can do what for each map. Users can manage only the maps they own or the maps which they are authorize to manage.

By default only owners can edit and manage maps, and anyone can view them.

In order to modify the Map Share Options settings you can click the Share link in the Map Detail Page.

Through the Share Options Settings Panel you can add or remove options for users and groups. The picture below shows an example.



You can set the following options:

    View (allows to view the map).

    Download (allows to view and download the map).

    Edit (allows to change the map’s metadata);

    Manage allows to update, delete, change share options, publish and unpublish the map.


Click on Save link in the menu to save these settings.