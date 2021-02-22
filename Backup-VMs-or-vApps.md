To backup a VM using the Cohesity extension for vCD, you must first create a protection group. A VM can only be protected by one protection group in vCD.

**Prerequisites**

VMs must be discovered and must not be inconsistent. See [Discover VMs](https://github.com/cohesity/cohesity-vcd-extension/wiki/Discover-VMs) for details. 

**To backup a VM:**

1. Log into vCD as a tenant user.
2. Click ![](images/hamburger_menu.png) and navigate to **Data Protection**.
3. Click **vApps/VMs** under **Data Protection** module.
4. Verify the status of VMs in the **Protection Status** column. 
   If any of the VMs that you want to back up are in an **Undiscovered** state, then you must first discover that VM. See [Discover VMs](https://github.com/cohesity/cohesity-vcd-extension/wiki/Discover-VMs) for details. 
5. If the status of the VM is **Unprotected**, right click on an **unprotected** VM, and click **Auto Protect vApp (to protect the vApp) or Protect VM (to protect individual VM)** .
   If you choose **AutoProtect vApp**, any VM that belongs to that vApp or any new VM created in that vApp will be automatically protected.
6. In this procedure, we will select **Protect VM**.
7. In the **Protect Now** window, Click **Create New Group**. You can select existing group as well.
8. Configure the protection group details and click **Save**.
   The **Protection Status** will be updated as **Protected** on success. 
   You can also login to the Cohesity cluster at this point to verify if the job was successfully created. 
   OR
   Verify the status as described in [Monitor Backup and Restore Tasks](https://github.com/cohesity/cohesity-vcd-extension/wiki/Monitor-Backup-and-Restore-Tasks).