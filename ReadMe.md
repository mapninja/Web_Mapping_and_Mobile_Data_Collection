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
2. Create a new feature class. The New Feature Class wizard opens. It walks you through the necessary steps to customize the feature class.
``Note:
A feature class is a collection of features that share the same geometry type and information model.
``
2. Type Damage_to_Residential_Buildings as the name for the feature class, type Damage to Residential Buildings as the alias, and choose Point Features as the feature type. Click Next.
3. When creating this feature class, choose a coordinate system. Coordinate systems allow your features to be projected properly and accurately on a map, making the features appear in the correct locations. For this tutorial, select WGS 1984 Web Mercator (auxiliary sphere). 
4. Click Next.
5. Click Next to accept the default XY Tolerance settings.
6. Click Next to accept the default database storage configuration.

###Set up the fields

The fields are a key part of your information model. They provide the structure of the information your field-workers collect and provide rules for the types of information collected about a feature.

1. The first field you create will be used to record the number of occupants that live in the building being inspected. Click the first empty field and type NUMOCCUP for Field Name. Under Data Type, choose Long Integer.
2. Under the Field Properties, click the Alias check box, and change the default alias NUMOCCUP to Number of Occupants. The alias is what your field-workers see on the data collection form, so it's important that it makes sense to them.
3. The next field you create takes advantage of the coded domain created earlier in this tutorial. Click the next empty field and type TYPDAMAGE. Choose Text as the data type.
Under Field Properties, type Extent of Damage as the alias for the field.
Check the empty Domain text box, and choose ExtentDamage.
Setting the domain
The final field to add is the description field. Name this field DESCDAMAGE and make it a text field. Update the alias to Description of Damage.
Note:
The full damage assessment template has more features than described in this tutorial. For a complete set of fields, download the Damage Assessment Template map package. However, you can continue the Collector tutorials using just the three fields you created.

Click Finish to complete the feature class creation.
The feature class you created is added to the map and appears in the table of contents in ArcMap.

To allow users to take pictures in the field and attach them to their assessment reports, enable attachments on the feature class you just created. To do so, right-click the feature class in the Catalog window, choose Manage, and click Create Attachments.



#Creating a Map to Share for Data Collection
[http://doc.arcgis.com/en/collector/android/create-maps/create-and-share-a-collector-map.htm](http://doc.arcgis.com/en/collector/android/create-maps/create-and-share-a-collector-map.htm)


