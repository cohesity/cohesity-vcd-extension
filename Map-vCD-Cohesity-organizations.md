Once the Cohesity extension is successfully deployed in vCD, you must configure the Cohesity cluster in vCD and map the tenants/organizations created in Cohesity cluster with a vCD organization.

**Note**: At least one tenant must be mapped. See [Cohesity VMware vCD Solution Brief](https://www.cohesity.com/resource-assets/solution-brief/Cohesity-VMware-vCD-Solution-Brief.pdf) for details. 

1. Log in to vCD provider view with admin credentials.

2. Click ![](images/hamburger_menu.png), and select **Data Protection.** 
   The **Configuration** page displays. 
   
3. Click **Add**. 
   The **Add Cohesity Cluster** page displays.
   
4. Enter the Cohesity cluster details such as IP address or hostname of the cluster along with SP credentials. 
   The Cohesity tenant is listed in the **Tenants Mapping** section.
   
5. Select the **vCD Tenant** and the **Cohesity Tenant** and click **Map**. 
   
6. In the **Tenant User Credentials** prompt, you can either **Create New Local User** or select an **Existing User**. 
   This tenant user credentials are used to execute all workflows for the tenant. 
   The tenant user must hold the following Cohesity privileges:<br/>

   **Data Protection Related:**

   - View Protection Jobs
   - Manage Protection Jobs
   - Protection Job Operator
   - Manage Sources
   - View Protection Policies
   - Search Objects

   **Recovery Management Related:**

   - View Recover Tasks
   - Manage Recover Tasks
   - Download File

7. Click **Save**. 
   The mapping is successfully created and the Cohesity cluster is added successfully and the vCD tenant user can now access Cohesity workflows through his tenant portal.

8. Click **OK**.
