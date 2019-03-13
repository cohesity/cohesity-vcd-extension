# Cohesity Extension for vCloud Director

Cohesity Extension for vCloud Director enables Managed Service Providers to offer data protection as a self-service in multi-tenant environments.

## Prerequisites

Software Required:

* vCloud Director: 9.5 or later
* Cohesity Data Platform: 6.2 or later
* Web browsers: Firefox, Google Chrome, Safari
* Yarn: 1.1 or later (To install Plugin Lifecycle Management)

## Installation Steps

This section describes the detailed steps to install and configure the Cohesity Extension for vCloud Director.

### Install VMware's Plugin-Lifecycle Management extension

Plugin-Lifecycle management is a tool provided in vCD Developer SDK that enables managing the plugin/extension lifecycle i.e. install, enable/disable, remove, list all extensions in vCD.

#### Steps (Install Plugin Lifecycle Management):

1) Clone vCD git repository. 

    https://github.com/vmware/vcd-ext-sdk.git

2) Navigate to local repository where below extension is cloned.

    https://github.com/vmware/vcd-ext-sdk/tree/master/ui/plugin-lifecycle

3) Rename "ui_ext_api.ini.template" to "ui_ext_api.ini" and configure below details:

    ```
    [DEFAULT]
    * vcduri=<vCD IP>
    * username=<admin username>
    * organization=System
    * password=<password>
    ```

4) Run command "yarn" followed by "yarn build" from plugin-lifecycle directory.

5) Run command "yarn deploy" from plugin-lifecycle directory.

6) Now "Plugin Lifecycle Management" extension will be visible in provider scope of vCD.


### Install Cohesity Extension:

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

    Provides summary of the vcd resources, and the associated cohesity protection status. 

    ![alt-text](/documentation/images/image10.png)

2) Protection for vApps/VMs
    * Enables user to protect and Un-protect VMs and vApps
    * On demand Backups for VMs and vApps.

3) Restore
    * Recover files, folders or VM from backed up objects

4) Monitor

    Monitoring backup and restore events executed from vcd extension.

    ![alt-text](/documentation/images/image15.png)


## Feedback
We love to hear from you. Please send your feedback and suggestions to cohesity-api-sdks@cohesity.com
