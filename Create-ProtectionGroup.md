To backup a VM using the Cohesity extension for vCD, you must first create a protection group. A VM can only be protected by one protection group in vCD.

**Prerequisites**

VMs must be discovered and must not be inconsistent. See [Discover VMs](https://github.com/cohesity/cohesity-vcd-extension/wiki/Discover-VMs) for details. 

**To create protection group:**

1. Log into vCD as a tenant user.
2. Click ![](images/hamburger_menu.png) and navigate to **Data Protection**.
3. Click **Protection Group** under **Data Protection** module.
4. Click **New**.
5. A new form will be displayed.
6. Select the cluster in which the protection group need to be created.
7. Fill up the required details for the protection group.
8. On click **Next**, it will navigate to object page where VMs can be selected for protection.
9. Click on **Add Object**.
<img src="images/addObject_protectionGroup.png" style="zoom:60%;" />

10. Select the object need to be protected.
11. Click on the source to auto protect the source or unprotect/exclude the source from auto protection(incase if it is auto protected already).
<img src="images/selectSource_protectionGroup.png" style="zoom:60%;" />

12. To select the source individually, click on the checkbox of the particular source.
13. After the protection source selection, click on the button **Save Selection**.
14. Click on **Finish** button.
15. Protection group will be created successfully.

   **Note**: Protection group can be restricted per organization VDC by setting **Restrict Protection Group per Org VDC** flag as **Yes** in the **Settings** page of provider. so the protection group of specific organization VDC cannot be used for protecting source under different organization VDC. <br/>