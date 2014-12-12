# PeopleSoft 8 Sensor Pack

## Overview

This Knowledge Sensor Pack can be used to help quantify and diagnose performance issues related to PeopleSoft and Jolt specific code.

## Plugin Details

| Name | PeopleSoft 8 Sensor Pack
| :--- | :---
| Supported dynaTrace Versions | >= 5.5
| Author | Eric.Horsman@dynatrace.com
| License | [dynaTrace BSD](dynaTraceBSD.txt)
| Support | [Not Supported](https://community.compuwareapm.com/community/display/DL/Support+Levels)
| Release History | Version 1.0
| Download | [dynaTrace_Peoplesoft8KSP_v1.0.zip](dynaTrace_Peoplesoft8KSP_v1.0.zip)

## Installation

  1. Save the attached file locally to the computer where the dynaTrace Diagnostics Client is installed. 

  2. Unzip the file. 

  3. In the dynaTrace Diagnostics Client, right-click on the Diagnostics Server and select 'Preferences...'. 

  4. Click on "Sensor Packs". 

  5. Click on the "Import..." button. 

  6. Select "Custom Sensor Type (*.dtdcs)" in the "Files of type" dropdown. 

  7. Navigate to the directory where you extracted the .dtdcs file and click "Open". 

You can confirm successful import by observing the PeopleSoft Sensor Pack in the Sensor Packs Panel. This Knowlege Sensor Pack is now _Placed_ and _Active_ within all System Profiles on this
Diagnostics Server.

Exercise the PeopleSoft 8 application.

To further understand the usage and user activities in context to PeopleSoft, specific Servlet attributes can be captured. To do so, follow these steps:

  1. Right Click on the configuration in which you wish to add Servlet attributes and select "Properties...". 

  2. In the left hand panel expand/select "All Agents" or the specific Application Instance that pertains to PeopleSoft. 

  3. Select "Sensor Configuration". 

  4. Find the "Servlets" Sensor Pack in the "Sensor Configuration" list. 

  5. Click on"Properties" in the "Options" column. 

  6. Within the "Configure Sensor Properties" dialog, click on the "Add" button below the "Attribute Capturing" section (lower half). 

  7. A new entry will appear under the "Source" column in the "Attribute Capturing" list. Select "Parameter" from the drop down if it is not already selected. 

  8. Type the term "Page" in the corresponding "Query" column 

  9. You have now added the "Page" parameter. Follow steps 6-8 to add the following additional parameters: 

    * FolderRef 

    * PortalActualURL 

    * cmd 

    * PanelGroupName 

    * Menu 

    * menugroup 

    * ICType 

    * ICScripProgramName 

  10. Select OK. 

If you have followed the steps correctly, your Servlet Sensor Properties screen should look like this:

![images_community/download/attachments/4849980/PeopleSoft8_Servlet_Parameters.jpg](images_community/download/attachments/4849980/PeopleSoft8_Servlet_Parameters.jpg)

You will need to deploy this change into your application by either performing a Hot Sensor Placement or restarting your Application.

Note ** - Some of these parameters may not be valuable to all PeopleSoft deployments, Please remove unnecessarily parameters after usage depicts the value of capturing each parameter.





