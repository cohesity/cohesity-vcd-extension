
1. Login to Github and navigate to the [Release section](https://github.com/cohesity/cohesity-vcd-extension/releases) and download the **dataProtection.zip** file. 
2. Extract the contents of this zip to a directory called dataProtection and change directory to this directory. Run the following commands:
    <br/>
   `unzip dataProtection.zip`
    <br/>
   `cd dataProtection`
3. Enter the VCD details in **ui_ext_api.ini** file and make sure the user is VCD system administrator.
   Example:
    <br/>
   `vcduri=https://<vcd-fqdn>`
    <br/>
   `username=<system-user-id>`
    <br/>
   `organization=System`
    <br/>
   `password=<user-password>`
4. Run the following command below to deploy the plugin.
    <br/>
    `python deploy.py deploy` 
    <br/>    <br/>
   To view the Cohesity extension, log in to VCD, click ![hamburger_menu](images/hamburger_menu.png), the extension will be visible as **Data Protection**.
    <br/>
   <img src="images/vcd_extension.png" alt="vcd extension" style="zoom:60%;" />