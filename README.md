## @edgraph-oss/platform-client@0.0.55

This generator creates TypeScript/JavaScript client that utilizes [axios](https://github.com/axios/axios). The generated Node module can be used in the following environments:

Environment
* Node.js
* Webpack
* Browserify

Language level
* ES5 - you must have a Promises/A+ library installed
* ES6

Module system
* CommonJS
* ES6 module system

It can be used in both TypeScript and JavaScript. In TypeScript, the definition will be automatically resolved via `package.json`. ([Reference](https://www.typescriptlang.org/docs/handbook/declaration-files/consumption.html))

### Building

To build and compile the typescript sources to javascript use:
```
npm install
npm run build
```

### Publishing

First build the package then run `npm publish`

### Consuming

navigate to the folder of your consuming project and run one of the following commands.

_published:_

```
npm install @edgraph-oss/platform-client@0.0.55 --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *https://api.dev.edgraph.com/tenant*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*APIClientsApi* | [**createTenantApiClientAsync**](docs/APIClientsApi.md#createtenantapiclientasync) | **POST** /tenants/{tenantId}/apiclients | Creates a new OpenId API Client
*APIClientsApi* | [**deleteTenantApiClientAsync**](docs/APIClientsApi.md#deletetenantapiclientasync) | **DELETE** /tenants/{tenantId}/apiclients/{clientId} | Deletes an OpenId API Client
*APIClientsApi* | [**getAllTenantApiClientsAsync**](docs/APIClientsApi.md#getalltenantapiclientsasync) | **GET** /tenants/{tenantId}/apiclients | Retrieves a list of OpenId API Clients associated to this tenant
*APIClientsApi* | [**getTenantApiClientByIdAsync**](docs/APIClientsApi.md#gettenantapiclientbyidasync) | **GET** /tenants/{tenantId}/apiclients/{clientId} | Retrieves an OpenId API Client
*APIClientsApi* | [**regenerateTenantApiClientSecretAsync**](docs/APIClientsApi.md#regeneratetenantapiclientsecretasync) | **PUT** /tenants/{tenantId}/apiclients/{clientId}/regeneratesecret | Regenerates an OpenId API Client\&#39;s secret
*APIClientsApi* | [**updateTenantApiClientAsync**](docs/APIClientsApi.md#updatetenantapiclientasync) | **PUT** /tenants/{tenantId}/apiclients/{clientId} | Updates an OpenId API Client
*AnalyticsConnectorsApi* | [**createConnector**](docs/AnalyticsConnectorsApi.md#createconnector) | **POST** /tenants/{tenantId}/analytics/connectors | Creates a new connector
*AnalyticsConnectorsApi* | [**deleteConnector**](docs/AnalyticsConnectorsApi.md#deleteconnector) | **DELETE** /tenants/{tenantId}/analytics/connectors/{connectorId} | Deletes a connector by Id
*AnalyticsConnectorsApi* | [**getADLSGen2ConnectorById**](docs/AnalyticsConnectorsApi.md#getadlsgen2connectorbyid) | **GET** /tenants/{tenantId}/analytics/connectors/{connectorId} | Retrieves a connector profile by Id
*AnalyticsConnectorsApi* | [**getPaginatedConnectors**](docs/AnalyticsConnectorsApi.md#getpaginatedconnectors) | **GET** /tenants/{tenantId}/analytics/connectors | Retrieves paginated connectors
*AnalyticsConnectorsApi* | [**updateConnector**](docs/AnalyticsConnectorsApi.md#updateconnector) | **PUT** /tenants/{tenantId}/analytics/connectors/{connectorId} | Updates a connector by Id
*AnalyticsDataLakeApi* | [**getPaginatedLakehouseRecords**](docs/AnalyticsDataLakeApi.md#getpaginatedlakehouserecords) | **GET** /tenants/{tenantId}/analytics/datalake/query | Retrieves gold-tier data from the lakehouse
*AnalyticsUserAuthorizationsApi* | [**getPaginatedUserAuthorizations**](docs/AnalyticsUserAuthorizationsApi.md#getpaginateduserauthorizations) | **GET** /tenants/{tenantId}/analytics/userauthorizations | Retrieves paginated user authorizations
*AnalyticsUserAuthorizationsApi* | [**softDeleteUserAuthorization**](docs/AnalyticsUserAuthorizationsApi.md#softdeleteuserauthorization) | **DELETE** /tenants/{tenantId}/analytics/userauthorizations/{userAuthorizationId} | Soft Deletes a user authorization by Id
*ApplicationsApi* | [**getTenantApplicationProfileByIdAsync**](docs/ApplicationsApi.md#gettenantapplicationprofilebyidasync) | **GET** /tenants/{tenantId}/applications/{applicationId} | Retrieves an application
*ApplicationsApi* | [**getTenantApplicationsAsync**](docs/ApplicationsApi.md#gettenantapplicationsasync) | **GET** /tenants/{tenantId}/applications | Retrieves a list of applications associated to this tenant
*ApplicationsSettingsApi* | [**getClientSettingsAsync**](docs/ApplicationsSettingsApi.md#getclientsettingsasync) | **GET** /tenants/{tenantId}/clients/{clientId}/settings | Retrieves a list of a Tenant\&#39;s ClientSettings.
*ApplicationsSettingsApi* | [**getClientSettingsTypesAsync**](docs/ApplicationsSettingsApi.md#getclientsettingstypesasync) | **GET** /tenants/{tenantId}/clients/{clientId}/settingstypes | Retrieves a list of ClientSettingsTypes.
*ApplicationsSettingsApi* | [**setClientSettingsAsync**](docs/ApplicationsSettingsApi.md#setclientsettingsasync) | **POST** /tenants/{tenantId}/clients/{clientId}/settings | Creates/updates a Tenant\&#39;s ClientSettings.
*ApplicationsTilesApi* | [**getTenantApplicationTilesAsync**](docs/ApplicationsTilesApi.md#gettenantapplicationtilesasync) | **GET** /tenants/{tenantId}/applicationtiles | Retrieves a list of applications licensed to the user that is currently logged in the context of this tenant
*CacheApi* | [**refreshUserProfileCache**](docs/CacheApi.md#refreshuserprofilecache) | **POST** /me/cache/refresh | Refreshes the user\&#39;s profile cache.
*CapacitiesApi* | [**assignMyGroupToCapacity**](docs/CapacitiesApi.md#assignmygrouptocapacity) | **POST** /tenants/{tenantId}/analytics/capacities | Assigns the specified group to the specified capacity.
*CapacitiesApi* | [**getAllAnalyticsPowerBiCapacities**](docs/CapacitiesApi.md#getallanalyticspowerbicapacities) | **GET** /tenants/{tenantId}/analytics/capacities | Retrieves a list of capacities in Power Bi that the user has access to.
*CapacitiesApi* | [**resumeCapacityAsync**](docs/CapacitiesApi.md#resumecapacityasync) | **POST** /tenants/{tenantId}/analytics/capacities/resume | Resumes currently suspended capacity
*CapacitiesApi* | [**suspendCapacityAsync**](docs/CapacitiesApi.md#suspendcapacityasync) | **POST** /tenants/{tenantId}/analytics/capacities/suspend | Suspends currently active capacity
*CategoriesApi* | [**addCategoryDataSteward**](docs/CategoriesApi.md#addcategorydatasteward) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards | Adds a Data Steward to a Category.
*CategoriesApi* | [**addCategoryDataStewardBulk**](docs/CategoriesApi.md#addcategorydatastewardbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/stewards | Adds a Data Steward to Categories.
*CategoriesApi* | [**certifyCategory**](docs/CategoriesApi.md#certifycategory) | **POST** /tenants/{tenantId}/statereporting/categories/{categoryId}/certify | Certifies a Category.
*CategoriesApi* | [**getDataUsersBulk**](docs/CategoriesApi.md#getdatausersbulk) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/datausers | Get all Data Users
*CategoriesApi* | [**getStateReportingCategories**](docs/CategoriesApi.md#getstatereportingcategories) | **GET** /tenants/{tenantId}/statereporting/categories | Retrieves a list of Categories.
*CategoriesApi* | [**removeCategoryDataOwner**](docs/CategoriesApi.md#removecategorydataowner) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Removes the Data Owner of a Category.
*CategoriesApi* | [**removeCategoryDataSteward**](docs/CategoriesApi.md#removecategorydatasteward) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards/{email} | Removes a Data Steward from a Category.
*CategoriesApi* | [**requestCategoryCertificationReminder**](docs/CategoriesApi.md#requestcategorycertificationreminder) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/certificationreminder | Requests a Certification Reminder to be sent.
*CategoriesApi* | [**setCategoryDataOwner**](docs/CategoriesApi.md#setcategorydataowner) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Sets the Data Owner of a Category.
*CategoriesApi* | [**setCategoryDataOwnerBulk**](docs/CategoriesApi.md#setcategorydataownerbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/owner | Sets the Data Owner of Categories.
*CategoriesApi* | [**uploadStateReportingCategory**](docs/CategoriesApi.md#uploadstatereportingcategory) | **POST** /tenants/{tenantId}/statereporting/categories/upload | Upload a Category via a JSON file.
*CategoriesApi* | [**uploadStateReportingPeriodsFromCategoryJson**](docs/CategoriesApi.md#uploadstatereportingperiodsfromcategoryjson) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/upload | Upload a Category via a JSON file.
*ChangeLogsApi* | [**getAllChangesAsync**](docs/ChangeLogsApi.md#getallchangesasync) | **GET** /tenants/{tenantId}/changes | 
*ClientBrandingApi* | [**getClientBrandingAsync**](docs/ClientBrandingApi.md#getclientbrandingasync) | **GET** /clients/{clientId}/branding | Public (unauthenticated) read of a client\&#39;s branding for the sign-in and other pre-auth  surfaces (Azure DevOps #17086). Returns only render fields + the override flag — never secrets,  storage internals, or other client configuration.
*ClientSettingsApi* | [**createClientSetting**](docs/ClientSettingsApi.md#createclientsetting) | **POST** /v2/tenants/{tenantId}/clients/{clientId}/settings | Create a Client-scope setting
*ClientSettingsApi* | [**deleteClientSetting**](docs/ClientSettingsApi.md#deleteclientsetting) | **DELETE** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Delete the Client-scope setting for a key, addressed by SettingType id or Code
*ClientSettingsApi* | [**getClientSetting**](docs/ClientSettingsApi.md#getclientsetting) | **GET** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Get a Client-scope setting
*ClientSettingsApi* | [**searchClientSettings**](docs/ClientSettingsApi.md#searchclientsettings) | **GET** /v2/tenants/{tenantId}/clients/{clientId}/settings | List Client-scope settings
*ClientSettingsApi* | [**setClientSetting**](docs/ClientSettingsApi.md#setclientsetting) | **PUT** /v2/tenants/{tenantId}/clients/{clientId}/settings | Create or update (upsert) a Client-scope setting, addressed by the SettingTypeId in the body
*ClientSettingsApi* | [**updateClientSetting**](docs/ClientSettingsApi.md#updateclientsetting) | **PUT** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Update the Client-scope setting for a key, addressed by SettingType id or Code
*ClientsSecretsApi* | [**addClientSecret**](docs/ClientsSecretsApi.md#addclientsecret) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/secrets | Creates a new secret for an OpenId client
*ClientsSecretsApi* | [**regenerateOneRosterApiClientSecretAsync**](docs/ClientsSecretsApi.md#regenerateonerosterapiclientsecretasync) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/regeneratesecret | Regenerate Client Secret
*CollectionsApi* | [**createCollection**](docs/CollectionsApi.md#createcollection) | **POST** /tenants/{tenantId}/validations/collections | Creates a Collection.
*CollectionsApi* | [**createContainer**](docs/CollectionsApi.md#createcontainer) | **POST** /tenants/{tenantId}/validations/collections/{collectionId}/containers | Creates a Container.
*CollectionsApi* | [**deleteCollection**](docs/CollectionsApi.md#deletecollection) | **DELETE** /tenants/{tenantId}/validations/collections/{collectionId} | Deletes a Collection.
*CollectionsApi* | [**deleteContainer**](docs/CollectionsApi.md#deletecontainer) | **DELETE** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Deletes a Container.
*CollectionsApi* | [**getCollectionById**](docs/CollectionsApi.md#getcollectionbyid) | **GET** /tenants/{tenantId}/validations/collections/{collectionId} | Retrieves a Collection by ID.
*CollectionsApi* | [**getCollectionJson**](docs/CollectionsApi.md#getcollectionjson) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/export | Retrieves the JSON representation of a Collection. Useful for exporting into other systems.
*CollectionsApi* | [**getCollections**](docs/CollectionsApi.md#getcollections) | **GET** /tenants/{tenantId}/validations/collections | Retrieves a list of Collections.
*CollectionsApi* | [**getCollectionsTree**](docs/CollectionsApi.md#getcollectionstree) | **GET** /tenants/{tenantId}/validations/categories/tree | Retrieves a list of Collections.
*CollectionsApi* | [**getContainerById**](docs/CollectionsApi.md#getcontainerbyid) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Retrieves a Container by ID.
*CollectionsApi* | [**getContainers**](docs/CollectionsApi.md#getcontainers) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/containers | Retrieves a list of Containers.
*CollectionsApi* | [**updateCollection**](docs/CollectionsApi.md#updatecollection) | **PUT** /tenants/{tenantId}/validations/collections/{collectionId} | Updates a Collection.
*CollectionsApi* | [**updateContainer**](docs/CollectionsApi.md#updatecontainer) | **PUT** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Updates a Container.
*CollectionsApi* | [**uploadCollectionJson**](docs/CollectionsApi.md#uploadcollectionjson) | **POST** /tenants/{tenantId}/validations/collections/import | Uploads a Collection JSON. Useful for importing from another system.
*ConfigurationsApi* | [**createAnalyticsConfigurationAsync**](docs/ConfigurationsApi.md#createanalyticsconfigurationasync) | **POST** /tenants/{tenantId}/analytics/configurations | Creates a new configuration.
*ConfigurationsApi* | [**deleteAnalyticsConfigurationAsync**](docs/ConfigurationsApi.md#deleteanalyticsconfigurationasync) | **DELETE** /tenants/{tenantId}/analytics/configurations/{configurationId} | Deletes a configuration.
*ConfigurationsApi* | [**getAllAnalyticsConfigurationsAsync**](docs/ConfigurationsApi.md#getallanalyticsconfigurationsasync) | **GET** /tenants/{tenantId}/analytics/configurations | Retrieves all configurations.
*ConfigurationsApi* | [**getAnalyticsConfigurationByIdAsync**](docs/ConfigurationsApi.md#getanalyticsconfigurationbyidasync) | **GET** /tenants/{tenantId}/analytics/configurations/{configurationId} | Retrieves a configuration by ID.
*ConfigurationsApi* | [**getAnalyticsConfigurationByTenantIdAsync**](docs/ConfigurationsApi.md#getanalyticsconfigurationbytenantidasync) | **GET** /tenants/{tenantId}/analytics/configurations/default | Retrieves current default configuration.
*ConfigurationsApi* | [**hasValidAnalyticsConfigurationAsync**](docs/ConfigurationsApi.md#hasvalidanalyticsconfigurationasync) | **GET** /tenants/{tenantId}/analytics/configurations/default/valid | Verifies if current default configuration has required values for correct functionality.
*ConfigurationsApi* | [**updateAnalyticsConfigurationAsync**](docs/ConfigurationsApi.md#updateanalyticsconfigurationasync) | **PUT** /tenants/{tenantId}/analytics/configurations/{configurationId} | Updates a configuration.
*ConfigurationsApi* | [**validateAADTokenAsync**](docs/ConfigurationsApi.md#validateaadtokenasync) | **POST** /tenants/{tenantId}/analytics/configurations/azure/testconnection | Verifies if AAD token generation is possible with user provided values.
*ConnectionsApi* | [**connectionTestedResponse**](docs/ConnectionsApi.md#connectiontestedresponse) | **POST** /tenants/{tenantId}/datasync/connections/testconnection | Tests availability of provided connection metadata.
*ConnectionsApi* | [**createEdFiConnection**](docs/ConnectionsApi.md#createedficonnection) | **POST** /tenants/{tenantId}/edfiadmin/connections | Creates a new Ed-Fi Connection.
*ConnectionsApi* | [**createTenantDataSyncConnection**](docs/ConnectionsApi.md#createtenantdatasyncconnection) | **POST** /tenants/{tenantId}/datasync/connections | Creates a new DataSync connection
*ConnectionsApi* | [**deleteEdFiConnection**](docs/ConnectionsApi.md#deleteedficonnection) | **DELETE** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Deletes an Ed-Fi Connection.
*ConnectionsApi* | [**deleteTenantDataSyncConnection**](docs/ConnectionsApi.md#deletetenantdatasyncconnection) | **DELETE** /tenants/{tenantId}/datasync/connections/{connectionId} | Delete a DataSync connection matching the primary key
*ConnectionsApi* | [**getAllTenantDataSyncConnections**](docs/ConnectionsApi.md#getalltenantdatasyncconnections) | **GET** /tenants/{tenantId}/datasync/connections | Retrieves a list of DataSync Connections
*ConnectionsApi* | [**getConnectionById**](docs/ConnectionsApi.md#getconnectionbyid) | **GET** /tenants/{tenantId}/oneroster/connections/{connectionId} | Retrieves the profile of a Connection.
*ConnectionsApi* | [**getEdFiConnectionById**](docs/ConnectionsApi.md#getedficonnectionbyid) | **GET** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Retrieves an Ed-Fi Connection by ID.
*ConnectionsApi* | [**getEdFiConnectionsAsync**](docs/ConnectionsApi.md#getedficonnectionsasync) | **GET** /tenants/{tenantId}/edfiadmin/connections | Retrieves a list of Ed-Fi Connections.
*ConnectionsApi* | [**getEdFiOdsBackupCodesDescriptorsAsync**](docs/ConnectionsApi.md#getedfiodsbackupcodesdescriptorsasync) | **GET** /tenants/{tenantId}/edfiadmin/connections/odsbackupcodes | Retrieves a list of Ed-Fi ODS backup codes.
*ConnectionsApi* | [**getPagedConnections**](docs/ConnectionsApi.md#getpagedconnections) | **GET** /tenants/{tenantId}/oneroster/connections | Retrieves a list of Connections.
*ConnectionsApi* | [**getTenantDataSyncConnectionProfileById**](docs/ConnectionsApi.md#gettenantdatasyncconnectionprofilebyid) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId} | Retrieves a specific DataSync connection using its primary key
*ConnectionsApi* | [**testConnectionDetailsAsync**](docs/ConnectionsApi.md#testconnectiondetailsasync) | **POST** /tenants/{tenantId}/oneroster/connections/test | Tests the connection by sending the connection details in the request payload
*ConnectionsApi* | [**testConnectionDetailsByIdAsync**](docs/ConnectionsApi.md#testconnectiondetailsbyidasync) | **POST** /tenants/{tenantId}/oneroster/connections/{connectionId}/test | Tests the connection by obtaining the details by ID
*ConnectionsApi* | [**updateEdFiConnection**](docs/ConnectionsApi.md#updateedficonnection) | **PUT** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Updates an Ed-Fi Connection.
*ConnectionsApi* | [**updateTenantDataSyncConnection**](docs/ConnectionsApi.md#updatetenantdatasyncconnection) | **PUT** /tenants/{tenantId}/datasync/connections/{connectionId} | Updates a DataSync connection matching the primary key
*ConnectionsByTypeDEPRECATEDApi* | [**createOrUpdateStateReportingConnectionByTypeV1**](docs/ConnectionsByTypeDEPRECATEDApi.md#createorupdatestatereportingconnectionbytypev1) | **PUT** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Creates or Update a Connection by ConnectionType.
*ConnectionsByTypeDEPRECATEDApi* | [**deleteStateReportingByTypeConnectionV1**](docs/ConnectionsByTypeDEPRECATEDApi.md#deletestatereportingbytypeconnectionv1) | **DELETE** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Deletes a Connection by Type
*ConnectionsByTypeDEPRECATEDApi* | [**getStateReportingConnectionByTypeV1**](docs/ConnectionsByTypeDEPRECATEDApi.md#getstatereportingconnectionbytypev1) | **GET** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Retrieves a Connection by Type.
*ConnectionsDEPRECATEDApi* | [**createStateReportingConnectionV1**](docs/ConnectionsDEPRECATEDApi.md#createstatereportingconnectionv1) | **POST** /tenants/{tenantId}/statereporting/connections | Creates a new Connection.
*ConnectionsDEPRECATEDApi* | [**deleteStateReportingConnectionV1**](docs/ConnectionsDEPRECATEDApi.md#deletestatereportingconnectionv1) | **DELETE** /tenants/{tenantId}/statereporting/connections/{connectionId} | Deletes a Connection.
*ConnectionsDEPRECATEDApi* | [**findStateReportingConnectionsV1**](docs/ConnectionsDEPRECATEDApi.md#findstatereportingconnectionsv1) | **GET** /tenants/{tenantId}/statereporting/connections | Retrieves a list of Connections.
*ConnectionsDEPRECATEDApi* | [**getStateReportingConnectionV1**](docs/ConnectionsDEPRECATEDApi.md#getstatereportingconnectionv1) | **GET** /tenants/{tenantId}/statereporting/connections/{connectionId} | Retrieves a Connection by ID.
*ConnectionsDEPRECATEDApi* | [**testStateReportingConnectionByIdV1**](docs/ConnectionsDEPRECATEDApi.md#teststatereportingconnectionbyidv1) | **POST** /tenants/{tenantId}/statereporting/connections/{connectionId}/testconnection | Tests a Connection by ID.
*ConnectionsDEPRECATEDApi* | [**testStateReportingConnectionByTypeV1**](docs/ConnectionsDEPRECATEDApi.md#teststatereportingconnectionbytypev1) | **POST** /tenants/{tenantId}/statereporting/connections/testconnection | Tests a Connection by Type.
*ConnectionsDEPRECATEDApi* | [**updateStateReportingConnectionV1**](docs/ConnectionsDEPRECATEDApi.md#updatestatereportingconnectionv1) | **PUT** /tenants/{tenantId}/statereporting/connections/{connectionId} | Updates a Connection.
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiDistricts**](docs/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfidistricts) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/districts | Retrieves a list of districts from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors**](docs/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfieducationorganizationiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/educationorganizationidentificationsystemdescriptors | Retrieves a list of education organization identification system descriptors from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiSchoolYears**](docs/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfischoolyears) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/schoolyears | Retrieves a list of school years from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiStaffIdDescriptors**](docs/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfistaffiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/staffidentificationsystemdescriptors | Retrieves a list of staff identification system descriptors from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiStudentIdDescriptors**](docs/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfistudentiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/studentidentificationsystemdescriptors | Retrieves a list of student identification system descriptors from an Ed-Fi API using the DataSync connection metadata
*ConnectionsEdFiApi* | [**getTenantDataSyncConnectionEdFiTermDescriptors**](docs/ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfitermdescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/termdescriptors | Retrieves a list of term descriptors from an Ed-Fi API using the DataSync connection metadata
*DomainsApi* | [**createTenantDomainAsync**](docs/DomainsApi.md#createtenantdomainasync) | **POST** /tenants/{tenantId}/domains | Creates a new domain
*DomainsApi* | [**deleteTenantDomainAsync**](docs/DomainsApi.md#deletetenantdomainasync) | **DELETE** /tenants/{tenantId}/domains/{domainName} | Deletes a user
*DomainsApi* | [**getAllTenantDomainsAsync**](docs/DomainsApi.md#getalltenantdomainsasync) | **GET** /tenants/{tenantId}/domains | Retrieves a list of domains associated to this tenant
*DomainsApi* | [**getTenantDomainProfileByNameAsync**](docs/DomainsApi.md#gettenantdomainprofilebynameasync) | **GET** /tenants/{tenantId}/domains/{domainName} | Retrieves a domain
*DomainsApi* | [**updateTenantDomainAsync**](docs/DomainsApi.md#updatetenantdomainasync) | **PUT** /tenants/{tenantId}/domains/{domainName} | Updates a domain
*DomainsApi* | [**verifyTenantDomainAsync**](docs/DomainsApi.md#verifytenantdomainasync) | **PUT** /tenants/{tenantId}/domains/{domainName}/verify | Verify a  tenant\&#39;s domain
*EdFiInstancesApi* | [**getAllEdFiAdminConnectionsFromAnalyticsAsync**](docs/EdFiInstancesApi.md#getalledfiadminconnectionsfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/connections | Retrieves a list of EdFi Admin connections
*EdFiInstancesApi* | [**getAllEdFiAdminInstancesFromAnalyticsAsync**](docs/EdFiInstancesApi.md#getalledfiadmininstancesfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/instances | Retrieves a list of EdFi Admin instances
*EdFiInstancesApi* | [**getEdFiAdminInstanceByIdFromAnalyticsAsync**](docs/EdFiInstancesApi.md#getedfiadmininstancebyidfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/instances/{instanceId} | Retrieves an Ed-Fi Admin instance by ID.
*EdFiSyncApi* | [**createEdFiSync**](docs/EdFiSyncApi.md#createedfisync) | **POST** /tenants/{tenantId}/jobs/edfisync | Creates an Ed-Fi Sync Job for a given tenant
*EdFiSyncApi* | [**executeEdFiSyncJob**](docs/EdFiSyncApi.md#executeedfisyncjob) | **PUT** /tenants/{tenantId}/jobs/edfisync/execute | Executes an Ed-Fi Sync Job
*EdFiSyncApi* | [**getEdFiSyncData**](docs/EdFiSyncApi.md#getedfisyncdata) | **GET** /tenants/{tenantId}/jobs/edfisync | Retrieves Ed-Fi Sync Connection Data for a given tenant
*EdFiSyncApi* | [**updateEdFiSync**](docs/EdFiSyncApi.md#updateedfisync) | **PUT** /tenants/{tenantId}/jobs/edfisync | Updates an Ed-Fi Sync for a given tenant
*EnrollmentAdminCapacityApi* | [**getCapacity**](docs/EnrollmentAdminCapacityApi.md#getcapacity) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/{schoolCode}/capacity | Searches Capacity for one school - one row per program x grade x school year.
*EnrollmentAdminContactsApi* | [**createEnrollmentContact**](docs/EnrollmentAdminContactsApi.md#createenrollmentcontact) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts | Creates an Enrollment Contact.
*EnrollmentAdminContactsApi* | [**getEnrollmentContactById**](docs/EnrollmentAdminContactsApi.md#getenrollmentcontactbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Gets an Enrollment Contact by its record id, with its linked students.
*EnrollmentAdminContactsApi* | [**getEnrollmentContactOverrides**](docs/EnrollmentAdminContactsApi.md#getenrollmentcontactoverrides) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides | Reads a contact\&#39;s override history, newest first.
*EnrollmentAdminContactsApi* | [**getEnrollmentContacts**](docs/EnrollmentAdminContactsApi.md#getenrollmentcontacts) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts | Searches Enrollment Contacts.
*EnrollmentAdminContactsApi* | [**overrideEnrollmentContactEmail**](docs/EnrollmentAdminContactsApi.md#overrideenrollmentcontactemail) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/email-override | Overrides a contact\&#39;s email address.
*EnrollmentAdminContactsApi* | [**overrideEnrollmentContactPhone**](docs/EnrollmentAdminContactsApi.md#overrideenrollmentcontactphone) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/phone-override | Overrides a contact\&#39;s phone number.
*EnrollmentAdminContactsApi* | [**removeEnrollmentContactEmailOverride**](docs/EnrollmentAdminContactsApi.md#removeenrollmentcontactemailoverride) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/email-override | Removes a contact\&#39;s email override, letting the SIS value show through again.
*EnrollmentAdminContactsApi* | [**removeEnrollmentContactPhoneOverride**](docs/EnrollmentAdminContactsApi.md#removeenrollmentcontactphoneoverride) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/phone-override | Removes a contact\&#39;s phone override, letting the SIS value show through again.
*EnrollmentAdminContactsApi* | [**unlockEnrollmentContactSignIn**](docs/EnrollmentAdminContactsApi.md#unlockenrollmentcontactsignin) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/unlock | Unlocks a contact\&#39;s sign-in, resetting exhausted parent-verification tries.
*EnrollmentAdminContactsApi* | [**updateEnrollmentContact**](docs/EnrollmentAdminContactsApi.md#updateenrollmentcontact) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Updates an Enrollment Contact name and its linked students.
*EnrollmentAdminProgramsApi* | [**createProgramCatalogEntry**](docs/EnrollmentAdminProgramsApi.md#createprogramcatalogentry) | **POST** /tenants/{tenantId}/enrollmentadmin/programs/catalog-entries | Creates a district catalog entry - a program the district defines once, which schools may  then be offered at. No school-identifying field; use POST .../programs/school-programs to  offer it at a school.
*EnrollmentAdminProgramsApi* | [**createSchoolProgram**](docs/EnrollmentAdminProgramsApi.md#createschoolprogram) | **POST** /tenants/{tenantId}/enrollmentadmin/programs/school-programs | Creates a school program - either adding an existing district catalog entry to a school  (a \&quot;school association\&quot;, when &#x60;programCatalogEntryId&#x60; is set) or creating a brand new  school-specific program (when it is not).
*EnrollmentAdminProgramsApi* | [**deleteProgramCatalogEntry**](docs/EnrollmentAdminProgramsApi.md#deleteprogramcatalogentry) | **DELETE** /tenants/{tenantId}/enrollmentadmin/programs/catalog-entries/{id} | Removes a district catalog entry.
*EnrollmentAdminProgramsApi* | [**deleteSchoolProgram**](docs/EnrollmentAdminProgramsApi.md#deleteschoolprogram) | **DELETE** /tenants/{tenantId}/enrollmentadmin/programs/school-programs/{id} | Removes a school program - the API equivalent of \&quot;remove a school association\&quot; when the  row is linked to a catalog entry, or a straightforward delete when it is school-specific.
*EnrollmentAdminProgramsApi* | [**getProgramById**](docs/EnrollmentAdminProgramsApi.md#getprogrambyid) | **GET** /tenants/{tenantId}/enrollmentadmin/programs/{id} | Gets a Program by its record id - a district catalog entry or a school-specific program.
*EnrollmentAdminProgramsApi* | [**getPrograms**](docs/EnrollmentAdminProgramsApi.md#getprograms) | **GET** /tenants/{tenantId}/enrollmentadmin/programs | Searches Programs - the union of district catalog entries and school-specific programs, in  one list distinguished by each row\&#39;s Scope.
*EnrollmentAdminProgramsApi* | [**updateProgramCatalogEntry**](docs/EnrollmentAdminProgramsApi.md#updateprogramcatalogentry) | **PUT** /tenants/{tenantId}/enrollmentadmin/programs/catalog-entries/{id} | Updates a district catalog entry\&#39;s own fields.
*EnrollmentAdminProgramsApi* | [**updateSchoolProgram**](docs/EnrollmentAdminProgramsApi.md#updateschoolprogram) | **PUT** /tenants/{tenantId}/enrollmentadmin/programs/school-programs/{id} | Updates a school program\&#39;s grades/capacity/zone/coordinates, and - only when it is  school-specific - its own Code/Name/ProgramType/EligibilityCriteria/RequiredDocuments.
*EnrollmentAdminResponsesApi* | [**getEnrollmentApplicationResponse**](docs/EnrollmentAdminResponsesApi.md#getenrollmentapplicationresponse) | **GET** /tenants/{tenantId}/enrollmentadmin/responses/{responseId} | Gets an Enrollment Application Response.
*EnrollmentAdminResponsesApi* | [**getEnrollmentApplicationResponses**](docs/EnrollmentAdminResponsesApi.md#getenrollmentapplicationresponses) | **GET** /tenants/{tenantId}/enrollmentadmin/responses | Searches Enrollment Application Responses.
*EnrollmentAdminSchoolsApi* | [**getEnrollmentSchool**](docs/EnrollmentAdminSchoolsApi.md#getenrollmentschool) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/code/{code} | Gets an Enrollment School by its school code, with the programs it runs.
*EnrollmentAdminSchoolsApi* | [**getEnrollmentSchoolById**](docs/EnrollmentAdminSchoolsApi.md#getenrollmentschoolbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/{id} | Gets an Enrollment School by its record id, with the programs it runs.
*EnrollmentAdminSchoolsApi* | [**getEnrollmentSchools**](docs/EnrollmentAdminSchoolsApi.md#getenrollmentschools) | **GET** /tenants/{tenantId}/enrollmentadmin/schools | Searches Enrollment Schools.
*EnrollmentAdminSchoolsApi* | [**setEnrollmentSchoolEnabled**](docs/EnrollmentAdminSchoolsApi.md#setenrollmentschoolenabled) | **PUT** /tenants/{tenantId}/enrollmentadmin/schools/code/{code}/enabled | Enables or disables an Enrollment School.
*EnrollmentAdminStudentsApi* | [**getEnrollmentStudent**](docs/EnrollmentAdminStudentsApi.md#getenrollmentstudent) | **GET** /tenants/{tenantId}/enrollmentadmin/students/{studentId} | Gets an Enrollment Student.
*EnrollmentAdminStudentsApi* | [**getEnrollmentStudents**](docs/EnrollmentAdminStudentsApi.md#getenrollmentstudents) | **GET** /tenants/{tenantId}/enrollmentadmin/students | Searches Enrollment Students.
*EnvironmentsApi* | [**createEnvironment**](docs/EnvironmentsApi.md#createenvironment) | **POST** /tenants/{tenantId}/validations/environments | Creates an Environment.
*EnvironmentsApi* | [**createStateReportingEnvironment**](docs/EnvironmentsApi.md#createstatereportingenvironment) | **POST** /tenants/{tenantId}/statereporting/environments | Creates a new Environment.
*EnvironmentsApi* | [**deleteEnvironment**](docs/EnvironmentsApi.md#deleteenvironment) | **DELETE** /tenants/{tenantId}/validations/environments/{environmentId} | Deletes an Environment.
*EnvironmentsApi* | [**deleteStateReportingEnvironment**](docs/EnvironmentsApi.md#deletestatereportingenvironment) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId} | Deletes an Environment.
*EnvironmentsApi* | [**getEnvironmentById**](docs/EnvironmentsApi.md#getenvironmentbyid) | **GET** /tenants/{tenantId}/validations/environments/{environmentId} | Retrieves an Environment by ID.
*EnvironmentsApi* | [**getEnvironments**](docs/EnvironmentsApi.md#getenvironments) | **GET** /tenants/{tenantId}/validations/environments | Retrieves a list of Environments.
*EnvironmentsApi* | [**getStateReportingEnvironment**](docs/EnvironmentsApi.md#getstatereportingenvironment) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId} | Retrieves an Environment by ID.
*EnvironmentsApi* | [**searchStateReportingEnvironments**](docs/EnvironmentsApi.md#searchstatereportingenvironments) | **GET** /tenants/{tenantId}/statereporting/environments | Retrieves a list of Environments.
*EnvironmentsApi* | [**testEnvironmentConnection**](docs/EnvironmentsApi.md#testenvironmentconnection) | **POST** /tenants/{tenantId}/validations/environments/testconnection | Tests if the provided connection string can establish a valid connection.
*EnvironmentsApi* | [**updateEnvironment**](docs/EnvironmentsApi.md#updateenvironment) | **PUT** /tenants/{tenantId}/validations/environments/{environmentId} | Updates an Environment.
*EnvironmentsApi* | [**updateStateReportingEnvironment**](docs/EnvironmentsApi.md#updatestatereportingenvironment) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId} | Updates an Environment.
*EnvironmentsConnectionsApi* | [**createStateReportingConnection**](docs/EnvironmentsConnectionsApi.md#createstatereportingconnection) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections | Creates a new Connection.
*EnvironmentsConnectionsApi* | [**deleteStateReportingConnection**](docs/EnvironmentsConnectionsApi.md#deletestatereportingconnection) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Deletes a Connection.
*EnvironmentsConnectionsApi* | [**findStateReportingConnections**](docs/EnvironmentsConnectionsApi.md#findstatereportingconnections) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections | Retrieves a list of Connections.
*EnvironmentsConnectionsApi* | [**getStateReportingConnection**](docs/EnvironmentsConnectionsApi.md#getstatereportingconnection) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Retrieves a Connection by ID.
*EnvironmentsConnectionsApi* | [**testStateReportingConnectionById**](docs/EnvironmentsConnectionsApi.md#teststatereportingconnectionbyid) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId}/testconnection | Tests a Connection by ID.
*EnvironmentsConnectionsApi* | [**testStateReportingConnectionByType**](docs/EnvironmentsConnectionsApi.md#teststatereportingconnectionbytype) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/testconnection | Tests a Connection by Type.
*EnvironmentsConnectionsApi* | [**updateStateReportingConnection**](docs/EnvironmentsConnectionsApi.md#updatestatereportingconnection) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Updates a Connection.
*EnvironmentsConnectionsByTypeApi* | [**createOrUpdateStateReportingConnectionByType**](docs/EnvironmentsConnectionsByTypeApi.md#createorupdatestatereportingconnectionbytype) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Creates or Update a Connection by ConnectionType.
*EnvironmentsConnectionsByTypeApi* | [**deleteStateReportingByTypeConnection**](docs/EnvironmentsConnectionsByTypeApi.md#deletestatereportingbytypeconnection) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Deletes a Connection by Type
*EnvironmentsConnectionsByTypeApi* | [**getStateReportingConnectionByType**](docs/EnvironmentsConnectionsByTypeApi.md#getstatereportingconnectionbytype) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Retrieves a Connection by Type.
*EnvironmentsReportingPeriodsApi* | [**cancelStateReportingPeriodRun**](docs/EnvironmentsReportingPeriodsApi.md#cancelstatereportingperiodrun) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/run | Cancel the Validation Run of a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**closeStateReportingPeriod**](docs/EnvironmentsReportingPeriodsApi.md#closestatereportingperiod) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/close | Closes a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**createStateReportingPeriod**](docs/EnvironmentsReportingPeriodsApi.md#createstatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Creates a new Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**deleteStateReportingPeriod**](docs/EnvironmentsReportingPeriodsApi.md#deletestatereportingperiod) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Deletes a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**getStateReportingPeriod**](docs/EnvironmentsReportingPeriodsApi.md#getstatereportingperiod) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Retrieves a Reporting Period by ID.
*EnvironmentsReportingPeriodsApi* | [**getStateReportingPeriodCertificationStatus**](docs/EnvironmentsReportingPeriodsApi.md#getstatereportingperiodcertificationstatus) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/certificationstatus | Retrieves the Certification Status of Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**getStateReportingPeriodValidationSummary**](docs/EnvironmentsReportingPeriodsApi.md#getstatereportingperiodvalidationsummary) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/validationsummary | Retrieves the Validation Summary of Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**getStateReportingPeriodValidationSummaryByCategory**](docs/EnvironmentsReportingPeriodsApi.md#getstatereportingperiodvalidationsummarybycategory) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/validationsummary/categories/{categoryId} | Retrieves the Validation Summary of Reporting Period by Category.
*EnvironmentsReportingPeriodsApi* | [**postStateReportingPeriod**](docs/EnvironmentsReportingPeriodsApi.md#poststatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/post | Posts a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**runStateReportingPeriod**](docs/EnvironmentsReportingPeriodsApi.md#runstatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/run | Run a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**searchStateReportingPeriods**](docs/EnvironmentsReportingPeriodsApi.md#searchstatereportingperiods) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Retrieves a list of Reporting Periods.
*EnvironmentsReportingPeriodsApi* | [**setStateReportingPeriodCurrentStep**](docs/EnvironmentsReportingPeriodsApi.md#setstatereportingperiodcurrentstep) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/steps/current | Sets the current step of a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**setStateReportingPeriodStepStatus**](docs/EnvironmentsReportingPeriodsApi.md#setstatereportingperiodstepstatus) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/steps/{stepNumber} | Sets the status of a Reporting Period step.
*EnvironmentsReportingPeriodsApi* | [**toggleStateReportingPeriodSelected**](docs/EnvironmentsReportingPeriodsApi.md#togglestatereportingperiodselected) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/toggle | Toggles the Selected state of a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**updateStateReportingPeriod**](docs/EnvironmentsReportingPeriodsApi.md#updatestatereportingperiod) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Updates a Reporting Period.
*EnvironmentsReportingPeriodsApi* | [**updateStateReportingPeriodBulk**](docs/EnvironmentsReportingPeriodsApi.md#updatestatereportingperiodbulk) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Updates Reporting Periods in bulk.
*EnvironmentsReportingPeriodsCategoriesApi* | [**searchStateReportingPeriodCategories**](docs/EnvironmentsReportingPeriodsCategoriesApi.md#searchstatereportingperiodcategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories | Retrieves the Categories of a Reporting Period.
*EnvironmentsReportingPeriodsCategoriesApi* | [**searchStateReportingPeriodSubCategories**](docs/EnvironmentsReportingPeriodsCategoriesApi.md#searchstatereportingperiodsubcategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories/{categoryId}/subcategories | Retrieves the Sub-Categories of a Reporting Period.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**deleteStateReportingPeriodRules**](docs/EnvironmentsReportingPeriodsRulesRecordsApi.md#deletestatereportingperiodrules) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules | Deletes the Rules of a Reporting Period.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**searchStateReportingPeriodRecords**](docs/EnvironmentsReportingPeriodsRulesRecordsApi.md#searchstatereportingperiodrecords) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/records | Retrieves the Invalid Records of all the Rules within a Reporting Period.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**searchStateReportingPeriodRuleRecords**](docs/EnvironmentsReportingPeriodsRulesRecordsApi.md#searchstatereportingperiodrulerecords) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records | Retrieves the Invalid Records of a Rule.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**setStateReportingPeriodRuleRecordPostFlag**](docs/EnvironmentsReportingPeriodsRulesRecordsApi.md#setstatereportingperiodrulerecordpostflag) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/{recordId}/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule\&#39;s Invalid Record.
*EnvironmentsReportingPeriodsRulesRecordsApi* | [**setStateReportingPeriodRuleRecordPostFlagBulk**](docs/EnvironmentsReportingPeriodsRulesRecordsApi.md#setstatereportingperiodrulerecordpostflagbulk) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule\&#39;s Invalid Records in bulk.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**addReportingPeriodSubmissionMetricsBulkV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#addreportingperiodsubmissionmetricsbulkv2) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics/bulk | Adds Metrics to a Submission in bulk.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**addReportingPeriodSubmissionMetricsV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#addreportingperiodsubmissionmetricsv2) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Adds Metrics to a Submission.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**cancelReportingPeriodSubmissionV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#cancelreportingperiodsubmissionv2) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/cancel | Cancels a Submission.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getReportingPeriodSubmissionLatestV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionlatestv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/latest | Retrieves the latest Submission of a Reporting Period.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getReportingPeriodSubmissionLogsV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionlogsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/logs | Retrieves a list of Submission Logs of a Reporting Period.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getReportingPeriodSubmissionMetricsV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionmetricsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Retrieves the Metrics of a Submission.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getReportingPeriodSubmissionV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId} | Retrieves the Submission of a Reporting Period.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**getStateReportingPeriodSubmissionsV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#getstatereportingperiodsubmissionsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions | Retrieves a list of Submissions of a Reporting Period.
*EnvironmentsReportingPeriodsSubmissionsApi* | [**setReportingPeriodSubmissionStatusV2**](docs/EnvironmentsReportingPeriodsSubmissionsApi.md#setreportingperiodsubmissionstatusv2) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/status | Sets the Status of a Submission.
*EvaluationSettingsApi* | [**getEvaluationSetting**](docs/EvaluationSettingsApi.md#getevaluationsetting) | **GET** /tenants/{tenantId}/evaluations/configuration | Gets the Evaluation Settings for a given tenant
*EvaluationSettingsApi* | [**setEvaluationSettingApplicationSetting**](docs/EvaluationSettingsApi.md#setevaluationsettingapplicationsetting) | **POST** /tenants/{tenantId}/evaluations/configuration/application | Sets the Application Settings of an Evaluation for a given Tenant
*EvaluationSettingsApi* | [**setEvaluationSettingUserSetting**](docs/EvaluationSettingsApi.md#setevaluationsettingusersetting) | **POST** /tenants/{tenantId}/evaluations/configuration/users | Sets the User Settings of an Evaluation for a given Tenant
*EvaluationsApi* | [**createEvaluation**](docs/EvaluationsApi.md#createevaluation) | **POST** /tenants/{tenantId}/evaluations | Creates a new Evaluation for a given tenant
*EvaluationsApi* | [**deleteEvaluation**](docs/EvaluationsApi.md#deleteevaluation) | **DELETE** /tenants/{tenantId}/evaluations/{evaluationId} | Deletes an Evaluation for a given tenant
*EvaluationsApi* | [**getEvaluation**](docs/EvaluationsApi.md#getevaluation) | **GET** /tenants/{tenantId}/evaluations/{evaluationId} | Get an Evaluation for a given tenant
*EvaluationsApi* | [**getEvaluationCount**](docs/EvaluationsApi.md#getevaluationcount) | **GET** /tenants/{tenantId}/evaluations/count | 
*EvaluationsApi* | [**searchEvaluationAppraisers**](docs/EvaluationsApi.md#searchevaluationappraisers) | **GET** /tenants/{tenantId}/evaluations/appraisers | Searches the Appraisers associated with an Evaluation for a given Tenant.
*EvaluationsApi* | [**searchEvaluationCampuses**](docs/EvaluationsApi.md#searchevaluationcampuses) | **GET** /tenants/{tenantId}/evaluations/campuses | Searches the Campuses associated with an Evaluation for a given Tenant.
*EvaluationsApi* | [**searchEvaluationForms**](docs/EvaluationsApi.md#searchevaluationforms) | **GET** /tenants/{tenantId}/evaluations/forms | Searches the Forms associated with an Evaluation for a given Tenant.
*EvaluationsApi* | [**searchEvaluationStaff**](docs/EvaluationsApi.md#searchevaluationstaff) | **GET** /tenants/{tenantId}/evaluations/staff | Searches the Staff associated with an Evaluation for a given Tenant.
*EvaluationsApi* | [**searchEvaluations**](docs/EvaluationsApi.md#searchevaluations) | **GET** /tenants/{tenantId}/evaluations | Searches the Evaluations for a given tenant
*EvaluationsApi* | [**updateEvaluation**](docs/EvaluationsApi.md#updateevaluation) | **PUT** /tenants/{tenantId}/evaluations/{evaluationId} | Updates an Evaluation for a given tenant
*FormComponentsApi* | [**getFormComponent**](docs/FormComponentsApi.md#getformcomponent) | **GET** /tenants/{tenantId}/forms/components/{formComponentId} | Get a Form Component.
*FormComponentsApi* | [**searchFormComponents**](docs/FormComponentsApi.md#searchformcomponents) | **GET** /tenants/{tenantId}/forms/components | Search Form Components
*FormsApi* | [**createForm**](docs/FormsApi.md#createform) | **POST** /tenants/{tenantId}/forms | Creates a new Form for a given tenant
*FormsApi* | [**createFullForm**](docs/FormsApi.md#createfullform) | **POST** /tenants/{tenantId}/forms/full | Fully creates a new Form for a given tenant (with Sections and Questions).
*FormsApi* | [**deleteForm**](docs/FormsApi.md#deleteform) | **DELETE** /tenants/{tenantId}/forms/{formId} | Deletes a Form.
*FormsApi* | [**duplicateForm**](docs/FormsApi.md#duplicateform) | **POST** /tenants/{tenantId}/forms/{formId}/duplicate | Duplicates all Form data for a given tenant (with Sections and Questions).
*FormsApi* | [**getForm**](docs/FormsApi.md#getform) | **GET** /tenants/{tenantId}/forms/{formId} | Get Form.
*FormsApi* | [**getFormAccess**](docs/FormsApi.md#getformaccess) | **GET** /tenants/{tenantId}/forms/{formId}/access | Get the Access Type for a Form.
*FormsApi* | [**importForm**](docs/FormsApi.md#importform) | **POST** /tenants/{tenantId}/forms/import | Imports all form data for a given tenant.
*FormsApi* | [**searchForms**](docs/FormsApi.md#searchforms) | **GET** /tenants/{tenantId}/forms | Search Forms
*FormsApi* | [**setFormAccess**](docs/FormsApi.md#setformaccess) | **PUT** /tenants/{tenantId}/forms/{formId}/access | Sets the Access Type for a Form.
*FormsApi* | [**updateForm**](docs/FormsApi.md#updateform) | **PUT** /tenants/{tenantId}/forms/{formId} | Updates a Form.
*FormsApi* | [**updateFullForm**](docs/FormsApi.md#updatefullform) | **PUT** /tenants/{tenantId}/forms/{formId}/full | Fully updates a Form for a given tenant (with Sections and Questions).
*GatewaysApi* | [**getAllAnalyticsGatewaysAsync**](docs/GatewaysApi.md#getallanalyticsgatewaysasync) | **GET** /tenants/{tenantId}/analytics/gateways | Retrieves a list of gateways in Power Bi that the user has access to.
*GroupsApi* | [**addUsersToGroupAsync**](docs/GroupsApi.md#adduserstogroupasync) | **POST** /tenants/{tenantId}/analytics/groups/{groupId}/users/bulk | Adds users to group.
*GroupsApi* | [**createAnalyticsPowerBiGroup**](docs/GroupsApi.md#createanalyticspowerbigroup) | **POST** /tenants/{tenantId}/analytics/groups | Creates a group.
*GroupsApi* | [**deleteAnalyticsPowerBiGroup**](docs/GroupsApi.md#deleteanalyticspowerbigroup) | **DELETE** /tenants/{tenantId}/analytics/groups/{groupId} | Deletes a group.
*GroupsApi* | [**getAnalyticsPowerBiGroupUsers**](docs/GroupsApi.md#getanalyticspowerbigroupusers) | **GET** /tenants/{tenantId}/analytics/groups/{groupId}/users | Retrieves all users for a specific group.
*GroupsApi* | [**getGroupsAsync**](docs/GroupsApi.md#getgroupsasync) | **GET** /tenants/{tenantId}/analytics/groups | Retrieves a list of groups.
*InstanceOnboardingStepsApi* | [**createInstanceOnboardingStepAsync**](docs/InstanceOnboardingStepsApi.md#createinstanceonboardingstepasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps | Creates an Onboarding Step.
*InstanceOnboardingStepsApi* | [**updateInstanceOnboardingStepAsync**](docs/InstanceOnboardingStepsApi.md#updateinstanceonboardingstepasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step.
*InstanceResourcesCountApi* | [**getAllInstanceResourcesCountAsync**](docs/InstanceResourcesCountApi.md#getallinstanceresourcescountasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/applications/{applicationId}/apiclients/{apiClientId}/resourcescount | Retrieves a paginated list of Instance Resources Count
*InstanceResourcesCountApi* | [**getAllInstanceResourcesCountJson**](docs/InstanceResourcesCountApi.md#getallinstanceresourcescountjson) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/applications/{applicationId}/apiclients/{apiClientId}/resourcescount/export | Retrieves the JSON representation of Instance Resources Count. Useful for exporting into other systems.
*InstancesApi* | [**addRelatedInstances**](docs/InstancesApi.md#addrelatedinstances) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/relatedinstances | Add related instances to root instance by Id
*InstancesApi* | [**addSchoolYear**](docs/InstancesApi.md#addschoolyear) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years | Adds an ODS database to an Instance.
*InstancesApi* | [**addSchoolYearRange**](docs/InstancesApi.md#addschoolyearrange) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/bulk | Adds multiple ODS databases to an instance.
*InstancesApi* | [**changeInstanceDatabaseTierAsync**](docs/InstancesApi.md#changeinstancedatabasetierasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/tiers | Changes the selected tier of an ODS database.
*InstancesApi* | [**cloneInstanceAsync**](docs/InstancesApi.md#cloneinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/clone | Clones an instance.
*InstancesApi* | [**createInstance**](docs/InstancesApi.md#createinstance) | **POST** /tenants/{tenantId}/oneroster/instances | Creates a new Instance.
*InstancesApi* | [**createInstanceAsync**](docs/InstancesApi.md#createinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances | Creates a new Instance.
*InstancesApi* | [**createInstanceV2**](docs/InstancesApi.md#createinstancev2) | **POST** /v2/tenants/{tenantId}/instances | Creates a new instance.
*InstancesApi* | [**deleteInstance**](docs/InstancesApi.md#deleteinstance) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId} | Deletes an Instance.
*InstancesApi* | [**deleteInstanceAsync**](docs/InstancesApi.md#deleteinstanceasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Deletes an Instance.
*InstancesApi* | [**deleteInstanceV2**](docs/InstancesApi.md#deleteinstancev2) | **DELETE** /v2/tenants/{tenantId}/instances/{instanceId} | Deletes an instance.
*InstancesApi* | [**deleteSchoolYearAsync**](docs/InstancesApi.md#deleteschoolyearasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year} | Removes an ODS database from an Instance.
*InstancesApi* | [**getEdFiAdminInstanceEndpoints**](docs/InstancesApi.md#getedfiadmininstanceendpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance.
*InstancesApi* | [**getEdFiAdminInstanceYearEndpoints**](docs/InstancesApi.md#getedfiadmininstanceyearendpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance.
*InstancesApi* | [**getInstanceById**](docs/InstancesApi.md#getinstancebyid) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId} | Retrieves an Instance by ID.
*InstancesApi* | [**getInstanceByIdAsync**](docs/InstancesApi.md#getinstancebyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Retrieves an Instance by ID.
*InstancesApi* | [**getInstanceCsvExport**](docs/InstancesApi.md#getinstancecsvexport) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves an Instance by ID.
*InstancesApi* | [**getInstanceCsvExportV2**](docs/InstancesApi.md#getinstancecsvexportv2) | **GET** /v2/tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format
*InstancesApi* | [**getInstanceEndpoints**](docs/InstancesApi.md#getinstanceendpoints) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/endpoints | Retrieves the One Roster endpoint URLs of an Instance.
*InstancesApi* | [**getInstancesAsync**](docs/InstancesApi.md#getinstancesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances | Retrieves a list of Instances.
*InstancesApi* | [**getPagedInstances**](docs/InstancesApi.md#getpagedinstances) | **GET** /tenants/{tenantId}/oneroster/instances | Retrieves a list of Instances.
*InstancesApi* | [**getTenantInstanceByIdV2**](docs/InstancesApi.md#gettenantinstancebyidv2) | **GET** /v2/tenants/{tenantId}/instances/{instanceId} | Get Instance by Id
*InstancesApi* | [**getTenantInstancesV2**](docs/InstancesApi.md#gettenantinstancesv2) | **GET** /v2/tenants/{tenantId}/instances | Get list of all instances for a tenant - V2
*InstancesApi* | [**isInstanceCustomIdAvailable**](docs/InstancesApi.md#isinstancecustomidavailable) | **GET** /tenants/{tenantId}/oneroster/instances/isinstancecustomidavailable/{customId} | Validate if instance is available
*InstancesApi* | [**loadApiMetadata**](docs/InstancesApi.md#loadapimetadata) | **POST** /tenants/{tenantId}/edfiadmin/api-metadata | Loads connection metadata.
*InstancesApi* | [**resetInstance**](docs/InstancesApi.md#resetinstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/resetinstance | Resets an Instance.
*InstancesApi* | [**resetInstanceAsync**](docs/InstancesApi.md#resetinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/resetinstance | Resets an Instance.
*InstancesApi* | [**resetInstanceCacheAsync**](docs/InstancesApi.md#resetinstancecacheasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetcache | Resets the cache of an Instance and the specified ODS database.
*InstancesApi* | [**resetSchoolYearAsync**](docs/InstancesApi.md#resetschoolyearasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetods | Resets the ODS database with the specified school year.
*InstancesApi* | [**setInstanceIsDefault**](docs/InstancesApi.md#setinstanceisdefault) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/default | Updates the isDefault property for an instance
*InstancesApi* | [**testConnectionDetailsByInstanceIdAsync**](docs/InstancesApi.md#testconnectiondetailsbyinstanceidasync) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/test | Tests the connection by obtaining the details by Instance ID
*InstancesApi* | [**testCredentialsConnection**](docs/InstancesApi.md#testcredentialsconnection) | **POST** /tenants/{tenantId}/edfiadmin/testconnection | Tests availability of provided connection metadata.
*InstancesApi* | [**testInstanceConnection**](docs/InstancesApi.md#testinstanceconnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/testconnection | Tests the connection of the Instance.
*InstancesApi* | [**testInstanceYearConnection**](docs/InstancesApi.md#testinstanceyearconnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/testconnection | Tests the connection of the Instance.
*InstancesApi* | [**truncateInstance**](docs/InstancesApi.md#truncateinstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/truncate | Truncates the Instance\&#39;s database
*InstancesApi* | [**updateInstance**](docs/InstancesApi.md#updateinstance) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId} | Updates an Instance.
*InstancesApi* | [**updateInstanceAsync**](docs/InstancesApi.md#updateinstanceasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Updates an Instance.
*InstancesApi* | [**updateInstanceV2**](docs/InstancesApi.md#updateinstancev2) | **PUT** /v2/tenants/{tenantId}/instances/{instanceId} | Updates an existing instance.
*InstancesApi* | [**validateCustomIdAvailable**](docs/InstancesApi.md#validatecustomidavailable) | **GET** /tenants/{tenantId}/edfiadmin/instances/validatecustomidavailable/{customId} | Validate if instance is available
*InstancesApplicationsApi* | [**createApplicationAsync**](docs/InstancesApplicationsApi.md#createapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Creates an Application.
*InstancesApplicationsApi* | [**createApplicationUserAccessAsync**](docs/InstancesApplicationsApi.md#createapplicationuseraccessasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Creates a new application access.
*InstancesApplicationsApi* | [**deleteApplicationAsync**](docs/InstancesApplicationsApi.md#deleteapplicationasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Deletes an Application.
*InstancesApplicationsApi* | [**deleteApplicationUserAccessAsync**](docs/InstancesApplicationsApi.md#deleteapplicationuseraccessasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Deletes an application user access.
*InstancesApplicationsApi* | [**getApplicationAccessAsync**](docs/InstancesApplicationsApi.md#getapplicationaccessasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Retrieves a list of application accesses.
*InstancesApplicationsApi* | [**getApplicationAccessByIdAsync**](docs/InstancesApplicationsApi.md#getapplicationaccessbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Retrieves an application access by ID.
*InstancesApplicationsApi* | [**getApplicationApiClientByIdAsync**](docs/InstancesApplicationsApi.md#getapplicationapiclientbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId} | Retrieves an API Client of an Application by ID.
*InstancesApplicationsApi* | [**getApplicationApiClientsAsync**](docs/InstancesApplicationsApi.md#getapplicationapiclientsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients | Retrieves the API Clients of an Application.
*InstancesApplicationsApi* | [**getApplicationByIdAsync**](docs/InstancesApplicationsApi.md#getapplicationbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Retrieves an Application by ID.
*InstancesApplicationsApi* | [**getApplicationsAsync**](docs/InstancesApplicationsApi.md#getapplicationsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Retrieves a list of Applications.
*InstancesApplicationsApi* | [**regenerateApiClientSecretAsync**](docs/InstancesApplicationsApi.md#regenerateapiclientsecretasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/regenerate | Regenerates the secret of an API Client.
*InstancesApplicationsApi* | [**regenerateApplicationApiClientCredentials**](docs/InstancesApplicationsApi.md#regenerateapplicationapiclientcredentials) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/regenerate | Regenerates an application\&#39;s API Client Credentials
*InstancesApplicationsApi* | [**syncApplicationAsync**](docs/InstancesApplicationsApi.md#syncapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/sync | Copies an Application from one instance to another/other instance(s)
*InstancesApplicationsApi* | [**updateApplicationAsync**](docs/InstancesApplicationsApi.md#updateapplicationasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Updates an Application.
*InstancesApplicationsApi* | [**updateApplicationUserAccessAsync**](docs/InstancesApplicationsApi.md#updateapplicationuseraccessasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Updates a new application access.
*InstancesAuthorizationStrategiesApi* | [**getAuthorizationStrategiesAsync**](docs/InstancesAuthorizationStrategiesApi.md#getauthorizationstrategiesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/authorizationstrategies | Retrieves a list of Authorization Strategies.
*InstancesClaimSetsApi* | [**createClaimSetAsync**](docs/InstancesClaimSetsApi.md#createclaimsetasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Creates a ClaimSet.
*InstancesClaimSetsApi* | [**deleteClaimSetAsync**](docs/InstancesClaimSetsApi.md#deleteclaimsetasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Deletes a ClaimSet.
*InstancesClaimSetsApi* | [**getClaimSetByIdAsync**](docs/InstancesClaimSetsApi.md#getclaimsetbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Retrieves a ClaimSet by ID.
*InstancesClaimSetsApi* | [**getClaimSetsAsync**](docs/InstancesClaimSetsApi.md#getclaimsetsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Retrieves a list of ClaimSets.
*InstancesClaimSetsApi* | [**getResourceClaimsGridAsync**](docs/InstancesClaimSetsApi.md#getresourceclaimsgridasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/resourceclaims | Retrieves a grid of Resource Claims.
*InstancesClaimSetsApi* | [**syncClaimSetAsync**](docs/InstancesClaimSetsApi.md#syncclaimsetasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/sync | Copies a Claim Set from one instance to another/other instance(s)
*InstancesClaimSetsApi* | [**updateClaimSetAsync**](docs/InstancesClaimSetsApi.md#updateclaimsetasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Updates a ClaimSet.
*InstancesClientsApi* | [**createClient**](docs/InstancesClientsApi.md#createclient) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Creates a new client
*InstancesClientsApi* | [**deleteClient**](docs/InstancesClientsApi.md#deleteclient) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Deletes a client by Id
*InstancesClientsApi* | [**getClientById**](docs/InstancesClientsApi.md#getclientbyid) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Retrieves a client by Id
*InstancesClientsApi* | [**getPagedClients**](docs/InstancesClientsApi.md#getpagedclients) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Retrieves a list of clients for a given instance
*InstancesClientsApi* | [**updateClient**](docs/InstancesClientsApi.md#updateclient) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Updates a client by Id
*InstancesDescriptorMappingsApi* | [**createDescriptorMapping**](docs/InstancesDescriptorMappingsApi.md#createdescriptormapping) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Creates a Descriptor Mapping.
*InstancesDescriptorMappingsApi* | [**deleteDescriptorMapping**](docs/InstancesDescriptorMappingsApi.md#deletedescriptormapping) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Deletes a Descriptor Mapping.
*InstancesDescriptorMappingsApi* | [**exportDescriptorMappings**](docs/InstancesDescriptorMappingsApi.md#exportdescriptormappings) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/export | Exports all Descriptor Mappings as a JSON file.
*InstancesDescriptorMappingsApi* | [**getDescriptorMappingById**](docs/InstancesDescriptorMappingsApi.md#getdescriptormappingbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Retrieves a Descriptor Mapping by ID.
*InstancesDescriptorMappingsApi* | [**getDescriptorMappings**](docs/InstancesDescriptorMappingsApi.md#getdescriptormappings) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Retrieves a list of Descriptors Mappings.
*InstancesDescriptorMappingsApi* | [**importDescriptorMappings**](docs/InstancesDescriptorMappingsApi.md#importdescriptormappings) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/import | Imports Descriptor Mappings from a JSON file.
*InstancesDescriptorMappingsApi* | [**updateDescriptorMapping**](docs/InstancesDescriptorMappingsApi.md#updatedescriptormapping) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Updates a Descriptor Mapping.
*InstancesDescriptorsApi* | [**createDescriptorAsync**](docs/InstancesDescriptorsApi.md#createdescriptorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Creates a Descriptor.
*InstancesDescriptorsApi* | [**deleteDescriptorAsync**](docs/InstancesDescriptorsApi.md#deletedescriptorasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Deletes a Descriptor.
*InstancesDescriptorsApi* | [**getDescriptorByIdAsync**](docs/InstancesDescriptorsApi.md#getdescriptorbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Retrieves a Descriptor by ID.
*InstancesDescriptorsApi* | [**getDescriptorNamespacesAsync**](docs/InstancesDescriptorsApi.md#getdescriptornamespacesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/namespaces | Retrieves a list of Descriptor Namespaces.
*InstancesDescriptorsApi* | [**getDescriptorsAsync**](docs/InstancesDescriptorsApi.md#getdescriptorsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Retrieves a list of Descriptors.
*InstancesDescriptorsApi* | [**updateDescriptorAsync**](docs/InstancesDescriptorsApi.md#updatedescriptorasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Updates a Descriptor.
*InstancesEducationOrganizationsEducationServiceCentersApi* | [**createEducationServiceCenterAsync**](docs/InstancesEducationOrganizationsEducationServiceCentersApi.md#createeducationservicecenterasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters | Creates an EducationServiceCenter.
*InstancesEducationOrganizationsEducationServiceCentersApi* | [**deleteEducationServiceCenterAsync**](docs/InstancesEducationOrganizationsEducationServiceCentersApi.md#deleteeducationservicecenterasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Deletes an EducationServiceCenter.
*InstancesEducationOrganizationsEducationServiceCentersApi* | [**getEducationServiceCenterByIdAsync**](docs/InstancesEducationOrganizationsEducationServiceCentersApi.md#geteducationservicecenterbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Retrieves an EducationServiceCenter by ID.
*InstancesEducationOrganizationsEducationServiceCentersApi* | [**updateEducationServiceCenterAsync**](docs/InstancesEducationOrganizationsEducationServiceCentersApi.md#updateeducationservicecenterasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Updates an EducationServiceCenter.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**createLocalEducationAgencyAsync**](docs/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#createlocaleducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Creates a LocalEducationAgency.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**deleteLocalEducationAgencyAsync**](docs/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#deletelocaleducationagencyasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Deletes a LocalEducationAgency.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**getLocalEducationAgencyByIdAsync**](docs/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getlocaleducationagencybyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Retrieves a LocalEducationAgency by ID.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**getlLocalEducationAgenciesAsync**](docs/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getllocaleducationagenciesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Retrieves a list of LocalEducationAgencies.
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**syncLocalEducationAgencyAsync**](docs/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#synclocaleducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId}/sync | Copies a LocalEducationAgency from one instance to another/other instance(s).
*InstancesEducationOrganizationsLocalEducationAgenciesApi* | [**updateLocalEducationAgencyAsync**](docs/InstancesEducationOrganizationsLocalEducationAgenciesApi.md#updatelocaleducationagencyasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Updates a LocalEducationAgency.
*InstancesEducationOrganizationsStateEducationAgenciesApi* | [**createStateEducationAgencyAsync**](docs/InstancesEducationOrganizationsStateEducationAgenciesApi.md#createstateeducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies | Creates a StateEducationAgency.
*InstancesEducationOrganizationsStateEducationAgenciesApi* | [**deleteStateEducationAgencyAsync**](docs/InstancesEducationOrganizationsStateEducationAgenciesApi.md#deletestateeducationagencyasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Deletes a StateEducationAgency.
*InstancesEducationOrganizationsStateEducationAgenciesApi* | [**getStateEducationAgencyByIdAsync**](docs/InstancesEducationOrganizationsStateEducationAgenciesApi.md#getstateeducationagencybyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Retrieves a StateEducationAgency by ID.
*InstancesEducationOrganizationsStateEducationAgenciesApi* | [**updateStateEducationAgencyAsync**](docs/InstancesEducationOrganizationsStateEducationAgenciesApi.md#updatestateeducationagencyasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Updates a StateEducationAgency.
*InstancesInstanceApplicationsApi* | [**createInstanceApplication**](docs/InstancesInstanceApplicationsApi.md#createinstanceapplication) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications | Creates an Instance Application
*InstancesInstanceApplicationsApi* | [**deleteInstanceApplication**](docs/InstancesInstanceApplicationsApi.md#deleteinstanceapplication) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Deletes an Instance Application
*InstancesInstanceApplicationsApi* | [**getInstanceApplicationById**](docs/InstancesInstanceApplicationsApi.md#getinstanceapplicationbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Retrieves an Instance Application by ID.
*InstancesInstanceApplicationsApi* | [**getInstanceApplications**](docs/InstancesInstanceApplicationsApi.md#getinstanceapplications) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications | Retrieves a paginated list of Instance applications
*InstancesInstanceApplicationsApi* | [**updateInstanceApplication**](docs/InstancesInstanceApplicationsApi.md#updateinstanceapplication) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Updates an Instance Application
*InstancesInstanceApplicationsAPIClientsApi* | [**createInstanceApiClient**](docs/InstancesInstanceApplicationsAPIClientsApi.md#createinstanceapiclient) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Creates an Instance ApiClient
*InstancesInstanceApplicationsAPIClientsApi* | [**deleteInstanceApiClient**](docs/InstancesInstanceApplicationsAPIClientsApi.md#deleteinstanceapiclient) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Deletes an Instance ApiClient
*InstancesInstanceApplicationsAPIClientsApi* | [**getInstanceApiClientById**](docs/InstancesInstanceApplicationsAPIClientsApi.md#getinstanceapiclientbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Retrieves an Instance ApiClient by ID.
*InstancesInstanceApplicationsAPIClientsApi* | [**getInstanceApiClients**](docs/InstancesInstanceApplicationsAPIClientsApi.md#getinstanceapiclients) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Retrieves a paginated list of Instance ApiClients
*InstancesInstanceApplicationsAPIClientsApi* | [**updateInstanceApiClient**](docs/InstancesInstanceApplicationsAPIClientsApi.md#updateinstanceapiclient) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Updates an Instance Application ApiClient
*InstancesLogsApi* | [**getInstanceHttpLogs**](docs/InstancesLogsApi.md#getinstancehttplogs) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/logs/http | Retrieves HTTP logs for a given instance
*InstancesReportsApi* | [**generateReportsAsync**](docs/InstancesReportsApi.md#generatereportsasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/generate | Queues a job to generate the report views in the ODS Database.
*InstancesReportsApi* | [**getReportsStatusAsync**](docs/InstancesReportsApi.md#getreportsstatusasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/status | Retrieves the status of the report views in Instance.
*InstancesReportsApi* | [**getSchoolsByTypeReportAsync**](docs/InstancesReportsApi.md#getschoolsbytypereportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/schoolsbytype/{localEducationAgencyId} | Retrieves a \&quot;Schools By Type\&quot; report.
*InstancesReportsApi* | [**getStudentEconomicSituationReportAsync**](docs/InstancesReportsApi.md#getstudenteconomicsituationreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentseconomicsituation/{localEducationAgencyId} | Retrieves a \&quot;Students Economic Situation\&quot; report.
*InstancesReportsApi* | [**getStudentEnrollmentByEthnicityReport**](docs/InstancesReportsApi.md#getstudentenrollmentbyethnicityreport) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/ethnicity/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Ethnicity\&quot; report.
*InstancesReportsApi* | [**getStudentEnrollmentByGenderReportAsync**](docs/InstancesReportsApi.md#getstudentenrollmentbygenderreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/gender/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Gender\&quot; report.
*InstancesReportsApi* | [**getStudentEnrollmentByRaceReportAsync**](docs/InstancesReportsApi.md#getstudentenrollmentbyracereportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/race/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Race\&quot; report.
*InstancesReportsApi* | [**getStudentsByProgramReportAsync**](docs/InstancesReportsApi.md#getstudentsbyprogramreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentsbyprogram/{localEducationAgencyId} | Retrieves a \&quot;Students By Program\&quot; report.
*InstancesReportsApi* | [**getTotalEnrollmentsReportAsync**](docs/InstancesReportsApi.md#gettotalenrollmentsreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/totalenrollments/{localEducationAgencyId} | Retrieves a \&quot;Total Enrollments\&quot; report.
*InstancesVendorsApi* | [**createVendorAsync**](docs/InstancesVendorsApi.md#createvendorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors | Creates a new Vendor.
*InstancesVendorsApi* | [**deleteVendorAsync**](docs/InstancesVendorsApi.md#deletevendorasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Deletes a Vendor.
*InstancesVendorsApi* | [**getVendorByIdAsync**](docs/InstancesVendorsApi.md#getvendorbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Retrieves a Vendor by ID.
*InstancesVendorsApi* | [**getVendorsAsync**](docs/InstancesVendorsApi.md#getvendorsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors | Retrieves a list of Vendors.
*InstancesVendorsApi* | [**syncVendorAsync**](docs/InstancesVendorsApi.md#syncvendorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId}/sync | Copies a Vendor from one instance to another/other instance(s).
*InstancesVendorsApi* | [**updateVendorAsync**](docs/InstancesVendorsApi.md#updatevendorasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Updates a Vendor.
*IntegrationProductsApi* | [**createIntegrationProduct**](docs/IntegrationProductsApi.md#createintegrationproduct) | **POST** /integrations/products | Creates an Integration Product.
*IntegrationProductsApi* | [**deleteIntegrationProduct**](docs/IntegrationProductsApi.md#deleteintegrationproduct) | **DELETE** /integrations/products/{productId} | Removes an Integration Product.
*IntegrationProductsApi* | [**getIntegrationProduct**](docs/IntegrationProductsApi.md#getintegrationproduct) | **GET** /integrations/products/{productId} | Gets an Integration Product.
*IntegrationProductsApi* | [**searchIntegrationProducts**](docs/IntegrationProductsApi.md#searchintegrationproducts) | **GET** /integrations/products | Search Integration Products.
*IntegrationProductsApi* | [**updateIntegrationProduct**](docs/IntegrationProductsApi.md#updateintegrationproduct) | **PUT** /integrations/products/{productId} | Updates an Integration Product.
*IntegrationTypesApi* | [**createIntegrationType**](docs/IntegrationTypesApi.md#createintegrationtype) | **POST** /integrations/types | Creates an Integration Type.
*IntegrationTypesApi* | [**deleteIntegrationType**](docs/IntegrationTypesApi.md#deleteintegrationtype) | **DELETE** /integrations/types/{typeId} | Removes an Integration Type.
*IntegrationTypesApi* | [**getIntegrationType**](docs/IntegrationTypesApi.md#getintegrationtype) | **GET** /integrations/types/{typeId} | Gets an Integration Type.
*IntegrationTypesApi* | [**searchIntegrationTypes**](docs/IntegrationTypesApi.md#searchintegrationtypes) | **GET** /integrations/types | Search Integration Types.
*IntegrationTypesApi* | [**updateIntegrationType**](docs/IntegrationTypesApi.md#updateintegrationtype) | **PUT** /integrations/types/{typeId} | Updates an Integration Type.
*IntegrationVendorsApi* | [**createIntegrationVendor**](docs/IntegrationVendorsApi.md#createintegrationvendor) | **POST** /integrations/vendors | Creates an Integration Vendor.
*IntegrationVendorsApi* | [**deleteIntegrationVendor**](docs/IntegrationVendorsApi.md#deleteintegrationvendor) | **DELETE** /integrations/vendors/{vendorId} | Removes an Integration Vendor.
*IntegrationVendorsApi* | [**getIntegrationVendor**](docs/IntegrationVendorsApi.md#getintegrationvendor) | **GET** /integrations/vendors/{vendorId} | Gets an Integration Vendor.
*IntegrationVendorsApi* | [**searchIntegrationVendors**](docs/IntegrationVendorsApi.md#searchintegrationvendors) | **GET** /integrations/vendors | Search Integration Vendors.
*IntegrationVendorsApi* | [**updateIntegrationVendor**](docs/IntegrationVendorsApi.md#updateintegrationvendor) | **PUT** /integrations/vendors/{vendorId} | Updates an Integration Vendor.
*InvitationsApi* | [**deleteTenantInvitationAsync**](docs/InvitationsApi.md#deletetenantinvitationasync) | **DELETE** /tenants/{tenantId}/invitations/{invitationId} | Deletes an invitation
*InvitationsApi* | [**getAllTenantInvitationsAsync**](docs/InvitationsApi.md#getalltenantinvitationsasync) | **GET** /tenants/{tenantId}/invitations | Retrieves a list of invitations associated to this tenant
*InvitationsApi* | [**getTenantInvitationByIdAsync**](docs/InvitationsApi.md#gettenantinvitationbyidasync) | **GET** /tenants/{tenantId}/invitations/{invitationId} | Retrieves a specific invitation
*InvitationsApi* | [**sendTenantInvitationAsync**](docs/InvitationsApi.md#sendtenantinvitationasync) | **POST** /tenants/{tenantId}/invitations | Creates and sends an invitation to a user
*JobExecutionLogsApi* | [**getAllTenantDataSyncJobExecutionLogs**](docs/JobExecutionLogsApi.md#getalltenantdatasyncjobexecutionlogs) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId}/executions/{jobExecutionId}/logs | Retrieves a list of DataSync Job Execution Logs
*JobExecutionsApi* | [**getAllTenantDataSyncJobExecutions**](docs/JobExecutionsApi.md#getalltenantdatasyncjobexecutions) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId}/executions | Retrieves a list of DataSync Job Executions
*JobExecutionsApi* | [**getTenantJobExecutionsByJobId**](docs/JobExecutionsApi.md#gettenantjobexecutionsbyjobid) | **GET** /tenants/{tenantId}/jobs/{jobId}/executions | Gets job executions by a given job Id
*JobTypesApi* | [**getAllTenantDataSyncJobTypes**](docs/JobTypesApi.md#getalltenantdatasyncjobtypes) | **GET** /tenants/{tenantId}/datasync/jobtypes | Retrieves a list of DataSync job types
*JobTypesApi* | [**getTenantDataSyncJobTypeProfileById**](docs/JobTypesApi.md#gettenantdatasyncjobtypeprofilebyid) | **GET** /tenants/{tenantId}/datasync/jobtypes/{jobTypeId} | Retrieves a specific DataSync job type using its primary key
*JobsApi* | [**activateTenantDataSyncJob**](docs/JobsApi.md#activatetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/activate | Activate a DataSync job matching the primary key
*JobsApi* | [**cancelJob**](docs/JobsApi.md#canceljob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/cancel | Requests a Job cancellation.
*JobsApi* | [**cancelTenantDataSyncJob**](docs/JobsApi.md#canceltenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/cancel | Cancel a DataSync job matching the primary key
*JobsApi* | [**createJob**](docs/JobsApi.md#createjob) | **POST** /tenants/{tenantId}/validations/jobs | Creates a Job.
*JobsApi* | [**createTenantDataSyncJob**](docs/JobsApi.md#createtenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs | Creates a new DataSync job
*JobsApi* | [**deactivateTenantDataSyncJob**](docs/JobsApi.md#deactivatetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/deactivate | Deactivate a DataSync job matching the primary key
*JobsApi* | [**deleteJob**](docs/JobsApi.md#deletejob) | **DELETE** /tenants/{tenantId}/validations/jobs/{jobId} | Deletes a Job.
*JobsApi* | [**deleteTenantDataSyncJob**](docs/JobsApi.md#deletetenantdatasyncjob) | **DELETE** /tenants/{tenantId}/datasync/jobs/{jobId} | Delete a DataSync job matching the primary key
*JobsApi* | [**executeJob**](docs/JobsApi.md#executejob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/execute | Requests a Job execution.
*JobsApi* | [**executeTenantDataSyncJob**](docs/JobsApi.md#executetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/execute | Execute a DataSync job matching the primary key
*JobsApi* | [**getAllTenantDataSyncJobs**](docs/JobsApi.md#getalltenantdatasyncjobs) | **GET** /tenants/{tenantId}/datasync/jobs | Retrieves a list of DataSync Jobs
*JobsApi* | [**getJobById**](docs/JobsApi.md#getjobbyid) | **GET** /tenants/{tenantId}/validations/jobs/{jobId} | Retrieves a Job by ID.
*JobsApi* | [**getJobs**](docs/JobsApi.md#getjobs) | **GET** /tenants/{tenantId}/validations/jobs | Retrieves a list of Jobs.
*JobsApi* | [**getTenantDataSyncJobProfileById**](docs/JobsApi.md#gettenantdatasyncjobprofilebyid) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId} | Retrieves a specific DataSync job using its primary key
*JobsApi* | [**restartJobSchedule**](docs/JobsApi.md#restartjobschedule) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/restart | Requests a Job schedule restart.
*JobsApi* | [**updateJob**](docs/JobsApi.md#updatejob) | **PUT** /tenants/{tenantId}/validations/jobs/{jobId} | Updates a Job.
*JobsApi* | [**updateTenantDataSyncJob**](docs/JobsApi.md#updatetenantdatasyncjob) | **PUT** /tenants/{tenantId}/datasync/jobs/{jobId} | Updates a DataSync job matching the primary key
*LogsApi* | [**getLogs**](docs/LogsApi.md#getlogs) | **GET** /tenants/{tenantId}/validations/logs | Retrieves a list of Logs.
*MyExtensionsApi* | [**removeUserExtension**](docs/MyExtensionsApi.md#removeuserextension) | **DELETE** /me/extensions/{code} | Removes a user\&#39;s profile extension.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/me/settings/{code}&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.
*MyExtensionsApi* | [**setUserExtension**](docs/MyExtensionsApi.md#setuserextension) | **POST** /me/extensions | Creates or update a user\&#39;s profile extension.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/me/settings&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.
*MyPreferencesApi* | [**getUserPreferences**](docs/MyPreferencesApi.md#getuserpreferences) | **GET** /me/preferences | Retrieves the user\&#39;s preferences.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/me/settings&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.
*MyPreferencesApi* | [**preference**](docs/MyPreferencesApi.md#preference) | **GET** /me/preferences/{code} | Retrieves a user\&#39;s preference by code.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/me/settings/{code}&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.
*MyPreferencesApi* | [**updateUserPreferenceAsync**](docs/MyPreferencesApi.md#updateuserpreferenceasync) | **POST** /me/preferences | Creates or update a user\&#39;s preference.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/me/settings&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.
*MyProfileApi* | [**getMyProfile**](docs/MyProfileApi.md#getmyprofile) | **GET** /v2/me | Get the profile of the user that is currently logged in.
*MyProfileApi* | [**getMyTenant**](docs/MyProfileApi.md#getmytenant) | **GET** /v2/me/tenants/{tenantId} | Get the tenant associated to the user.
*MyProfileApi* | [**getUserCacheAsync**](docs/MyProfileApi.md#getusercacheasync) | **GET** /me | Retrieves the profile of the user that is currently logged in, including the user\&#39;s preferences and its associated tenants
*MySettingsApi* | [**createMySetting**](docs/MySettingsApi.md#createmysetting) | **POST** /me/settings | Create a User-scope setting
*MySettingsApi* | [**deleteMySetting**](docs/MySettingsApi.md#deletemysetting) | **DELETE** /me/settings/{settingIdOrCode} | Delete the User-scope setting for a key, addressed by SettingType id or Code
*MySettingsApi* | [**getMySetting**](docs/MySettingsApi.md#getmysetting) | **GET** /me/settings/{settingIdOrCode} | Get a User-scope setting
*MySettingsApi* | [**searchMySettings**](docs/MySettingsApi.md#searchmysettings) | **GET** /me/settings | List User-scope settings
*MySettingsApi* | [**setMySetting**](docs/MySettingsApi.md#setmysetting) | **PUT** /me/settings | Create or update (upsert) a User-scope setting, addressed by the SettingTypeId in the body
*MySettingsApi* | [**updateMySetting**](docs/MySettingsApi.md#updatemysetting) | **PUT** /me/settings/{settingIdOrCode} | Update the User-scope setting for a key, addressed by SettingType id or Code
*MyTenantsApi* | [**getUserTenants**](docs/MyTenantsApi.md#getusertenants) | **GET** /me/tenants | Retrieves the Tenants of the User that is currently logged in.
*MyTenantsApi* | [**searchMyLicenses**](docs/MyTenantsApi.md#searchmylicenses) | **GET** /v2/me/tenants/{tenantId}/licenses | Search the user\&#39;s licenses.
*MyTenantsApi* | [**searchMyTenants**](docs/MyTenantsApi.md#searchmytenants) | **GET** /v2/me/tenants | Searches tenants associated to the user.
*ObservationSettingsApi* | [**addAvailablePersona**](docs/ObservationSettingsApi.md#addavailablepersona) | **POST** /tenants/{tenantId}/observations/settings/personas | Adds a persona for a given Tenant
*ObservationSettingsApi* | [**getApplicationSettings**](docs/ObservationSettingsApi.md#getapplicationsettings) | **GET** /tenants/{tenantId}/observations/settings/application | Gets the application settings for the tenant
*ObservationSettingsApi* | [**getPaginatedForms**](docs/ObservationSettingsApi.md#getpaginatedforms) | **GET** /tenants/{tenantId}/observations/forms | Get Paginated Forms
*ObservationSettingsApi* | [**getPaginatedPersonas**](docs/ObservationSettingsApi.md#getpaginatedpersonas) | **GET** /tenants/{tenantId}/observations/settings/personas | Gets available personas
*ObservationSettingsApi* | [**getPaginatedStaffClassifications**](docs/ObservationSettingsApi.md#getpaginatedstaffclassifications) | **GET** /tenants/{tenantId}/observations/settings/available-staffclassifications | Get Paginated Available StaffClassifications
*ObservationSettingsApi* | [**getStaffClassificationsSettings**](docs/ObservationSettingsApi.md#getstaffclassificationssettings) | **GET** /tenants/{tenantId}/observations/settings/staffclassifications | Gets the staffClassification settings for the tenant
*ObservationSettingsApi* | [**getTEATenantOrganizations**](docs/ObservationSettingsApi.md#getteatenantorganizations) | **GET** /tenants/{tenantId}/observations/tenantorganizations | Get TEA tenant organizations
*ObservationSettingsApi* | [**setApplicationSettings**](docs/ObservationSettingsApi.md#setapplicationsettings) | **POST** /tenants/{tenantId}/observations/settings/application | Sets the Application Settings of an Observation for a given Tenant
*ObservationSettingsApi* | [**setRolePersonasSettings**](docs/ObservationSettingsApi.md#setrolepersonassettings) | **POST** /tenants/{tenantId}/observations/settings/rolepersonas | Updates personas assigned to a role configuration of the tenants setting
*ObservationSettingsApi* | [**verifySysAdminCredentials**](docs/ObservationSettingsApi.md#verifysysadmincredentials) | **GET** /tenants/{tenantId}/observations/settings/verify-credentials | Gets the staffClassification settings for the tenant
*ObservationsApi* | [**createObservation**](docs/ObservationsApi.md#createobservation) | **POST** /tenants/{tenantId}/observations | Creates a new Observation for a given tenant
*ObservationsApi* | [**createObservationSubmission**](docs/ObservationsApi.md#createobservationsubmission) | **POST** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/submit | Creates a submission for an available form referencing an existing observation
*ObservationsApi* | [**deleteObservation**](docs/ObservationsApi.md#deleteobservation) | **DELETE** /tenants/{tenantId}/observations/{observationId} | Deletes an Observation for a given tenant
*ObservationsApi* | [**getAvailableCampusesTotalEvaluees**](docs/ObservationsApi.md#getavailablecampusestotalevaluees) | **GET** /tenants/{tenantId}/observations/total-evaluees | Get the total number of evaluees across all available campuses
*ObservationsApi* | [**getDashboard**](docs/ObservationsApi.md#getdashboard) | **GET** /tenants/{tenantId}/observations/dashboards/{dashboardId} | Get Observation Dashboard
*ObservationsApi* | [**getDashboardPreferences**](docs/ObservationsApi.md#getdashboardpreferences) | **GET** /tenants/{tenantId}/observations/dashboards/{dashboardId}/preferences | Save user preferences for a given Dashboard
*ObservationsApi* | [**getEvalueeSections**](docs/ObservationsApi.md#getevalueesections) | **GET** /tenants/{tenantId}/observations/evaluees/{evalueeId}/sections | Gets the Sections of an evaluee.
*ObservationsApi* | [**getFormQuestions**](docs/ObservationsApi.md#getformquestions) | **GET** /tenants/{tenantId}/observations/available-forms/{formId}/sections/{sectionId}/questions | Search Questions
*ObservationsApi* | [**getFormSections**](docs/ObservationsApi.md#getformsections) | **GET** /tenants/{tenantId}/observations/available-forms/{formId}/sections | Search Observation Form Sections
*ObservationsApi* | [**getObservationById**](docs/ObservationsApi.md#getobservationbyid) | **GET** /tenants/{tenantId}/observations/{observationId} | Get an Observation for a given tenant
*ObservationsApi* | [**getObservationDraft**](docs/ObservationsApi.md#getobservationdraft) | **GET** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/draft | Get an observation form\&#39;s draft
*ObservationsApi* | [**getObservationSubmission**](docs/ObservationsApi.md#getobservationsubmission) | **GET** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/submission | Gets a submission for a specific observation
*ObservationsApi* | [**getPaginatedAvailableCampuses**](docs/ObservationsApi.md#getpaginatedavailablecampuses) | **GET** /tenants/{tenantId}/observations/campuses | Get Available Campuses
*ObservationsApi* | [**getPaginatedAvailableForms**](docs/ObservationsApi.md#getpaginatedavailableforms) | **GET** /tenants/{tenantId}/observations/available-forms | Get Paginated Available Forms
*ObservationsApi* | [**getPaginatedCampusSections**](docs/ObservationsApi.md#getpaginatedcampussections) | **GET** /tenants/{tenantId}/observations/campuses/{campusId}/sections | Retrieves a list of Sections for a given available campus.
*ObservationsApi* | [**getPaginatedCampusesWithEvaluees**](docs/ObservationsApi.md#getpaginatedcampuseswithevaluees) | **GET** /tenants/{tenantId}/observations/campuses-with-evaluees | Get a paginated list of the available campuses that have evaluees, each with its complete list of evaluees.
*ObservationsApi* | [**getPaginatedEvaluees**](docs/ObservationsApi.md#getpaginatedevaluees) | **GET** /tenants/{tenantId}/observations/evaluees | Get paginated evaluees
*ObservationsApi* | [**getPaginatedObservations**](docs/ObservationsApi.md#getpaginatedobservations) | **GET** /tenants/{tenantId}/observations | Get Paginated Observations for a given tenant
*ObservationsApi* | [**getSubmittedObservationsCount**](docs/ObservationsApi.md#getsubmittedobservationscount) | **GET** /tenants/{tenantId}/submittedobservations | Get submitted Observations count
*ObservationsApi* | [**saveDashboardPreferences**](docs/ObservationsApi.md#savedashboardpreferences) | **POST** /tenants/{tenantId}/observations/dashboards/{dashboardId}/preferences | Save user preferences for a given Dashboard
*ObservationsApi* | [**searchPaginatedEvaluees**](docs/ObservationsApi.md#searchpaginatedevaluees) | **GET** /tenants/{tenantId}/observations/search/evaluees | Search paginated evaluees
*ObservationsApi* | [**updateObservation**](docs/ObservationsApi.md#updateobservation) | **PUT** /tenants/{tenantId}/observations/{observationId} | Update an Observation for a given tenant
*ObservationsApi* | [**upsertObservationDraft**](docs/ObservationsApi.md#upsertobservationdraft) | **POST** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/draft | Creates a draft for an observation forms
*ObservationsApi* | [**verifyDashboardAccess**](docs/ObservationsApi.md#verifydashboardaccess) | **POST** /tenants/{tenantId}/observations/dashboards/access | Verify user access to dashboards
*OnboardingStepsApi* | [**createOnboardingStep**](docs/OnboardingStepsApi.md#createonboardingstep) | **POST** /tenants/{tenantId}/onboardingsteps | Creates an Onboarding Step.
*OnboardingStepsApi* | [**getOnboardingSteps**](docs/OnboardingStepsApi.md#getonboardingsteps) | **GET** /tenants/{tenantId}/onboardingsteps | Gets a list of Onboarding Steps.
*OnboardingStepsApi* | [**updateOnboardingStep**](docs/OnboardingStepsApi.md#updateonboardingstep) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step.
*OnboardingStepsConnectionsApi* | [**createOnboardingStepConnection**](docs/OnboardingStepsConnectionsApi.md#createonboardingstepconnection) | **POST** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections | Creates an Onboarding Step connection.
*OnboardingStepsConnectionsApi* | [**getOnboardingStepConnectionById**](docs/OnboardingStepsConnectionsApi.md#getonboardingstepconnectionbyid) | **GET** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Get an Onboarding Step connection by Id
*OnboardingStepsConnectionsApi* | [**updateOnboardingStepConnection**](docs/OnboardingStepsConnectionsApi.md#updateonboardingstepconnection) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Update an Onboarding Step connection by Id
*OrganizationsApi* | [**createOrganizationAsync**](docs/OrganizationsApi.md#createorganizationasync) | **POST** /tenants/{tenantId}/organizations | Creates an Organization.
*OrganizationsApi* | [**deleteOrganizationAsync**](docs/OrganizationsApi.md#deleteorganizationasync) | **DELETE** /tenants/{tenantId}/organizations/{organizationIdentifier} | Deletes an Organization.
*OrganizationsApi* | [**getOrganizationByIdAsync**](docs/OrganizationsApi.md#getorganizationbyidasync) | **GET** /tenants/{tenantId}/organizations/{organizationIdentifier} | Retrieves an Organization by ID.
*OrganizationsApi* | [**getOrganizationsAsync**](docs/OrganizationsApi.md#getorganizationsasync) | **GET** /tenants/{tenantId}/organizations | Retrieves a list of Organizations.
*OrganizationsApi* | [**updateOrganizationAsync**](docs/OrganizationsApi.md#updateorganizationasync) | **PUT** /tenants/{tenantId}/organizations/{organizationIdentifier} | Updates an Organization.
*PartnershipsApi* | [**getAllPartnerships**](docs/PartnershipsApi.md#getallpartnerships) | **GET** /tenants/{tenantId}/partnerships | Retrieves a list of Partnerships.
*PartnershipsApi* | [**getPartnershipById**](docs/PartnershipsApi.md#getpartnershipbyid) | **GET** /tenants/{tenantId}/partnerships/{partnershipId} | Retrieves a Partnership by ID.
*ProvidersApi* | [**getAllTenantDataSyncProviders**](docs/ProvidersApi.md#getalltenantdatasyncproviders) | **GET** /tenants/{tenantId}/datasync/providers | Retrieves a list of DataSync providers
*ProvidersApi* | [**getTenantDataSyncProviderProfileById**](docs/ProvidersApi.md#gettenantdatasyncproviderprofilebyid) | **GET** /tenants/{tenantId}/datasync/providers/{providerId} | Retrieves a specific DataSync provider using its primary key
*QuestionsApi* | [**createQuestion**](docs/QuestionsApi.md#createquestion) | **POST** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions | Creates a new Question for a given section
*QuestionsApi* | [**deleteQuestion**](docs/QuestionsApi.md#deletequestion) | **DELETE** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Deletes a Question.
*QuestionsApi* | [**getQuestion**](docs/QuestionsApi.md#getquestion) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Get Question.
*QuestionsApi* | [**searchQuestions**](docs/QuestionsApi.md#searchquestions) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions | Search Questions
*QuestionsApi* | [**updateQuestion**](docs/QuestionsApi.md#updatequestion) | **PUT** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Updates a Question.
*RegistrationsApi* | [**getOnboardingApplicationsAsync**](docs/RegistrationsApi.md#getonboardingapplicationsasync) | **GET** /public/applications | Gets a list of applications available for registration/onboarding
*RegistrationsApi* | [**getRegistrationApprovalStatusAsync**](docs/RegistrationsApi.md#getregistrationapprovalstatusasync) | **GET** /registrations/{registrationId} | Gets the approval status of a registration
*RegistrationsApi* | [**submitTenantRegistrationAsync**](docs/RegistrationsApi.md#submittenantregistrationasync) | **POST** /registrations | Submits a tenant\&#39;s registration request
*RegistrationsAzureMarketplaceApi* | [**submitTenantRegistrationAzureMonaAsync**](docs/RegistrationsAzureMarketplaceApi.md#submittenantregistrationazuremonaasync) | **POST** /registrations/azure/mona | Submits a tenant\&#39;s registration request received through Azure [M]arketplace [On]boarding [A]ccelerator (MONA)
*ReportingPeriodsApi* | [**addReportingPeriodSubmissionMetrics**](docs/ReportingPeriodsApi.md#addreportingperiodsubmissionmetrics) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Adds Metrics to a Submission.
*ReportingPeriodsApi* | [**addReportingPeriodSubmissionMetricsBulk**](docs/ReportingPeriodsApi.md#addreportingperiodsubmissionmetricsbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics/bulk | Adds Metrics to a Submission in bulk.
*ReportingPeriodsApi* | [**cancelReportingPeriodSubmission**](docs/ReportingPeriodsApi.md#cancelreportingperiodsubmission) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/cancel | Cancels a Submission.
*ReportingPeriodsApi* | [**closeReportingPeriodAsync**](docs/ReportingPeriodsApi.md#closereportingperiodasync) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/close | Closes the state of a Reporting Period.
*ReportingPeriodsApi* | [**deleteReportingPeriodRules**](docs/ReportingPeriodsApi.md#deletereportingperiodrules) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules | Delete the Reporting Period and Associated Rules
*ReportingPeriodsApi* | [**getReportingPeriodCertificationStatus**](docs/ReportingPeriodsApi.md#getreportingperiodcertificationstatus) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/certificationstatus | Retrieves the Certification Status of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodRecords**](docs/ReportingPeriodsApi.md#getreportingperiodrecords) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/records | Retrieves the Invalid Records of all the Rules within a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodRuleRecords**](docs/ReportingPeriodsApi.md#getreportingperiodrulerecords) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records | Retrieves the Invalid Records of a Rule.
*ReportingPeriodsApi* | [**getReportingPeriodSubmission**](docs/ReportingPeriodsApi.md#getreportingperiodsubmission) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId} | Retrieves the Submission of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodSubmissionLatest**](docs/ReportingPeriodsApi.md#getreportingperiodsubmissionlatest) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/latest | Retrieves the latest Submission of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodSubmissionLogs**](docs/ReportingPeriodsApi.md#getreportingperiodsubmissionlogs) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/logs | Retrieves a list of Submission Logs of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodSubmissionMetrics**](docs/ReportingPeriodsApi.md#getreportingperiodsubmissionmetrics) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Retrieves the Metrics of a Submission.
*ReportingPeriodsApi* | [**getReportingPeriodSubmissions**](docs/ReportingPeriodsApi.md#getreportingperiodsubmissions) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions | Retrieves a list of Submissions of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodValidationSummary**](docs/ReportingPeriodsApi.md#getreportingperiodvalidationsummary) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/validationsummary | Retrieves the Validation Summary of a Reporting Period.
*ReportingPeriodsApi* | [**getReportingPeriodValidationSummaryByCategoryId**](docs/ReportingPeriodsApi.md#getreportingperiodvalidationsummarybycategoryid) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/validationsummary/categories/{categoryId} | Retrieves the Validation Summary of a Reporting Period for a Category.
*ReportingPeriodsApi* | [**getReportingPeriods**](docs/ReportingPeriodsApi.md#getreportingperiods) | **GET** /tenants/{tenantId}/statereporting/reportingperiods | Retrieves a list of Reporting Periods.
*ReportingPeriodsApi* | [**postReportingPeriod**](docs/ReportingPeriodsApi.md#postreportingperiod) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/post | Post a Reporting Period.
*ReportingPeriodsApi* | [**runReportingPeriodValidations**](docs/ReportingPeriodsApi.md#runreportingperiodvalidations) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/run | Run Reporting Period Validations.
*ReportingPeriodsApi* | [**setReportingPeriodRuleRecordExcludeFromPostFlagBulk**](docs/ReportingPeriodsApi.md#setreportingperiodrulerecordexcludefrompostflagbulk) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule\&#39;s Invalid Records.
*ReportingPeriodsApi* | [**setReportingPeriodSubmissionStatus**](docs/ReportingPeriodsApi.md#setreportingperiodsubmissionstatus) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/status | Sets the Status of a Submission.
*ReportingPeriodsApi* | [**toggleReportingPeriodSelection**](docs/ReportingPeriodsApi.md#togglereportingperiodselection) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/toggle | Toggles the Selected state of a Reporting Period.
*ReportingPeriodsApi* | [**updateReportingPeriodBulk**](docs/ReportingPeriodsApi.md#updatereportingperiodbulk) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods | Updates Reporting Periods in bulk.
*ReportsApi* | [**createReportAsync**](docs/ReportsApi.md#createreportasync) | **POST** /tenants/{tenantId}/analytics/reports | Creates a new report (Does not upload pbix file).
*ReportsApi* | [**deleteReportAsync**](docs/ReportsApi.md#deletereportasync) | **DELETE** /tenants/{tenantId}/analytics/reports/{reportId} | Removes a report.
*ReportsApi* | [**downloadReportAsync**](docs/ReportsApi.md#downloadreportasync) | **GET** /tenants/{tenantId}/analytics/reports/download/{reportId}/{groupId} | Retrieves the PBIX for any report in the list in order to download.
*ReportsApi* | [**getAllTenantAnalyticsWorkspaceReportsAsync**](docs/ReportsApi.md#getalltenantanalyticsworkspacereportsasync) | **GET** /tenants/{tenantId}/analytics/reports | Retrieves all reports.
*ReportsApi* | [**getAnalyticsTenantUsersAsync**](docs/ReportsApi.md#getanalyticstenantusersasync) | **GET** /tenants/{tenantId}/analytics/users | Searchable, paginated list of tenant users for the Manage Access \&quot;specific users\&quot; picker.
*ReportsApi* | [**getReportAccessAsync**](docs/ReportsApi.md#getreportaccessasync) | **GET** /tenants/{tenantId}/analytics/reports/{reportId}/access | Retrieves the audience-targeting (Manage Access) configuration for a report.
*ReportsApi* | [**getReportByIdAsync**](docs/ReportsApi.md#getreportbyidasync) | **GET** /tenants/{tenantId}/analytics/reports/{reportId} | Retrieves a Report by ID.
*ReportsApi* | [**syncLatestVersion**](docs/ReportsApi.md#synclatestversion) | **POST** /tenants/{tenantId}/analytics/reports/synclatestversion | Sync latest version
*ReportsApi* | [**syncWorkspacesAsync**](docs/ReportsApi.md#syncworkspacesasync) | **POST** /tenants/{tenantId}/analytics/reports/sync | Triggers workspace, ODS and DW automation.
*ReportsApi* | [**updateReportAccessAsync**](docs/ReportsApi.md#updatereportaccessasync) | **PUT** /tenants/{tenantId}/analytics/reports/{reportId}/access | Updates the audience-targeting (Manage Access) configuration for a report.
*ReportsApi* | [**updateReportAsync**](docs/ReportsApi.md#updatereportasync) | **PUT** /tenants/{tenantId}/analytics/reports/{reportId} | Updates a report.
*RulesApi* | [**createRule**](docs/RulesApi.md#createrule) | **POST** /tenants/{tenantId}/validations/rules | Creates a Rule.
*RulesApi* | [**deleteRule**](docs/RulesApi.md#deleterule) | **DELETE** /tenants/{tenantId}/validations/rules/{ruleId} | Deletes a Rule.
*RulesApi* | [**getRuleById**](docs/RulesApi.md#getrulebyid) | **GET** /tenants/{tenantId}/validations/rules/{ruleId} | Retrieves a Rule by ID.
*RulesApi* | [**getRules**](docs/RulesApi.md#getrules) | **GET** /tenants/{tenantId}/validations/rules | Retrieves a list of Rules.
*RulesApi* | [**updateRule**](docs/RulesApi.md#updaterule) | **PUT** /tenants/{tenantId}/validations/rules/{ruleId} | Updates a Rule.
*SectionsApi* | [**createSection**](docs/SectionsApi.md#createsection) | **POST** /tenants/{tenantId}/forms/{formId}/sections | Creates a new Section for a given form
*SectionsApi* | [**deleteSection**](docs/SectionsApi.md#deletesection) | **DELETE** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Deletes a Section.
*SectionsApi* | [**getSection**](docs/SectionsApi.md#getsection) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Get Section.
*SectionsApi* | [**getSectionAcademicSubjects**](docs/SectionsApi.md#getsectionacademicsubjects) | **GET** /tenants/{tenantId}/sections/academicSubjects | Retrieves a list of Section Academic Subjects.
*SectionsApi* | [**getSectionById**](docs/SectionsApi.md#getsectionbyid) | **GET** /tenants/{tenantId}/sections/{sectionId} | Retrieves a Section by ID.
*SectionsApi* | [**getSectionCourses**](docs/SectionsApi.md#getsectioncourses) | **GET** /tenants/{tenantId}/sections/courses | Retrieves a list of Section Courses.
*SectionsApi* | [**getSectionGradeLevels**](docs/SectionsApi.md#getsectiongradelevels) | **GET** /tenants/{tenantId}/sections/gradeLevels | Retrieves a list of Section Grade Levels.
*SectionsApi* | [**getSectionSchools**](docs/SectionsApi.md#getsectionschools) | **GET** /tenants/{tenantId}/sections/schools | Retrieves a list of Section Schools.
*SectionsApi* | [**getSectionSessions**](docs/SectionsApi.md#getsectionsessions) | **GET** /tenants/{tenantId}/sections/sessions | Retrieves a list of Section Sessions.
*SectionsApi* | [**getSectionTerms**](docs/SectionsApi.md#getsectionterms) | **GET** /tenants/{tenantId}/sections/terms | Retrieves a list of Section Terms.
*SectionsApi* | [**getSections**](docs/SectionsApi.md#getsections) | **GET** /tenants/{tenantId}/sections | Retrieves a list of Sections.
*SectionsApi* | [**searchSections**](docs/SectionsApi.md#searchsections) | **GET** /tenants/{tenantId}/forms/{formId}/sections | Search Sections
*SectionsApi* | [**updateSection**](docs/SectionsApi.md#updatesection) | **PUT** /tenants/{tenantId}/forms/{formId}/sections/{sectionId} | Updates a Section.
*SettingsApi* | [**getTenantSettings**](docs/SettingsApi.md#gettenantsettings) | **GET** /tenants/{tenantId}/settings | Retrieves a list of the Tenant\&#39;s settings.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/v2/tenants/{tenantId}/settings&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.
*SettingsApi* | [**getTenantSettingsByCode**](docs/SettingsApi.md#gettenantsettingsbycode) | **GET** /tenants/{tenantId}/settings/{code} | Retrieves a Tenant\&#39;s settings by code.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/v2/tenants/{tenantId}/settings/{code}&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.
*SettingsApi* | [**setTenantSettings**](docs/SettingsApi.md#settenantsettings) | **POST** /tenants/{tenantId}/settings/{code} | Creates/updates a Tenant\&#39;s settings.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/v2/tenants/{tenantId}/settings&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.
*StaffClassificationsApi* | [**createStaffClassification**](docs/StaffClassificationsApi.md#createstaffclassification) | **POST** /tenants/{tenantId}/staffclassifications | Creates a StaffClassification.
*StaffClassificationsApi* | [**deleteStaffClassification**](docs/StaffClassificationsApi.md#deletestaffclassification) | **DELETE** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Deletes a StaffClassification.
*StaffClassificationsApi* | [**getStaffClassificationById**](docs/StaffClassificationsApi.md#getstaffclassificationbyid) | **GET** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Retrieves a StaffClassification by ID.
*StaffClassificationsApi* | [**getStaffClassifications**](docs/StaffClassificationsApi.md#getstaffclassifications) | **GET** /tenants/{tenantId}/staffclassifications | Retrieves a list of StaffClassifications.
*StaffClassificationsApi* | [**getStaffClassificationsNamespaces**](docs/StaffClassificationsApi.md#getstaffclassificationsnamespaces) | **GET** /tenants/{tenantId}/staffclassifications/namespaces | Retrieves a list of unique Staff Classification Namespaces.
*StaffClassificationsApi* | [**updateStaffClassification**](docs/StaffClassificationsApi.md#updatestaffclassification) | **PUT** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Updates a StaffClassification.
*StateReportingStepsApi* | [**getSteps**](docs/StateReportingStepsApi.md#getsteps) | **GET** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Get Steps Status for the tenant.
*StateReportingStepsApi* | [**updateStep**](docs/StateReportingStepsApi.md#updatestep) | **POST** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Update Steps Status for the tenant.
*SubmissionsApi* | [**createSubmission**](docs/SubmissionsApi.md#createsubmission) | **POST** /tenants/{tenantId}/forms/{formId}/submissions | Creates a new Submission for a given question
*SubmissionsApi* | [**deleteSubmission**](docs/SubmissionsApi.md#deletesubmission) | **DELETE** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Deletes a Submission.
*SubmissionsApi* | [**exportSubmissions**](docs/SubmissionsApi.md#exportsubmissions) | **GET** /tenants/{tenantId}/forms/{formId}/submissions/export | Exports Submission data for a Form for a given tenant. (With JSON and CSV support)
*SubmissionsApi* | [**getSubmission**](docs/SubmissionsApi.md#getsubmission) | **GET** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Get Submission.
*SubmissionsApi* | [**searchSubmissions**](docs/SubmissionsApi.md#searchsubmissions) | **GET** /tenants/{tenantId}/forms/{formId}/submissions | Search Submissions
*SubmissionsApi* | [**updateSubmission**](docs/SubmissionsApi.md#updatesubmission) | **PUT** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Updates a Submission.
*SubscriptionsApi* | [**createTenantSubscriptionAsync**](docs/SubscriptionsApi.md#createtenantsubscriptionasync) | **POST** /tenants/{tenantId}/subscriptions | Creates a new subscription
*SubscriptionsApi* | [**getAllTenantSubscriptionApplications**](docs/SubscriptionsApi.md#getalltenantsubscriptionapplications) | **GET** /tenants/{tenantId}/subscriptions/applications | Retrieves a list of applications available for subscription.
*SubscriptionsApi* | [**getAllTenantSubscriptionsAsync**](docs/SubscriptionsApi.md#getalltenantsubscriptionsasync) | **GET** /tenants/{tenantId}/subscriptions | Retrieves a list of subscriptions associated to this tenant
*SubscriptionsApi* | [**getTenantSubscriptionProfileByIdAsync**](docs/SubscriptionsApi.md#gettenantsubscriptionprofilebyidasync) | **GET** /tenants/{tenantId}/subscriptions/{subscriptionId} | Retrieves a subscription
*SubscriptionsApi* | [**updateTenantSubscriptionAsync**](docs/SubscriptionsApi.md#updatetenantsubscriptionasync) | **PUT** /tenants/{tenantId}/subscriptions/{subscriptionId} | Updates a subscription
*TagsApi* | [**createTag**](docs/TagsApi.md#createtag) | **POST** /tenants/{tenantId}/validations/tags | Creates a Tag.
*TagsApi* | [**deleteTag**](docs/TagsApi.md#deletetag) | **DELETE** /tenants/{tenantId}/validations/tags/{tagId} | Deletes a Tag.
*TagsApi* | [**getTagById**](docs/TagsApi.md#gettagbyid) | **GET** /tenants/{tenantId}/validations/tags/{tagId} | Retrieves a Tag by ID.
*TagsApi* | [**getTags**](docs/TagsApi.md#gettags) | **GET** /tenants/{tenantId}/validations/tags | Retrieves a list of Tags.
*TagsApi* | [**updateTag**](docs/TagsApi.md#updatetag) | **PUT** /tenants/{tenantId}/validations/tags/{tagId} | Updates a Tag.
*TenantBrandingApi* | [**updateTenantBranding**](docs/TenantBrandingApi.md#updatetenantbranding) | **PUT** /tenants/{tenantId}/branding | Updates the branding of tenant
*TenantInstancesApi* | [**loadOnboardingStepEdFiApiMetadata**](docs/TenantInstancesApi.md#loadonboardingstepedfiapimetadata) | **POST** /tenants/{tenantId}/onboardingsteps/edfi-api-metadata | Loads connection metadata.
*TenantInstancesApi* | [**testOnboardingStepConnection**](docs/TenantInstancesApi.md#testonboardingstepconnection) | **POST** /tenants/{tenantId}/onboardingsteps/testconnection | Tests availability of provided connection metadata.
*TenantIntegrationsApi* | [**addTenantIntegration**](docs/TenantIntegrationsApi.md#addtenantintegration) | **POST** /tenants/{tenantId}/integrations | Creates an Integration for a tenant.
*TenantIntegrationsApi* | [**deleteTenantIntegration**](docs/TenantIntegrationsApi.md#deletetenantintegration) | **DELETE** /tenants/{tenantId}/integrations/{id} | Removes a tenant Integration.
*TenantIntegrationsApi* | [**getTenantIntegration**](docs/TenantIntegrationsApi.md#gettenantintegration) | **GET** /tenants/{tenantId}/integrations/{id} | Gets a tenant Integration.
*TenantIntegrationsApi* | [**searchIntegrations**](docs/TenantIntegrationsApi.md#searchintegrations) | **GET** /tenants/{tenantId}/integrations | Search a Tenant\&#39;s Integrations
*TenantIntegrationsApi* | [**updateTenantIntegration**](docs/TenantIntegrationsApi.md#updatetenantintegration) | **PUT** /tenants/{tenantId}/integrations/{id} | Updates a tenant Integration.
*TenantJobsDSLApi* | [**createDslJob**](docs/TenantJobsDSLApi.md#createdsljob) | **POST** /tenants/{tenantId}/jobs/dsl | Creates a DSL Sync Job for a given tenant
*TenantJobsDSLApi* | [**executeDslJob**](docs/TenantJobsDSLApi.md#executedsljob) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId}/execute | Executes a DSL Sync Job for a given tenant
*TenantJobsDSLApi* | [**getDslJob**](docs/TenantJobsDSLApi.md#getdsljob) | **GET** /tenants/{tenantId}/jobs/dsl/{jobId} | Retrieves a DSL jobs profile for a given tenant
*TenantJobsDSLApi* | [**updateDslJob**](docs/TenantJobsDSLApi.md#updatedsljob) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId} | Updates a DSL Sync Job for a given tenant
*TenantJobsInstructionalInsightsApi* | [**createInstructionalInsightsSecuritySyncJob**](docs/TenantJobsInstructionalInsightsApi.md#createinstructionalinsightssecuritysyncjob) | **POST** /tenants/{tenantId}/jobs/instructionalinsights | Creates an Instructional Insights Security Sync Job for a given tenant
*TenantJobsInstructionalInsightsApi* | [**executeInstructionalInsightsSecuritySyncJob**](docs/TenantJobsInstructionalInsightsApi.md#executeinstructionalinsightssecuritysyncjob) | **POST** /tenants/{tenantId}/jobs/instructionalinsights/execute | Executes an Instructional Insights Security Sync Job
*TenantJobsInstructionalInsightsApi* | [**getInstructionalInsightsSecuritySyncJob**](docs/TenantJobsInstructionalInsightsApi.md#getinstructionalinsightssecuritysyncjob) | **GET** /tenants/{tenantId}/jobs/instructionalinsights | Retrieves an Instructional Insights Security Sync Job for a given tenant
*TenantJobsInstructionalInsightsApi* | [**searchInstructionalInsightsSecuritySyncJobExecutionLogs**](docs/TenantJobsInstructionalInsightsApi.md#searchinstructionalinsightssecuritysyncjobexecutionlogs) | **GET** /tenants/{tenantId}/jobs/instructionalinsights/executions/{executionId}/logs | Searches Instructional Insights Security Sync Job Execution Logs for a given tenant and execution
*TenantJobsInstructionalInsightsApi* | [**searchInstructionalInsightsSecuritySyncJobExecutions**](docs/TenantJobsInstructionalInsightsApi.md#searchinstructionalinsightssecuritysyncjobexecutions) | **GET** /tenants/{tenantId}/jobs/instructionalinsights/executions | Searches Instructional Insights Security Sync Job Executions for a given tenant
*TenantJobsInstructionalInsightsApi* | [**updateInstructionalInsightsSecuritySyncJob**](docs/TenantJobsInstructionalInsightsApi.md#updateinstructionalinsightssecuritysyncjob) | **PUT** /tenants/{tenantId}/jobs/instructionalinsights | Updates an Instructional Insights Security Sync Job for a given tenant
*TenantSecurityScoreSyncApi* | [**createSecurityScoreSyncJob**](docs/TenantSecurityScoreSyncApi.md#createsecurityscoresyncjob) | **POST** /tenants/{tenantId}/jobs/securityscore | Creates an Security Score Sync Job for a given tenant
*TenantSecurityScoreSyncApi* | [**executeSecurityScoreSyncJob**](docs/TenantSecurityScoreSyncApi.md#executesecurityscoresyncjob) | **POST** /tenants/{tenantId}/jobs/securityscore/execute | Executes an Security Score Sync Job
*TenantSecurityScoreSyncApi* | [**getSecurityScoreSyncJob**](docs/TenantSecurityScoreSyncApi.md#getsecurityscoresyncjob) | **GET** /tenants/{tenantId}/jobs/securityscore | Retrieves a Security Score Sync Job for a given tenant
*TenantSecurityScoreSyncApi* | [**getSecurityScoreSyncJobExecution**](docs/TenantSecurityScoreSyncApi.md#getsecurityscoresyncjobexecution) | **GET** /tenants/{tenantId}/jobs/securityscore/{jobId}/executions/{jobExecutionId} | Retrieves a Security Score Sync Job Execution for a given tenant
*TenantSecurityScoreSyncApi* | [**updateSecurityScoreSyncJob**](docs/TenantSecurityScoreSyncApi.md#updatesecurityscoresyncjob) | **PUT** /tenants/{tenantId}/jobs/securityscore | Updates a Security Score Sync for a given tenant
*TenantSettingTypesApi* | [**getAllSettingTypes**](docs/TenantSettingTypesApi.md#getallsettingtypes) | **GET** /tenants/settings | Retrieves all setting types
*TenantSettingsApi* | [**createTenantSetting**](docs/TenantSettingsApi.md#createtenantsetting) | **POST** /v2/tenants/{tenantId}/settings | Create a Tenant-scope setting
*TenantSettingsApi* | [**deleteTenantSetting**](docs/TenantSettingsApi.md#deletetenantsetting) | **DELETE** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Delete the Tenant-scope setting for a key, addressed by SettingType id or Code
*TenantSettingsApi* | [**getTenantSetting**](docs/TenantSettingsApi.md#gettenantsetting) | **GET** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Get a Tenant-scope setting
*TenantSettingsApi* | [**searchTenantSettings**](docs/TenantSettingsApi.md#searchtenantsettings) | **GET** /v2/tenants/{tenantId}/settings | List Tenant-scope settings
*TenantSettingsApi* | [**setTenantSetting**](docs/TenantSettingsApi.md#settenantsetting) | **PUT** /v2/tenants/{tenantId}/settings | Create or update (upsert) a Tenant-scope setting, addressed by the SettingTypeId in the body
*TenantSettingsApi* | [**updateTenantSetting**](docs/TenantSettingsApi.md#updatetenantsetting) | **PUT** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Update the Tenant-scope setting for a key, addressed by SettingType id or Code
*TenantsApi* | [**getTenantByIdAsync**](docs/TenantsApi.md#gettenantbyidasync) | **GET** /tenants/{tenantId} | Retrieves the profile of a specific tenant
*TenantsApi* | [**updateTenantAsync**](docs/TenantsApi.md#updatetenantasync) | **PUT** /tenants/{tenantId} | Updates a tenant\&#39;s profile
*UsersApi* | [**activateTenantUserAsync**](docs/UsersApi.md#activatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/activate | Activates a user
*UsersApi* | [**createTenantLocalUserAsync**](docs/UsersApi.md#createtenantlocaluserasync) | **POST** /tenants/{tenantId}/users | Creates a user in the local identity provider
*UsersApi* | [**deactivateTenantUserAsync**](docs/UsersApi.md#deactivatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/deactivate | Deactivates a user
*UsersApi* | [**deleteTenantUserAsync**](docs/UsersApi.md#deletetenantuserasync) | **DELETE** /tenants/{tenantId}/users/{userId} | Deletes a user
*UsersApi* | [**getAllFormUsers**](docs/UsersApi.md#getallformusers) | **GET** /tenants/{tenantId}/forms/users | Get All Users
*UsersApi* | [**getAllTenantUsersAsync**](docs/UsersApi.md#getalltenantusersasync) | **GET** /tenants/{tenantId}/users | Retrieves a list of users associated to this tenant
*UsersApi* | [**getAllUsers**](docs/UsersApi.md#getallusers) | **GET** /tenants/{tenantId}/statereporting/users | Get All Users
*UsersApi* | [**getTenantUser**](docs/UsersApi.md#gettenantuser) | **GET** /v2/tenants/{tenantId}/users/{userId} | Get User
*UsersApi* | [**getTenantUserProfileByIdAsync**](docs/UsersApi.md#gettenantuserprofilebyidasync) | **GET** /tenants/{tenantId}/users/{userId} | Retrieves a user
*UsersApi* | [**getUserTenant**](docs/UsersApi.md#getusertenant) | **GET** /v2/tenants/{tenantId}/users/{userId}/tenant | Get User Tenant
*UsersApi* | [**getUserTenantStatusProfile**](docs/UsersApi.md#getusertenantstatusprofile) | **GET** /tenants/{tenantId}/users/{email}/status | Searches a user by email and retrieves it\&#39;s minimal information and status.
*UsersApi* | [**resetMfaStatusAsync**](docs/UsersApi.md#resetmfastatusasync) | **PUT** /tenants/{tenantId}/users/{userId}/resetmfa | Reset the MFA Status for the User
*UsersApi* | [**resetPasswordTenantUserAsync**](docs/UsersApi.md#resetpasswordtenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/resetpassword | Resets a user\&#39;s password
*UsersApi* | [**searchTenantUsers**](docs/UsersApi.md#searchtenantusers) | **GET** /v2/tenants/{tenantId}/users | Search Users
*UsersApi* | [**searchUserLicenses**](docs/UsersApi.md#searchuserlicenses) | **GET** /v2/tenants/{tenantId}/users/{userId}/licenses | Search User Licenses
*UsersApi* | [**searchUserLicensesBulk**](docs/UsersApi.md#searchuserlicensesbulk) | **GET** /v2/tenants/{tenantId}/users/licensesBulk | Search user licenses in bulk.
*UsersApi* | [**updateTenantUserAsync**](docs/UsersApi.md#updatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId} | Creates or updates a user
*UsersEducationOrganizationsApi* | [**addUserEducationOrganization**](docs/UsersEducationOrganizationsApi.md#addusereducationorganization) | **POST** /tenants/{tenantId}/users/{userId}/educationorganizations | Adds an Education Organization to a user.
*UsersEducationOrganizationsApi* | [**getUserEducationOrganizations**](docs/UsersEducationOrganizationsApi.md#getusereducationorganizations) | **GET** /tenants/{tenantId}/users/{userId}/educationorganizations | Gets the Education Organizations of a user.
*UsersEducationOrganizationsApi* | [**removeUserEducationOrganization**](docs/UsersEducationOrganizationsApi.md#removeusereducationorganization) | **DELETE** /tenants/{tenantId}/users/{userId}/educationorganizations/{educationOrganizationId} | Removes an Education Organization from a user.
*UsersEducationOrganizationsApi* | [**updateUserEducationOrganization**](docs/UsersEducationOrganizationsApi.md#updateusereducationorganization) | **PUT** /tenants/{tenantId}/users/{userId}/educationorganizations/{educationOrganizationId} | Updates the Education Organization of a user.
*UsersLicensesApi* | [**assignLicenseTenantUserAsync**](docs/UsersLicensesApi.md#assignlicensetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assign | Assigns a license to a user in the context of a specific tenant
*UsersLicensesApi* | [**assignLicenseTenantUserBulkAsync**](docs/UsersLicensesApi.md#assignlicensetenantuserbulkasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assignbulk | Assigns one or more licenses to a user in the context of a specific tenant
*UsersLicensesApi* | [**getAllTenantUserApplicationLicensesAsync**](docs/UsersLicensesApi.md#getalltenantuserapplicationlicensesasync) | **GET** /tenants/{tenantId}/users/{userId}/licenses | Retrieves a list of user licenses in the context of a specific tenant
*UsersLicensesApi* | [**revokeLicenseTenantUserAsync**](docs/UsersLicensesApi.md#revokelicensetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revoke | Revokes a license from a user in the context of a specific tenant
*UsersLicensesApi* | [**revokeLicenseTenantUserBulkAsync**](docs/UsersLicensesApi.md#revokelicensetenantuserbulkasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revokebulk | Revokes one or more licenses from a user in the context of a specific tenant
*UsersSEOAAsApi* | [**addUserSEOAA**](docs/UsersSEOAAsApi.md#adduserseoaa) | **POST** /v2/tenants/{tenantId}/users/{userId}/seoaas | Add User SEOAAs
*UsersSEOAAsApi* | [**deleteUserSEOAA**](docs/UsersSEOAAsApi.md#deleteuserseoaa) | **DELETE** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Delete User SEOAAs
*UsersSEOAAsApi* | [**searchUserSEOAA**](docs/UsersSEOAAsApi.md#searchuserseoaa) | **GET** /v2/tenants/{tenantId}/users/{userId}/seoaas | Search User SEOAAs
*UsersSEOAAsApi* | [**updateUserSEOAA**](docs/UsersSEOAAsApi.md#updateuserseoaa) | **PUT** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Update User SEOAAs
*UsersSectionsApi* | [**addUserSection**](docs/UsersSectionsApi.md#addusersection) | **POST** /tenants/{tenantId}/users/{userId}/sections | Adds a Section to a user.
*UsersSectionsApi* | [**addUserSectionBulk**](docs/UsersSectionsApi.md#addusersectionbulk) | **POST** /tenants/{tenantId}/users/{userId}/sections/bulk | Adds Sections to a user in bulk.
*UsersSectionsApi* | [**getUserSections**](docs/UsersSectionsApi.md#getusersections) | **GET** /tenants/{tenantId}/users/{userId}/sections | Gets the Sections of a user.
*UsersSectionsApi* | [**removeUserSection**](docs/UsersSectionsApi.md#removeusersection) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Removes a Section from a user.
*UsersSectionsApi* | [**removeUserSectionBulk**](docs/UsersSectionsApi.md#removeusersectionbulk) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/bulk | Removes Sections from a user in bulk.
*UsersSectionsApi* | [**updateUserSection**](docs/UsersSectionsApi.md#updateusersection) | **PUT** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Updates the Section of a user.
*UsersSectionsApi* | [**updateUserSectionBulk**](docs/UsersSectionsApi.md#updateusersectionbulk) | **PUT** /tenants/{tenantId}/users/{userId}/sections/bulk | Updates the Section of a user in bulk.
*V1Api* | [**releaseUserLockout**](docs/V1Api.md#releaseuserlockout) | **PUT** /tenants/{tenantId}/users/{userId}/releaselockout | 
*ValidationResultsAPIApi* | [**findResultsApiJobRunRecordsAsync**](docs/ValidationResultsAPIApi.md#findresultsapijobrunrecordsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/records | Retrieves a list of Job Run Records from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiJobRunRuleRecordsAsync**](docs/ValidationResultsAPIApi.md#findresultsapijobrunrulerecordsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId}/records | Retrieves a list of Job Run Rule Records from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiJobRunRulesAsync**](docs/ValidationResultsAPIApi.md#findresultsapijobrunrulesasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules | Retrieves a list of Job Run Rules from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiJobRunsAsync**](docs/ValidationResultsAPIApi.md#findresultsapijobrunsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs | Retrieves a list of Job Runs from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiJobsAsync**](docs/ValidationResultsAPIApi.md#findresultsapijobsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs | Retrieves a list of Jobs from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiRuleSummaries**](docs/ValidationResultsAPIApi.md#findresultsapirulesummaries) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/summary | Retrieves a list Rule Summaries from the Validation Results API.
*ValidationResultsAPIApi* | [**findResultsApiRulesAsync**](docs/ValidationResultsAPIApi.md#findresultsapirulesasync) | **GET** /tenants/{tenantId}/validations/results-api/rules | Retrieves a list of Rules from Validation Results API.
*ValidationResultsAPIApi* | [**getLatestJobRunAsync**](docs/ValidationResultsAPIApi.md#getlatestjobrunasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/latest | Retrieves the latest Job Run from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiJobById**](docs/ValidationResultsAPIApi.md#getresultsapijobbyid) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId} | Retrieves a Job by ID from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiJobRunByIdAsync**](docs/ValidationResultsAPIApi.md#getresultsapijobrunbyidasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId} | Retrieves a Job Run by ID from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiJobRunRuleByIdAsync**](docs/ValidationResultsAPIApi.md#getresultsapijobrunrulebyidasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId} | Retrieves a Job Run Rule by ID from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiRuleByIdAsync**](docs/ValidationResultsAPIApi.md#getresultsapirulebyidasync) | **GET** /tenants/{tenantId}/validations/results-api/rules/{ruleId} | Retrieves a Rule by ID from the Validation Results API.
*ValidationResultsAPIApi* | [**getResultsApiRuleSummary**](docs/ValidationResultsAPIApi.md#getresultsapirulesummary) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId}/summary | Get Rule Summary by ID from the Validation Results API.
*WebhooksApi* | [**createWebhookAsync**](docs/WebhooksApi.md#createwebhookasync) | **POST** /tenants/{tenantId}/webhooks | Creates a new Webhook
*WebhooksApi* | [**deleteWebhookAsync**](docs/WebhooksApi.md#deletewebhookasync) | **DELETE** /tenants/{tenantId}/webhooks/{webhookId} | Removes a webhook.
*WebhooksApi* | [**getAllWebhookSubscriptionsAsync**](docs/WebhooksApi.md#getallwebhooksubscriptionsasync) | **GET** /tenants/{tenantId}/webhooks/events | 
*WebhooksApi* | [**getAllWebhooksAsync**](docs/WebhooksApi.md#getallwebhooksasync) | **GET** /tenants/{tenantId}/webhooks | Retrieves a list of webhooks.
*WebhooksApi* | [**getWebhookByIdAsync**](docs/WebhooksApi.md#getwebhookbyidasync) | **GET** /tenants/{tenantId}/webhooks/{webhookId} | Retrieves a webhook by ID.
*WebhooksApi* | [**requestWebhookReRun**](docs/WebhooksApi.md#requestwebhookrerun) | **POST** /tenants/{tenantId}/webhooks/{webhookId}/dispatches/{dispatchId}/rerun | 
*WebhooksApi* | [**updateWebhookAsync**](docs/WebhooksApi.md#updatewebhookasync) | **PUT** /tenants/{tenantId}/webhooks/{webhookId} | Updates a webhook


### Documentation For Models

 - [AnalyticsApiADLSGen2ConnectorsV1AuthenticationType](docs/AnalyticsApiADLSGen2ConnectorsV1AuthenticationType.md)
 - [AnalyticsApiADLSGen2ConnectorsV1ServicePrincipalAuthentication](docs/AnalyticsApiADLSGen2ConnectorsV1ServicePrincipalAuthentication.md)
 - [AnalyticsApiCapacitiesV1AnalyticsCapacity](docs/AnalyticsApiCapacitiesV1AnalyticsCapacity.md)
 - [AnalyticsApiCapacitiesV1AssignCapacityRequest](docs/AnalyticsApiCapacitiesV1AssignCapacityRequest.md)
 - [AnalyticsApiCapacitiesV1CapacityResponse](docs/AnalyticsApiCapacitiesV1CapacityResponse.md)
 - [AnalyticsApiCapacitiesV1ResumeCapacityRequest](docs/AnalyticsApiCapacitiesV1ResumeCapacityRequest.md)
 - [AnalyticsApiCapacitiesV1SuspendCapacityRequest](docs/AnalyticsApiCapacitiesV1SuspendCapacityRequest.md)
 - [AnalyticsApiConfigurationsV1AnalyticsAzureAd](docs/AnalyticsApiConfigurationsV1AnalyticsAzureAd.md)
 - [AnalyticsApiConfigurationsV1AnalyticsConfiguration](docs/AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)
 - [AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel](docs/AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel.md)
 - [AnalyticsApiConfigurationsV1AnalyticsPowerBi](docs/AnalyticsApiConfigurationsV1AnalyticsPowerBi.md)
 - [AnalyticsApiConfigurationsV1AnalyticsTriggerOption](docs/AnalyticsApiConfigurationsV1AnalyticsTriggerOption.md)
 - [AnalyticsApiConfigurationsV1ConfigurationResponse](docs/AnalyticsApiConfigurationsV1ConfigurationResponse.md)
 - [AnalyticsApiConfigurationsV1CreateConfigurationRequest](docs/AnalyticsApiConfigurationsV1CreateConfigurationRequest.md)
 - [AnalyticsApiConfigurationsV1HasValidConfigurationResponse](docs/AnalyticsApiConfigurationsV1HasValidConfigurationResponse.md)
 - [AnalyticsApiConfigurationsV1TestConnectionResponse](docs/AnalyticsApiConfigurationsV1TestConnectionResponse.md)
 - [AnalyticsApiConfigurationsV1UpdateConfigurationRequest](docs/AnalyticsApiConfigurationsV1UpdateConfigurationRequest.md)
 - [AnalyticsApiConnectorsV1ConnectorDeletedResponse](docs/AnalyticsApiConnectorsV1ConnectorDeletedResponse.md)
 - [AnalyticsApiGroupsV1AddGroupUsersRequest](docs/AnalyticsApiGroupsV1AddGroupUsersRequest.md)
 - [AnalyticsApiGroupsV1AnalyticsGroupUser](docs/AnalyticsApiGroupsV1AnalyticsGroupUser.md)
 - [AnalyticsApiGroupsV1CreateGroupRequest](docs/AnalyticsApiGroupsV1CreateGroupRequest.md)
 - [AnalyticsApiGroupsV1GroupResponse](docs/AnalyticsApiGroupsV1GroupResponse.md)
 - [AnalyticsApiGroupsV1GroupUsersResponse](docs/AnalyticsApiGroupsV1GroupUsersResponse.md)
 - [AnalyticsApiGroupsV1GroupsResponse](docs/AnalyticsApiGroupsV1GroupsResponse.md)
 - [AnalyticsApiLakehousesV1LakehouseRecord](docs/AnalyticsApiLakehousesV1LakehouseRecord.md)
 - [AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse](docs/AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse.md)
 - [AnalyticsApiReportsV1AnalyticsEmbedToken](docs/AnalyticsApiReportsV1AnalyticsEmbedToken.md)
 - [AnalyticsApiReportsV1AnalyticsReport](docs/AnalyticsApiReportsV1AnalyticsReport.md)
 - [AnalyticsApiReportsV1AnalyticsReportDataset](docs/AnalyticsApiReportsV1AnalyticsReportDataset.md)
 - [AnalyticsApiReportsV1DownloadReportResponse](docs/AnalyticsApiReportsV1DownloadReportResponse.md)
 - [AnalyticsApiReportsV1ReportIdResponse](docs/AnalyticsApiReportsV1ReportIdResponse.md)
 - [AnalyticsApiReportsV1ReportPaginatedItemsResponse](docs/AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)
 - [AnalyticsApiReportsV1ReportPreferenceDetailsResponse](docs/AnalyticsApiReportsV1ReportPreferenceDetailsResponse.md)
 - [AnalyticsApiReportsV1ReportPreferencesResponse](docs/AnalyticsApiReportsV1ReportPreferencesResponse.md)
 - [AnalyticsApiReportsV1ReportPreferencesSavedResponse](docs/AnalyticsApiReportsV1ReportPreferencesSavedResponse.md)
 - [AnalyticsApiReportsV1ReportResponse](docs/AnalyticsApiReportsV1ReportResponse.md)
 - [AnalyticsApiReportsV1ReportSource](docs/AnalyticsApiReportsV1ReportSource.md)
 - [AnalyticsApiReportsV1SyncLatestVersionRequest](docs/AnalyticsApiReportsV1SyncLatestVersionRequest.md)
 - [AnalyticsApiReportsV1SyncWorkspacesRequest](docs/AnalyticsApiReportsV1SyncWorkspacesRequest.md)
 - [AnalyticsApiUserAuthorizationsV1SchoolYear](docs/AnalyticsApiUserAuthorizationsV1SchoolYear.md)
 - [AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse](docs/AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse.md)
 - [AnalyticsApiUserAuthorizationsV1UserAuthorizationsListResponse](docs/AnalyticsApiUserAuthorizationsV1UserAuthorizationsListResponse.md)
 - [AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse](docs/AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse.md)
 - [ApplicationApiApplicationV1ApplicationListResponse](docs/ApplicationApiApplicationV1ApplicationListResponse.md)
 - [ApplicationApiApplicationV1ApplicationProfileResponse](docs/ApplicationApiApplicationV1ApplicationProfileResponse.md)
 - [ApplicationApiApplicationV1ApplicationStatus](docs/ApplicationApiApplicationV1ApplicationStatus.md)
 - [ApplicationApiApplicationV1ApplicationSubscriptionType](docs/ApplicationApiApplicationV1ApplicationSubscriptionType.md)
 - [ApplicationApiApplicationV1ApplicationType](docs/ApplicationApiApplicationV1ApplicationType.md)
 - [ApplicationApiApplicationV1PaginatedItemsResponse](docs/ApplicationApiApplicationV1PaginatedItemsResponse.md)
 - [ApplicationApiApplicationV1Role](docs/ApplicationApiApplicationV1Role.md)
 - [ApplicationApiApplicationV1UrlType](docs/ApplicationApiApplicationV1UrlType.md)
 - [ChangeLogChangeV1ChangeLogResponse](docs/ChangeLogChangeV1ChangeLogResponse.md)
 - [ChangeLogChangeV1ChangeLogResponsePaginatedItemsViewModel](docs/ChangeLogChangeV1ChangeLogResponsePaginatedItemsViewModel.md)
 - [DataSyncApiConnectionV1ConnectionListResponse](docs/DataSyncApiConnectionV1ConnectionListResponse.md)
 - [DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel](docs/DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel.md)
 - [DataSyncApiConnectionV1ConnectionMetadata](docs/DataSyncApiConnectionV1ConnectionMetadata.md)
 - [DataSyncApiConnectionV1ConnectionProfileResponse](docs/DataSyncApiConnectionV1ConnectionProfileResponse.md)
 - [DataSyncApiConnectionV1ConnectionTestedResponse](docs/DataSyncApiConnectionV1ConnectionTestedResponse.md)
 - [DataSyncApiConnectionV1TestConnectionRequest](docs/DataSyncApiConnectionV1TestConnectionRequest.md)
 - [DataSyncApiDslV1CreateJobRequest](docs/DataSyncApiDslV1CreateJobRequest.md)
 - [DataSyncApiDslV1DslJobExecutedResponse](docs/DataSyncApiDslV1DslJobExecutedResponse.md)
 - [DataSyncApiDslV1DslProfile](docs/DataSyncApiDslV1DslProfile.md)
 - [DataSyncApiDslV1JobCreatedResponse](docs/DataSyncApiDslV1JobCreatedResponse.md)
 - [DataSyncApiDslV1UpdateJobRequest](docs/DataSyncApiDslV1UpdateJobRequest.md)
 - [DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobMode](docs/DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobMode.md)
 - [DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile](docs/DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile.md)
 - [DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProvider](docs/DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProvider.md)
 - [DataSyncApiEdFiRosterSyncV1UseSSAInsteadOfSEOAAOptions](docs/DataSyncApiEdFiRosterSyncV1UseSSAInsteadOfSEOAAOptions.md)
 - [DataSyncApiJobExecutionLogV1JobExecutionLogEntry](docs/DataSyncApiJobExecutionLogV1JobExecutionLogEntry.md)
 - [DataSyncApiJobExecutionLogV1JobExecutionLogEntryPaginatedItemsViewModel](docs/DataSyncApiJobExecutionLogV1JobExecutionLogEntryPaginatedItemsViewModel.md)
 - [DataSyncApiJobExecutionLogV1MessageType](docs/DataSyncApiJobExecutionLogV1MessageType.md)
 - [DataSyncApiJobExecutionV1ChildJob](docs/DataSyncApiJobExecutionV1ChildJob.md)
 - [DataSyncApiJobExecutionV1JobExecutionListResponse](docs/DataSyncApiJobExecutionV1JobExecutionListResponse.md)
 - [DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel](docs/DataSyncApiJobExecutionV1JobExecutionListResponsePaginatedItemsViewModel.md)
 - [DataSyncApiJobExecutionV1JobExecutionStatus](docs/DataSyncApiJobExecutionV1JobExecutionStatus.md)
 - [DataSyncApiJobExecutionV1Metric](docs/DataSyncApiJobExecutionV1Metric.md)
 - [DataSyncApiJobTypeV1JobMetadataField](docs/DataSyncApiJobTypeV1JobMetadataField.md)
 - [DataSyncApiJobTypeV1JobTypeListResponse](docs/DataSyncApiJobTypeV1JobTypeListResponse.md)
 - [DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel](docs/DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel.md)
 - [DataSyncApiJobTypeV1JobTypeProfileResponse](docs/DataSyncApiJobTypeV1JobTypeProfileResponse.md)
 - [DataSyncApiJobTypeV1Profile](docs/DataSyncApiJobTypeV1Profile.md)
 - [DataSyncApiJobV1ActivateJobRequest](docs/DataSyncApiJobV1ActivateJobRequest.md)
 - [DataSyncApiJobV1CancelJobRequest](docs/DataSyncApiJobV1CancelJobRequest.md)
 - [DataSyncApiJobV1ChildJob](docs/DataSyncApiJobV1ChildJob.md)
 - [DataSyncApiJobV1DataRefreshType](docs/DataSyncApiJobV1DataRefreshType.md)
 - [DataSyncApiJobV1DeactivateJobRequest](docs/DataSyncApiJobV1DeactivateJobRequest.md)
 - [DataSyncApiJobV1ExecuteJobRequest](docs/DataSyncApiJobV1ExecuteJobRequest.md)
 - [DataSyncApiJobV1JobExecutionMetadata](docs/DataSyncApiJobV1JobExecutionMetadata.md)
 - [DataSyncApiJobV1JobExecutionRequestedResponse](docs/DataSyncApiJobV1JobExecutionRequestedResponse.md)
 - [DataSyncApiJobV1JobExecutionStatus](docs/DataSyncApiJobV1JobExecutionStatus.md)
 - [DataSyncApiJobV1JobListResponse](docs/DataSyncApiJobV1JobListResponse.md)
 - [DataSyncApiJobV1JobListResponsePaginatedItemsViewModel](docs/DataSyncApiJobV1JobListResponsePaginatedItemsViewModel.md)
 - [DataSyncApiJobV1JobMetadata](docs/DataSyncApiJobV1JobMetadata.md)
 - [DataSyncApiJobV1JobProfileResponse](docs/DataSyncApiJobV1JobProfileResponse.md)
 - [DataSyncApiJobV1JobStatus](docs/DataSyncApiJobV1JobStatus.md)
 - [DataSyncApiJobV1Metric](docs/DataSyncApiJobV1Metric.md)
 - [DataSyncApiJobV1Schedule](docs/DataSyncApiJobV1Schedule.md)
 - [DataSyncApiProviderV1ConnectionMetadataField](docs/DataSyncApiProviderV1ConnectionMetadataField.md)
 - [DataSyncApiProviderV1ConnectionType](docs/DataSyncApiProviderV1ConnectionType.md)
 - [DataSyncApiProviderV1ProviderListResponse](docs/DataSyncApiProviderV1ProviderListResponse.md)
 - [DataSyncApiProviderV1ProviderListResponsePaginatedItemsViewModel](docs/DataSyncApiProviderV1ProviderListResponsePaginatedItemsViewModel.md)
 - [DataSyncApiProviderV1ProviderProfileResponse](docs/DataSyncApiProviderV1ProviderProfileResponse.md)
 - [DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile](docs/DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile.md)
 - [DataSyncApiSecurityScoreSyncV1SecurityScoreSyncJobExecutedResponse](docs/DataSyncApiSecurityScoreSyncV1SecurityScoreSyncJobExecutedResponse.md)
 - [DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile](docs/DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile.md)
 - [EdFiAdminApiApplicationAccessV1ApplicationAccessResponse](docs/EdFiAdminApiApplicationAccessV1ApplicationAccessResponse.md)
 - [EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel](docs/EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel.md)
 - [EdFiAdminApiApplicationAccessV1ApplicationUserAccessResponse](docs/EdFiAdminApiApplicationAccessV1ApplicationUserAccessResponse.md)
 - [EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest](docs/EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest.md)
 - [EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest](docs/EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest.md)
 - [EdGraphCommonErrorsCoreProblemDetails](docs/EdGraphCommonErrorsCoreProblemDetails.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsConnectionMetadata](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsConnectionMetadata.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminContactStudentRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminContactStudentRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateSchoolProgramRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateSchoolProgramRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminSetSchoolEnabledRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramCatalogEntryRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramCatalogEntryRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolProgramRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolProgramRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionValidationRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionValidationRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionValidationRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionValidationRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsDataRefreshType](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsDataRefreshType.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsJobCategory](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsJobCategory.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsJobMetadata](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsJobMetadata.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsSchedule](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsSchedule.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterClaimDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterClaimDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantAdditionalSetting](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantAdditionalSetting.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviderId](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviderId.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviderStatus](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviderStatus.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviders](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantIdentityProviders.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantSetting](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsTenantSetting.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactSignInUnlockedResultDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactSignInUnlockedResultDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminGradeCapacityDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminGradeCapacityDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolAssociationDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolAssociationDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolProgramResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolProgramResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraiserResponse](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraiserResponse.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraiserSearchStatus](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraiserSearchStatus.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffResponse](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffResponse.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchStatus](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchStatus.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionValidationResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionValidationResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionVisibilityConditionDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionVisibilityConditionDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionVisibilityRuleDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionVisibilityRuleDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesRole](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesRole.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDtoPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionListResponseDtoPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionProfileResponseDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesSubscriptionProfileResponseDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponse](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponse.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsLatestRunDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsLatestRunDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto](docs/EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody](docs/EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody](docs/EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody](docs/EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody](docs/EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest](docs/EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicense](docs/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicense.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseRole](docs/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseRole.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResult](docs/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResult.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk](docs/EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody](docs/EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody](docs/EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody](docs/EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody.md)
 - [EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody](docs/EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody.md)
 - [EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO](docs/EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO.md)
 - [EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfilePipelineDTO](docs/EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfilePipelineDTO.md)
 - [EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesMappedConnectorListResponse](docs/EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesMappedConnectorListResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLog](docs/EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLog.md)
 - [EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto](docs/EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto.md)
 - [EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult](docs/EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult.md)
 - [EdGraphHttpAggregatorsTenantApiServicesFormsV1Form](docs/EdGraphHttpAggregatorsTenantApiServicesFormsV1Form.md)
 - [EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest](docs/EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceCreatedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceCreatedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponse](docs/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceUpdatedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceUpdatedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsCampusWithEvalueesResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsCampusWithEvalueesResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsFormConfigurationRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsFormConfigurationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsFormConfigurationResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsFormConfigurationResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsFormVersionConfigurationRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsFormVersionConfigurationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsFormVersionConfigurationResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsFormVersionConfigurationResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsGetAvailableCampusesTotalEvalueesResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsGetAvailableCampusesTotalEvalueesResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsGetCampusesWithEvalueesResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsGetCampusesWithEvalueesResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsStaffClassificationNamespaceConfiguration](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsStaffClassificationNamespaceConfiguration.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsStaffClassificationNamespaceRole](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsStaffClassificationNamespaceRole.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertReportPreferenceDetails](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertReportPreferenceDetails.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse](docs/EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApi](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApi.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiDataModel](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiDataModel.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUrls](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUrls.md)
 - [EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest](docs/EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest](docs/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult](docs/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult.md)
 - [EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest](docs/EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse.md)
 - [EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest](docs/EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsRequestsReportAccessRequest](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsRequestsReportAccessRequest.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationRole](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationRole.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTileResponseWithUserApplicationLicense](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTileResponseWithUserApplicationLicense.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationUrl](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationUrl.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesClientBrandingResponse](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesClientBrandingResponse.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesReportAccessResponseDto](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesReportAccessResponseDto.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesTenantStatus](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesTenantStatus.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheTenantEducationOrganizationResponse](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheTenantEducationOrganizationResponse.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheTenantResponse](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheTenantResponse.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicense](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicense.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicense](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicense.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLogin](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLogin.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfilePreference](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfilePreference.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenant](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenant.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenantLicense](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenantLicense.md)
 - [EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenantLicenseRole](docs/EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserTenantLicenseRole.md)
 - [EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest](docs/EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest.md)
 - [EdGraphServicesStateReportingV1AddSubmissionMetricsRequest](docs/EdGraphServicesStateReportingV1AddSubmissionMetricsRequest.md)
 - [EdGraphServicesStateReportingV1Category](docs/EdGraphServicesStateReportingV1Category.md)
 - [EdGraphServicesStateReportingV1CreateEnvironmentRequest](docs/EdGraphServicesStateReportingV1CreateEnvironmentRequest.md)
 - [EdGraphServicesStateReportingV1CreateReportingPeriodRequest](docs/EdGraphServicesStateReportingV1CreateReportingPeriodRequest.md)
 - [EdGraphServicesStateReportingV1DataUser](docs/EdGraphServicesStateReportingV1DataUser.md)
 - [EdGraphServicesStateReportingV1EnvironmentCreatedResponse](docs/EdGraphServicesStateReportingV1EnvironmentCreatedResponse.md)
 - [EdGraphServicesStateReportingV1EnvironmentDeletedResponse](docs/EdGraphServicesStateReportingV1EnvironmentDeletedResponse.md)
 - [EdGraphServicesStateReportingV1EnvironmentListResponse](docs/EdGraphServicesStateReportingV1EnvironmentListResponse.md)
 - [EdGraphServicesStateReportingV1EnvironmentProfileResponse](docs/EdGraphServicesStateReportingV1EnvironmentProfileResponse.md)
 - [EdGraphServicesStateReportingV1EnvironmentUpdatedResponse](docs/EdGraphServicesStateReportingV1EnvironmentUpdatedResponse.md)
 - [EdGraphServicesStateReportingV1PaginatedCategories](docs/EdGraphServicesStateReportingV1PaginatedCategories.md)
 - [EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse](docs/EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse.md)
 - [EdGraphServicesStateReportingV1PaginatedRecords](docs/EdGraphServicesStateReportingV1PaginatedRecords.md)
 - [EdGraphServicesStateReportingV1PaginatedRecordsTypesReportingPeriodRecords](docs/EdGraphServicesStateReportingV1PaginatedRecordsTypesReportingPeriodRecords.md)
 - [EdGraphServicesStateReportingV1PaginatedRecordsTypesReportingPeriodRecordsTypesRule](docs/EdGraphServicesStateReportingV1PaginatedRecordsTypesReportingPeriodRecordsTypesRule.md)
 - [EdGraphServicesStateReportingV1PaginatedReportingPeriods](docs/EdGraphServicesStateReportingV1PaginatedReportingPeriods.md)
 - [EdGraphServicesStateReportingV1PaginatedRuleRecords](docs/EdGraphServicesStateReportingV1PaginatedRuleRecords.md)
 - [EdGraphServicesStateReportingV1PaginatedSubCategories](docs/EdGraphServicesStateReportingV1PaginatedSubCategories.md)
 - [EdGraphServicesStateReportingV1PaginatedSubmissionLogs](docs/EdGraphServicesStateReportingV1PaginatedSubmissionLogs.md)
 - [EdGraphServicesStateReportingV1PaginatedSubmissions](docs/EdGraphServicesStateReportingV1PaginatedSubmissions.md)
 - [EdGraphServicesStateReportingV1PipelineRun](docs/EdGraphServicesStateReportingV1PipelineRun.md)
 - [EdGraphServicesStateReportingV1PostReportingPeriodRequest](docs/EdGraphServicesStateReportingV1PostReportingPeriodRequest.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus](docs/EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodCertificationStatusCategory](docs/EdGraphServicesStateReportingV1ReportingPeriodCertificationStatusCategory.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodListResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodListResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodPostedResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodPostedResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodProfileResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodProfileResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodRunResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodRunResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodStep](docs/EdGraphServicesStateReportingV1ReportingPeriodStep.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodStepStatus](docs/EdGraphServicesStateReportingV1ReportingPeriodStepStatus.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodToggledResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodToggledResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodValidationSummary](docs/EdGraphServicesStateReportingV1ReportingPeriodValidationSummary.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId](docs/EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse](docs/EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse.md)
 - [EdGraphServicesStateReportingV1ReportingPeriodValidationsRunDto](docs/EdGraphServicesStateReportingV1ReportingPeriodValidationsRunDto.md)
 - [EdGraphServicesStateReportingV1Rule](docs/EdGraphServicesStateReportingV1Rule.md)
 - [EdGraphServicesStateReportingV1RunReportingPeriodRequest](docs/EdGraphServicesStateReportingV1RunReportingPeriodRequest.md)
 - [EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest](docs/EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest.md)
 - [EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest](docs/EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest.md)
 - [EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequestTypesRecord](docs/EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequestTypesRecord.md)
 - [EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest](docs/EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest.md)
 - [EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest](docs/EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest.md)
 - [EdGraphServicesStateReportingV1SetSubmissionStatusRequest](docs/EdGraphServicesStateReportingV1SetSubmissionStatusRequest.md)
 - [EdGraphServicesStateReportingV1SubCategory](docs/EdGraphServicesStateReportingV1SubCategory.md)
 - [EdGraphServicesStateReportingV1SubmissionCancelledResponse](docs/EdGraphServicesStateReportingV1SubmissionCancelledResponse.md)
 - [EdGraphServicesStateReportingV1SubmissionListResponse](docs/EdGraphServicesStateReportingV1SubmissionListResponse.md)
 - [EdGraphServicesStateReportingV1SubmissionLog](docs/EdGraphServicesStateReportingV1SubmissionLog.md)
 - [EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse](docs/EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse.md)
 - [EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse](docs/EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse.md)
 - [EdGraphServicesStateReportingV1SubmissionMetricsDetails](docs/EdGraphServicesStateReportingV1SubmissionMetricsDetails.md)
 - [EdGraphServicesStateReportingV1SubmissionMetricsResponse](docs/EdGraphServicesStateReportingV1SubmissionMetricsResponse.md)
 - [EdGraphServicesStateReportingV1SubmissionProfile](docs/EdGraphServicesStateReportingV1SubmissionProfile.md)
 - [EdGraphServicesStateReportingV1SubmissionStatus](docs/EdGraphServicesStateReportingV1SubmissionStatus.md)
 - [EdGraphServicesStateReportingV1SubmissionStatusSetResponse](docs/EdGraphServicesStateReportingV1SubmissionStatusSetResponse.md)
 - [EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest](docs/EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest.md)
 - [EdGraphServicesStateReportingV1UpdateEnvironmentRequest](docs/EdGraphServicesStateReportingV1UpdateEnvironmentRequest.md)
 - [EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest](docs/EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest.md)
 - [EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequestTypesReportingPeriod](docs/EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequestTypesReportingPeriod.md)
 - [EdGraphServicesStateReportingV1UpdateReportingPeriodRequest](docs/EdGraphServicesStateReportingV1UpdateReportingPeriodRequest.md)
 - [EdGraphServicesStateReportingV1ValidationResultRecord](docs/EdGraphServicesStateReportingV1ValidationResultRecord.md)
 - [EdGraphServicesStateReportingV1ValidationSummaryCategory](docs/EdGraphServicesStateReportingV1ValidationSummaryCategory.md)
 - [EdGraphServicesStateReportingV1ValidationSummarySubCategory](docs/EdGraphServicesStateReportingV1ValidationSummarySubCategory.md)
 - [EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest](docs/EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest.md)
 - [EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse](docs/EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse.md)
 - [EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest](docs/EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest.md)
 - [EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequestEntry](docs/EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequestEntry.md)
 - [EdfiAdminApiEdfiAdminV1AddSchoolYearRequest](docs/EdfiAdminApiEdfiAdminV1AddSchoolYearRequest.md)
 - [EdfiAdminApiEdfiAdminV1ApplicationEndpoint](docs/EdfiAdminApiEdfiAdminV1ApplicationEndpoint.md)
 - [EdfiAdminApiEdfiAdminV1AuthorizationStrategiesResponse](docs/EdfiAdminApiEdfiAdminV1AuthorizationStrategiesResponse.md)
 - [EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest](docs/EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest.md)
 - [EdfiAdminApiEdfiAdminV1ClaimSet](docs/EdfiAdminApiEdfiAdminV1ClaimSet.md)
 - [EdfiAdminApiEdfiAdminV1ClaimSetDetailsResourceClaim](docs/EdfiAdminApiEdfiAdminV1ClaimSetDetailsResourceClaim.md)
 - [EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1CloneInstanceRequest](docs/EdfiAdminApiEdfiAdminV1CloneInstanceRequest.md)
 - [EdfiAdminApiEdfiAdminV1CloneInstanceResponse](docs/EdfiAdminApiEdfiAdminV1CloneInstanceResponse.md)
 - [EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest](docs/EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest](docs/EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest](docs/EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest](docs/EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest](docs/EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateInstanceRequest](docs/EdfiAdminApiEdfiAdminV1CreateInstanceRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateInstanceRequestSchoolYear](docs/EdfiAdminApiEdfiAdminV1CreateInstanceRequestSchoolYear.md)
 - [EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest](docs/EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest](docs/EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest](docs/EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest.md)
 - [EdfiAdminApiEdfiAdminV1CreateVendorRequest](docs/EdfiAdminApiEdfiAdminV1CreateVendorRequest.md)
 - [EdfiAdminApiEdfiAdminV1DatabaseTier](docs/EdfiAdminApiEdfiAdminV1DatabaseTier.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse](docs/EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorMapping](docs/EdfiAdminApiEdfiAdminV1DescriptorMapping.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse](docs/EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorMappingModelEntity](docs/EdfiAdminApiEdfiAdminV1DescriptorMappingModelEntity.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse](docs/EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse](docs/EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse](docs/EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorType](docs/EdfiAdminApiEdfiAdminV1DescriptorType.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse](docs/EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse](docs/EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse.md)
 - [EdfiAdminApiEdfiAdminV1EdFiApplication](docs/EdfiAdminApiEdfiAdminV1EdFiApplication.md)
 - [EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse](docs/EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse.md)
 - [EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse](docs/EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1EdFiApplicationListResponse](docs/EdfiAdminApiEdfiAdminV1EdFiApplicationListResponse.md)
 - [EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse](docs/EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse.md)
 - [EdfiAdminApiEdfiAdminV1EdFiConnection](docs/EdfiAdminApiEdfiAdminV1EdFiConnection.md)
 - [EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse](docs/EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse.md)
 - [EdfiAdminApiEdfiAdminV1EdFiConnectionListModel](docs/EdfiAdminApiEdfiAdminV1EdFiConnectionListModel.md)
 - [EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse](docs/EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse.md)
 - [EdfiAdminApiEdfiAdminV1EdFiConnectionTier](docs/EdfiAdminApiEdfiAdminV1EdFiConnectionTier.md)
 - [EdfiAdminApiEdfiAdminV1EdFiConnectionTierListModel](docs/EdfiAdminApiEdfiAdminV1EdFiConnectionTierListModel.md)
 - [EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse](docs/EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptor](docs/EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptor.md)
 - [EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse](docs/EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse.md)
 - [EdfiAdminApiEdfiAdminV1EducationOrganization](docs/EdfiAdminApiEdfiAdminV1EducationOrganization.md)
 - [EdfiAdminApiEdfiAdminV1EducationOrganizationAddress](docs/EdfiAdminApiEdfiAdminV1EducationOrganizationAddress.md)
 - [EdfiAdminApiEdfiAdminV1EducationOrganizationCategoryDescriptor](docs/EdfiAdminApiEdfiAdminV1EducationOrganizationCategoryDescriptor.md)
 - [EdfiAdminApiEdfiAdminV1EducationServiceCenter](docs/EdfiAdminApiEdfiAdminV1EducationServiceCenter.md)
 - [EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse](docs/EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1GenderRepresentation](docs/EdfiAdminApiEdfiAdminV1GenderRepresentation.md)
 - [EdfiAdminApiEdfiAdminV1GenerateReportsResponse](docs/EdfiAdminApiEdfiAdminV1GenerateReportsResponse.md)
 - [EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse](docs/EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse.md)
 - [EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse](docs/EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse.md)
 - [EdfiAdminApiEdfiAdminV1Instance](docs/EdfiAdminApiEdfiAdminV1Instance.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse](docs/EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApiClientListResponse](docs/EdfiAdminApiEdfiAdminV1InstanceApiClientListResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse](docs/EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse](docs/EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse](docs/EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse](docs/EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse](docs/EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponse](docs/EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1InstanceDatabase](docs/EdfiAdminApiEdfiAdminV1InstanceDatabase.md)
 - [EdfiAdminApiEdfiAdminV1InstanceDatabaseJobs](docs/EdfiAdminApiEdfiAdminV1InstanceDatabaseJobs.md)
 - [EdfiAdminApiEdfiAdminV1InstanceDatabases](docs/EdfiAdminApiEdfiAdminV1InstanceDatabases.md)
 - [EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse](docs/EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceListModel](docs/EdfiAdminApiEdfiAdminV1InstanceListModel.md)
 - [EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1InstanceOdsDatabase](docs/EdfiAdminApiEdfiAdminV1InstanceOdsDatabase.md)
 - [EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse](docs/EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponse](docs/EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponse.md)
 - [EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1InstanceType](docs/EdfiAdminApiEdfiAdminV1InstanceType.md)
 - [EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse](docs/EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1LocalEducationAgency](docs/EdfiAdminApiEdfiAdminV1LocalEducationAgency.md)
 - [EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse](docs/EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponse](docs/EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponse.md)
 - [EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1OdsApiConnectionEndpoint](docs/EdfiAdminApiEdfiAdminV1OdsApiConnectionEndpoint.md)
 - [EdfiAdminApiEdfiAdminV1OdsApiDiscoveryApi](docs/EdfiAdminApiEdfiAdminV1OdsApiDiscoveryApi.md)
 - [EdfiAdminApiEdfiAdminV1OdsApiDiscoveryApiDataModel](docs/EdfiAdminApiEdfiAdminV1OdsApiDiscoveryApiDataModel.md)
 - [EdfiAdminApiEdfiAdminV1Onboarding](docs/EdfiAdminApiEdfiAdminV1Onboarding.md)
 - [EdfiAdminApiEdfiAdminV1OnboardingStep](docs/EdfiAdminApiEdfiAdminV1OnboardingStep.md)
 - [EdfiAdminApiEdfiAdminV1RaceRepresentation](docs/EdfiAdminApiEdfiAdminV1RaceRepresentation.md)
 - [EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse](docs/EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse.md)
 - [EdfiAdminApiEdfiAdminV1RelatedInstance](docs/EdfiAdminApiEdfiAdminV1RelatedInstance.md)
 - [EdfiAdminApiEdfiAdminV1ReportsStatusResponse](docs/EdfiAdminApiEdfiAdminV1ReportsStatusResponse.md)
 - [EdfiAdminApiEdfiAdminV1ResetInstanceResponse](docs/EdfiAdminApiEdfiAdminV1ResetInstanceResponse.md)
 - [EdfiAdminApiEdfiAdminV1ResourceClaim](docs/EdfiAdminApiEdfiAdminV1ResourceClaim.md)
 - [EdfiAdminApiEdfiAdminV1SaveClaimSetRequest](docs/EdfiAdminApiEdfiAdminV1SaveClaimSetRequest.md)
 - [EdfiAdminApiEdfiAdminV1SaveClaimSetResponse](docs/EdfiAdminApiEdfiAdminV1SaveClaimSetResponse.md)
 - [EdfiAdminApiEdfiAdminV1SchoolCountRepresentation](docs/EdfiAdminApiEdfiAdminV1SchoolCountRepresentation.md)
 - [EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse](docs/EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse.md)
 - [EdfiAdminApiEdfiAdminV1SecretEncryptionMetadata](docs/EdfiAdminApiEdfiAdminV1SecretEncryptionMetadata.md)
 - [EdfiAdminApiEdfiAdminV1SecretValueType](docs/EdfiAdminApiEdfiAdminV1SecretValueType.md)
 - [EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest](docs/EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest.md)
 - [EdfiAdminApiEdfiAdminV1StateEducationAgency](docs/EdfiAdminApiEdfiAdminV1StateEducationAgency.md)
 - [EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse](docs/EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse](docs/EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse.md)
 - [EdfiAdminApiEdfiAdminV1StudentEconomicSituationRepresentation](docs/EdfiAdminApiEdfiAdminV1StudentEconomicSituationRepresentation.md)
 - [EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse](docs/EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse.md)
 - [EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse](docs/EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse.md)
 - [EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse](docs/EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse.md)
 - [EdfiAdminApiEdfiAdminV1StudentProgramRepresentation](docs/EdfiAdminApiEdfiAdminV1StudentProgramRepresentation.md)
 - [EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse](docs/EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse.md)
 - [EdfiAdminApiEdfiAdminV1SyncApplicationRequest](docs/EdfiAdminApiEdfiAdminV1SyncApplicationRequest.md)
 - [EdfiAdminApiEdfiAdminV1SyncClaimSetRequest](docs/EdfiAdminApiEdfiAdminV1SyncClaimSetRequest.md)
 - [EdfiAdminApiEdfiAdminV1SyncEntry](docs/EdfiAdminApiEdfiAdminV1SyncEntry.md)
 - [EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest](docs/EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest.md)
 - [EdfiAdminApiEdfiAdminV1SyncResponse](docs/EdfiAdminApiEdfiAdminV1SyncResponse.md)
 - [EdfiAdminApiEdfiAdminV1SyncVendorRequest](docs/EdfiAdminApiEdfiAdminV1SyncVendorRequest.md)
 - [EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest](docs/EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest.md)
 - [EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse](docs/EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse.md)
 - [EdfiAdminApiEdfiAdminV1TierOdsApiConnection](docs/EdfiAdminApiEdfiAdminV1TierOdsApiConnection.md)
 - [EdfiAdminApiEdfiAdminV1TierOdsApiConnectionListModel](docs/EdfiAdminApiEdfiAdminV1TierOdsApiConnectionListModel.md)
 - [EdfiAdminApiEdfiAdminV1TierSqlConnection](docs/EdfiAdminApiEdfiAdminV1TierSqlConnection.md)
 - [EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse](docs/EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse.md)
 - [EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest](docs/EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest](docs/EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest](docs/EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest](docs/EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest](docs/EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest](docs/EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateInstanceRequest](docs/EdfiAdminApiEdfiAdminV1UpdateInstanceRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest](docs/EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest](docs/EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest](docs/EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest.md)
 - [EdfiAdminApiEdfiAdminV1UpdateVendorRequest](docs/EdfiAdminApiEdfiAdminV1UpdateVendorRequest.md)
 - [EdfiAdminApiEdfiAdminV1Vendor](docs/EdfiAdminApiEdfiAdminV1Vendor.md)
 - [EdfiAdminApiEdfiAdminV1VendorCreatedResponse](docs/EdfiAdminApiEdfiAdminV1VendorCreatedResponse.md)
 - [EdfiAdminApiEdfiAdminV1VendorListResponse](docs/EdfiAdminApiEdfiAdminV1VendorListResponse.md)
 - [EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel](docs/EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel.md)
 - [EdfiAdminApiEdfiAdminV1VendorProfileResponse](docs/EdfiAdminApiEdfiAdminV1VendorProfileResponse.md)
 - [EdfiAdminApiEdfiAdminV1VendorUpdatedResponse](docs/EdfiAdminApiEdfiAdminV1VendorUpdatedResponse.md)
 - [EnrollmentApiEnrollmentApplicationResponsesV1ApplicationPathwayMessage](docs/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationPathwayMessage.md)
 - [EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseContactMessage](docs/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseContactMessage.md)
 - [EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse](docs/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse.md)
 - [EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseScreenMessage](docs/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseScreenMessage.md)
 - [EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse](docs/EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse.md)
 - [EnrollmentApiEnrollmentStudentsV1AllowedApplicationProfileIdMessage](docs/EnrollmentApiEnrollmentStudentsV1AllowedApplicationProfileIdMessage.md)
 - [EnrollmentApiEnrollmentStudentsV1StudentContactMessage](docs/EnrollmentApiEnrollmentStudentsV1StudentContactMessage.md)
 - [EnrollmentApiEnrollmentStudentsV1StudentResponse](docs/EnrollmentApiEnrollmentStudentsV1StudentResponse.md)
 - [EnrollmentApiEnrollmentStudentsV1StudentsSearchResponse](docs/EnrollmentApiEnrollmentStudentsV1StudentsSearchResponse.md)
 - [EvaluationApiEvaluationSettingsV1ApplicationSetResponse](docs/EvaluationApiEvaluationSettingsV1ApplicationSetResponse.md)
 - [EvaluationApiEvaluationSettingsV1EvaluationSettingResponse](docs/EvaluationApiEvaluationSettingsV1EvaluationSettingResponse.md)
 - [EvaluationApiEvaluationSettingsV1FormConfigurationResponse](docs/EvaluationApiEvaluationSettingsV1FormConfigurationResponse.md)
 - [EvaluationApiEvaluationSettingsV1FormVersionConfigurationResponse](docs/EvaluationApiEvaluationSettingsV1FormVersionConfigurationResponse.md)
 - [EvaluationApiEvaluationSettingsV1PersonaResponse](docs/EvaluationApiEvaluationSettingsV1PersonaResponse.md)
 - [EvaluationApiEvaluationSettingsV1RoleConfigurationResponse](docs/EvaluationApiEvaluationSettingsV1RoleConfigurationResponse.md)
 - [EvaluationApiEvaluationSettingsV1ScheduleType](docs/EvaluationApiEvaluationSettingsV1ScheduleType.md)
 - [EvaluationApiEvaluationSettingsV1SetApplicationRequest](docs/EvaluationApiEvaluationSettingsV1SetApplicationRequest.md)
 - [EvaluationApiEvaluationSettingsV1SetFormConfigurationRequest](docs/EvaluationApiEvaluationSettingsV1SetFormConfigurationRequest.md)
 - [EvaluationApiEvaluationSettingsV1SetFormVersionConfigurationRequest](docs/EvaluationApiEvaluationSettingsV1SetFormVersionConfigurationRequest.md)
 - [EvaluationApiEvaluationSettingsV1SetUsersRequest](docs/EvaluationApiEvaluationSettingsV1SetUsersRequest.md)
 - [EvaluationApiEvaluationSettingsV1UsersSetResponse](docs/EvaluationApiEvaluationSettingsV1UsersSetResponse.md)
 - [EvaluationApiEvaluationsV1CampusResponse](docs/EvaluationApiEvaluationsV1CampusResponse.md)
 - [EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel](docs/EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel.md)
 - [EvaluationApiEvaluationsV1CreateEvaluationRequest](docs/EvaluationApiEvaluationsV1CreateEvaluationRequest.md)
 - [EvaluationApiEvaluationsV1EvaluationCountResponse](docs/EvaluationApiEvaluationsV1EvaluationCountResponse.md)
 - [EvaluationApiEvaluationsV1EvaluationCreatedResponse](docs/EvaluationApiEvaluationsV1EvaluationCreatedResponse.md)
 - [EvaluationApiEvaluationsV1EvaluationDeletedResponse](docs/EvaluationApiEvaluationsV1EvaluationDeletedResponse.md)
 - [EvaluationApiEvaluationsV1EvaluationResponse](docs/EvaluationApiEvaluationsV1EvaluationResponse.md)
 - [EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel](docs/EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel.md)
 - [EvaluationApiEvaluationsV1EvaluationStatus](docs/EvaluationApiEvaluationsV1EvaluationStatus.md)
 - [EvaluationApiEvaluationsV1EvaluationUpdatedResponse](docs/EvaluationApiEvaluationsV1EvaluationUpdatedResponse.md)
 - [EvaluationApiEvaluationsV1FormResponse](docs/EvaluationApiEvaluationsV1FormResponse.md)
 - [EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel](docs/EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel.md)
 - [EvaluationApiEvaluationsV1OrganizationDiscriminator](docs/EvaluationApiEvaluationsV1OrganizationDiscriminator.md)
 - [EvaluationApiEvaluationsV1OrganizationIdentifierType](docs/EvaluationApiEvaluationsV1OrganizationIdentifierType.md)
 - [EvaluationApiEvaluationsV1UpdateEvaluationRequest](docs/EvaluationApiEvaluationsV1UpdateEvaluationRequest.md)
 - [FormApiFormComponentsV1FormComponentResponse](docs/FormApiFormComponentsV1FormComponentResponse.md)
 - [FormApiFormComponentsV1FormComponentResponsePaginatedItemsViewModel](docs/FormApiFormComponentsV1FormComponentResponsePaginatedItemsViewModel.md)
 - [FormApiFormComponentsV1FormComponentType](docs/FormApiFormComponentsV1FormComponentType.md)
 - [FormApiFormsV1AudienceType](docs/FormApiFormsV1AudienceType.md)
 - [FormApiFormsV1CreateFormRequest](docs/FormApiFormsV1CreateFormRequest.md)
 - [FormApiFormsV1CreateFullFormRequest](docs/FormApiFormsV1CreateFullFormRequest.md)
 - [FormApiFormsV1CreateFullQuestionRequest](docs/FormApiFormsV1CreateFullQuestionRequest.md)
 - [FormApiFormsV1CreateFullQuestionValidationRequest](docs/FormApiFormsV1CreateFullQuestionValidationRequest.md)
 - [FormApiFormsV1CreateFullSectionRequest](docs/FormApiFormsV1CreateFullSectionRequest.md)
 - [FormApiFormsV1FormAccessResponse](docs/FormApiFormsV1FormAccessResponse.md)
 - [FormApiFormsV1FormAccessSetResponse](docs/FormApiFormsV1FormAccessSetResponse.md)
 - [FormApiFormsV1FormCreatedResponse](docs/FormApiFormsV1FormCreatedResponse.md)
 - [FormApiFormsV1FormDeletedResponse](docs/FormApiFormsV1FormDeletedResponse.md)
 - [FormApiFormsV1FormDuplicatedResponse](docs/FormApiFormsV1FormDuplicatedResponse.md)
 - [FormApiFormsV1FormSource](docs/FormApiFormsV1FormSource.md)
 - [FormApiFormsV1FormStatus](docs/FormApiFormsV1FormStatus.md)
 - [FormApiFormsV1FormUpdatedResponse](docs/FormApiFormsV1FormUpdatedResponse.md)
 - [FormApiFormsV1FullFormCreatedResponse](docs/FormApiFormsV1FullFormCreatedResponse.md)
 - [FormApiFormsV1FullFormUpdatedResponse](docs/FormApiFormsV1FullFormUpdatedResponse.md)
 - [FormApiFormsV1SetFormAccessRequest](docs/FormApiFormsV1SetFormAccessRequest.md)
 - [FormApiFormsV1UpdateFormRequest](docs/FormApiFormsV1UpdateFormRequest.md)
 - [FormApiFormsV1UpdateFullFormRequest](docs/FormApiFormsV1UpdateFullFormRequest.md)
 - [FormApiFormsV1UpdateFullQuestionRequest](docs/FormApiFormsV1UpdateFullQuestionRequest.md)
 - [FormApiFormsV1UpdateFullQuestionValidationRequest](docs/FormApiFormsV1UpdateFullQuestionValidationRequest.md)
 - [FormApiFormsV1UpdateFullSectionRequest](docs/FormApiFormsV1UpdateFullSectionRequest.md)
 - [FormApiQuestionsV1QuestionCreatedResponse](docs/FormApiQuestionsV1QuestionCreatedResponse.md)
 - [FormApiQuestionsV1QuestionDeletedResponse](docs/FormApiQuestionsV1QuestionDeletedResponse.md)
 - [FormApiQuestionsV1QuestionType](docs/FormApiQuestionsV1QuestionType.md)
 - [FormApiQuestionsV1QuestionUpdatedResponse](docs/FormApiQuestionsV1QuestionUpdatedResponse.md)
 - [FormApiQuestionsV1QuestionVisibilityCondition](docs/FormApiQuestionsV1QuestionVisibilityCondition.md)
 - [FormApiQuestionsV1QuestionVisibilityRule](docs/FormApiQuestionsV1QuestionVisibilityRule.md)
 - [FormApiSectionsV1CreateSectionRequest](docs/FormApiSectionsV1CreateSectionRequest.md)
 - [FormApiSectionsV1SectionCreatedResponse](docs/FormApiSectionsV1SectionCreatedResponse.md)
 - [FormApiSectionsV1SectionDeletedResponse](docs/FormApiSectionsV1SectionDeletedResponse.md)
 - [FormApiSectionsV1SectionResponse](docs/FormApiSectionsV1SectionResponse.md)
 - [FormApiSectionsV1SectionResponsePaginatedItemsViewModel](docs/FormApiSectionsV1SectionResponsePaginatedItemsViewModel.md)
 - [FormApiSectionsV1SectionUpdatedResponse](docs/FormApiSectionsV1SectionUpdatedResponse.md)
 - [FormApiSectionsV1UpdateSectionRequest](docs/FormApiSectionsV1UpdateSectionRequest.md)
 - [FormApiSubmissionsV1CreateSubmissionRequest](docs/FormApiSubmissionsV1CreateSubmissionRequest.md)
 - [FormApiSubmissionsV1ExportStatus](docs/FormApiSubmissionsV1ExportStatus.md)
 - [FormApiSubmissionsV1ExportType](docs/FormApiSubmissionsV1ExportType.md)
 - [FormApiSubmissionsV1SubmissionCreatedResponse](docs/FormApiSubmissionsV1SubmissionCreatedResponse.md)
 - [FormApiSubmissionsV1SubmissionDeletedResponse](docs/FormApiSubmissionsV1SubmissionDeletedResponse.md)
 - [FormApiSubmissionsV1SubmissionResponse](docs/FormApiSubmissionsV1SubmissionResponse.md)
 - [FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel](docs/FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel.md)
 - [FormApiSubmissionsV1SubmissionUpdatedResponse](docs/FormApiSubmissionsV1SubmissionUpdatedResponse.md)
 - [FormApiSubmissionsV1SubmissionsExportedResponse](docs/FormApiSubmissionsV1SubmissionsExportedResponse.md)
 - [FormApiSubmissionsV1UpdateSubmissionRequest](docs/FormApiSubmissionsV1UpdateSubmissionRequest.md)
 - [GoogleProtobufWellKnownTypesListValue](docs/GoogleProtobufWellKnownTypesListValue.md)
 - [GoogleProtobufWellKnownTypesNullValue](docs/GoogleProtobufWellKnownTypesNullValue.md)
 - [GoogleProtobufWellKnownTypesStruct](docs/GoogleProtobufWellKnownTypesStruct.md)
 - [GoogleProtobufWellKnownTypesValue](docs/GoogleProtobufWellKnownTypesValue.md)
 - [GoogleProtobufWellKnownTypesValueKindOneofCase](docs/GoogleProtobufWellKnownTypesValueKindOneofCase.md)
 - [IMSAdminApiV1ClientsAccessTokenType](docs/IMSAdminApiV1ClientsAccessTokenType.md)
 - [IMSAdminApiV1ClientsAddClientSecretRequest](docs/IMSAdminApiV1ClientsAddClientSecretRequest.md)
 - [IMSAdminApiV1ClientsClaim](docs/IMSAdminApiV1ClientsClaim.md)
 - [IMSAdminApiV1ClientsClientCreatedResponse](docs/IMSAdminApiV1ClientsClientCreatedResponse.md)
 - [IMSAdminApiV1ClientsClientDeletedResponse](docs/IMSAdminApiV1ClientsClientDeletedResponse.md)
 - [IMSAdminApiV1ClientsClientListResponse](docs/IMSAdminApiV1ClientsClientListResponse.md)
 - [IMSAdminApiV1ClientsClientProfileResponse](docs/IMSAdminApiV1ClientsClientProfileResponse.md)
 - [IMSAdminApiV1ClientsClientSecretAddedResponse](docs/IMSAdminApiV1ClientsClientSecretAddedResponse.md)
 - [IMSAdminApiV1ClientsClientSecretRegeneratedResponse](docs/IMSAdminApiV1ClientsClientSecretRegeneratedResponse.md)
 - [IMSAdminApiV1ClientsClientUpdatedResponse](docs/IMSAdminApiV1ClientsClientUpdatedResponse.md)
 - [IMSAdminApiV1ClientsPaginatedItemsResponse](docs/IMSAdminApiV1ClientsPaginatedItemsResponse.md)
 - [IMSAdminApiV1ClientsRegenerateClientSecretRequest](docs/IMSAdminApiV1ClientsRegenerateClientSecretRequest.md)
 - [IMSAdminApiV1ClientsSecret](docs/IMSAdminApiV1ClientsSecret.md)
 - [IMSAdminApiV1ClientsTokenExpiration](docs/IMSAdminApiV1ClientsTokenExpiration.md)
 - [IMSAdminApiV1ClientsTokenUsage](docs/IMSAdminApiV1ClientsTokenUsage.md)
 - [IMSAdminApiV1ClientsUpdateClientRequest](docs/IMSAdminApiV1ClientsUpdateClientRequest.md)
 - [IMSAdminApiV1ConnectionsConnectionDetails](docs/IMSAdminApiV1ConnectionsConnectionDetails.md)
 - [IMSAdminApiV1ConnectionsConnectionDetailsMetadata](docs/IMSAdminApiV1ConnectionsConnectionDetailsMetadata.md)
 - [IMSAdminApiV1ConnectionsConnectionListResponse](docs/IMSAdminApiV1ConnectionsConnectionListResponse.md)
 - [IMSAdminApiV1ConnectionsConnectionProfileResponse](docs/IMSAdminApiV1ConnectionsConnectionProfileResponse.md)
 - [IMSAdminApiV1ConnectionsConnectionTestedResponse](docs/IMSAdminApiV1ConnectionsConnectionTestedResponse.md)
 - [IMSAdminApiV1ConnectionsPagedConnectionsResponse](docs/IMSAdminApiV1ConnectionsPagedConnectionsResponse.md)
 - [IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest](docs/IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest.md)
 - [IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest](docs/IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest.md)
 - [IMSAdminApiV1ConnectionsTestConnectionDetailsRequest](docs/IMSAdminApiV1ConnectionsTestConnectionDetailsRequest.md)
 - [IMSAdminApiV1DbBackupCodesDbBackupCode](docs/IMSAdminApiV1DbBackupCodesDbBackupCode.md)
 - [IMSAdminApiV1InstancesCreateInstanceRequest](docs/IMSAdminApiV1InstancesCreateInstanceRequest.md)
 - [IMSAdminApiV1InstancesExportState](docs/IMSAdminApiV1InstancesExportState.md)
 - [IMSAdminApiV1InstancesGetInstanceCsvExportResponse](docs/IMSAdminApiV1InstancesGetInstanceCsvExportResponse.md)
 - [IMSAdminApiV1InstancesInstanceCsvExportedResponse](docs/IMSAdminApiV1InstancesInstanceCsvExportedResponse.md)
 - [IMSAdminApiV1InstancesInstanceEndpointsResponse](docs/IMSAdminApiV1InstancesInstanceEndpointsResponse.md)
 - [IMSAdminApiV1InstancesInstanceListResponse](docs/IMSAdminApiV1InstancesInstanceListResponse.md)
 - [IMSAdminApiV1InstancesInstanceProfileResponse](docs/IMSAdminApiV1InstancesInstanceProfileResponse.md)
 - [IMSAdminApiV1InstancesInstanceResetResponse](docs/IMSAdminApiV1InstancesInstanceResetResponse.md)
 - [IMSAdminApiV1InstancesInstanceTruncatedResponse](docs/IMSAdminApiV1InstancesInstanceTruncatedResponse.md)
 - [IMSAdminApiV1InstancesPagedInstancesResponse](docs/IMSAdminApiV1InstancesPagedInstancesResponse.md)
 - [IMSAdminApiV1InstancesUpdateInstanceRequest](docs/IMSAdminApiV1InstancesUpdateInstanceRequest.md)
 - [IMSAdminApiV1TiersTier](docs/IMSAdminApiV1TiersTier.md)
 - [IdentityApiApiClientV1AccessTokenType](docs/IdentityApiApiClientV1AccessTokenType.md)
 - [IdentityApiApiClientV1ApiClaim](docs/IdentityApiApiClientV1ApiClaim.md)
 - [IdentityApiApiClientV1ApiClientCreatedResponse](docs/IdentityApiApiClientV1ApiClientCreatedResponse.md)
 - [IdentityApiApiClientV1ApiClientListResponse](docs/IdentityApiApiClientV1ApiClientListResponse.md)
 - [IdentityApiApiClientV1ApiClientPaginatedItemsResponse](docs/IdentityApiApiClientV1ApiClientPaginatedItemsResponse.md)
 - [IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel](docs/IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel.md)
 - [IdentityApiApiClientV1ApiClientProfileResponse](docs/IdentityApiApiClientV1ApiClientProfileResponse.md)
 - [IdentityApiApiClientV1ApiClientSecretRegeneratedResponse](docs/IdentityApiApiClientV1ApiClientSecretRegeneratedResponse.md)
 - [IdentityApiApiClientV1ApiClientUpdatedResponse](docs/IdentityApiApiClientV1ApiClientUpdatedResponse.md)
 - [IdentityApiApiClientV1Claim](docs/IdentityApiApiClientV1Claim.md)
 - [IdentityApiApiClientV1CreateApiClientRequest](docs/IdentityApiApiClientV1CreateApiClientRequest.md)
 - [IdentityApiApiClientV1RegenerateApiClientSecretRequest](docs/IdentityApiApiClientV1RegenerateApiClientSecretRequest.md)
 - [IdentityApiApiClientV1TokenExpiration](docs/IdentityApiApiClientV1TokenExpiration.md)
 - [IdentityApiApiClientV1TokenUsage](docs/IdentityApiApiClientV1TokenUsage.md)
 - [IdentityApiApiClientV1UpdateApiClientRequest](docs/IdentityApiApiClientV1UpdateApiClientRequest.md)
 - [IdentityApiClientSettingsTypeV1ClientSettingsTypeResponse](docs/IdentityApiClientSettingsTypeV1ClientSettingsTypeResponse.md)
 - [IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse](docs/IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse.md)
 - [IdentityApiInstructionalInsightsV1CallbackNotificationMessage](docs/IdentityApiInstructionalInsightsV1CallbackNotificationMessage.md)
 - [IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest](docs/IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest.md)
 - [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse](docs/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse.md)
 - [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse](docs/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse.md)
 - [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionLogMessage](docs/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionLogMessage.md)
 - [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionMessage](docs/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionMessage.md)
 - [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionMetricMessage](docs/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutionMetricMessage.md)
 - [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobInputMessage](docs/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobInputMessage.md)
 - [IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse](docs/IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse.md)
 - [IdentityApiInstructionalInsightsV1JobExecutionMessage](docs/IdentityApiInstructionalInsightsV1JobExecutionMessage.md)
 - [IdentityApiInstructionalInsightsV1RetryPolicyMessage](docs/IdentityApiInstructionalInsightsV1RetryPolicyMessage.md)
 - [IdentityApiInstructionalInsightsV1ScheduleMessage](docs/IdentityApiInstructionalInsightsV1ScheduleMessage.md)
 - [IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse](docs/IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse.md)
 - [IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse](docs/IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse.md)
 - [IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest](docs/IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest.md)
 - [IdentityApiInvitationV1AssignLicenseRequest](docs/IdentityApiInvitationV1AssignLicenseRequest.md)
 - [IdentityApiInvitationV1InvitationListResponse](docs/IdentityApiInvitationV1InvitationListResponse.md)
 - [IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel](docs/IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel.md)
 - [IdentityApiInvitationV1InvitationResponse](docs/IdentityApiInvitationV1InvitationResponse.md)
 - [IdentityApiInvitationV1InvitationSentResponse](docs/IdentityApiInvitationV1InvitationSentResponse.md)
 - [IdentityApiInvitationV1InvitationStatus](docs/IdentityApiInvitationV1InvitationStatus.md)
 - [IdentityApiStaffClassificationV1CreateStaffClassificationRequest](docs/IdentityApiStaffClassificationV1CreateStaffClassificationRequest.md)
 - [IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse](docs/IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse.md)
 - [IdentityApiStaffClassificationV1GetStaffClassificationsResponse](docs/IdentityApiStaffClassificationV1GetStaffClassificationsResponse.md)
 - [IdentityApiStaffClassificationV1StaffClassificationCreatedResponse](docs/IdentityApiStaffClassificationV1StaffClassificationCreatedResponse.md)
 - [IdentityApiStaffClassificationV1StaffClassificationDeletedResponse](docs/IdentityApiStaffClassificationV1StaffClassificationDeletedResponse.md)
 - [IdentityApiStaffClassificationV1StaffClassificationLicense](docs/IdentityApiStaffClassificationV1StaffClassificationLicense.md)
 - [IdentityApiStaffClassificationV1StaffClassificationLicenseRequest](docs/IdentityApiStaffClassificationV1StaffClassificationLicenseRequest.md)
 - [IdentityApiStaffClassificationV1StaffClassificationResponse](docs/IdentityApiStaffClassificationV1StaffClassificationResponse.md)
 - [IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse](docs/IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse.md)
 - [IdentityApiStaffClassificationV1UpdateStaffClassificationRequest](docs/IdentityApiStaffClassificationV1UpdateStaffClassificationRequest.md)
 - [IdentityApiUserV1ActivateUserRequest](docs/IdentityApiUserV1ActivateUserRequest.md)
 - [IdentityApiUserV1AddSectionBulkRequest](docs/IdentityApiUserV1AddSectionBulkRequest.md)
 - [IdentityApiUserV1AddSectionBulkRequestTypesSectionDto](docs/IdentityApiUserV1AddSectionBulkRequestTypesSectionDto.md)
 - [IdentityApiUserV1AddSectionRequest](docs/IdentityApiUserV1AddSectionRequest.md)
 - [IdentityApiUserV1ComputedLicense](docs/IdentityApiUserV1ComputedLicense.md)
 - [IdentityApiUserV1ComputedLicenseApplicationRole](docs/IdentityApiUserV1ComputedLicenseApplicationRole.md)
 - [IdentityApiUserV1DeactivateUserRequest](docs/IdentityApiUserV1DeactivateUserRequest.md)
 - [IdentityApiUserV1EducationOrganization](docs/IdentityApiUserV1EducationOrganization.md)
 - [IdentityApiUserV1EducationOrganizationAddedResponse](docs/IdentityApiUserV1EducationOrganizationAddedResponse.md)
 - [IdentityApiUserV1EducationOrganizationPaginatedItemsResponse](docs/IdentityApiUserV1EducationOrganizationPaginatedItemsResponse.md)
 - [IdentityApiUserV1EducationOrganizationRemovedResponse](docs/IdentityApiUserV1EducationOrganizationRemovedResponse.md)
 - [IdentityApiUserV1EducationOrganizationUpdatedResponse](docs/IdentityApiUserV1EducationOrganizationUpdatedResponse.md)
 - [IdentityApiUserV1GetSEOAAsResponse](docs/IdentityApiUserV1GetSEOAAsResponse.md)
 - [IdentityApiUserV1GetSectionsResponse](docs/IdentityApiUserV1GetSectionsResponse.md)
 - [IdentityApiUserV1GetUserPreferencesResponse](docs/IdentityApiUserV1GetUserPreferencesResponse.md)
 - [IdentityApiUserV1LicenseAssignedBulkResponse](docs/IdentityApiUserV1LicenseAssignedBulkResponse.md)
 - [IdentityApiUserV1LicenseAssignedResponse](docs/IdentityApiUserV1LicenseAssignedResponse.md)
 - [IdentityApiUserV1LicenseRevokedBulkResponse](docs/IdentityApiUserV1LicenseRevokedBulkResponse.md)
 - [IdentityApiUserV1LicenseRevokedResponse](docs/IdentityApiUserV1LicenseRevokedResponse.md)
 - [IdentityApiUserV1LicenseStatus](docs/IdentityApiUserV1LicenseStatus.md)
 - [IdentityApiUserV1LocalUserCreatedResponse](docs/IdentityApiUserV1LocalUserCreatedResponse.md)
 - [IdentityApiUserV1PasswordResettedResponse](docs/IdentityApiUserV1PasswordResettedResponse.md)
 - [IdentityApiUserV1Preference](docs/IdentityApiUserV1Preference.md)
 - [IdentityApiUserV1ReleaseUserLockoutResponse](docs/IdentityApiUserV1ReleaseUserLockoutResponse.md)
 - [IdentityApiUserV1RemoveSectionBulkRequest](docs/IdentityApiUserV1RemoveSectionBulkRequest.md)
 - [IdentityApiUserV1ResetPasswordRequest](docs/IdentityApiUserV1ResetPasswordRequest.md)
 - [IdentityApiUserV1RevokeLicenseRequest](docs/IdentityApiUserV1RevokeLicenseRequest.md)
 - [IdentityApiUserV1RevokeStrategy](docs/IdentityApiUserV1RevokeStrategy.md)
 - [IdentityApiUserV1SEOAAAddedResponse](docs/IdentityApiUserV1SEOAAAddedResponse.md)
 - [IdentityApiUserV1SEOAAResponse](docs/IdentityApiUserV1SEOAAResponse.md)
 - [IdentityApiUserV1SEOAAUpdatedResponse](docs/IdentityApiUserV1SEOAAUpdatedResponse.md)
 - [IdentityApiUserV1SectionAddedBulkResponse](docs/IdentityApiUserV1SectionAddedBulkResponse.md)
 - [IdentityApiUserV1SectionAddedResponse](docs/IdentityApiUserV1SectionAddedResponse.md)
 - [IdentityApiUserV1SectionRemovedBulkResponse](docs/IdentityApiUserV1SectionRemovedBulkResponse.md)
 - [IdentityApiUserV1SectionRemovedResponse](docs/IdentityApiUserV1SectionRemovedResponse.md)
 - [IdentityApiUserV1SectionResponse](docs/IdentityApiUserV1SectionResponse.md)
 - [IdentityApiUserV1SectionResponseGetPaginatedItemsResponse](docs/IdentityApiUserV1SectionResponseGetPaginatedItemsResponse.md)
 - [IdentityApiUserV1SectionUpdatedBulkResponse](docs/IdentityApiUserV1SectionUpdatedBulkResponse.md)
 - [IdentityApiUserV1SectionUpdatedResponse](docs/IdentityApiUserV1SectionUpdatedResponse.md)
 - [IdentityApiUserV1SetUserExtensionRequest](docs/IdentityApiUserV1SetUserExtensionRequest.md)
 - [IdentityApiUserV1Tenant](docs/IdentityApiUserV1Tenant.md)
 - [IdentityApiUserV1TenantSource](docs/IdentityApiUserV1TenantSource.md)
 - [IdentityApiUserV1TenantStatus](docs/IdentityApiUserV1TenantStatus.md)
 - [IdentityApiUserV1TenantType](docs/IdentityApiUserV1TenantType.md)
 - [IdentityApiUserV1UpdateSectionBulkRequest](docs/IdentityApiUserV1UpdateSectionBulkRequest.md)
 - [IdentityApiUserV1UpdateSectionBulkRequestTypesSectionDto](docs/IdentityApiUserV1UpdateSectionBulkRequestTypesSectionDto.md)
 - [IdentityApiUserV1UpdateSectionRequest](docs/IdentityApiUserV1UpdateSectionRequest.md)
 - [IdentityApiUserV1UserActivatedResponse](docs/IdentityApiUserV1UserActivatedResponse.md)
 - [IdentityApiUserV1UserDeactivatedResponse](docs/IdentityApiUserV1UserDeactivatedResponse.md)
 - [IdentityApiUserV1UserExtension](docs/IdentityApiUserV1UserExtension.md)
 - [IdentityApiUserV1UserExtensionRemovedResponse](docs/IdentityApiUserV1UserExtensionRemovedResponse.md)
 - [IdentityApiUserV1UserExtensionSetResponse](docs/IdentityApiUserV1UserExtensionSetResponse.md)
 - [IdentityApiUserV1UserListResponse](docs/IdentityApiUserV1UserListResponse.md)
 - [IdentityApiUserV1UserListResponsePaginatedItemsViewModel](docs/IdentityApiUserV1UserListResponsePaginatedItemsViewModel.md)
 - [IdentityApiUserV1UserLogin](docs/IdentityApiUserV1UserLogin.md)
 - [IdentityApiUserV1UserPreferenceUpdatedResponse](docs/IdentityApiUserV1UserPreferenceUpdatedResponse.md)
 - [IdentityApiUserV1UserTenantProfile](docs/IdentityApiUserV1UserTenantProfile.md)
 - [IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel](docs/IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel.md)
 - [IdentityApiUserV1UserTenantProfileTypesUserTenantEducationOrganizationProfile](docs/IdentityApiUserV1UserTenantProfileTypesUserTenantEducationOrganizationProfile.md)
 - [IdentityApiUserV1UserTenantProfileTypesUserTenantLicenseProfile](docs/IdentityApiUserV1UserTenantProfileTypesUserTenantLicenseProfile.md)
 - [IdentityApiUserV1UserTenantProfileTypesUserTenantLicenseProfileTypesUserTenantLicenseRoleProfile](docs/IdentityApiUserV1UserTenantProfileTypesUserTenantLicenseProfileTypesUserTenantLicenseRoleProfile.md)
 - [IdentityApiUserV1UserTenantStatusProfile](docs/IdentityApiUserV1UserTenantStatusProfile.md)
 - [IdentityApiUserV1UserUpdatedResponse](docs/IdentityApiUserV1UserUpdatedResponse.md)
 - [IdentityApiUserV2TenantMeProfile](docs/IdentityApiUserV2TenantMeProfile.md)
 - [IdentityApiUserV2UserExtension](docs/IdentityApiUserV2UserExtension.md)
 - [IdentityApiUserV2UserLicenseProfileResponse](docs/IdentityApiUserV2UserLicenseProfileResponse.md)
 - [IdentityApiUserV2UserLicenseRole](docs/IdentityApiUserV2UserLicenseRole.md)
 - [IdentityApiUserV2UserLicensesResponse](docs/IdentityApiUserV2UserLicensesResponse.md)
 - [IdentityApiUserV2UserLogin](docs/IdentityApiUserV2UserLogin.md)
 - [IdentityApiUserV2UserMeProfile](docs/IdentityApiUserV2UserMeProfile.md)
 - [IdentityApiUserV2UserMeTenantsResponse](docs/IdentityApiUserV2UserMeTenantsResponse.md)
 - [IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel](docs/IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel.md)
 - [IdentityApiUserV2UserProfileResponse](docs/IdentityApiUserV2UserProfileResponse.md)
 - [IdentityApiUserV2UserTenantProfileResponse](docs/IdentityApiUserV2UserTenantProfileResponse.md)
 - [IdentityApiUserV2UsersSearchResponse](docs/IdentityApiUserV2UsersSearchResponse.md)
 - [MicrosoftAspNetCoreMvcNoContentResult](docs/MicrosoftAspNetCoreMvcNoContentResult.md)
 - [MicrosoftAspNetCoreMvcProblemDetails](docs/MicrosoftAspNetCoreMvcProblemDetails.md)
 - [MicrosoftAspNetCoreMvcValidationProblemDetails](docs/MicrosoftAspNetCoreMvcValidationProblemDetails.md)
 - [RegistrationApiRegistrationV2ApprovalStatus](docs/RegistrationApiRegistrationV2ApprovalStatus.md)
 - [RegistrationApiRegistrationV2SubmitTenantRegistrationRequest](docs/RegistrationApiRegistrationV2SubmitTenantRegistrationRequest.md)
 - [RegistrationApiRegistrationV2TenantType](docs/RegistrationApiRegistrationV2TenantType.md)
 - [SettingsApiClientSettingsV1ClientSettingMessage](docs/SettingsApiClientSettingsV1ClientSettingMessage.md)
 - [SettingsApiClientSettingsV1CreateClientSettingResponse](docs/SettingsApiClientSettingsV1CreateClientSettingResponse.md)
 - [SettingsApiClientSettingsV1SearchClientSettingsResponse](docs/SettingsApiClientSettingsV1SearchClientSettingsResponse.md)
 - [SettingsApiClientSettingsV1SetClientSettingResponse](docs/SettingsApiClientSettingsV1SetClientSettingResponse.md)
 - [SettingsApiTenantSettingsV1CreateTenantSettingResponse](docs/SettingsApiTenantSettingsV1CreateTenantSettingResponse.md)
 - [SettingsApiTenantSettingsV1SearchTenantSettingsResponse](docs/SettingsApiTenantSettingsV1SearchTenantSettingsResponse.md)
 - [SettingsApiTenantSettingsV1SetTenantSettingResponse](docs/SettingsApiTenantSettingsV1SetTenantSettingResponse.md)
 - [SettingsApiTenantSettingsV1TenantSettingMessage](docs/SettingsApiTenantSettingsV1TenantSettingMessage.md)
 - [SettingsApiUserSettingsV1CreateUserSettingResponse](docs/SettingsApiUserSettingsV1CreateUserSettingResponse.md)
 - [SettingsApiUserSettingsV1SearchUserSettingsResponse](docs/SettingsApiUserSettingsV1SearchUserSettingsResponse.md)
 - [SettingsApiUserSettingsV1SetUserSettingResponse](docs/SettingsApiUserSettingsV1SetUserSettingResponse.md)
 - [SettingsApiUserSettingsV1UserSettingMessage](docs/SettingsApiUserSettingsV1UserSettingMessage.md)
 - [SystemNetHttpStatusCode](docs/SystemNetHttpStatusCode.md)
 - [TenantApiIntegrationsV1CreateIntegrationProductRequest](docs/TenantApiIntegrationsV1CreateIntegrationProductRequest.md)
 - [TenantApiIntegrationsV1CreateIntegrationProductResponse](docs/TenantApiIntegrationsV1CreateIntegrationProductResponse.md)
 - [TenantApiIntegrationsV1CreateIntegrationRequest](docs/TenantApiIntegrationsV1CreateIntegrationRequest.md)
 - [TenantApiIntegrationsV1CreateIntegrationResponse](docs/TenantApiIntegrationsV1CreateIntegrationResponse.md)
 - [TenantApiIntegrationsV1CreateIntegrationTypeRequest](docs/TenantApiIntegrationsV1CreateIntegrationTypeRequest.md)
 - [TenantApiIntegrationsV1CreateIntegrationTypeResponse](docs/TenantApiIntegrationsV1CreateIntegrationTypeResponse.md)
 - [TenantApiIntegrationsV1CreateIntegrationVendorRequest](docs/TenantApiIntegrationsV1CreateIntegrationVendorRequest.md)
 - [TenantApiIntegrationsV1CreateIntegrationVendorResponse](docs/TenantApiIntegrationsV1CreateIntegrationVendorResponse.md)
 - [TenantApiIntegrationsV1DeleteIntegrationProductResponse](docs/TenantApiIntegrationsV1DeleteIntegrationProductResponse.md)
 - [TenantApiIntegrationsV1DeleteIntegrationResponse](docs/TenantApiIntegrationsV1DeleteIntegrationResponse.md)
 - [TenantApiIntegrationsV1DeleteIntegrationTypeResponse](docs/TenantApiIntegrationsV1DeleteIntegrationTypeResponse.md)
 - [TenantApiIntegrationsV1DeleteIntegrationVendorResponse](docs/TenantApiIntegrationsV1DeleteIntegrationVendorResponse.md)
 - [TenantApiIntegrationsV1GetIntegrationProductResponse](docs/TenantApiIntegrationsV1GetIntegrationProductResponse.md)
 - [TenantApiIntegrationsV1GetIntegrationResponse](docs/TenantApiIntegrationsV1GetIntegrationResponse.md)
 - [TenantApiIntegrationsV1GetIntegrationTypeResponse](docs/TenantApiIntegrationsV1GetIntegrationTypeResponse.md)
 - [TenantApiIntegrationsV1GetIntegrationVendorResponse](docs/TenantApiIntegrationsV1GetIntegrationVendorResponse.md)
 - [TenantApiIntegrationsV1Integration](docs/TenantApiIntegrationsV1Integration.md)
 - [TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel](docs/TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel.md)
 - [TenantApiIntegrationsV1IntegrationProduct](docs/TenantApiIntegrationsV1IntegrationProduct.md)
 - [TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel](docs/TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel.md)
 - [TenantApiIntegrationsV1IntegrationType](docs/TenantApiIntegrationsV1IntegrationType.md)
 - [TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel](docs/TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel.md)
 - [TenantApiIntegrationsV1IntegrationVendor](docs/TenantApiIntegrationsV1IntegrationVendor.md)
 - [TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel](docs/TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel.md)
 - [TenantApiIntegrationsV1UpdateIntegrationProductRequest](docs/TenantApiIntegrationsV1UpdateIntegrationProductRequest.md)
 - [TenantApiIntegrationsV1UpdateIntegrationRequest](docs/TenantApiIntegrationsV1UpdateIntegrationRequest.md)
 - [TenantApiIntegrationsV1UpdateIntegrationTypeRequest](docs/TenantApiIntegrationsV1UpdateIntegrationTypeRequest.md)
 - [TenantApiIntegrationsV1UpdateIntegrationVendorRequest](docs/TenantApiIntegrationsV1UpdateIntegrationVendorRequest.md)
 - [TenantApiPartnershipV1PaginatedItemsResponse](docs/TenantApiPartnershipV1PaginatedItemsResponse.md)
 - [TenantApiPartnershipV1ParternshipTenantResponse](docs/TenantApiPartnershipV1ParternshipTenantResponse.md)
 - [TenantApiPartnershipV1PartnershipByIdResponse](docs/TenantApiPartnershipV1PartnershipByIdResponse.md)
 - [TenantApiPartnershipV1PartnershipResponse](docs/TenantApiPartnershipV1PartnershipResponse.md)
 - [TenantApiPartnershipV1PartnershipSyncDTO](docs/TenantApiPartnershipV1PartnershipSyncDTO.md)
 - [TenantApiPartnershipV1PartnershipSyncDirection](docs/TenantApiPartnershipV1PartnershipSyncDirection.md)
 - [TenantApiPartnershipV1PartnershipSyncType](docs/TenantApiPartnershipV1PartnershipSyncType.md)
 - [TenantApiPartnershipV1TenantType](docs/TenantApiPartnershipV1TenantType.md)
 - [TenantApiSectionsV1AcademicSubjectListResponse](docs/TenantApiSectionsV1AcademicSubjectListResponse.md)
 - [TenantApiSectionsV1CourseListResponse](docs/TenantApiSectionsV1CourseListResponse.md)
 - [TenantApiSectionsV1GradeLevelListResponse](docs/TenantApiSectionsV1GradeLevelListResponse.md)
 - [TenantApiSectionsV1PaginatedAcademicSubjectsResponse](docs/TenantApiSectionsV1PaginatedAcademicSubjectsResponse.md)
 - [TenantApiSectionsV1PaginatedCoursesResponse](docs/TenantApiSectionsV1PaginatedCoursesResponse.md)
 - [TenantApiSectionsV1PaginatedGradeLevelsResponse](docs/TenantApiSectionsV1PaginatedGradeLevelsResponse.md)
 - [TenantApiSectionsV1PaginatedItemsResponse](docs/TenantApiSectionsV1PaginatedItemsResponse.md)
 - [TenantApiSectionsV1PaginatedSchoolsResponse](docs/TenantApiSectionsV1PaginatedSchoolsResponse.md)
 - [TenantApiSectionsV1PaginatedSessionsResponse](docs/TenantApiSectionsV1PaginatedSessionsResponse.md)
 - [TenantApiSectionsV1PaginatedTermsResponse](docs/TenantApiSectionsV1PaginatedTermsResponse.md)
 - [TenantApiSectionsV1SchoolListResponse](docs/TenantApiSectionsV1SchoolListResponse.md)
 - [TenantApiSectionsV1SectionListResponse](docs/TenantApiSectionsV1SectionListResponse.md)
 - [TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse](docs/TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse.md)
 - [TenantApiSectionsV1SectionProfileResponse](docs/TenantApiSectionsV1SectionProfileResponse.md)
 - [TenantApiSectionsV1SectionSource](docs/TenantApiSectionsV1SectionSource.md)
 - [TenantApiSectionsV1SessionListResponse](docs/TenantApiSectionsV1SessionListResponse.md)
 - [TenantApiSectionsV1TermListResponse](docs/TenantApiSectionsV1TermListResponse.md)
 - [TenantApiTenantV1CreateDomainRequest](docs/TenantApiTenantV1CreateDomainRequest.md)
 - [TenantApiTenantV1CreateOrganizationRequest](docs/TenantApiTenantV1CreateOrganizationRequest.md)
 - [TenantApiTenantV1CreateSubscriptionRequest](docs/TenantApiTenantV1CreateSubscriptionRequest.md)
 - [TenantApiTenantV1DeploymentType](docs/TenantApiTenantV1DeploymentType.md)
 - [TenantApiTenantV1DomainCreatedResponse](docs/TenantApiTenantV1DomainCreatedResponse.md)
 - [TenantApiTenantV1DomainProfileResponse](docs/TenantApiTenantV1DomainProfileResponse.md)
 - [TenantApiTenantV1DomainStatus](docs/TenantApiTenantV1DomainStatus.md)
 - [TenantApiTenantV1DomainUpdatedResponse](docs/TenantApiTenantV1DomainUpdatedResponse.md)
 - [TenantApiTenantV1DomainVerifiedResponse](docs/TenantApiTenantV1DomainVerifiedResponse.md)
 - [TenantApiTenantV1GetAppSettingsResponse](docs/TenantApiTenantV1GetAppSettingsResponse.md)
 - [TenantApiTenantV1GetOrganizationsPaginatedResponse](docs/TenantApiTenantV1GetOrganizationsPaginatedResponse.md)
 - [TenantApiTenantV1IdentityProviderId](docs/TenantApiTenantV1IdentityProviderId.md)
 - [TenantApiTenantV1IdentityProviderStatus](docs/TenantApiTenantV1IdentityProviderStatus.md)
 - [TenantApiTenantV1LicenseType](docs/TenantApiTenantV1LicenseType.md)
 - [TenantApiTenantV1Onboarding](docs/TenantApiTenantV1Onboarding.md)
 - [TenantApiTenantV1OnboardingStep](docs/TenantApiTenantV1OnboardingStep.md)
 - [TenantApiTenantV1OnboardingStepsReponse](docs/TenantApiTenantV1OnboardingStepsReponse.md)
 - [TenantApiTenantV1Organization](docs/TenantApiTenantV1Organization.md)
 - [TenantApiTenantV1OrganizationCreatedResponse](docs/TenantApiTenantV1OrganizationCreatedResponse.md)
 - [TenantApiTenantV1OrganizationDeletedResponse](docs/TenantApiTenantV1OrganizationDeletedResponse.md)
 - [TenantApiTenantV1OrganizationGetPaginatedItemsResponse](docs/TenantApiTenantV1OrganizationGetPaginatedItemsResponse.md)
 - [TenantApiTenantV1OrganizationUpdatedResponse](docs/TenantApiTenantV1OrganizationUpdatedResponse.md)
 - [TenantApiTenantV1SetAppSettingsRequest](docs/TenantApiTenantV1SetAppSettingsRequest.md)
 - [TenantApiTenantV1SetAppSettingsResponse](docs/TenantApiTenantV1SetAppSettingsResponse.md)
 - [TenantApiTenantV1SubscriptionCreatedResponse](docs/TenantApiTenantV1SubscriptionCreatedResponse.md)
 - [TenantApiTenantV1SubscriptionProfileResponse](docs/TenantApiTenantV1SubscriptionProfileResponse.md)
 - [TenantApiTenantV1SubscriptionStatus](docs/TenantApiTenantV1SubscriptionStatus.md)
 - [TenantApiTenantV1SubscriptionUpdatedResponse](docs/TenantApiTenantV1SubscriptionUpdatedResponse.md)
 - [TenantApiTenantV1TenantAdditionalSetting](docs/TenantApiTenantV1TenantAdditionalSetting.md)
 - [TenantApiTenantV1TenantAppSettings](docs/TenantApiTenantV1TenantAppSettings.md)
 - [TenantApiTenantV1TenantBrandingBackground](docs/TenantApiTenantV1TenantBrandingBackground.md)
 - [TenantApiTenantV1TenantBrandingLogo](docs/TenantApiTenantV1TenantBrandingLogo.md)
 - [TenantApiTenantV1TenantBrandingResponse](docs/TenantApiTenantV1TenantBrandingResponse.md)
 - [TenantApiTenantV1TenantIdentityProviders](docs/TenantApiTenantV1TenantIdentityProviders.md)
 - [TenantApiTenantV1TenantProfileResponse](docs/TenantApiTenantV1TenantProfileResponse.md)
 - [TenantApiTenantV1TenantSetting](docs/TenantApiTenantV1TenantSetting.md)
 - [TenantApiTenantV1TenantSettingTypesListResponse](docs/TenantApiTenantV1TenantSettingTypesListResponse.md)
 - [TenantApiTenantV1TenantSettingTypesListResponsePaginatedItemsViewModel](docs/TenantApiTenantV1TenantSettingTypesListResponsePaginatedItemsViewModel.md)
 - [TenantApiTenantV1TenantSettingsTypeAttribute](docs/TenantApiTenantV1TenantSettingsTypeAttribute.md)
 - [TenantApiTenantV1TenantStatus](docs/TenantApiTenantV1TenantStatus.md)
 - [TenantApiTenantV1TenantType](docs/TenantApiTenantV1TenantType.md)
 - [TenantApiTenantV1TenantUpdatedResponse](docs/TenantApiTenantV1TenantUpdatedResponse.md)
 - [TenantApiTenantV1UpdateDomainRequest](docs/TenantApiTenantV1UpdateDomainRequest.md)
 - [TenantApiTenantV1UpdateOrganizationRequest](docs/TenantApiTenantV1UpdateOrganizationRequest.md)
 - [TenantApiTenantV1UpdateSubscriptionRequest](docs/TenantApiTenantV1UpdateSubscriptionRequest.md)
 - [TenantApiTenantV1VerifyDomainRequest](docs/TenantApiTenantV1VerifyDomainRequest.md)
 - [TenantApiWebhookV1CreateWebhookRequest](docs/TenantApiWebhookV1CreateWebhookRequest.md)
 - [TenantApiWebhookV1PaginatedItemsResponse](docs/TenantApiWebhookV1PaginatedItemsResponse.md)
 - [TenantApiWebhookV1PaginatedWebhookEventItemsResponse](docs/TenantApiWebhookV1PaginatedWebhookEventItemsResponse.md)
 - [TenantApiWebhookV1ReRunRequestedResponse](docs/TenantApiWebhookV1ReRunRequestedResponse.md)
 - [TenantApiWebhookV1RequestReRunRequest](docs/TenantApiWebhookV1RequestReRunRequest.md)
 - [TenantApiWebhookV1UpdateWebhookRequest](docs/TenantApiWebhookV1UpdateWebhookRequest.md)
 - [TenantApiWebhookV1WebhookEventResponse](docs/TenantApiWebhookV1WebhookEventResponse.md)
 - [TenantApiWebhookV1WebhookIdResponse](docs/TenantApiWebhookV1WebhookIdResponse.md)
 - [TenantApiWebhookV1WebhookReRunStrategy](docs/TenantApiWebhookV1WebhookReRunStrategy.md)
 - [TenantApiWebhookV1WebhookResponse](docs/TenantApiWebhookV1WebhookResponse.md)
 - [TenantApiWebhookV1WebhookSchema](docs/TenantApiWebhookV1WebhookSchema.md)
 - [TenantApiWebhookV1WebhookSubscriberResponse](docs/TenantApiWebhookV1WebhookSubscriberResponse.md)
 - [ValidationsApiContainersV1AddDataStewardBulkRequest](docs/ValidationsApiContainersV1AddDataStewardBulkRequest.md)
 - [ValidationsApiContainersV1AddDataStewardBulkRequestTypesCollection](docs/ValidationsApiContainersV1AddDataStewardBulkRequestTypesCollection.md)
 - [ValidationsApiContainersV1AddDataStewardRequest](docs/ValidationsApiContainersV1AddDataStewardRequest.md)
 - [ValidationsApiContainersV1CategoriesWithDataUsersResponse](docs/ValidationsApiContainersV1CategoriesWithDataUsersResponse.md)
 - [ValidationsApiContainersV1CertificationReminderRequestedResponse](docs/ValidationsApiContainersV1CertificationReminderRequestedResponse.md)
 - [ValidationsApiContainersV1CertificationStatusSetResponse](docs/ValidationsApiContainersV1CertificationStatusSetResponse.md)
 - [ValidationsApiContainersV1CollectionUploadedResponse](docs/ValidationsApiContainersV1CollectionUploadedResponse.md)
 - [ValidationsApiContainersV1CollectionUploadedResponseTypesUploadResult](docs/ValidationsApiContainersV1CollectionUploadedResponseTypesUploadResult.md)
 - [ValidationsApiContainersV1CollectionUser](docs/ValidationsApiContainersV1CollectionUser.md)
 - [ValidationsApiContainersV1ContainerDto](docs/ValidationsApiContainersV1ContainerDto.md)
 - [ValidationsApiContainersV1ContainerDtoTypesTagDto](docs/ValidationsApiContainersV1ContainerDtoTypesTagDto.md)
 - [ValidationsApiContainersV1CreateCollectionRequest](docs/ValidationsApiContainersV1CreateCollectionRequest.md)
 - [ValidationsApiContainersV1CreateContainerRequest](docs/ValidationsApiContainersV1CreateContainerRequest.md)
 - [ValidationsApiContainersV1DataOwnerSetBulkResponse](docs/ValidationsApiContainersV1DataOwnerSetBulkResponse.md)
 - [ValidationsApiContainersV1DataOwnerSetBulkResponseTypesCollection](docs/ValidationsApiContainersV1DataOwnerSetBulkResponseTypesCollection.md)
 - [ValidationsApiContainersV1DataOwnerSetResponse](docs/ValidationsApiContainersV1DataOwnerSetResponse.md)
 - [ValidationsApiContainersV1DataStewardAddedBulkResponse](docs/ValidationsApiContainersV1DataStewardAddedBulkResponse.md)
 - [ValidationsApiContainersV1DataStewardAddedBulkResponseTypesCollection](docs/ValidationsApiContainersV1DataStewardAddedBulkResponseTypesCollection.md)
 - [ValidationsApiContainersV1DataStewardAddedResponse](docs/ValidationsApiContainersV1DataStewardAddedResponse.md)
 - [ValidationsApiContainersV1DataUserResponse](docs/ValidationsApiContainersV1DataUserResponse.md)
 - [ValidationsApiContainersV1GetJsonResponse](docs/ValidationsApiContainersV1GetJsonResponse.md)
 - [ValidationsApiContainersV1PaginatedCategoryTreeResponse](docs/ValidationsApiContainersV1PaginatedCategoryTreeResponse.md)
 - [ValidationsApiContainersV1PaginatedCategoryTreeResponseTypesCategoryTree](docs/ValidationsApiContainersV1PaginatedCategoryTreeResponseTypesCategoryTree.md)
 - [ValidationsApiContainersV1PaginatedCategoryTreeResponseTypesSubCategoryTree](docs/ValidationsApiContainersV1PaginatedCategoryTreeResponseTypesSubCategoryTree.md)
 - [ValidationsApiContainersV1PaginatedContainers](docs/ValidationsApiContainersV1PaginatedContainers.md)
 - [ValidationsApiContainersV1SetDataOwnerBulkRequest](docs/ValidationsApiContainersV1SetDataOwnerBulkRequest.md)
 - [ValidationsApiContainersV1SetDataOwnerBulkRequestTypesCollection](docs/ValidationsApiContainersV1SetDataOwnerBulkRequestTypesCollection.md)
 - [ValidationsApiContainersV1SetDataOwnerRequest](docs/ValidationsApiContainersV1SetDataOwnerRequest.md)
 - [ValidationsApiContainersV1UpdateCollectionRequest](docs/ValidationsApiContainersV1UpdateCollectionRequest.md)
 - [ValidationsApiContainersV1UpdateContainerRequest](docs/ValidationsApiContainersV1UpdateContainerRequest.md)
 - [ValidationsApiContainersV1UploadCollectionRequest](docs/ValidationsApiContainersV1UploadCollectionRequest.md)
 - [ValidationsApiContainersV1Url](docs/ValidationsApiContainersV1Url.md)
 - [ValidationsApiCoreV1CreatedResponse](docs/ValidationsApiCoreV1CreatedResponse.md)
 - [ValidationsApiCoreV1InstanceType](docs/ValidationsApiCoreV1InstanceType.md)
 - [ValidationsApiCoreV1Provider](docs/ValidationsApiCoreV1Provider.md)
 - [ValidationsApiDbEnvironmentsV1AzureSynapseSqlServerlessConnection](docs/ValidationsApiDbEnvironmentsV1AzureSynapseSqlServerlessConnection.md)
 - [ValidationsApiDbEnvironmentsV1CreateRequest](docs/ValidationsApiDbEnvironmentsV1CreateRequest.md)
 - [ValidationsApiDbEnvironmentsV1DbEnvironmentDto](docs/ValidationsApiDbEnvironmentsV1DbEnvironmentDto.md)
 - [ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments](docs/ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments.md)
 - [ValidationsApiDbEnvironmentsV1SqlServerConnection](docs/ValidationsApiDbEnvironmentsV1SqlServerConnection.md)
 - [ValidationsApiDbEnvironmentsV1TestConnectionRequest](docs/ValidationsApiDbEnvironmentsV1TestConnectionRequest.md)
 - [ValidationsApiDbEnvironmentsV1TestConnectionResponse](docs/ValidationsApiDbEnvironmentsV1TestConnectionResponse.md)
 - [ValidationsApiDbEnvironmentsV1UpdateRequest](docs/ValidationsApiDbEnvironmentsV1UpdateRequest.md)
 - [ValidationsApiJobsV1ChildJob](docs/ValidationsApiJobsV1ChildJob.md)
 - [ValidationsApiJobsV1DataRefreshType](docs/ValidationsApiJobsV1DataRefreshType.md)
 - [ValidationsApiJobsV1JobExecutionStatus](docs/ValidationsApiJobsV1JobExecutionStatus.md)
 - [ValidationsApiJobsV1JobListResponse](docs/ValidationsApiJobsV1JobListResponse.md)
 - [ValidationsApiJobsV1JobMetadata](docs/ValidationsApiJobsV1JobMetadata.md)
 - [ValidationsApiJobsV1JobProfileResponse](docs/ValidationsApiJobsV1JobProfileResponse.md)
 - [ValidationsApiJobsV1JobStatus](docs/ValidationsApiJobsV1JobStatus.md)
 - [ValidationsApiJobsV1Metric](docs/ValidationsApiJobsV1Metric.md)
 - [ValidationsApiJobsV1PaginatedItemsResponse](docs/ValidationsApiJobsV1PaginatedItemsResponse.md)
 - [ValidationsApiJobsV1Schedule](docs/ValidationsApiJobsV1Schedule.md)
 - [ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest](docs/ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest.md)
 - [ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest](docs/ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest.md)
 - [ValidationsApiReportingPeriodsV1CertificationStatus](docs/ValidationsApiReportingPeriodsV1CertificationStatus.md)
 - [ValidationsApiReportingPeriodsV1CertificationStatusCategory](docs/ValidationsApiReportingPeriodsV1CertificationStatusCategory.md)
 - [ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse](docs/ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse.md)
 - [ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse](docs/ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse.md)
 - [ValidationsApiReportingPeriodsV1PaginatedRecords](docs/ValidationsApiReportingPeriodsV1PaginatedRecords.md)
 - [ValidationsApiReportingPeriodsV1PaginatedRecordsTypesReportingPeriodRecords](docs/ValidationsApiReportingPeriodsV1PaginatedRecordsTypesReportingPeriodRecords.md)
 - [ValidationsApiReportingPeriodsV1PaginatedRecordsTypesReportingPeriodRecordsTypesRule](docs/ValidationsApiReportingPeriodsV1PaginatedRecordsTypesReportingPeriodRecordsTypesRule.md)
 - [ValidationsApiReportingPeriodsV1PaginatedReportingPeriods](docs/ValidationsApiReportingPeriodsV1PaginatedReportingPeriods.md)
 - [ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2](docs/ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2.md)
 - [ValidationsApiReportingPeriodsV1PaginatedSubmissions](docs/ValidationsApiReportingPeriodsV1PaginatedSubmissions.md)
 - [ValidationsApiReportingPeriodsV1PipelineRun](docs/ValidationsApiReportingPeriodsV1PipelineRun.md)
 - [ValidationsApiReportingPeriodsV1PostRequest](docs/ValidationsApiReportingPeriodsV1PostRequest.md)
 - [ValidationsApiReportingPeriodsV1PostedResponse](docs/ValidationsApiReportingPeriodsV1PostedResponse.md)
 - [ValidationsApiReportingPeriodsV1ReportingPeriodDto](docs/ValidationsApiReportingPeriodsV1ReportingPeriodDto.md)
 - [ValidationsApiReportingPeriodsV1ReportingPeriodValidationsRunDto](docs/ValidationsApiReportingPeriodsV1ReportingPeriodValidationsRunDto.md)
 - [ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse](docs/ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse.md)
 - [ValidationsApiReportingPeriodsV1RunResponse](docs/ValidationsApiReportingPeriodsV1RunResponse.md)
 - [ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest](docs/ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest.md)
 - [ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequestTypesRecord](docs/ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequestTypesRecord.md)
 - [ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest](docs/ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest.md)
 - [ValidationsApiReportingPeriodsV1SubmissionCancelledResponse](docs/ValidationsApiReportingPeriodsV1SubmissionCancelledResponse.md)
 - [ValidationsApiReportingPeriodsV1SubmissionListResponse](docs/ValidationsApiReportingPeriodsV1SubmissionListResponse.md)
 - [ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse](docs/ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse.md)
 - [ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse](docs/ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse.md)
 - [ValidationsApiReportingPeriodsV1SubmissionMetricsDetails](docs/ValidationsApiReportingPeriodsV1SubmissionMetricsDetails.md)
 - [ValidationsApiReportingPeriodsV1SubmissionMetricsResponse](docs/ValidationsApiReportingPeriodsV1SubmissionMetricsResponse.md)
 - [ValidationsApiReportingPeriodsV1SubmissionProfile](docs/ValidationsApiReportingPeriodsV1SubmissionProfile.md)
 - [ValidationsApiReportingPeriodsV1SubmissionStatus](docs/ValidationsApiReportingPeriodsV1SubmissionStatus.md)
 - [ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse](docs/ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse.md)
 - [ValidationsApiReportingPeriodsV1ToggleSelectedRequest](docs/ValidationsApiReportingPeriodsV1ToggleSelectedRequest.md)
 - [ValidationsApiReportingPeriodsV1ToggledResponse](docs/ValidationsApiReportingPeriodsV1ToggledResponse.md)
 - [ValidationsApiReportingPeriodsV1UpdateBulkRequest](docs/ValidationsApiReportingPeriodsV1UpdateBulkRequest.md)
 - [ValidationsApiReportingPeriodsV1UpdateBulkRequestTypesReportingPeriod](docs/ValidationsApiReportingPeriodsV1UpdateBulkRequestTypesReportingPeriod.md)
 - [ValidationsApiReportingPeriodsV1UpdatedBulkResponse](docs/ValidationsApiReportingPeriodsV1UpdatedBulkResponse.md)
 - [ValidationsApiReportingPeriodsV1ValidationResultRecord](docs/ValidationsApiReportingPeriodsV1ValidationResultRecord.md)
 - [ValidationsApiReportingPeriodsV1ValidationSummary](docs/ValidationsApiReportingPeriodsV1ValidationSummary.md)
 - [ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId](docs/ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId.md)
 - [ValidationsApiReportingPeriodsV1ValidationSummaryCategory](docs/ValidationsApiReportingPeriodsV1ValidationSummaryCategory.md)
 - [ValidationsApiReportingPeriodsV1ValidationSummarySubCategory](docs/ValidationsApiReportingPeriodsV1ValidationSummarySubCategory.md)
 - [ValidationsApiResultsV1RuleSummary](docs/ValidationsApiResultsV1RuleSummary.md)
 - [ValidationsApiRulesV1CreateRequest](docs/ValidationsApiRulesV1CreateRequest.md)
 - [ValidationsApiRulesV1PaginatedRules](docs/ValidationsApiRulesV1PaginatedRules.md)
 - [ValidationsApiRulesV1RuleDto](docs/ValidationsApiRulesV1RuleDto.md)
 - [ValidationsApiRulesV1UpdateRequest](docs/ValidationsApiRulesV1UpdateRequest.md)
 - [ValidationsApiRulesV1Url](docs/ValidationsApiRulesV1Url.md)
 - [ValidationsApiRulesV1UrlType](docs/ValidationsApiRulesV1UrlType.md)
 - [ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse](docs/ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse.md)
 - [ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest](docs/ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest.md)
 - [ValidationsApiTagsV1CreateRequest](docs/ValidationsApiTagsV1CreateRequest.md)
 - [ValidationsApiTagsV1PaginatedTags](docs/ValidationsApiTagsV1PaginatedTags.md)
 - [ValidationsApiTagsV1TagDto](docs/ValidationsApiTagsV1TagDto.md)
 - [ValidationsApiTagsV1UpdateRequest](docs/ValidationsApiTagsV1UpdateRequest.md)
 - [ValidationsApiValidationResultsV1FindResponse](docs/ValidationsApiValidationResultsV1FindResponse.md)
 - [ValidationsApiValidationResultsV1ValidationResultDto](docs/ValidationsApiValidationResultsV1ValidationResultDto.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization


Authentication schemes defined for the API:
<a id="oauth2"></a>
### oauth2

- **Type**: OAuth
- **Flow**: application
- **Authorization URL**: 
- **Scopes**: 
 - **https://api.edgraph.com/auth/tenant**: EdGraph Platform - Tenant Api

