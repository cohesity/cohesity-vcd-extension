# Cohesity Extension for vCloud Director

This extension integrates with vCloud Director HTML5 UI and enables multi-tenant self-service operations using Cohesity REST API.

## Prerequisites

The reader of the vCD Extension guide must be familiar with:

    * Understand vCD v9.5 and internal working
    * Familiar with Cohesity DataPlatform and DataProtect

vCloud Director: 9.5 or later
Yarn: 1.1 or later
Cohesity Data Platform: 4.x
Web browsers: Latest Mozilla Firefox/ Google Chrome


## Installation Steps

This section describes the detailed steps to install and configure the Cohesity vCD extension on vCD.

====================================
Install Plugin-Lifecycle Management.
====================================

Plugin-Lifecycle management is a tool provided in vCD Developer SDK. It enables to manage the plugin/extension lifecycle i.e. install, enable/disable, remove, list all extensions in vCD.

Steps (Install Plugin Lifecycle Management):

1) Clone below vCD git repository. 

    https://github.com/vmware/vcd-ext-sdk.git

2) Follow the instructions to build.

    https://github.com/vmware/vcd-ext-sdk/blob/master/.travis.yml

3) Navigate to local repository where below extension is cloned.

    https://github.com/vmware/vcd-ext-sdk/tree/master/ui/plugin-lifecycle

4) Rename "ui_ext_api.ini.template" to "ui_ext_api.ini" and configure below details:

[DEFAULT]
    vcduri=<vCD IP>
    username=<admin username>
    organization=System
    password=<password>

5) Run command "yarn" followed by "yarn build" from plugin-lifecycle directory.

6) Run command "yarn deploy" from plugin-lifecycle directory.

7) Now "Plugin Lifecycle Management" extension will be visible in provider scope of vCD.

===================================
Steps (Install Cohesity Extension):
===================================

1) Navigate to vCD and login as a provider.
	
    ![alt-text](/documentation/images/image5.png)

2) Click on hamburger icon and select "Plugin Lifecycle Management"

    ![alt-text](/documentation/images/image6.png)

3) Click on upload.

    ![alt-text](/documentation/images/image7.png)

4) Click on “Select zip To Upload” and Navigate to the plugin.zip file for cohesity extension.

    ![alt-text](/documentation/images/image8.png)

5) Follow the instructions on screen to upload the plugin.

    ![alt-text](/documentation/images/image9.png)

6) On success, the uploaded extension will be visible under specified tenant Hamburger Icon.

## Features

1) Overview
2) vApps
3) Restore
4) Monitor


## Feedback
Please send your feedback and suggestions to cohesity-api-sdks@cohesity.com
