# Archimap
Archimap plugin for GLPI

This plugin enables you to create Visio-like (architecture) diagrams with elements of the inventory (computers, databases, applications, dataflows, locations, suppliers).<br/>
The plugin implements the [Draw.io]("http://www.draw.io")'s graphical tool in the GLPI context.<br/>
Compared to the standard draw.io tool, one tab has been added, containing the GLPI assets.<br/>
You can add these stencils to the drawing pane as any other stencil (archimate, uml, etc). <br/>
But these stencils are each linked to an inventory class : when you type a label in the stencil, an autocomplete function is looking into GLPI for inventory assets containing this label and these items can be chosen in a dropdown list.
When one item of the list is selected, its GLPI properties are linked to the graphical object.<br/>
Based on these GLPI properties, the appearance of the object on the drawing pane can be modified (background color, contour line) or some additional properties can be displayed in the graphical object (description, type, status, ...)
When these properties are changed in the inventory, the label and/or appearance of the graphical object is also adapted : so, when you change the name of an application in GLPI, all the graphical objects in all the diagrams are adapted, or when you change the status of an application, its appearance changes in all diagrams too.
Consequently, your diagrams are centralized in the GLPI database, and have a uniform presentation, with up to date information and appearance.<br/>
You can add new GLPI assets in the GLPI tab by modifying the file plugins\archimap\drawio\src\main\webapp\stencils\glpi.xml and govern their appearance through the Css file plugins\archimap\drawio\src\main\webapp\styles\default.xml
Per diagram, you can specify which are your display preferences (look in the menu File->Preferences) : you can choose which properties are displayed as label (name, description, ...) and whether icons are also displayed to further identify the graphical objects.
