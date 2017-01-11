Bonn University - GESIS Institute
#####OSCOSS Project


#OJSIntegrationRestAPIplugin
Rest API Plugin for OJS to work with external web based authoring and text editing and publishing systems


Github source code of the plugin:
https://github.com/OSCOSS/OJSIntegrationRestAPIplugin


####Use case : FidusWriter
Our focus of use case was the working with FidusWriter collaborative authoring tool(https://www.fiduswriter.org) while
the the code is written as open as possible for any software that can deploy Rest API to integrate with OJS.

##Installation:
#####1.First step
An installation of OJS is needed. To install OJS please followup its readme in https://github.com/pkp/ojs/

To have its latest version please check out the master branch.

#####2.Second step
Download and copy the plugin files from github into plugins/generic/ojsIntegrationRestApi folder inside your OJS folder.
Create the folder if it does not exist. You can achieve this by running these commands:

```
cd plugins/generic/
git clone https://github.com/OSCOSS/OJSIntegrationRestAPIplugin.git
mv OJSIntegrationRestAPIplugin ojsIntegrationRestAPI
cd ../..
```

Then, run the upgrade script to register the plugin with the system by running:

```
php tools/upgrade.php upgrade
```

#####3.To Activate:
Enable the plugin via the OJS website interface:

Make sure you have set up at least one journal on your site. Otherwise the settings menu does not show.

Open the OJS interface and select "ENABLE" under Settings "OJS REST API Integration Plugin" under the following routes:

 in OJS 3.0 :
 
 setting > website > plugins

in OJS < 3.0:
 
Home > User > Journal Management > Plugin Management

##Documentation

Provided calls:
GET: RestApiGatewayPlugin/Journals?userEmail="Afshin@test.com"

####OJS 3 usage manual:
https://pkp.gitbooks.io/ojs3/content/en

####Sample OJS plugin:
https://pkp.sfu.ca/ojs/docs/technicalreference/2.1/pluginsSamplePlugin.html

####OJS 3 code report:
https://pkp.sfu.ca/ojs/doxygen/master/html/modules.html

####Ojs plugins basics:
https://pkp.sfu.ca/ojs/docs/technicalreference/2.1/plugins.html

####About Gateway Plugins
https://pkp.sfu.ca/ojs/docs/userguide/2.3.3/journalManagementGatewayPlugins.html
