# Employ-Merge-Join-To-Merge-Two-Flat-File-data-sources
Using SSIS tool to import multiple sources flat files into your Database

StepI: 
1.Open business intelligence development studio.
2. Click on File-> New -> Project.
3. Select Integration service project in new project window and give the appropriate name and location for project. And click ok.
4. The new project screen contains the following:

Tool Box on left side bar
Solution Explorer on upper right bar
Property Window on lower right bar
Control flow, data flow, event Handlers, Package Explorer in tab windows
Connection Manager Window in the bottom
5. Right click on the Connection Manager Tab, click on new FLAT File Connection Menu Item.

6. Connection manager editor opens up which contains 4 tabs, General, Columns, Advanced and Preview.

In General Tab, enter connection manager name and description (optional). Select source file, file format and delimiter. If first row of source file contains headers, then select the checkbox “Column names in the first data row".
Select Column tab and check whether all columns are properly mapped or not.
Select advance tab. Here you can add, remove or modify columns as per output stream requirement.
Select preview tab to check how your output will look like:
7. Click on OK. It will create a flat file connection manager for your source file.
8. Now Drag Data Flow Task from the Toolbox into the Control Flow Container.

9. Double Click on the Data Flow Task. It will show Data flow Container tab for selected Data Flow Task. You can see three item categories in Toolbox.

Data flow sources - Source makes data from different external data sources available to the other components in the data flow.
Data flow transformations - Transformations can perform tasks such as updating, summarizing, cleaning, merging, and distributing data.
Data flow destinations - Destination writes the data from a data flow to a specific data store, or creates an in-memory dataset.
10. Drag a Flat file Source Component from Data Flow Sources into Data Flow Container window.

11. Double Click on the Flat File Source Component, it will display flat File source Editor. The window contain three tabs:

Connection Manager - Here we will specify source connection manager which we created for source file. If source file contains null values, select “Retain null values from Source as null values in the data flow” checkbox.
Columns -This tab allows the user to select required output columns and user can also change the output column names.
Error Output - Using this tab, the user can decide the behavior of the component in case of failure. There are three options:
Ignore Failure: Selecting this will ignore any failure while reading rows from source and the package will continue executing even any error occurred.
Redirect Row: Selecting this will redirect the failed rows to other component which is connected with the error precedence constraints.
Fail component: Selecting this will stop the execution of package in case of failure.

StepII: 

