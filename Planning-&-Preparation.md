### Enable CORS on the Cohesity Cluster 

vCloud Director extension makes cross origin API requests to the Cohesity Cluster. To enable support for CORS (cross-origin resource sharing) headers on the Cohesity Cluster:

1.  Log in to the Cohesity cluster with valid credentials. 
2. To enable iris_cli:
   1. Click  ![](images\1.png)  in the dashboard, and select **Download CLI**. 
   2. Download the extension depending on your OS and click **Close**.
3.  Run the following command to make the iris_cli executable:
    `chmod +x iris_cli` 
4. To enable support for CORS:
   1.  Run the following command to connect to the cluster: 
       `./iris_cli -server {cohesity_cluster} -username {username} -password {password}` 
   2.  Replace **vcd_hostname** with the hostname of your vCloud Director server in the command below and run it in the shell to enable CORS. 
      <br/>`cluster update-gflag gflag-name="iris_cors_origins" gflag-value="https://{vcd_hostname}" service-name=iris reason="Enabling_CORS"`
      <br/><br/>`cluster update-gflag gflag-name="iris_alllowed_referrer_urls" gflag-value="https://{vcd_hostname}" service-name=iris reason="Enabling_Referer_Url"`
   3.  Restart IRIS service as follows:
       `cluster restart service-names=iris` 
   4.  Exit the shell.
       `exit` 

###  Register VCD as a Source 

VCD must be registered as a source on the Cohesity cluster. To do this: 

1. In the Cohesity cluster, navigate to **Data Protection** > **Sources**.
2. Click the plus icon to register a **Hypervisor** source. 
3. In **Select Hypervisor Source Type**, select *VMware:vCloud Director* from the drop down list.
4. Configure the IP address or hostname of VCD along with the credentials of VCD instance and click **Connect**.
   The vCenters present in the VCD are listed. 
5. Select the appropriate vCenter, enter credentials and click **Register**. 
   The hypervisor is registered successfully.

###  Create Organizations on Cohesity Cluster 

 To create a tenant/organization on a Cohesity cluster, you must first enable organizations on your cluster and then create a new organization. 

**Note**:  The term tenant also refers to an organization, and these terms have been used interchangeably throughout the document.  

####  **Enable Organizations on your Cluster** 

To enable organizations:

1. Log in to the Cohesity cluster as an administrator. 
2. Navigate to **Settings** > **Cluster > Summary** and click **Configure**.
3. Click on the toggle button to **Enable Organizations**.
4. (Optional) Toggle on **Allow multiple organizations to use one Storage Domain** option as well.
5. Click **Save**. 

####  **Create a new organization in Cohesity cluster** 

To create a new organization/tenant: 
**Note**: Make sure that the VCD is registered as a source.

1. On your cluster, navigate to **Settings** > **Cluster** > **Organizations.**
   1. Click **Add Organization**.
   2. Configure the organization details and click **Add**. 
2. Select **Storage Domain** for the organization from the drop down list. 
   You can either select an existing domain from the list or add a new domain. To add a new domain:
   1. Click **Add Storage Domain**. 
   2. Enter a new domain name and click **Show Advanced Settings**.
   3. Select the required configuration and click **Create Storage Domain**. 
3. (Optional) Select **Views** from the drop down list. 
4. Click **Assign Users/Groups** to assign users to the organization. 
   1. Select **Add User**.
      You can either select existing users or add a new user. 
   2. Enter the user details with credentials and click **Add**. 
      The new user is added successfully.
   3. Click **Assign**. 
5. Under **Sources**, click **Assign** **Objects** to assign a source to this organization.
   Select the VCD organisation from the source tree to which this newly created Cohesity tenant should bind and click **Assign**.
6. Click **Assign Policies and Protection Groups** to assign some policies to this organization and click **Assign**. 
7. Click **Save**.
   An organization/tenant is successfully created. 