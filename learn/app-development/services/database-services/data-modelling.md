---
title: "Data Modelling"
id: ""
---

A **data model** describes the structure of the database: the tables, columns, keys, and relationships. The data model for imported databases can be viewed from within the app using **DB Designer**. DB Designer for a specific database can be accessed by selecting the _database_ from the **Databases** Resource option**.**

[![](../../../assets/db_designer_open.png)](../../../assets/db_designer_open.png)

# Configuration Settings

**Settings tab** can be used to interact with the database and ensure that the data model is in sync with the database. It shows the connection settings of the selected database.

**NOTE**:

- All these options are available **ONLY** for Data Model in **Edit Mode**.
- DB Schemas for HSQL and for databases categorized as "Other Databases" at the time of import cannot be edited and hence are rendered as Read-Only schemas.

From this tab you can:

| Action | Description |
| --- | --- |
|  | **Re-import** enables you to build the data model from the database again. This would bring in changes made to the database and will revert all changes done by the database designer. |
|  | **Export** will move the data model to the database of your choice. You can choose to export to the current database or to a different database. **NOTE: You can only export to the same database system as the original import, you can change the database but not the database system.** |
|  | **Save** Database will save the db in your app workspace, this is the draft copy of the database solely available to your app. |
|  | **Delete** would delete the data model from the app. |

## Advanced Settings

Apart from the basic Database settings like host details, schema name etc., WaveMaker provides some **advanced database configuration options**.

| Setting | Description |
| --- | --- |
| **Java Package** | WaveMaker generates Java classes for you when you import a database. If you want a different Java package name than the default name we generate, type it in here. |

# Database Designer

**Design tab** renders the database components – tables, columns, and relationships. [![](../../../assets/db_designer_schema.png)](../../../assets/db_designer_schema.png)

Using this tab, you can:

| Action | Description |
| --- | --- |
| +Table | **Add **tables |
|  | **Delete** tables |
|  | **Search** for tables within the designer |
|  | **Update DB** with the changes made from the DB Designer. A preview dialog will open which will list all the changes made to the DB. Script tab will show the same changes in script format. |
|  | **Revert DB** designer to undo any changes made. **Note** this will not get any changes made to the database, use Re-Import for that. |
|  | **Re-import** enables you to build the data model from the database again. This would bring in changes made to the database and will revert all changes done from the database designer. |
|  | **Save** database will save the changes to your workspace. **Note** to save it to the database use the Update DB option. |
| **Table Modification** upon selecting a table |
| Name | change the name of the tables |
| ADD COLUMN | add columns, [know more](/learn/app-development/services/database-services/working-database-schema/#add-tables-columns) |
| **Primary Key** configuration |
| Type | can be single or composite |
| Select Column | Column (columns in case of composite key) to be set as primary key |
| Generator Type | how the primary key columns gets its values - assigned - user entry or auto increment - for integer type, [know more](/learn/app-development/services/database-services/working-database-schema/#identity-generators) |
| **Unique Constraints** |
| Name | Columns whose values need to be restricted as unique |
| **Column modifications** for selected column |
| Name |  |
| SQL and Java Types | It is advisable to make changes to Java Types rather than SQL Types unless you want the changes to be reflected in the database, in which case you need to export the database. You can review the type conversion from Java to SQL type from this document: [Java Types vs SQL Data Types](../../../assets/JavaTypesVsDBTypes-Sheet.pdf) |
| Constraints | Nullable or not. NOTE: Primary Key and Unique Kay constraints need to be modified at the Table level. Foreign Key constraint can be modified from the respective Relation |
| **Relations** between tables |
|  | Relations cannot be modified, you need to delete and add a new relation if needed, [know more](/learn/app-development/services/database-services/working-database-schema/#database-relationships). |

**Notes**:

- Any changes made to the database design, needs to be **Exported/Updated** for the changes to be synced with the database. Save alone does not ensure syncing.
- Design changes are restricted to Data Model in Edit Mode. For Read-Only DBs, HsqlDB, DB2 and other databases design modifications are restricted to Java Type changes and virtual relation settings. [Know more about import modes from here](/learn/app-development/services/database-services/database-schema-import-modes/)

< Working with Databases

DB Schema Import Modes >

Working with DB Schema >

5\. Creating Backend Services

- 5.1 Overview
    - [i. Accessing Data](/learn/app-development/services/creating-backend-services/#accessing-data)
        - [○ Life-cycle of data](/learn/app-development/services/creating-backend-services/#life-cycle)
    - [ii. Manipulating Data](/learn/app-development/services/creating-backend-services/#manipulating-data)
        - [○ Life-cycle of Events](/learn/app-development/services/creating-backend-services/#life-cycle-events)
    - [iii. REST APIs](/learn/app-development/services/creating-backend-services/#rest-apis)
- 5.2 Web Services
    - [i. Overview](/learn/services/web-services/web-services/#overview)
    - [ii. Variables for Invocation](/learn/services/web-services/web-services/#service-variable)
    - iii. Working with SOAP Services
        - [○ Overview](/learn/app-development/services/web-services/web-services/working-with-soap-services/#SOAP-service-setup)
        - [○ SOAP Service Setup](/learn/app-development/services/web-services/working-with-soap-services/#SOAP-service-setup)
        - [○ SOAP Service Settings](/learn/app-development/services/web-services/working-with-soap-services/#SOAP-service-settings)
        - [○ Generated REST APIs](/learn/app-development/services/web-services/working-with-soap-services/#generated-rest-apis)
        - [○ SOAP Service Usage](/learn/app-development/services/web-services/working-with-soap-services/#SOAP-service-usage)
    - iv. Working with REST Services
        - [○ Overview](/learn/app-development/services/web-services/rest-services/)
        - [○ Test REST Service](/learn/app-development/services/web-services/rest-services/#test-API)
        - [○ Configure REST Service](/learn/app-development/services/web-services/rest-services/#configure-REST-service)
        - [○ REST Service Usage](/learn/app-development/services/web-services/rest-services/#REST-service-usage)
    - iii. Working with Web Sockets
        - [○ Overview](/learn/app-development/services/web-services/working-with-websockets/)
        - [○ Service Integration](/learn/app-development/services/web-services/working-with-websockets/#import)
        - [○ Service Consumption](/learn/app-development/services/web-services/working-with-websockets/#variable)
        - [○ Use Cases](/learn/app-development/services/web-services/working-with-websockets/#use-cases)
- [5.3 Database Services](/learn/app-development/services/database-services/database-services/)
    - [i. Overview](/learn/app-development/services/database-services/database-services/#)
    - [ii. Supported Databases](/learn/app-development/services/database-services/database-services/#supported-databases)
    - iii. Working with Databases
        - [○ Overview](/learn/app-development/services/database-services/working-with-databases/#)
        - [○ Adding Database](/learn/app-development/services/database-services/working-with-databases/#integrating-database)
        - [○ Database Actions](/learn/app-development/services/database-services/working-with-databases/#database-actions)
    - [iv. Data Modelling](#)
        - [○ Overview](#)
        - [○ Configuration Settings](#configuration-settings)
        - [○ Database Designer](#database-designer)
            - [● Schema Import Modes](/learn/app-development/services/database-services/database-schema-import-modes/)
        - ○ Working with Database Schema
            - [● Overview](/learn/app-development/services/database-services/working-database-schema/)
            - [● Adding Tables and Columns](/learn/app-development/services/database-services/working-database-schema/#add-tables-columns)
            - [● Working with Relationships](/learn/app-development/services/database-services/working-database-schema/#database-relationships)
            - [● Identity Generators for Primary Key Column](/learn/app-development/services/database-services/working-database-schema/#identity-generators)
            - [● Column Metadata Configuration](/learn/app-development/services/database-services/working-database-schema/#column-metadata-configuration)
            - [● Virtual Primary Keys and Relations](/learn/app-development/services/database-services/working-database-schema/#virtual-primary-keys)
            - [● Temporal Support](/learn/app-development/services/database-services/temporal-support/)
    - v. Databases Access
        - [○ Overview](/learn/app-development/services/database-access/)
        - ○ Working with Queries
            - [● Overview](/learn/app-development/services/database-services/working-with-queries/)
            - [● Query Editor](/learn/app-development/services/database-services/working-with-queries/#query-editor)
            - [● Types of Queries](/learn/app-development/services/database-services/working-with-queries/#query-types)
            - [● Query Creation](/learn/app-development/services/database-services/working-with-queries/#query-creation)
            - [● Query Usage](/learn/app-development/services/database-services/working-with-queries/#query-usage)
            - [● Parameterised Query Creation](/learn/app-development/services/database-services/working-with-queries/#query-creation-parameterised)
            - [● Query Operation Type](/learn/app-development/services/database-services/working-with-queries/#query-op-types)
            - [● Query Architecture](/learn/app-development/services/database-services/working-with-queries/#query-architecture)
        - ○ Working with Stored Procedures
            - [● Overview](/learn/app-development/services/db-services/working-stored-procedures/)
            - [● Procedure Creation](/learn/app-development/services/db-services/working-stored-procedures/#procedure-creation)
            - [● Procedure Parameters](/learn/app-development/services/db-services/working-stored-procedures/#proc-params)
            - [● Procedure Invocation](/learn/app-development/services/db-services/working-stored-procedures/#procedure-invocation)
            - [● Procedure Architecture](/learn/app-development/services/db-services/working-stored-procedures/#procedure-architecture)
        - [○ Versioning of Queries and Procedures](/learn/app-development/services/database-services/versioning-queries-procedures/)
        - [○ Blob Support for Queries and Procedures](/learn/app-development/services/database-services/blob-support-queries-procedures/)
        - [○ Invoking Queries & Procedures from Java Service](/learn/app-development/services/database-services/invoking-queriesprocedures-java-services/)
        - [○ Database Views](/learn/app-development/services/db-services/database-views/)
        - ○ Database Tools
            - [● Overview](/learn/app-development/services/database-tools/)
            - [● DB Shell](/learn/app-development/services/database-tools/#db-shell)
            - [● DB Scripts](/learn/app-development/services/database-tools/#db-scripts)
                - [● Import DB](/learn/app-development/services/database-tools/#import-db)
                - [● Export DB](/learn/app-development/services/database-tools/#export-db)
    - vi. ORM Artifacts
        - [○ Database Integration Process](/learn/app-development/services/db-services/orm-artifacts/#database-integration-process)
        - [○ Layered Architecture](/learn/app-development/services/db-services/orm-artifacts/#layered-architecture)
        - [○ Generated Files](/learn/app-development/services/db-services/orm-artifacts/#generated-files)
        - [○ Generated APIs](/learn/app-development/services/db-services/orm-artifacts/#generated-apis)
            - [● CRUD APIs](/learn/app-development/services/db-services/orm-artifacts/#crud-apis)
            - [● Query APIs](/learn/app-development/services/db-services/orm-artifacts/#query-apis)
            - [● Custom Query Syntax](/learn/app-development/services/db-services/orm-artifacts/#custom-query-syntax)
- 5.4 Java Services
    - [i. Overview](/learn/app-development/services/java-services/java-service/#overview)
    - [ii. Java Services Framework](/learn/app-development/services/java-services/java-service/#java-services-framework)
    - iii. Integration Services
        - [○ Current Loggedin User](/learn/app-development/services/java-services/java-integration-services/#loggedin-user)
        - [○ External Java Libraries](/learn/app-development/services/java-services/java-integration-services/#external-java-libraries)
        - [○ Database Entities](/learn/app-development/services/java-services/java-integration-services/#db-services)
        - [○ Named Queries](/learn/app-development/services/java-services/java-integration-services/#query-service)
        - [○ Imported Web Services](/learn/app-development/services/java-services/java-integration-services/#web-services)
    - [iv. Service Variables](/learn/app-development/services/java-services/service-variables/)
    - [v. Generated REST APIs](/learn/app-development/services/java-services/generated-rest-apis-api-designer/)
- 5.5 API Designer
    - [i. Overview](/learn/app-development/services/api-designer/api/)
    - [ii. Database Services APIs](/learn/app-development/services/api-designer/database-service-apis/)
    - [iii. Web Services APIs](/learn/app-development/services/api-designer/web-service-apis/)
    - [iv. Java Services APIs](/learn/app-development/services/api-designer/java-service-apis/)
    - [v. Security Services APIs](/learn/app-development/services/api-designer/security-service-apis/)
- 5.6 3rd Party Libraries
    - [i. Overview](/learn/app-development/services/3rd-party-libraries/)
    - [ii. Including resource files](/learn/app-development/services/3rd-party-libraries/#resource-files)
    - [iii. Using third-party JavaScript file](/learn/app-development/services/3rd-party-libraries/using-3rd-party-javascript-files/)
    - [iv. Using third-party jar file](/learn/app-development/services/3rd-party-libraries/using-3rd-party-jar-files/)