# Datasets Uploading

The most important resource type in GeoNode is the Dataset. A dataset represents spatial information so it can be displayed inside a map.
To better understand what we are talking about lets upload your first dataset.

It is possible to upload a Datasets in two ways:

   From the All Resources page, by clicking Add Resource which displays a list including Upload dataset link:



   From the Datasets page, by clicking on New which displays a list including Upload dataset link:


On the next page:

Through the Select files button you can select files from your disk, make sure they are valid raster or vector spatial data, then you can click to Upload button.

A progress bar shows the operation made during the dataset upload and alerts you when the process is over.



In this example the ONA_Territory ESRI Shapefile, with all its mandatory files (.shp, .shx, .dbf and .prj), has been chosen. When the process ends click on View button

The dataset view will open, where you can click the edit>edit metadata button to edit the metadata for the dataset.


Editing Metadata
Metadata contains all the information related to the dataset. They provide essential information for its identification and its comprehension. Metadata also make the dataset more easily retrievable through search by other users.

The Metadata of a dataset can be changed through a Edit Metadata form which involves four steps, one for each type of metadata considered:

You can open the Metadata form of a Dataset by clicking the Edit Metadata link from the Edit options on the Dataset Page.

   - Basic Metadata

      The first two steps are mandatory (no datasets will be published if the required information are not provided) whereas the last two are optional.


      In the first step the system asks you to insert the following metadata:

         Thumbnail of the dataset (click Edit to change it);

         Title of the dataset, which should be clear and understandable;

         Abstract; brief narrative summary of the content of the dataset

         Creation/Publication/Revision Dates which define the time period that is covered by the dataset;

         Keywords, which should be chosen within the available list. The contributor search for available keywords by clicking on the searching bar, or on the folder logo representing, or by entering the first letters of the desired word;

         Category which the dataset belongs to;

         Group which the dataset is linked to.
   
   - Location and Licenses

      The following list shows what kinds of metadata you are required to enter (see also the picture below):

         Language of the dataset;

         License of the dataset;

         DOI of the dataset; if available, this represents the Digital Object Identifier of the resource

         Attribution of the dataset; authority or function assigned, as to a ruler, legislative assembly, delegate, or the like

         Regions, which informs on the spatial extent covered by the dataset. Proposed extents cover the following scales: global, continental, regional, national;

         Data Quality statement (general explanation of the data producer’s knowledge about the lineage of a dataset);

         Potential Restrictions on dataset sharing.

   - Optional Metadata

      Complementary information are:
         Edition to indicate the reference or the source of the dataset;

         Purpose of the dataset and its objectives;

         Supplemental information that can provide a better understanding of the uploaded dataset;

         Maintenance frequency of the dataset;

         users who are Responsible for the dataset, its Owner, and the Author of its metadata;

         Spatial representation type used.

         Related resources to link one or multiple resources to the document. These will be visible inside the Dataset Information panel

   - Dataset Attributes
      At this step you can enrich the dataset attributes with useful information like the following:

         The Label displayed
   
         A detailed Description
   
         The Display Order
   
         The Display Type; the default value is Label, which means that the value of the attribute will be rendered as a plain text. There’s the possibility to instruct GeoNode to threat the values as different media-types. As an instance, if the values of the selected attribute will contain image urls, by selecting the IMAGE Display Type you will allow GeoNode to render the image directly when querying the dataset from the maps. The same for VIDEO, AUDIO or IFRAME mime types.
   
         The Visibile flag; allows you to instruct GeoNode wether or not hiding an attribute from the Get Feature Type outcomes
