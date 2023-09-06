[Preparation course for Databricks Data Engineer Associate certification exam (Versions 2 and 3)](https://www.udemy.com/course/databricks-certified-data-engineer-associate/learn/lecture/34664668#overview)


### Databricks Lakehouse Platform
- Workspace
    - Data Engineering
    - Data Warehouse
    - Machine Learnig

- Runtime
    - Spark
    - Delta Lake
    - Multicloud Service Providers

- Control Plane
    - Databricks Account
        - Web UI
        - Cluster Management
        - Workflows
        - Notebooks

- Data plane
    - Cluster VMs
    - Storage(DBFS)

### Unity Catalog
A data governance solution

Data governance is the process of managing the availability, usability, integrity and security of the data present in the an enterprise
- Help implement privacy regulations GDPR, CCPA etc
- Controls access to data
- Ensures that data is trustworthy and not misused

Four key areas
- Data access control - files, tables, ML models and RBAC
- Data Audit, Data Linage both upstream and downstream
- Data Discoverability
- Data Lineage

user management, access control, data explorer and metastore management are centralized

Unit catalog and Hive store are different and do not use with Unity catalog. Data Lineage is not available in Hivestore
One for region.

The Metastore itself is stored and maintained within Databricks control plane and we do not have to.

Azure Connector for Data bricks

### Resources for Unity catalog
- 






