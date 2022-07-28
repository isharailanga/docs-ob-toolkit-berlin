#Upgrading WSO2 Open Banking from 2.0 to 3.0

This section guides on how to upgrade your WSO2 Open Banking 2.0 setup to WSO2 Open Banking 3.0 (Accelerator Model). 

!!! note
    WSO2 Open Banking 2.0 is based on the WSO2 API Manager 3.1.0 and WSO2 Identity Server 5.10.0 products.

!!! tip
    In your Open Banking 2.0.0 database, verify the column size of the following:

     |Database|Table|Column|Data type|Size|
     |--------|-----|------|---------|----|
     |`openbank_apimgtdb`|`SP_METADATA`|`VALUE`| `VARCHAR` | 4096 |

     - If the column size is less than 4096, execute the following command against the `SP_METADATA` table:

        ``` 
        ALTER TABLE SP_METADATA MODIFY VALUE VARCHAR(4096); 
        ```

The diagram below explains the flow of upgrading the WSO2 Open Banking solution:

  [![](../../assets/img/install-and-setup/upgrading-the-solution/migration-flow.png)](../../assets/img/install-and-setup/upgrading-the-solution/migration-flow.png)

Follow the topics below in the given order:

  1. [Upgrading to WSO2 API Manager 3.2.0](upgrading-wso2-api-manager-320.md) <br/>
  2. [Upgrading to WSO2 Identity Sever 5.11.0](upgrading-wso2-identity-server.md) <br/>
  3. [Upgrading API Manager 3.2.0 to 4.0.0](upgrading-wso2-api-manager-400.md) <br/>
  4. [Migrating Open Banking Data](open-banking-data-migration.md) <br/>
  5. [Configuring After Migration](modifications-after-migration.md)