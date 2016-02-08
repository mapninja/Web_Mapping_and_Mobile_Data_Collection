#Web Mapping and Mobile Data Collection

This session will explore using ArcGIS, ArcGIS Online and Collector for ArcGIS to create an integrated spatial data collection system. We'll be using some of the very well prepared materials created by Esri for this session. Please note that the ArcGIS Online usernames and passwords that you will use during this workshop are recycled so that the materials you place under these profiles is not permanently accessible.


##Using ArcGIS Desktop and ArcGIS Online for Mobile Data Collection with Collector for ArcGIS

###Preparing your data in ArcGIS for Desktop

[http://doc.arcgis.com/en/collector/android/create-maps/prepare-data-desktop.htm](http://doc.arcgis.com/en/collector/android/create-maps/prepare-data-desktop.htm)

####Create your geodatabase

Geodatabases organize and store data you collect. Ultimately you'll create a feature class to store damage assessment reports, but first you need to create the geodatabase that holds the feature class. Take the following steps to create a file geodatabase by using the Catalog window in ArcMap.

1.  Start ArcMap and open the Catalog window.
2.  Right-click the file folder in the Catalog tree where you want to create the file geodatabase.
Point to New.
3.  Click File Geodatabase to create a new file geodatabase in the location you selected. Name your geodatabase Tutorial.

###Define geodatabase domains

Some fields in your data should be populated from a set of choices. By creating domains in your geodatabase, you provide a list of choices your users can choose from when they are collecting data. Later in this tutorial, when you set up the fields, you'll use the domain.

1. In the Catalog tree, right-click the geodatabase and click Properties.
2. Click the Domains tab.
3. Click the first empty field under Domain Name and type ExtentDamage for the new domain.
4. Press the Tab key or click the new domain's description field, and type a description for the domain.
``Tip:
When creating a new domain, specify a name that describes the parameter it governs. The description is a small sentence describing the purpose of the domain.
``  

5. Click the field next to Domain Type, click the drop-down arrow, click Coded Values from the list of domain types, and choose Text as the Field Type.
6. Click the first empty field under Coded values and type Affected for the first valid code.
``
Tip:
When entering coded values, make sure the code field matches the Field Type specified in the Domain Properties.
``
7. Press the Tab key or click the new coded value's Description field. Type Affected as the user-friendly description for this coded value.
8. Repeat steps 5 and 6 until all valid values and their descriptions have been typed. The end product resembles the following image:
9. Click OK to create the new domain in the geodatabase and close the dialog box.

###Define the feature class

Next, you'll create the feature class to hold the collected information. Feature classes are essentially containers for information, where the pieces of information share similar characteristics, whether that be their geometry or their attributes.

1. Right-click the geodatabase, point to New, and click Feature Class.
Create a new feature class

``Note:
A feature class is a collection of features that share the same geometry type and information model.
``

2. The New Feature Class wizard opens. It walks you through the necessary steps to customize the feature class.

3. Type Damage_to_Residential_Buildings as the name for the feature class, type Damage to Residential Buildings as the alias, and choose Point Features as the feature type. Click Next.
4. When creating this feature class, choose a coordinate system. Coordinate systems allow your features to be projected properly and accurately on a map, making the features appear in the correct locations. For this tutorial, select WGS 1984 Web Mercator (auxiliary sphere). Click Next.
Choose the spatial reference
Click Next to accept the default XY Tolerance settings.
Click Next to accept the default database storage configuration.

#Creating a Map to Share for Data Collection
[http://doc.arcgis.com/en/collector/android/create-maps/create-and-share-a-collector-map.htm](http://doc.arcgis.com/en/collector/android/create-maps/create-and-share-a-collector-map.htm)


