The first step before we execute the vCD workflows is to make sure that VMs are discovered by Cohesity. You can check the status based on the **Protection Status** field.  

1. In the vCloud Director Tenant View, click ![](images/hamburger_menu.png) and navigate to **Data Protection** > **vApps/VMs**.
2. Check the status of all the VMs in the **Protection Status** field. 
3. If the status is **Undiscovered** for any VM, click **Discover**.
   This initiates a refresh operation on the vCD source.
