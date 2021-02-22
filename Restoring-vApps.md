***To restore a vApp:***

1. In the vCloud Director, click ![](images/hamburger_menu.png) and navigate to **Data Protection** > **Restore**.
2. Click **vApp**.
3. You can search for a specific vApp name or use wildcard characters such as * to list all the VMs in the vApp.
4. Select a specific vApp, and click **Continue**. 
5. Configure the details:
   1. Under vApp Details, enter a prefix and suffix that will help you identify the vApp being restored. 
   2. Under VM Details, enter a similar prefix.
6. Under **Restore Properties**, select the snapshot that you want to recover.
7. Click **Restore**. 
8. In the **Confirmation** dialog, click **Yes**. 
   To check the status, in the main dashboard, navigate to **Monitor** to check for the recovery task as described in [Monitor Backup and Restore Tasks](https://github.com/cohesity/cohesity-vcd-extension/wiki/Monitor-Backup-and-Restore-Tasks).
