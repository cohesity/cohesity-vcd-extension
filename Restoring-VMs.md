***To restore a VM:***

1. In the vCloud Director, click ![](images/hamburger_menu.png) and navigate to **Data Protection** > **Restore**.
2. Click **VM**.
3. Search for a VM to restore. 
4. Select the VM and click **Continue**. 
5. In the **Restore VM** page, select the snapshot and provide a prefix and suffix.<br/>
   **Note**: Prefix or suffix is required to ensure that the VM name is unique. 
6. By default, the VM is restored back to the original location. However, you can choose to recover to a new location by toggling on the option. <br/>
   **Note** : Restore to an alternate location is only supported for Cohesity cluster running version 6.4.1c, 6.5.1 and above.
7. Click **Restore**.
8. In the **Confirmation** dialog, click **Yes**. 
   A success message is displayed. 
   To check the status, navigate to **Monitor** to check for the recovery task as described in [Monitor Backup and Restore Tasks](https://github.com/cohesity/cohesity-vcd-extension/wiki/Monitor-Backup-and-Restore-Tasks).