# Índice de vistas de sistema y de monitoreo

Vistas de sistema (6.1, esquema SYS: metadatos) y vistas de monitoreo (6.2, prefijo `M_`: datos de ejecución), ordenadas alfabéticamente.

| Vista | Descripción (EN) |
| --- | --- |
| [ABSTRACT_SQL_PLANS](6-System-Views-Reference/6.01-System-Views/ABSTRACT_SQL_PLANS-System-View.md) | Lists information about abstract SQL plans. |
| [ACCESSIBLE_VIEWS](6-System-Views-Reference/6.01-System-Views/ACCESSIBLE_VIEWS-System-View.md) | Provides information about accessible views for a given user. |
| [ADAPTER_CAPABILITIES](6-System-Views-Reference/6.01-System-Views/ADAPTER_CAPABILITIES-System-View.md) | Displays supported capabilities for each adapter. |
| [ADAPTER_LOCATIONS](6-System-Views-Reference/6.01-System-Views/ADAPTER_LOCATIONS-System-View.md) | Displays the location of adapters. |
| [ADAPTERS](6-System-Views-Reference/6.01-System-Views/ADAPTERS-System-View.md) | Displays adapters available in the SAP HANA system. |
| [AFL_AREAS](6-System-Views-Reference/6.01-System-Views/AFL_AREAS-System-View.md) | Provides information about available AFL areas. |
| [AFL_FUNCTION_PARAMETERS](6-System-Views-Reference/6.01-System-Views/AFL_FUNCTION_PARAMETERS-System-View.md) | Provides information about parameters of AFL functions. |
| [AFL_FUNCTION_PROPERTIES](6-System-Views-Reference/6.01-System-Views/AFL_FUNCTION_PROPERTIES-System-View.md) | Provides information about available AFL function properties. |
| [AFL_FUNCTIONS](6-System-Views-Reference/6.01-System-Views/AFL_FUNCTIONS-System-View.md) | Provides information about available AFL functions. |
| [AFL_PACKAGES](6-System-Views-Reference/6.01-System-Views/AFL_PACKAGES-System-View.md) | Provides information about available AFL packages. |
| [AFL_TEXTS](6-System-Views-Reference/6.01-System-Views/AFL_TEXTS-System-View.md) | Provides information about available AFL texts. |
| [AGENT_CONFIGURATION](6-System-Views-Reference/6.01-System-Views/AGENT_CONFIGURATION-System-View.md) | Provides agent configuration information. |
| [AGENT_GROUPS](6-System-Views-Reference/6.01-System-Views/AGENT_GROUPS-System-View.md) | Lists active data provisioning agent groups in the system. |
| [AGENTS](6-System-Views-Reference/6.01-System-Views/AGENTS-System-View.md) | Lists active data provisioning agents in the system. |
| [ALL_AUDIT_LOG](6-System-Views-Reference/6.01-System-Views/ALL_AUDIT_LOG-System-View.md) | Provides information about audit records, including those for XSA events. You must have AUDIT ADMIN, AUDIT OPERATOR, or AUDIT READ system privileges to access this view. |
| [ANNOTATIONS](6-System-Views-Reference/6.01-System-Views/ANNOTATIONS-System-View.md) | Provides information about annotations that have been added to SQL objects. |
| [ANONYMIZATION_VIEW_COLUMNS](6-System-Views-Reference/6.01-System-Views/ANONYMIZATION_VIEW_COLUMNS-System-View.md) | Provides information about the anonymized columns in SAP HANA database. |
| [ANONYMIZATION_VIEWS](6-System-Views-Reference/6.01-System-Views/ANONYMIZATION_VIEWS-System-View.md) | Provides information about anonymized views in the SAP HANA database. |
| [APPLICATION_CONNECTION_HISTORY](6-System-Views-Reference/6.01-System-Views/APPLICATION_CONNECTION_HISTORY-System-View.md) | Provides stored application connection history information. |
| [APPLICATION_ENCRYPTION_KEYS](6-System-Views-Reference/6.01-System-Views/APPLICATION_ENCRYPTION_KEYS-System-View.md) | Provides information about encryption keys used by applications. |
| [ASSOCIATIONS](6-System-Views-Reference/6.01-System-Views/ASSOCIATIONS-System-View.md) | Provides information about associations. |
| [AUDIT_ACTIONS](6-System-Views-Reference/6.01-System-Views/AUDIT_ACTIONS-System-View.md) | Provides information about all available audit actions. |
| [AUDIT_LOG](6-System-Views-Reference/6.01-System-Views/AUDIT_LOG-System-View.md) | Provides information about audit records, with the exception of XSA-auditing. You must have the AUDIT ADMIN, AUDIT OPERATOR, or AUDIT READ system privilege to access this view. |
| [AUDIT_POLICIES](6-System-Views-Reference/6.01-System-Views/AUDIT_POLICIES-System-View.md) | Provides information about audit policies. |
| [AUTHORIZATION_GRAPH](6-System-Views-Reference/6.01-System-Views/AUTHORIZATION_GRAPH-System-View.md) | Provides information about authorization dependencies of complex database objects. |
| [AUTHORIZATION_OBJECTS](6-System-Views-Reference/6.01-System-Views/AUTHORIZATION_OBJECTS-System-View.md) | Provides information regarding authorization objects. |
| [AUTHORIZATION_TYPES](6-System-Views-Reference/6.01-System-Views/AUTHORIZATION_TYPES-System-View.md) | Provides information about object types and subtypes used by authorization object IDs. |
| [CDS_ANNOTATION_ASSIGNMENTS](6-System-Views-Reference/6.01-System-Views/CDS_ANNOTATION_ASSIGNMENTS-System-View.md) | Provides CDS annotation assignments. |
| [CDS_ANNOTATION_VALUES](6-System-Views-Reference/6.01-System-Views/CDS_ANNOTATION_VALUES-System-View.md) | Provides CDS annotation values. |
| [CDS_ARTIFACT_NAMES](6-System-Views-Reference/6.01-System-Views/CDS_ARTIFACT_NAMES-System-View.md) | Provides CDS artifact names. |
| [CDS_ASSOCIATIONS](6-System-Views-Reference/6.01-System-Views/CDS_ASSOCIATIONS-System-View.md) | Provides definitions for CDS associations. |
| [CDS_ENTITIES](6-System-Views-Reference/6.01-System-Views/CDS_ENTITIES-System-View.md) | Provides information about CDS entities. |
| [CDS_VIEWS](6-System-Views-Reference/6.01-System-Views/CDS_VIEWS-System-View.md) | Provides definitions for CDS views. |
| [CERTIFICATES](6-System-Views-Reference/6.01-System-Views/CERTIFICATES-System-View.md) | Provides information about certificates useable in PSEs. |
| [CLIENTSIDE_ENCRYPTION_COLUMN_KEYS](6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_COLUMN_KEYS-System-View.md) | Provides column encryption key information. |
| [CLIENTSIDE_ENCRYPTION_KEYPAIRS](6-System-Views-Reference/6.01-System-Views/CLIENTSIDE_ENCRYPTION_KEYPAIRS-System-View.md) | Provides information about client public keys in the SAP HANA database. |
| [COLLATIONS](6-System-Views-Reference/6.01-System-Views/COLLATIONS-System-View.md) | Provides the list of collations that can be specified in an ORDER BY clause. |
| [COLUMNS System View - Deprecated](6-System-Views-Reference/6.01-System-Views/COLUMNS-System-View-Deprecated.md) | This view is deprecated. Use either the TABLE_COLUMNS or VIEW_COLUMNS system view instead. |
| [CONFIGURATION_PARAMETER_PROPERTIES](6-System-Views-Reference/6.01-System-Views/CONFIGURATION_PARAMETER_PROPERTIES-System-View.md) | Displays metadata and properties of the public configuration parameters for SAP HANA. |
| [CONSTRAINTS](6-System-Views-Reference/6.01-System-Views/CONSTRAINTS-System-View.md) | Provides information about defined constraints for tables. |
| [CONVERT_INTERNAL_TYPE_INTO_NAME](6-System-Views-Reference/6.01-System-Views/CONVERT_INTERNAL_TYPE_INTO_NAME-System-View.md) | For internal use only. |
| [CREDENTIALS](6-System-Views-Reference/6.01-System-Views/CREDENTIALS-System-View.md) | Provides information about credentials for users and components. |
| [CS_ALL_COLUMNS](6-System-Views-Reference/6.01-System-Views/CS_ALL_COLUMNS-System-View.md) | Provides information from all columns of column tables, including internal ones. |
| [CS_BO_VIEWS](6-System-Views-Reference/6.01-System-Views/CS_BO_VIEWS-System-View.md) | Provides information about business object views for column store join views. |
| [CS_CONCAT_COLUMNS](6-System-Views-Reference/6.01-System-Views/CS_CONCAT_COLUMNS-System-View.md) | Provides information on concat columns in the database. |
| [CS_FREESTYLE_COLUMNS](6-System-Views-Reference/6.01-System-Views/CS_FREESTYLE_COLUMNS-System-View.md) | Provides freestyle search columns for column store join views. |
| [CS_JOIN_CONDITIONS](6-System-Views-Reference/6.01-System-Views/CS_JOIN_CONDITIONS-System-View.md) | Provides join conditions for column store join views. |
| [CS_JOIN_CONSTRAINTS](6-System-Views-Reference/6.01-System-Views/CS_JOIN_CONSTRAINTS-System-View.md) | Provides join constraints for column store join views. |
| [CS_JOIN_PATHS](6-System-Views-Reference/6.01-System-Views/CS_JOIN_PATHS-System-View.md) | Provides join paths for column store join views. |
| [CS_JOIN_TABLES](6-System-Views-Reference/6.01-System-Views/CS_JOIN_TABLES-System-View.md) | Provides information about the physical tables referred to by column store join views. |
| [CS_KEY_FIGURES](6-System-Views-Reference/6.01-System-Views/CS_KEY_FIGURES-System-View.md) | Provides information about the key figures defined for column store join views. |
| [CS_VIEW_COLUMNS](6-System-Views-Reference/6.01-System-Views/CS_VIEW_COLUMNS-System-View.md) | Provides information about the columns defined for column store join views. |
| [CS_VIEW_PARAMETERS](6-System-Views-Reference/6.01-System-Views/CS_VIEW_PARAMETERS-System-View.md) | Provides a list of parameters of the objects in the SAP HANA database. Only calculation views are considered. The parameters of a view are parsed from the definition of the underlying scenario. |
| [DATA_STATISTICS](6-System-Views-Reference/6.01-System-Views/DATA_STATISTICS-System-View.md) | Provides an overview of data statistics objects. |
| [DATA_TYPES](6-System-Views-Reference/6.01-System-Views/DATA_TYPES-System-View.md) | Provides information about available SQL data types. |
| [DEPENDENCY_RULE_COLUMNS](6-System-Views-Reference/6.01-System-Views/DEPENDENCY_RULE_COLUMNS-System-View.md) | For internal use only. Provides a list dependency rule columns in the system. |
| [DEPENDENCY_RULES](6-System-Views-Reference/6.01-System-Views/DEPENDENCY_RULES-System-View.md) | For internal use only. Provides a list of dependency rules in the system. |
| [DYNAMIC_RESULT_CACHE](6-System-Views-Reference/6.01-System-Views/DYNAMIC_RESULT_CACHE-System-View.md) | Provides information about metadata objects that are enabled for a dynamic result cache. |
| [DYNAMIC_RESULT_CACHE_INDEX_COLUMNS](6-System-Views-Reference/6.01-System-Views/DYNAMIC_RESULT_CACHE_INDEX_COLUMNS-System-View.md) | Provides information about the indexes of dynamic result caches. |
| [EFFECTIVE_APPLICATION_PRIVILEGES](6-System-Views-Reference/6.01-System-Views/EFFECTIVE_APPLICATION_PRIVILEGES-System-View.md) | Provides information about the application privileges of the specified user. |
| [EFFECTIVE_MASK_EXPRESSIONS](6-System-Views-Reference/6.01-System-Views/EFFECTIVE_MASK_EXPRESSIONS-System-View.md) | Provides information as to how data is exposed to certain users in terms of data masking. |
| [EFFECTIVE_PRIVILEGE_GRANTEES](6-System-Views-Reference/6.01-System-Views/EFFECTIVE_PRIVILEGE_GRANTEES-System-View.md) | Provides information about who was granted (explicitly or implicitly via roles) a specified privilege. |
| [EFFECTIVE_PRIVILEGES](6-System-Views-Reference/6.01-System-Views/EFFECTIVE_PRIVILEGES-System-View.md) | Provides the privileges of the specified user. |
| [EFFECTIVE_ROLE_GRANTEES](6-System-Views-Reference/6.01-System-Views/EFFECTIVE_ROLE_GRANTEES-System-View.md) | Provides information regarding the users and roles that the role is granted to. |
| [EFFECTIVE_ROLES](6-System-Views-Reference/6.01-System-Views/EFFECTIVE_ROLES-System-View.md) | Provides the roles of the current user. |
| [EFFECTIVE_STRUCTURED_PRIVILEGES](6-System-Views-Reference/6.01-System-Views/EFFECTIVE_STRUCTURED_PRIVILEGES-System-View.md) | Displays the structured privileges applied to an object. |
| [ELEMENT_TYPES](6-System-Views-Reference/6.01-System-Views/ELEMENT_TYPES-System-View.md) | Provides information about available multivalued types. |
| [ENCRYPTION_ROOT_KEYS](6-System-Views-Reference/6.01-System-Views/ENCRYPTION_ROOT_KEYS-System-View.md) | Provides information about root keys. |
| [EPM_MODELS](6-System-Views-Reference/6.01-System-Views/EPM_MODELS-System-View.md) | Provides information about available EPM Models. |
| [EPM_QUERY_SOURCES](6-System-Views-Reference/6.01-System-Views/EPM_QUERY_SOURCES-System-View.md) | Provides information about available EPM query source. |
| [EXPLAIN_CALL_PLANS](6-System-Views-Reference/6.01-System-Views/EXPLAIN_CALL_PLANS-System-View.md) | Provides information about the compiled plan of a given procedure. |
| [EXPLAIN_PLAN_TABLE](6-System-Views-Reference/6.01-System-Views/EXPLAIN_PLAN_TABLE-System-View.md) | Provides information about SQL query plan explanation results. |
| [FLEXIBLE_TABLES](6-System-Views-Reference/6.01-System-Views/FLEXIBLE_TABLES-System-View.md) | Provides information about available flexible tables. |
| [FULL_SYSTEM_INFO_DUMPS](6-System-Views-Reference/6.01-System-Views/FULL_SYSTEM_INFO_DUMPS-System-View.md) | Provides the FSIDs for the current database/tenant. |
| [FULLTEXT_INDEXES](6-System-Views-Reference/6.01-System-Views/FULLTEXT_INDEXES-System-View.md) | Provides information about fulltext indexes on table columns. |
| [FUNCTION_PARAMETER_COLUMNS](6-System-Views-Reference/6.01-System-Views/FUNCTION_PARAMETER_COLUMNS-System-View.md) | Provides information about columns that are available for function table parameters. |
| [FUNCTION_PARAMETERS](6-System-Views-Reference/6.01-System-Views/FUNCTION_PARAMETERS-System-View.md) | Provides information about parameters for functions. |
| [FUNCTIONS](6-System-Views-Reference/6.01-System-Views/FUNCTIONS-System-View.md) | Provides information about available functions. |
| [GEOCODE_INDEXES](6-System-Views-Reference/6.01-System-Views/GEOCODE_INDEXES-System-View.md) | Provides information about geocode indexes on tables. |
| [GRANTED_PRIVILEGES](6-System-Views-Reference/6.01-System-Views/GRANTED_PRIVILEGES-System-View.md) | Provides information about privileges and roles granted to users. |
| [GRANTED_ROLES](6-System-Views-Reference/6.01-System-Views/GRANTED_ROLES-System-View.md) | Provides information about roles granted to users or other roles. |
| [GRAPH_WORKSPACE_COLUMNS](6-System-Views-Reference/6.01-System-Views/GRAPH_WORKSPACE_COLUMNS-System-View.md) | Provides information on the constituent entities and columns of graph workspaces. |
| [GRAPH_WORKSPACES](6-System-Views-Reference/6.01-System-Views/GRAPH_WORKSPACES-System-View.md) | Provides information about graph workspaces in the database. |
| [HAS_NEEDED_SYSTEM_PRIV](6-System-Views-Reference/6.01-System-Views/HAS_NEEDED_SYSTEM_PRIV-System-View.md) | For internal use only. |
| [HAS_NEEDED_SYSTEM_PRIV_INCL_SYS_STAT](6-System-Views-Reference/6.01-System-Views/HAS_NEEDED_SYSTEM_PRIV_INCL_SYS_STAT-System-View.md) | For internal use only. |
| [HIERARCHY_OBJECTS](6-System-Views-Reference/6.01-System-Views/HIERARCHY_OBJECTS-System-View.md) | Provides the list of objects that hierarchy navigation functions can be run on. |
| [HINTS](6-System-Views-Reference/6.01-System-Views/HINTS-System-View.md) | Provides all available hints to be used in WITH HINT clauses. |
| [INDEX_COLUMNS](6-System-Views-Reference/6.01-System-Views/INDEX_COLUMNS-System-View.md) | Provides information about index columns. |
| [INDEXES](6-System-Views-Reference/6.01-System-Views/INDEXES-System-View.md) | Provides information about indexes on tables. |
| [INVALID_CONNECT_ATTEMPTS](6-System-Views-Reference/6.01-System-Views/INVALID_CONNECT_ATTEMPTS-System-View.md) | Provides the number of invalid connection attempts for a user between two successful connections. |
| [JWT_PROVIDERS](6-System-Views-Reference/6.01-System-Views/JWT_PROVIDERS-System-View.md) | Lists all of the JWT providers configured in the SAP HANA database. |
| [JWT_USER_MAPPINGS](6-System-Views-Reference/6.01-System-Views/JWT_USER_MAPPINGS-System-View.md) | Lists all of the user-JWT mappings configured in the SAP HANA database. |
| [KEY_MANAGEMENT_CONFIGURATIONS](6-System-Views-Reference/6.01-System-Views/KEY_MANAGEMENT_CONFIGURATIONS-System-View.md) | Displays information about the existing key management configurations. |
| [LCM_PRODUCT_INSTANCES](6-System-Views-Reference/6.01-System-Views/LCM_PRODUCT_INSTANCES-System-View.md) | Provides information about all installed product instances. |
| [LCM_PRODUCT_INSTANCES_INCLUDED](6-System-Views-Reference/6.01-System-Views/LCM_PRODUCT_INSTANCES_INCLUDED-System-View.md) | Provides information about all installed included product instances. |
| [LCM_PRODUCTS](6-System-Views-Reference/6.01-System-Views/LCM_PRODUCTS-System-View.md) | Provides information about all installed product versions. |
| [LCM_SOFTWARE_COMPONENTS](6-System-Views-Reference/6.01-System-Views/LCM_SOFTWARE_COMPONENTS-System-View.md) | Provides all installed software component versions. |
| [LCM_SWID](6-System-Views-Reference/6.01-System-Views/LCM_SWID-System-View.md) | Provides all software ID tags for installed software. |
| [LDAP_PROVIDER_URLS](6-System-Views-Reference/6.01-System-Views/LDAP_PROVIDER_URLS-System-View.md) | Lists all LDAP provider URLs. |
| [LDAP_PROVIDERS](6-System-Views-Reference/6.01-System-Views/LDAP_PROVIDERS-System-View.md) | Lists all LDAP providers. |
| [LDAP_USERS](6-System-Views-Reference/6.01-System-Views/LDAP_USERS-System-View.md) | Shows information about the users using LDAP authorization. |
| [LIBRARIES](6-System-Views-Reference/6.01-System-Views/LIBRARIES-System-View.md) | Provides information about available public language libraries. |
| [LIBRARY_MEMBERS](6-System-Views-Reference/6.01-System-Views/LIBRARY_MEMBERS-System-View.md) | Provides member information for SQLScript userdefined libraries. |
| [M_ABSTRACT_SQL_PLAN_OVERVIEW](6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_OVERVIEW-System-View.md) | Provides the status of each Plan Stability Manager on every index server in SAP HANA. |
| [M_ABSTRACT_SQL_PLAN_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_ABSTRACT_SQL_PLAN_STATISTICS-System-View.md) | Provides SQL query runtime statistics. |
| [M_ACTIVE_PROCEDURES](6-System-Views-Reference/6.02-Monitoring-Views/M_ACTIVE_PROCEDURES-System-View.md) | Provides statistics of procedure execution. |
| [M_ACTIVE_STATEMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_ACTIVE_STATEMENTS-System-View.md) | Provides a prepared statements list. |
| [M_ADMISSION_CONTROL_EVENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_ADMISSION_CONTROL_EVENTS-System-View.md) | Displays information about significant events. |
| [M_ADMISSION_CONTROL_QUEUES](6-System-Views-Reference/6.02-Monitoring-Views/M_ADMISSION_CONTROL_QUEUES-System-View.md) | Provides detailed information regarding queued session requests by Session-Wise Admission Control. |
| [M_ADMISSION_CONTROL_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_ADMISSION_CONTROL_STATISTICS-System-View.md) | Provides the overall statistics values of the Session-Wise Admission Control feature. |
| [M_AFL_FUNCTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_AFL_FUNCTIONS-System-View.md) | Provides application function execution information. |
| [M_AFL_STATES](6-System-Views-Reference/6.02-Monitoring-Views/M_AFL_STATES-System-View.md) | Provides information about AFL states. |
| [M_AGENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_AGENTS-System-View.md) | Provides agent host information. |
| [M_ANONYMIZATION_VIEWS](6-System-Views-Reference/6.02-Monitoring-Views/M_ANONYMIZATION_VIEWS-System-View.md) | Provides runtime information about anonymized views. |
| [M_ASYNCHRONOUS_TABLE_REPLICAS](6-System-Views-Reference/6.02-Monitoring-Views/M_ASYNCHRONOUS_TABLE_REPLICAS-System-View.md) | Provides detailed information about asynchronous table replicas. Deprecated. |
| [M_ASYNCHRONOUS_TABLE_REPLICAS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_ASYNCHRONOUS_TABLE_REPLICAS_RESET-System-View.md) | Shows aggregated information on caches (since last reset). |
| [M_ATTACHED_STORAGES](6-System-Views-Reference/6.02-Monitoring-Views/M_ATTACHED_STORAGES-System-View.md) | Provides information about currently attached devices. |
| [M_BACKUP_CATALOG](6-System-Views-Reference/6.02-Monitoring-Views/M_BACKUP_CATALOG-System-View.md) | Provides common data for all backup catalog entries. |
| [M_BACKUP_CATALOG_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_BACKUP_CATALOG_FILES-System-View.md) | Provides location information for all backup catalog entries. |
| [M_BACKUP_CONFIGURATION](6-System-Views-Reference/6.02-Monitoring-Views/M_BACKUP_CONFIGURATION-System-View.md) | Provides backup configuration statistics. |
| [M_BACKUP_HISTORY_BROKEN](6-System-Views-Reference/6.02-Monitoring-Views/M_BACKUP_HISTORY_BROKEN-System-View.md) | Provides information about broken backup history entries. |
| [M_BACKUP_PROGRESS](6-System-Views-Reference/6.02-Monitoring-Views/M_BACKUP_PROGRESS-System-View.md) | Provides the progress of the most recent backup. |
| [M_BACKUP_SIZE_ESTIMATIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_BACKUP_SIZE_ESTIMATIONS-System-View.md) | Provides the estimated size of the next data backup. |
| [M_BLOCKED_TRANSACTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_BLOCKED_TRANSACTIONS-System-View.md) | Provides a transaction list waiting for locks. |
| [M_BUFFER_CACHE_POOL_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_BUFFER_CACHE_POOL_STATISTICS-System-View.md) | Provides statistics for each buffer pool in a cache. |
| [M_BUFFER_CACHE_POOL_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_BUFFER_CACHE_POOL_STATISTICS_RESET-System-View.md) | Provides statistics for each buffer pool in a cache since the last reset. |
| [M_BUFFER_CACHE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_BUFFER_CACHE_STATISTICS-System-View.md) | Provides a cache level overview of the configuration, cache status, and memory usage. |
| [M_BUFFER_CACHE_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_BUFFER_CACHE_STATISTICS_RESET-System-View.md) | Provides a cache level overview of the configuration, cache status, and memory usage since the last reset. |
| [M_CACHE_ENTRIES](6-System-Views-Reference/6.02-Monitoring-Views/M_CACHE_ENTRIES-System-View.md) | Provides cache entry information. |
| [M_CACHES](6-System-Views-Reference/6.02-Monitoring-Views/M_CACHES-System-View.md) | Provides aggregated information on caches. |
| [M_CACHES_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_CACHES_RESET-System-View.md) | Provides aggregated information on caches since the last reset. |
| [M_CATALOG_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_CATALOG_MEMORY-System-View.md) | Provides memory usage information by catalog manager. |
| [M_CE_CALCSCENARIO_HINTS](6-System-Views-Reference/6.02-Monitoring-Views/M_CE_CALCSCENARIO_HINTS-System-View.md) | Exposes all hints that are defined in a calculation scenario. |
| [M_CE_CALCSCENARIOS](6-System-Views-Reference/6.02-Monitoring-Views/M_CE_CALCSCENARIOS-System-View.md) | Provides all available calculation scenarios. |
| [M_CE_CALCSCENARIOS_OVERVIEW](6-System-Views-Reference/6.02-Monitoring-Views/M_CE_CALCSCENARIOS_OVERVIEW-System-View.md) | Provides an overview of Calcscenarios without JSON representation. |
| [M_CE_CALCVIEW_DEPENDENCIES](6-System-Views-Reference/6.02-Monitoring-Views/M_CE_CALCVIEW_DEPENDENCIES-System-View.md) | Provides all views that are referencing a CalculationScenario. |
| [M_CE_DEBUG_INFOS](6-System-Views-Reference/6.02-Monitoring-Views/M_CE_DEBUG_INFOS-System-View.md) | Provides debug information after the execution of a calculation scenario. |
| [M_CE_DEBUG_JSONS](6-System-Views-Reference/6.02-Monitoring-Views/M_CE_DEBUG_JSONS-System-View.md) | Provides all available JSONS (original, instantiated, or optimized) of a scenario for a concrete query. |
| [M_CE_DEBUG_NODE_MAPPING](6-System-Views-Reference/6.02-Monitoring-Views/M_CE_DEBUG_NODE_MAPPING-System-View.md) | Provides information about node mapping between calculation nodes and Runtime nodes after execution. |
| [M_CE_PLE_CALCSCENARIOS](6-System-Views-Reference/6.02-Monitoring-Views/M_CE_PLE_CALCSCENARIOS-System-View.md) | Provides all available calculation scenarios created by the PlanningEngine. |
| [M_CLIENT_VERSIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_CLIENT_VERSIONS-System-View.md) | Provides versions of all supported client applications. |
| [M_COLLECTION_TABLE_VIRTUAL_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_COLLECTION_TABLE_VIRTUAL_FILES-System-View.md) | Provides information about the virtual files for JSON collections. |
| [M_COLLECTION_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_COLLECTION_TABLES-System-View.md) | Provides information about JSON collections. |
| [M_COMPACTION_THREAD](6-System-Views-Reference/6.02-Monitoring-Views/M_COMPACTION_THREAD-System-View.md) | Provides compaction thread statistics. |
| [M_CONDITIONAL_VARIABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_CONDITIONAL_VARIABLES-System-View.md) | Provides semaphore statistics. |
| [M_CONDITIONAL_VARIABLES_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_CONDITIONAL_VARIABLES_RESET-System-View.md) | Semaphore statistics (since last reset) . |
| [M_CONFIGURATION_PARAMETER_VALUES](6-System-Views-Reference/6.02-Monitoring-Views/M_CONFIGURATION_PARAMETER_VALUES-System-View.md) | Displays landscape service parameter values. |
| [M_CONNECTION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_CONNECTION_STATISTICS-System-View.md) | Provides detailed statistics on each connection between an application and database. |
| [M_CONNECTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_CONNECTIONS-System-View.md) | Provides detailed information on connections between a client and a database. Information includes: connection status, client information, connection type, and resource utilization. |
| [M_CONSISTENCY_CHECK_HISTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_CONSISTENCY_CHECK_HISTORY-System-View.md) | Provides table check run information. |
| [M_CONSISTENCY_CHECK_HISTORY_ERRORS](6-System-Views-Reference/6.02-Monitoring-Views/M_CONSISTENCY_CHECK_HISTORY_ERRORS-System-View.md) | Lists the errors that were found within a specified check run. |
| [M_CONTAINER_DIRECTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_CONTAINER_DIRECTORY-System-View.md) | Provides container directory statistics. |
| [M_CONTAINER_NAME_DIRECTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_CONTAINER_NAME_DIRECTORY-System-View.md) | Provides ContainerNameDirectory statistics. |
| [M_CONTEXT_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_CONTEXT_MEMORY-System-View.md) | Provides memory allocator statistics. |
| [M_CONTEXT_MEMORY_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_CONTEXT_MEMORY_RESET-System-View.md) | Provides memory allocator statistics since the last reset. |
| [M_CONVERTER_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_CONVERTER_STATISTICS-System-View.md) | Provides converter statistics. |
| [M_CONVERTER_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_CONVERTER_STATISTICS_RESET-System-View.md) | Provides converter statistics since the last reset. |
| [M_CS_ALL_COLUMN_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_ALL_COLUMN_STATISTICS-System-View.md) | Provides information on how many scans and index searches were performed on any specified columns. |
| [M_CS_ALL_COLUMNS](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_ALL_COLUMNS-System-View.md) | Provides runtime information for all columns in column tables, including internal column tables. |
| [M_CS_COLUMNS](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_COLUMNS-System-View.md) | Provides runtime information about columns in column tables. |
| [M_CS_COLUMNS_PERSISTENCE](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_COLUMNS_PERSISTENCE-System-View.md) | Provides column persistence information for column tables. |
| [M_CS_INDEXES](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_INDEXES-System-View.md) | Provides information for column store indexes. |
| [M_CS_LOADS](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_LOADS-System-View.md) | Provides a history of column loads. |
| [M_CS_LOB_SPACE_RECLAIMS](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_LOB_SPACE_RECLAIMS-System-View.md) | Provides information regarding executed LOB garbage collection runs. |
| [M_CS_LOG_REPLAY_QUEUE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_LOG_REPLAY_QUEUE_STATISTICS-System-View.md) | Provides information about column store log replay queue statistics. |
| [M_CS_LOG_REPLAY_QUEUE_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_LOG_REPLAY_QUEUE_STATISTICS_RESET-System-View.md) | Provides information about column store log replay queue statistics since the last reset. |
| [M_CS_MVCC](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_MVCC-System-View.md) | Provides column store MVCC information. |
| [M_CS_NSE_ADVISOR](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_NSE_ADVISOR-System-View.md) | Provides an SQL interface of the NSE Recommendation Engine and advice on changing the load unit (page/ column) for certain tables in the SAP HANA system, balancing out performance and memory – thus achieving a low… |
| [M_CS_PARTITIONS System View - Deprecated](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_PARTITIONS-System-View-Deprecated.md) | This view is deprecated. Use either the TABLE_PARTITIONS or M_CS_TABLES system view instead. |
| [M_CS_RECORD_LOCK_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_RECORD_LOCK_STATISTICS-System-View.md) | Provides column store record lock information. |
| [M_CS_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_TABLES-System-View.md) | Provides runtime data for column tables. |
| [M_CS_UNLOADS](6-System-Views-Reference/6.02-Monitoring-Views/M_CS_UNLOADS-System-View.md) | Provides a history of column unloads. |
| [M_CUSTOMIZABLE_FUNCTIONALITIES](6-System-Views-Reference/6.02-Monitoring-Views/M_CUSTOMIZABLE_FUNCTIONALITIES-System-View.md) | Provides information about the enablement status of restricted features in databases. The full content of this view is only accessible from the system database. |
| [M_DATA_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_STATISTICS-System-View.md) | Lists data statistics generated when you query column and row store object. |
| [M_DATA_VOLUME_PAGE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_VOLUME_PAGE_STATISTICS-System-View.md) | Provides page usage statistics on data volumes. |
| [M_DATA_VOLUME_PAGE_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_VOLUME_PAGE_STATISTICS_RESET-System-View.md) | Provides information about FreeBlockManager SizeClass statistics since the last reset. |
| [M_DATA_VOLUME_PARTITION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_VOLUME_PARTITION_STATISTICS-System-View.md) | Provides data volume partition statistics. |
| [M_DATA_VOLUME_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_VOLUME_STATISTICS-System-View.md) | Provides information on data volume statistics. |
| [M_DATA_VOLUME_SUPERBLOCK_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_VOLUME_SUPERBLOCK_STATISTICS-System-View.md) | Provides FreeBlockManager Superblock statistics. |
| [M_DATA_VOLUMES](6-System-Views-Reference/6.02-Monitoring-Views/M_DATA_VOLUMES-System-View.md) | Provides data volume statistics. |
| [M_DATABASE](6-System-Views-Reference/6.02-Monitoring-Views/M_DATABASE-System-View.md) | Provides database information. |
| [M_DATABASE_HISTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_DATABASE_HISTORY-System-View.md) | Provides installation version history. |
| [M_DATABASE_REPLICA_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_DATABASE_REPLICA_STATISTICS-System-View.md) | Provides statistics on databases involved in replication. |
| [M_DATABASE_REPLICAS](6-System-Views-Reference/6.02-Monitoring-Views/M_DATABASE_REPLICAS-System-View.md) | Provides source and target information for databases involved in replication. |
| [M_DATABASES](6-System-Views-Reference/6.02-Monitoring-Views/M_DATABASES-System-View.md) | Provides information about all databases in the system. The full content of this view is only accessible from the system database. |
| [M_DEBUG_CONNECTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_DEBUG_CONNECTIONS-System-View.md) | Provides an overview of connections used per debug session. |
| [M_DEBUG_SESSIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_DEBUG_SESSIONS-System-View.md) | Provides an overview of debug sessions and their properties. |
| [M_DELTA_MERGE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_DELTA_MERGE_STATISTICS-System-View.md) | Provides information on table delta merge statistics. |
| [M_DISK_USAGE](6-System-Views-Reference/6.02-Monitoring-Views/M_DISK_USAGE-System-View.md) | Provides disk usage information on host basis group by resource types. |
| [M_DISKS](6-System-Views-Reference/6.02-Monitoring-Views/M_DISKS-System-View.md) | Provides information about disk configuration and utilization of the host machine. |
| [M_DSO_OPERATIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_DSO_OPERATIONS-System-View.md) | Provides information about data store object (DSO) operations. |
| [M_DYNAMIC_RESULT_CACHE](6-System-Views-Reference/6.02-Monitoring-Views/M_DYNAMIC_RESULT_CACHE-System-View.md) | Lists statistics for the dynamic result cache. |
| [M_DYNAMIC_RESULT_CACHE_EXCLUSIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_DYNAMIC_RESULT_CACHE_EXCLUSIONS-System-View.md) | Lists cache exclusions of the dynamic result cache. |
| [M_EFFECTIVE_PASSWORD_POLICY](6-System-Views-Reference/6.02-Monitoring-Views/M_EFFECTIVE_PASSWORD_POLICY-System-View.md) | Provides information about password policy parameters for database users. |
| [M_EFFECTIVE_TABLE_PLACEMENT](6-System-Views-Reference/6.02-Monitoring-Views/M_EFFECTIVE_TABLE_PLACEMENT-System-View.md) | Provides information about effective placement of tables. |
| [M_ENCRYPTION_OVERVIEW](6-System-Views-Reference/6.02-Monitoring-Views/M_ENCRYPTION_OVERVIEW-System-View.md) | Reports the encryption status for all data at rest where encryption is supported. |
| [M_EPM_SESSIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_EPM_SESSIONS-System-View.md) | Provides all EPM sessions with detailed information. |
| [M_ERROR_CODES](6-System-Views-Reference/6.02-Monitoring-Views/M_ERROR_CODES-System-View.md) | Provides error codes with descriptions. |
| [M_ES_CONNECTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_CONNECTIONS-System-View.md) | Provides extended storage connection information. |
| [M_ES_DBSPACE_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_DBSPACE_FILES-System-View.md) | Provides extended storage dbspace file information. |
| [M_ES_DBSPACES](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_DBSPACES-System-View.md) | Provides extended storage dbspace information. |
| [M_ES_DELTA_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_DELTA_MEMORY-System-View.md) | Provides extended storage DELTA memory information. |
| [M_ES_DELTA_MERGE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_DELTA_MERGE_STATISTICS-System-View.md) | Provides extended storage delta merge statistics information. |
| [M_ES_EXPENSIVE_STATEMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_EXPENSIVE_STATEMENTS-System-View.md) | Provides extended storage expensive statement information. |
| [M_ES_LOCKS](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_LOCKS-System-View.md) | Provides extended storage lock information. |
| [M_ES_OVERVIEW](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_OVERVIEW-System-View.md) | Provides extended storage overview information. |
| [M_ES_RESULT_CACHE](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_RESULT_CACHE-System-View.md) | Provides details about each result that has been cached. You must have the EXTENDED STORAGE ADMIN privilege to access this view. |
| [M_ES_SERVICE_REPLICATION](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_SERVICE_REPLICATION-System-View.md) | Provides extended storage service replication information. |
| [M_ES_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_TABLES-System-View.md) | Provides extended storage table information. |
| [M_ES_TRANSACTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_ES_TRANSACTIONS-System-View.md) | Provides extended storage transaction information. |
| [M_EVENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_EVENTS-System-View.md) | Provides information about internal events. |
| [M_EXECUTED_STATEMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_EXECUTED_STATEMENTS-System-View.md) | Provides all statement executions that belong to a specified category. |
| [M_EXPENSIVE_STATEMENT_EXECUTION_LOCATION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_EXPENSIVE_STATEMENT_EXECUTION_LOCATION_STATISTICS-System.md) | Provides location statistics for expensive statements. |
| [M_EXPENSIVE_STATEMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_EXPENSIVE_STATEMENTS-System-View.md) | Provides all statements with a duration longer than a specified threshold. |
| [M_EXPORT_BINARY_STATUS](6-System-Views-Reference/6.02-Monitoring-Views/M_EXPORT_BINARY_STATUS-System-View.md) | Provides export status information for the current session. |
| [M_EXTRACTORS](6-System-Views-Reference/6.02-Monitoring-Views/M_EXTRACTORS-System-View.md) | Provides direct extractor connection (DXC) status information |
| [M_FEATURE_USAGE](6-System-Views-Reference/6.02-Monitoring-Views/M_FEATURE_USAGE-System-View.md) | Provides detailed feature usage statistics. |
| [M_FEATURES](6-System-Views-Reference/6.02-Monitoring-Views/M_FEATURES-System-View.md) | Provides information about all supported features. |
| [M_FULLTEXT_COLUMN_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_FULLTEXT_COLUMN_STATISTICS-System-View.md) | Tracks the usage of fulltext indexes. |
| [M_FULLTEXT_QUEUES](6-System-Views-Reference/6.02-Monitoring-Views/M_FULLTEXT_QUEUES-System-View.md) | Provides fulltext index queue status. |
| [M_FUZZY_SEARCH_INDEXES](6-System-Views-Reference/6.02-Monitoring-Views/M_FUZZY_SEARCH_INDEXES-System-View.md) | Provides runtime information of fuzzy search indexes of column tables. |
| [M_GARBAGE_COLLECTION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_GARBAGE_COLLECTION_STATISTICS-System-View.md) | Provides garbage collection and history manager statistics. |
| [M_GARBAGE_COLLECTION_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_GARBAGE_COLLECTION_STATISTICS_RESET-System-View.md) | Provides accumulated garbage collection and history manager statistics since the last reset. |
| [M_HA_DR_PROVIDERS](6-System-Views-Reference/6.02-Monitoring-Views/M_HA_DR_PROVIDERS-System-View.md) | Provides information about loaded HA/DR providers. |
| [M_HEAP_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_HEAP_MEMORY-System-View.md) | Provides memory allocator statistics. |
| [M_HEAP_MEMORY_AREAS](6-System-Views-Reference/6.02-Monitoring-Views/M_HEAP_MEMORY_AREAS-System-View.md) | Provides memory fragmentation details. |
| [M_HEAP_MEMORY_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_HEAP_MEMORY_RESET-System-View.md) | Provides memory allocator statistics since the last reset. |
| [M_HISTORY_INDEX_LAST_COMMIT_ID](6-System-Views-Reference/6.02-Monitoring-Views/M_HISTORY_INDEX_LAST_COMMIT_ID-System-View.md) | Provides the last commit ID of a history index for each session. |
| [M_HOST_AGENT_INFORMATION](6-System-Views-Reference/6.02-Monitoring-Views/M_HOST_AGENT_INFORMATION-System-View.md) | Displays computer system information retrieved from the SAP Host Agent. |
| [M_HOST_AGENT_METRICS](6-System-Views-Reference/6.02-Monitoring-Views/M_HOST_AGENT_METRICS-System-View.md) | Displays performance metrics retrieved from the SAP Host Agent. |
| [M_HOST_INFORMATION](6-System-Views-Reference/6.02-Monitoring-Views/M_HOST_INFORMATION-System-View.md) | Provides host information such as machine and OS configuration. |
| [M_HOST_NETWORK_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_HOST_NETWORK_STATISTICS-System-View.md) | Provides information about the network statistics of a host. |
| [M_HOST_RESOURCE_UTILIZATION](6-System-Views-Reference/6.02-Monitoring-Views/M_HOST_RESOURCE_UTILIZATION-System-View.md) | Provides information about host resource utilization by all processes (including non-SAP HANA processes). CPU time is in milliseconds and added across all cores since system start. |
| [M_IMPORT_BINARY_STATUS](6-System-Views-Reference/6.02-Monitoring-Views/M_IMPORT_BINARY_STATUS-System-View.md) | Provides import status information for the current session. |
| [M_INDEXING_QUEUES](6-System-Views-Reference/6.02-Monitoring-Views/M_INDEXING_QUEUES-System-View.md) | Provides the status of indexing queues. |
| [M_INIFILE_CONTENT_HISTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENT_HISTORY-System-View.md) | Provides change history information for configuration (ini) files. |
| [M_INIFILE_CONTENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILE_CONTENTS-System-View.md) | Provides configuration information from INI files. |
| [M_INIFILES](6-System-Views-Reference/6.02-Monitoring-Views/M_INIFILES-System-View.md) | Provides information about all configuration files. |
| [M_JOB_HISTORY_INFO](6-System-Views-Reference/6.02-Monitoring-Views/M_JOB_HISTORY_INFO-System-View.md) | Provides a history of long running system operations. |
| [M_JOB_PROGRESS](6-System-Views-Reference/6.02-Monitoring-Views/M_JOB_PROGRESS-System-View.md) | Provides information about current long running system operations. |
| [M_JOBEXECUTORS](6-System-Views-Reference/6.02-Monitoring-Views/M_JOBEXECUTORS-System-View.md) | Provides job executor statistics. |
| [M_JOBEXECUTORS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_JOBEXECUTORS_RESET-System-View.md) | Provides values accumulated since the last reset of the main view M_JOBEXECUTORS. |
| [M_JOIN_DATA_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_JOIN_DATA_STATISTICS-System-View.md) | Provides column store join engine join statistics. |
| [M_JOIN_TRANSLATION_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_JOIN_TRANSLATION_TABLES-System-View.md) | Provides column store join engine translation tables statistics. |
| [M_JOINENGINE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_JOINENGINE_STATISTICS-System-View.md) | Provides statistics about join engine runtime objects used for column store join operations. |
| [M_KERNEL_PROFILER](6-System-Views-Reference/6.02-Monitoring-Views/M_KERNEL_PROFILER-System-View.md) | Displays the state and provides information about Kernel Profilers in the system. You must have the RESOURCE ADMIN or TRACE ADMIN system privileges to use this view. |
| [M_LANDSCAPE_HOST_CONFIGURATION](6-System-Views-Reference/6.02-Monitoring-Views/M_LANDSCAPE_HOST_CONFIGURATION-System-View.md) | Specifies the host roles in a distributed landscape. |
| [M_LICENSE](6-System-Views-Reference/6.02-Monitoring-Views/M_LICENSE-System-View.md) | Provides information on the currently valid license for the SAP HANA database that is installed on this system. |
| [M_LICENSE_MEASUREMENT_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_LICENSE_MEASUREMENT_STATISTICS-System-View.md) | Collects license measurement statistics from tenant databases. |
| [M_LICENSE_MEASUREMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_LICENSE_MEASUREMENTS-System-View.md) | Product usage measurements for licensing. |
| [M_LICENSE_USAGE_HISTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_LICENSE_USAGE_HISTORY-System-View.md) | Information on the maximum resource consumption per time period, used for validity check of license installed on this system (if any). |
| [M_LICENSES](6-System-Views-Reference/6.02-Monitoring-Views/M_LICENSES-System-View.md) | Provides information on all of the licenses (if any) that are installed on this system. |
| [M_LIVECACHE_CONTAINER_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_CONTAINER_STATISTICS-System-View.md) | Provides accumulated liveCache container statistics. |
| [M_LIVECACHE_CONTAINER_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_CONTAINER_STATISTICS_RESET-System-View.md) | Provides accumulated LiveCache container statistics since last reset. |
| [M_LIVECACHE_LOCK_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_LOCK_STATISTICS-System-View.md) | Provides accumulated LiveCache lock statistics. |
| [M_LIVECACHE_LOCK_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_LOCK_STATISTICS_RESET-System-View.md) | LiveCache lock statistics (since last reset). |
| [M_LIVECACHE_LOCKS](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_LOCKS-System-View.md) | Detailed information on the Object Management System (OMS) locks. |
| [M_LIVECACHE_OMS_VERSIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_OMS_VERSIONS-System-View.md) | Detailed information on the OMS versions that currently exists. |
| [M_LIVECACHE_PROCEDURE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_PROCEDURE_STATISTICS-System-View.md) | Provides accumulated LiveCache procedure statistics. |
| [M_LIVECACHE_PROCEDURE_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_PROCEDURE_STATISTICS_RESET-System-View.md) | LiveCache procedure statistics (since last reset). |
| [M_LIVECACHE_SCHEMA_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_SCHEMA_STATISTICS-System-View.md) | Provides accumulated liveCache schema statistics. |
| [M_LIVECACHE_SCHEMA_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_LIVECACHE_SCHEMA_STATISTICS_RESET-System-View.md) | Provides accumulated LiveCache schema statistics since the last reset. |
| [M_LOAD_HISTORY_HOST](6-System-Views-Reference/6.02-Monitoring-Views/M_LOAD_HISTORY_HOST-System-View.md) | Host specific load history KPIs. |
| [M_LOAD_HISTORY_INFO](6-System-Views-Reference/6.02-Monitoring-Views/M_LOAD_HISTORY_INFO-System-View.md) | Load history KPI description. |
| [M_LOAD_HISTORY_SERVICE](6-System-Views-Reference/6.02-Monitoring-Views/M_LOAD_HISTORY_SERVICE-System-View.md) | Lists servicespecific load history KPIs. |
| [M_LOCK_WAITS_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_LOCK_WAITS_STATISTICS-System-View.md) | Provides the accumulated lock wait count and duration for record locks, table locks, and metadata locks for all available services from database start up until the current time. |
| [M_LOG_BUFFERS](6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_BUFFERS-System-View.md) | Provides information about log buffer statistics. |
| [M_LOG_BUFFERS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_BUFFERS_RESET-System-View.md) | Provides log buffer statistics since the last reset. |
| [M_LOG_PARTITIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_PARTITIONS-System-View.md) | Provides log partition statistics. |
| [M_LOG_PARTITIONS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_PARTITIONS_RESET-System-View.md) | Provides log partition statistics since the last reset. |
| [M_LOG_REPLAY_QUEUE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_REPLAY_QUEUE_STATISTICS-System-View.md) | Provides information about log replay queue statistics. |
| [M_LOG_REPLAY_QUEUE_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_REPLAY_QUEUE_STATISTICS_RESET-System-View.md) | Provides information about log replay queue statistics. |
| [M_LOG_SEGMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_SEGMENTS-System-View.md) | Provides log segment statistics. |
| [M_LOG_SEGMENTS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_LOG_SEGMENTS_RESET-System-View.md) | Provides log segment statistics since the last reset. |
| [M_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_MEMORY-System-View.md) | Deprecated. For servicespecific information related to memory, use the M_SERVICE_MEMORY System View topic and for hostspecific information related to memory, use the M_HOST_RESOURCE_UTILIZATION System View topic. |
| [M_MEMORY_OBJECT_DISPOSITIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_MEMORY_OBJECT_DISPOSITIONS-System-View.md) | Displays the dispositionspecific memory object statistics. |
| [M_MEMORY_OBJECTS](6-System-Views-Reference/6.02-Monitoring-Views/M_MEMORY_OBJECTS-System-View.md) | Returns memory object statistics. |
| [M_MEMORY_OBJECTS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_MEMORY_OBJECTS_RESET-System-View.md) | Provides values accumulated since the last reset of the main view M_MEMORY_OBJECTS. |
| [M_MEMORY_PROFILER](6-System-Views-Reference/6.02-Monitoring-Views/M_MEMORY_PROFILER-System-View.md) | Provides memory profiler information. |
| [M_MEMORY_RECLAIM_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_MEMORY_RECLAIM_STATISTICS-System-View.md) | Provides statistics for reclaiming memory (for example, defragmentation, unloading of memory objects, and so on). |
| [M_MEMORY_RECLAIM_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_MEMORY_RECLAIM_STATISTICS_RESET-System-View.md) | Provides statistics for reclaiming memory (for example, defragmentation, unloading of memory objects, and so on) since the last reset. |
| [M_MERGED_TRACES](6-System-Views-Reference/6.02-Monitoring-Views/M_MERGED_TRACES-System-View.md) | Contains the merged content of the server trace files for all of the SAP HANA services. |
| [M_METADATA_CACHE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_METADATA_CACHE_STATISTICS-System-View.md) | Provides information regarding the efficiency and use of the metadata cache. |
| [M_MONITOR_COLUMNS](6-System-Views-Reference/6.02-Monitoring-Views/M_MONITOR_COLUMNS-System-View.md) | All the columns in the monitoring views. |
| [M_MONITORS](6-System-Views-Reference/6.02-Monitoring-Views/M_MONITORS-System-View.md) | Provides available monitoring view information. |
| [M_MULTIDIMENSIONAL_STATEMENT_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_MULTIDIMENSIONAL_STATEMENT_STATISTICS-System-View.md) | Displays all multidimensional statement statistics gathered since the server started. This information does not persist when you restart the server. |
| [M_MUTEXES](6-System-Views-Reference/6.02-Monitoring-Views/M_MUTEXES-System-View.md) | Provides information about single mutex (mutual exclusion) objects or groups of mutex objects. |
| [M_MUTEXES_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_MUTEXES_RESET-System-View.md) | Provides mutex statistics since the last reset. |
| [M_MVCC_OVERVIEW](6-System-Views-Reference/6.02-Monitoring-Views/M_MVCC_OVERVIEW-System-View.md) | Provides an overview of the row-store Multiversion Concurrency Control (MVCC) manager. |
| [M_MVCC_SNAPSHOTS](6-System-Views-Reference/6.02-Monitoring-Views/M_MVCC_SNAPSHOTS-System-View.md) | Provides detailed snapshot information of the Multiversion Concurrency Control (MVCC) manager. |
| [M_MVCC_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_MVCC_TABLES-System-View.md) | Provides statistics for the row-store Multiversion Concurrency Control (MVCC) manager. |
| [M_NUMA_NODES](6-System-Views-Reference/6.02-Monitoring-Views/M_NUMA_NODES-System-View.md) | Provides resource availability information on each NUMA node in the hardware topology, including inter-node distances and neighbor information. |
| [M_NUMA_RESOURCES](6-System-Views-Reference/6.02-Monitoring-Views/M_NUMA_RESOURCES-System-View.md) | Provides information on overall resource availability for the system. |
| [M_OBJECT_LOCK_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_OBJECT_LOCK_STATISTICS-System-View.md) | Provides lock contention statistics, including lock wait count, wait time, and failed count, for each object. |
| [M_OBJECT_LOCK_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_OBJECT_LOCK_STATISTICS_RESET-System-View.md) | Provides lock contention statistics, including lock wait count, wait time, and failed count for each object since the last reset. |
| [M_OBJECT_LOCKS](6-System-Views-Reference/6.02-Monitoring-Views/M_OBJECT_LOCKS-System-View.md) | Provides the status of currently acquired locks on objects with detailed information such as lock acquisition time and lock mode. |
| [M_OUT_OF_MEMORY_EVENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_OUT_OF_MEMORY_EVENTS-System-View.md) | Provides a list of the last 20 out-of-memory (OOM) events. |
| [M_OUT_OF_MEMORY_EVENTS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_OUT_OF_MEMORY_EVENTS_RESET-System-View.md) | Provides a list of the last out-of-memory (OOM) events since the last reset. |
| [M_PAGEACCESS_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_PAGEACCESS_STATISTICS-System-View.md) | Provides PageAccess statistics. |
| [M_PAGEACCESS_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_PAGEACCESS_STATISTICS_RESET-System-View.md) | Provides the PageAccess statistics since the last reset. |
| [M_PASSWORD_POLICY](6-System-Views-Reference/6.02-Monitoring-Views/M_PASSWORD_POLICY-System-View.md) | Defines effective password policy settings. |
| [M_PERFTRACE](6-System-Views-Reference/6.02-Monitoring-Views/M_PERFTRACE-System-View.md) | Displays the state of the current performance trace. The performance trace provides detailed information about query execution. |
| [M_PERSISTENCE_ENCRYPTION_KEYS](6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_ENCRYPTION_KEYS-System-View.md) | Provides information about encryption page keys. |
| [M_PERSISTENCE_ENCRYPTION_STATUS](6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_ENCRYPTION_STATUS-System-View.md) | Provides information about persistence encryption. |
| [M_PERSISTENCE_MANAGERS](6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_MANAGERS-System-View.md) | Provides persistence manager statistics. |
| [M_PERSISTENCE_MANAGERS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENCE_MANAGERS_RESET-System-View.md) | Provides persistence manager statistics since the last reset. |
| [M_PERSISTENT_MEMORY_VOLUME_DATA_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENT_MEMORY_VOLUME_DATA_FILES-System-View.md) | Reports metadata statistics about files created by SAP HANA services for data storage on the persistent memory volumes. |
| [M_PERSISTENT_MEMORY_VOLUME_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENT_MEMORY_VOLUME_STATISTICS-System-View.md) | Reports the statistics of physical lifecycle events of blocks managed by SAP HANA services on the persistent memory volumes. |
| [M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENT_MEMORY_VOLUME_STATISTICS_RESET-System-View.md) | Reports the statistics of physical lifecycle events of blocks managed by SAP HANA services on the persistent memory volumes since the last reset. |
| [M_PERSISTENT_MEMORY_VOLUMES](6-System-Views-Reference/6.02-Monitoring-Views/M_PERSISTENT_MEMORY_VOLUMES-System-View.md) | Reports the capacity, usage and metadata of persistent memory volumes. |
| [M_PLE_RUNTIME_OBJECTS](6-System-Views-Reference/6.02-Monitoring-Views/M_PLE_RUNTIME_OBJECTS-System-View.md) | Lists all the internal cache objects created to support the planning sessions, with details about each one. |
| [M_PLE_SESSIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_PLE_SESSIONS-System-View.md) | Lists all planning sessions on the system as well as their status and details. |
| [M_PLUGIN_MANIFESTS](6-System-Views-Reference/6.02-Monitoring-Views/M_PLUGIN_MANIFESTS-System-View.md) | Provides information about installed plugins. |
| [M_PLUGIN_STATUS](6-System-Views-Reference/6.02-Monitoring-Views/M_PLUGIN_STATUS-System-View.md) | Provides status for plugins. |
| [M_PREPARED_STATEMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_PREPARED_STATEMENTS-System-View.md) | Provides information about prepared statements. |
| [M_QUERY_CACHED_PLANS System View - Deprecated](6-System-Views-Reference/6.02-Monitoring-Views/M_QUERY_CACHED_PLANS-System-View-Deprecated.md) | Provides query cached plan information. |
| [M_READWRITELOCKS](6-System-Views-Reference/6.02-Monitoring-Views/M_READWRITELOCKS-System-View.md) | Provides read and write lock statistics. |
| [M_READWRITELOCKS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_READWRITELOCKS_RESET-System-View.md) | Provides read/write lock statistics since the last reset. |
| [M_RECORD_LOCKS](6-System-Views-Reference/6.02-Monitoring-Views/M_RECORD_LOCKS-System-View.md) | Provides the record lock status. |
| [M_RECOVERY_PROGRESS](6-System-Views-Reference/6.02-Monitoring-Views/M_RECOVERY_PROGRESS-System-View.md) | Shows the progress of the most recent recoveries of tenant databases. M_RECOVERY_PROGRESS is in the SYS_DATABASES schema of a system database. |
| [M_REMOTE_CONNECTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_CONNECTIONS-System-View.md) | Provides detailed information on remote connections between databases and remote sources. The information includes connection status, adapter name, and adapter properties. |
| [M_REMOTE_SOURCE_LATENCY_HISTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SOURCE_LATENCY_HISTORY-System-View.md) |  |
| [M_REMOTE_SOURCE_LATENCY_STATUS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SOURCE_LATENCY_STATUS-System-View.md) | Provides remote source latency status information. |
| [M_REMOTE_SOURCE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SOURCE_STATISTICS-System-View.md) | Returns the remote source operational statistics for monitoring data provisioning components. |
| [M_REMOTE_SOURCES](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SOURCES-System-View.md) | Provides remote source information. |
| [M_REMOTE_STATEMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_STATEMENTS-System-View.md) | Displays detailed information about executed remote queries. This information includes the query status and the number of fetched rows. |
| [M_REMOTE_SUBSCRIPTION_COMMIT_SEQUENCE_CONTAINERS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTION_COMMIT_SEQUENCE_CONTAINERS-System-View.md) | Lists all real time data elements such as markers and commit / rollback rows in the remote subscription commit sequence container. |
| [M_REMOTE_SUBSCRIPTION_COMMIT_SEQUENCE_GROUP_CONTAINERS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTION_COMMIT_SEQUENCE_GROUP_CONTAINERS.md) | Lists all CommitSequece virtual files for a remote source, and the number of entries stored in each virtual file. |
| [M_REMOTE_SUBSCRIPTION_COMPONENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTION_COMPONENTS-System-View.md) | Provides remote subscription component information. |
| [M_REMOTE_SUBSCRIPTION_DISTRIBUTOR_QUEUE_DATA_CONTAINERS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTION_DISTRIBUTOR_QUEUE_DATA_CONTAINERS.md) | Lists all real time data elements between begin-marker and end-marker for the remote subscription. |
| [M_REMOTE_SUBSCRIPTION_LOB_CONTAINERS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTION_LOB_CONTAINERS-System-View.md) | Lists all lob container IDs for each remote subscription transaction. |
| [M_REMOTE_SUBSCRIPTION_ROLLBACK_SAVEPOINT_CONTAINERS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTION_ROLLBACK_SAVEPOINT_CONTAINERS-System.md) | Lists all rollback save points for each remote subscription transaction. |
| [M_REMOTE_SUBSCRIPTION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTION_STATISTICS-System-View.md) | Provides remote subscription statistic information. |
| [M_REMOTE_SUBSCRIPTION_TRANSACTION_CONTAINERS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTION_TRANSACTION_CONTAINERS-System-View.md) | Lists all real time data rowsets in the remote subscription transaction container. |
| [M_REMOTE_SUBSCRIPTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_SUBSCRIPTIONS-System-View.md) | Provides the status and run-time information of a remote subscription. |
| [M_REMOTE_TABLE_REPLICAS](6-System-Views-Reference/6.02-Monitoring-Views/M_REMOTE_TABLE_REPLICAS-System-View.md) | Provides remote table replication information. |
| [M_REORG_ALGORITHMS](6-System-Views-Reference/6.02-Monitoring-Views/M_REORG_ALGORITHMS-System-View.md) | Provides information about landscape redistribution algorithms. |
| [M_REPLICATION_LOG](6-System-Views-Reference/6.02-Monitoring-Views/M_REPLICATION_LOG-System-View.md) | Provides replication log monitoring information. |
| [M_REPO_TRANSPORT_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_REPO_TRANSPORT_FILES-System-View.md) | Provides information about all repository transport files. |
| [M_RESULT_CACHE](6-System-Views-Reference/6.02-Monitoring-Views/M_RESULT_CACHE-System-View.md) | Provides result cache information. |
| [M_RESULT_CACHE_EXCLUSIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_RESULT_CACHE_EXCLUSIONS-System-View.md) | Provides information about result cache exclusions. |
| [M_RESULT_CACHE_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_RESULT_CACHE_RESET-System-View.md) | Provides information about result cache statistics. |
| [M_RS_INDEXES](6-System-Views-Reference/6.02-Monitoring-Views/M_RS_INDEXES-System-View.md) | Provides the statistics for B-tree and CPB-tree indexes. |
| [M_RS_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_RS_MEMORY-System-View.md) | Provides RS memory statistics. |
| [M_RS_TABLE_VERSION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_RS_TABLE_VERSION_STATISTICS-System-View.md) | Provides information on row table versions: detailed version counts and used sizes. |
| [M_RS_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_RS_TABLES-System-View.md) | Provides information about row tables, including detailed table sizes and record count. |
| [M_SAVEPOINT_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_SAVEPOINT_STATISTICS-System-View.md) | Provides information about executed savepoints. |
| [M_SAVEPOINT_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_SAVEPOINT_STATISTICS_RESET-System-View.md) | Provides the savepoint statistics since the last reset. |
| [M_SAVEPOINTS](6-System-Views-Reference/6.02-Monitoring-Views/M_SAVEPOINTS-System-View.md) | Displays current and historical savepoint statistics. |
| [M_SECURESTORE](6-System-Views-Reference/6.02-Monitoring-Views/M_SECURESTORE-System-View.md) | Provides secure store monitoring information. |
| [M_SEMAPHORES](6-System-Views-Reference/6.02-Monitoring-Views/M_SEMAPHORES-System-View.md) | Provides semaphore statistics. |
| [M_SEMAPHORES_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_SEMAPHORES_RESET-System-View.md) | Provides semaphore statistics since the last reset. |
| [M_SEQUENCES](6-System-Views-Reference/6.02-Monitoring-Views/M_SEQUENCES-System-View.md) | Provides statistics for sequence caches. |
| [M_SERIES_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_SERIES_TABLES-System-View.md) | Provides statistics on the physical contents of series tables. |
| [M_SERVICE_COMPONENT_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_COMPONENT_MEMORY-System-View.md) | Provides servicespecific memory usage by logical component. |
| [M_SERVICE_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_MEMORY-System-View.md) | Displays detailed memory utilization information by services. |
| [M_SERVICE_NETWORK_IO](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_NETWORK_IO-System-View.md) | Provides service network I/O statistics. |
| [M_SERVICE_NETWORK_IO_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_NETWORK_IO_RESET-System-View.md) | Provides the service network I/O statistics since the last reset. |
| [M_SERVICE_NETWORK_METHOD_IO](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_NETWORK_METHOD_IO-System-View.md) | Displays the number of calls and amount of data that is sent and received. |
| [M_SERVICE_NETWORK_METHOD_IO_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_NETWORK_METHOD_IO_RESET-System-View.md) | Provides service network method I/O statistics since the last reset. |
| [M_SERVICE_REPLICATION](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_REPLICATION-System-View.md) | Provides information about replicated services. |
| [M_SERVICE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_STATISTICS-System-View.md) | Provides statistics on active services. |
| [M_SERVICE_THREAD_CALLSTACKS](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_THREAD_CALLSTACKS-System-View.md) | Provides stack frame information for service threads. |
| [M_SERVICE_THREAD_SAMPLES](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_THREAD_SAMPLES-System-View.md) | Displays detailed information about locks held by threads. |
| [M_SERVICE_THREADS](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_THREADS-System-View.md) | Displays detailed information about threads created by services. |
| [M_SERVICE_TRACES](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_TRACES-System-View.md) | Provides configured trace components for each service type. |
| [M_SERVICE_TYPES](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICE_TYPES-System-View.md) | Provides information about service types. |
| [M_SERVICES](6-System-Views-Reference/6.02-Monitoring-Views/M_SERVICES-System-View.md) | Provides the status of all services. |
| [M_SESSION_CONTEXT](6-System-Views-Reference/6.02-Monitoring-Views/M_SESSION_CONTEXT-System-View.md) | Displays the session variables set for each connection. |
| [M_SHARED_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_SHARED_MEMORY-System-View.md) | Provides shared memory usage information for the SAP HANA indexserver. |
| [M_SNAPSHOTS](6-System-Views-Reference/6.02-Monitoring-Views/M_SNAPSHOTS-System-View.md) | Provides information about existing snapshots. |
| [M_SQL_CLIENT_NETWORK_IO](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_CLIENT_NETWORK_IO-System-View.md) | Provides the client and server elapsed time as well as message sizes for client network messages. |
| [M_SQL_PLAN_CACHE](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE-System-View.md) | Provides statistics for an individual execution plan. |
| [M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS-System-View.md) | Provides statistics for hosts where plans were executed. |
| [M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE_EXECUTION_LOCATION_STATISTICS_RESET-System.md) | Provides statistics for hosts where plans were executed. |
| [M_SQL_PLAN_CACHE_OVERVIEW](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE_OVERVIEW-System-View.md) | Provides overall statistics of evicted and cached plans |
| [M_SQL_PLAN_CACHE_PARAMETERS](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE_PARAMETERS-System-View.md) | Provides bind parameters for statements cached in SQL Plan Cache. It saves a parameter set of the most expensive execution for each plan. |
| [M_SQL_PLAN_CACHE_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_CACHE_RESET-System-View.md) | Provides statistics of an individual execution plan since the last reset. |
| [M_SQL_PLAN_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_STATISTICS-System-View.md) | Provides statistics of a live or evicted individual execution plan. |
| [M_SQL_PLAN_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_SQL_PLAN_STATISTICS_RESET-System-View.md) | Provides statistics of a live or evicted individual execution plan since the last reset. |
| [M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_CODE_COVERAGE_OBJECT_DEFINITIONS-System-View.md) | Provides definitions for the objects referenced in SQLScript code coverage results. |
| [M_SQLSCRIPT_CODE_COVERAGE_RESULTS](6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_CODE_COVERAGE_RESULTS-System-View.md) | Provides per-session SQLScript code coverage results. |
| [M_SQLSCRIPT_PLAN_PROFILER_RESULTS](6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_PLAN_PROFILER_RESULTS-System-View.md) | Stores the results generated by the SQLScript plan profiler. |
| [M_SQLSCRIPT_PLAN_PROFILERS](6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_PLAN_PROFILERS-System-View.md) | Lists the sessions and procedures that are currently being profiled by the SQLScript plan profiler. |
| [M_SQLSCRIPT_VARIABLE_CACHE System view](6-System-Views-Reference/6.02-Monitoring-Views/M_SQLSCRIPT_VARIABLE_CACHE-System-view.md) | Provides runtime information about procedures and functions that have variable caches defined. |
| [M_STATISTICS_LASTVALUES](6-System-Views-Reference/6.02-Monitoring-Views/M_STATISTICS_LASTVALUES-System-View.md) | Provides an in-memory version of _SYS_STATISTICS.STATISTICS_LASTVALUES. |
| [M_STREAMING_APPLICATIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_APPLICATIONS-System-View.md) | Provides streaming application monitoring information. |
| [M_STREAMING_PROJECT_ADAPTER_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_PROJECT_ADAPTER_STATISTICS-System-View.md) | Provides streaming project adapter statistics monitoring information. |
| [M_STREAMING_PROJECT_ADAPTERS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_PROJECT_ADAPTERS-System-View.md) | Provides streaming project adapter monitoring information. |
| [M_STREAMING_PROJECT_GD_SUBSCRIPTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_PROJECT_GD_SUBSCRIPTIONS-System-View.md) | Provides streaming project Guaranteed Delivery (GD) subscription monitoring information. |
| [M_STREAMING_PROJECT_PUBLISHERS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_PROJECT_PUBLISHERS-System-View.md) | Provides streaming project publishers monitoring information. |
| [M_STREAMING_PROJECT_STREAMS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_PROJECT_STREAMS-System-View.md) | Provides streaming project stream monitoring information. |
| [M_STREAMING_PROJECT_SUBSCRIBERS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_PROJECT_SUBSCRIBERS-System-View.md) | Provides monitoring information regarding streaming project subscribers. |
| [M_STREAMING_PROJECTS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_PROJECTS-System-View.md) | Provides streaming project monitoring information. |
| [M_STREAMING_SCHEMAS](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_SCHEMAS-System-View.md) | Provides streaming schema monitoring information. |
| [M_STREAMING_SERVICES](6-System-Views-Reference/6.02-Monitoring-Views/M_STREAMING_SERVICES-System-View.md) | Provides streaming service monitoring information. |
| [M_SYSTEM_AVAILABILITY](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_AVAILABILITY-System-View.md) | Monitors the availability of the system. |
| [M_SYSTEM_DATA_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_DATA_STATISTICS-System-View.md) | Lists data statistics generated by the server when you query a column and row store object. |
| [M_SYSTEM_INFORMATION_STATEMENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_INFORMATION_STATEMENTS-System-View.md) | Provides system information statements. |
| [M_SYSTEM_LIMITS](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_LIMITS-System-View.md) | Provides system limit information. |
| [M_SYSTEM_OVERVIEW](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_OVERVIEW-System-View.md) | Provides an overview of system status including important resource usage information and alerts. |
| [M_SYSTEM_REPLICATION](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_REPLICATION-System-View.md) | Monitors system replication information. |
| [M_SYSTEM_REPLICATION_MVCC_HISTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_REPLICATION_MVCC_HISTORY-System-View.md) | Displays the global multi-version concurrency control (MVCC) timestamp history in the secondary site for system replication. The global MVCC timestamp of the secondary site is updated after a chunk of logs from the… |
| [M_SYSTEM_REPLICATION_TAKEOVER_HISTORY](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_REPLICATION_TAKEOVER_HISTORY-System-View.md) | Provides access to a history of HSR takeover executions. |
| [M_SYSTEM_REPLICATION_TIMETRAVEL](6-System-Views-Reference/6.02-Monitoring-Views/M_SYSTEM_REPLICATION_TIMETRAVEL-System-View.md) | Provides information about the valid time travel range for each service on a secondary site. |
| [M_TABLE_LOB_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_LOB_FILES-System-View.md) | Provides information about all LOB files that belong to a table. |
| [M_TABLE_LOB_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_LOB_STATISTICS-System-View.md) | Provides information about the aggregated file and packed LOB statistics per host, port, table, partition, and column. |
| [M_TABLE_LOCATIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_LOCATIONS-System-View.md) | Provides information about tables and their logical location. Physical locations are shown in M_TABLE_PERSISTENCE_LOCATIONS. |
| [M_TABLE_LOCKS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_LOCKS-System-View.md) | Shows table locks. |
| [M_TABLE_PARTITION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PARTITION_STATISTICS-System-View.md) | Returns the table partition runtime statistics for column store partition tables only. This view is empty if the partition_statistics_select_enabled property in the `indexserver.ini` configuration file is disabled. |
| [M_TABLE_PARTITIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PARTITIONS-System-View.md) | Provides information regarding partitionspecific memory and disk usage for partitioned tables. |
| [M_TABLE_PERSISTENCE_LOCATION_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PERSISTENCE_LOCATION_STATISTICS-System-View.md) | Provides persistence storage statistics for tables partitions and services. |
| [M_TABLE_PERSISTENCE_LOCATIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PERSISTENCE_LOCATIONS-System-View.md) | Provides information about column store tables and their physical data locations. |
| [M_TABLE_PERSISTENCE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PERSISTENCE_STATISTICS-System-View.md) | Provides persistence virtual file summary statistics for tables. |
| [M_TABLE_PERSISTENT_MEMORY_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PERSISTENT_MEMORY_FILES-System-View.md) | Displays the persistent memory file information for all of the tables in the database. |
| [M_TABLE_PLACEMENT_LOCATIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PLACEMENT_LOCATIONS-System-View.md) | Provides table placement location monitoring information. |
| [M_TABLE_PRUNING_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_PRUNING_STATISTICS-System-View.md) | Provides an interface to access statistics for historical data. This data helps detect unexpectedly heavy historical processing by an application, including disclosure of unqualified historical queries as well as… |
| [M_TABLE_REPLICAS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_REPLICAS-System-View.md) | Provides detailed information on asynchronous/synchronous table replicas. |
| [M_TABLE_REPLICAS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_REPLICAS_RESET-System-View.md) | Provides detailed information on asynchronous/synchronous table replicas. |
| [M_TABLE_SNAPSHOTS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_SNAPSHOTS-System-View.md) | Provides snapshot information for tables that are blocked by table-wise GC. |
| [M_TABLE_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_STATISTICS-System-View.md) | Returns the table runtime statistics. |
| [M_TABLE_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_STATISTICS_RESET-System-View.md) | Returns the table DML runtime statistics since the last reset. |
| [M_TABLE_VIRTUAL_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLE_VIRTUAL_FILES-System-View.md) | Provides information about all virtual files that belong to a table. |
| [M_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_TABLES-System-View.md) | Provides information on row and column tables, as well as collection tables (JSON Document Store). |
| [M_TASKS](6-System-Views-Reference/6.02-Monitoring-Views/M_TASKS-System-View.md) | Provides task monitoring information. |
| [M_TEMPORARY_JOIN_CONDITIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_TEMPORARY_JOIN_CONDITIONS-System-View.md) | Provides information about temporary join conditions. |
| [M_TEMPORARY_JOIN_CONSTRAINTS](6-System-Views-Reference/6.02-Monitoring-Views/M_TEMPORARY_JOIN_CONSTRAINTS-System-View.md) | Provides information about temporary join constraints. |
| [M_TEMPORARY_KEY_FIGURES](6-System-Views-Reference/6.02-Monitoring-Views/M_TEMPORARY_KEY_FIGURES-System-View.md) | Provides information about temporary key figures. |
| [M_TEMPORARY_OBJECT_DEPENDENCIES](6-System-Views-Reference/6.02-Monitoring-Views/M_TEMPORARY_OBJECT_DEPENDENCIES-System-View.md) | Provides information about temporary object dependencies for transient objects. |
| [M_TEMPORARY_TABLE_COLUMNS](6-System-Views-Reference/6.02-Monitoring-Views/M_TEMPORARY_TABLE_COLUMNS-System-View.md) | Provides information about temporary table columns. |
| [M_TEMPORARY_TABLES](6-System-Views-Reference/6.02-Monitoring-Views/M_TEMPORARY_TABLES-System-View.md) | Provides information about temporary tables. |
| [M_TEMPORARY_VIEW_COLUMNS](6-System-Views-Reference/6.02-Monitoring-Views/M_TEMPORARY_VIEW_COLUMNS-System-View.md) | Provides information about temporary view columns. |
| [M_TEMPORARY_VIEWS](6-System-Views-Reference/6.02-Monitoring-Views/M_TEMPORARY_VIEWS-System-View.md) | Displays temporary views. |
| [M_TEXT_ANALYSIS_LANGUAGES](6-System-Views-Reference/6.02-Monitoring-Views/M_TEXT_ANALYSIS_LANGUAGES-System-View.md) | Provides a list of supported languages. |
| [M_TEXT_ANALYSIS_MIME_TYPES](6-System-Views-Reference/6.02-Monitoring-Views/M_TEXT_ANALYSIS_MIME_TYPES-System-View.md) | Provides a list of supported mime types. |
| [M_TIMEZONE_ALERTS](6-System-Views-Reference/6.02-Monitoring-Views/M_TIMEZONE_ALERTS-System-View.md) | Provides information about alerts relating to the status of SAP HANA internal timezone conversion. |
| [M_TOPOLOGY_TREE](6-System-Views-Reference/6.02-Monitoring-Views/M_TOPOLOGY_TREE-System-View.md) | Provides information about SAP HANA nameserver topology content. |
| [M_TRACE_CONFIGURATION](6-System-Views-Reference/6.02-Monitoring-Views/M_TRACE_CONFIGURATION-System-View.md) | Provides information about trace configuration statistics. |
| [M_TRACE_CONFIGURATION_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_TRACE_CONFIGURATION_RESET-System-View.md) | Provides information about trace configuration statistics since the last reset. |
| [M_TRACEFILE_CONTENTS](6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILE_CONTENTS-System-View.md) | Provides SAP HANA information from trace files. |
| [M_TRACEFILES](6-System-Views-Reference/6.02-Monitoring-Views/M_TRACEFILES-System-View.md) | Provides information about all trace files. |
| [M_TRANS_TOKENS](6-System-Views-Reference/6.02-Monitoring-Views/M_TRANS_TOKENS-System-View.md) | Provides information about all active transaction tokens. |
| [M_TRANSACTIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_TRANSACTIONS-System-View.md) | Provides information about all transactions created by users or the database. |
| [M_UNDO_CLEANUP_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_UNDO_CLEANUP_FILES-System-View.md) | Provides information about undo files and cleanup files. |
| [M_VERSION_MEMORY](6-System-Views-Reference/6.02-Monitoring-Views/M_VERSION_MEMORY-System-View.md) | Provides information about memory use of the row-store Multiversion Concurrency Control (MVCC) manager. |
| [M_VOLUME_FILES](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_FILES-System-View.md) | Provides information about volume files. |
| [M_VOLUME_IO_DETAILED_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_DETAILED_STATISTICS-System-View.md) | Provides detailed statistics about file access. |
| [M_VOLUME_IO_DETAILED_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_DETAILED_STATISTICS_RESET-System-View.md) | Provides detailed statistics about file access since the last reset. |
| [M_VOLUME_IO_PERFORMANCE_STATISTICS System View - Deprecated](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_PERFORMANCE_STATISTICS-System-View-Deprecated.md) | Deprecated. Use M_VOLUME_IO_TOTAL_STATISTICS instead. |
| [M_VOLUME_IO_PERFORMANCE_STATISTICS_RESET System View - Deprecated](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_PERFORMANCE_STATISTICS_RESET-System-View.md) | Deprecated. Use M_VOLUME_IO_TOTAL_STATISTICS instead. |
| [M_VOLUME_IO_RETRY_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_RETRY_STATISTICS-System-View.md) | Provides file access retry statistics. |
| [M_VOLUME_IO_RETRY_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_RETRY_STATISTICS_RESET-System-View.md) | Provides file access retry statistics since the last reset. |
| [M_VOLUME_IO_STATISTICS System View - Deprecated](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_STATISTICS-System-View-Deprecated.md) | Deprecated. Use M_VOLUME_IO_TOTAL_STATISTICS instead. |
| [M_VOLUME_IO_STATISTICS_RESET System View - Deprecated](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_STATISTICS_RESET-System-View-Deprecated.md) | Deprecated. Use M_VOLUME_IO_TOTAL_STATISTICS instead. |
| [M_VOLUME_IO_TOTAL_STATISTICS](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_TOTAL_STATISTICS-System-View.md) | Shows information about basic I/O operations on I/O subsystems (paths). |
| [M_VOLUME_IO_TOTAL_STATISTICS_RESET](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_IO_TOTAL_STATISTICS_RESET-System-View.md) | Provides file access statistics since the last reset. |
| [M_VOLUME_SIZES](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUME_SIZES-System-View.md) | Provides information about volume sizes used by SAP HANA servers. |
| [M_VOLUMES](6-System-Views-Reference/6.02-Monitoring-Views/M_VOLUMES-System-View.md) | Provides information about the volumes used by SAP HANA servers. |
| [M_WORKLOAD](6-System-Views-Reference/6.02-Monitoring-Views/M_WORKLOAD-System-View.md) | Provides information about the database workload collected every minute. |
| [M_WORKLOAD_CAPTURES](6-System-Views-Reference/6.02-Monitoring-Views/M_WORKLOAD_CAPTURES-System-View.md) | Provides information about workload captures. |
| [M_WORKLOAD_REPLAY_PREPROCESSES](6-System-Views-Reference/6.02-Monitoring-Views/M_WORKLOAD_REPLAY_PREPROCESSES-System-View.md) | Provides information about preprocesses for captured workloads. |
| [M_WORKLOAD_REPLAYS](6-System-Views-Reference/6.02-Monitoring-Views/M_WORKLOAD_REPLAYS-System-View.md) | Provides information about workload replays. |
| [M_XS_APPLICATION_ISSUES](6-System-Views-Reference/6.02-Monitoring-Views/M_XS_APPLICATION_ISSUES-System-View.md) | Lists issues related to applications in SAP HANA XS. |
| [M_XS_APPLICATIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_XS_APPLICATIONS-System-View.md) | Provides information about applications deployed and running in SAP HANA XS. |
| [M_XS_PUBLIC_URLS](6-System-Views-Reference/6.02-Monitoring-Views/M_XS_PUBLIC_URLS-System-View.md) | Provides a list of URLs under which this database can be reached. |
| [M_XS_SESSIONS](6-System-Views-Reference/6.02-Monitoring-Views/M_XS_SESSIONS-System-View.md) | Provides information about sessions running in SAP HANA XS. |
| [OBJECT_DEPENDENCIES](6-System-Views-Reference/6.01-System-Views/OBJECT_DEPENDENCIES-System-View.md) | Provides information about dependencies between objects, such as which views refer to a specific table. |
| [OBJECT_PRIVILEGES](6-System-Views-Reference/6.01-System-Views/OBJECT_PRIVILEGES-System-View.md) | Provides information about the types of objects and privileges that can be granted to those types of objects. |
| [OBJECTS](6-System-Views-Reference/6.01-System-Views/OBJECTS-System-View.md) | Provides information about available objects. |
| [OWNERSHIP](6-System-Views-Reference/6.01-System-Views/OWNERSHIP-System-View.md) | Provides owner information for the objects available to the user who is querying the view. |
| [PARTITIONED_TABLES](6-System-Views-Reference/6.01-System-Views/PARTITIONED_TABLES-System-View.md) | Provides general partitioning information for all partitions of a table. |
| [PERSISTENCE_HISTORY](6-System-Views-Reference/6.01-System-Views/PERSISTENCE_HISTORY-System-View.md) | Records the database version history. |
| [PINNED_SQL_PLANS](6-System-Views-Reference/6.01-System-Views/PINNED_SQL_PLANS-System-View.md) | Provides information on currently pinned SQL plans and corresponding hints. |
| [PRIVILEGES](6-System-Views-Reference/6.01-System-Views/PRIVILEGES-System-View.md) | Provides information about available privileges. |
| [PROCEDURE_OBJECTS](6-System-Views-Reference/6.01-System-Views/PROCEDURE_OBJECTS-System-View.md) | Contains the results of the system procedure GET_PROCEDURE_OBJECTS. |
| [PROCEDURE_PARAMETER_COLUMNS](6-System-Views-Reference/6.01-System-Views/PROCEDURE_PARAMETER_COLUMNS-System-View.md) | Lists available columns of table parameters of stored procedures. |
| [PROCEDURE_PARAMETERS](6-System-Views-Reference/6.01-System-Views/PROCEDURE_PARAMETERS-System-View.md) | Provides information about the stored procedure parameters. |
| [PROCEDURE_ROUTES](6-System-Views-Reference/6.01-System-Views/PROCEDURE_ROUTES-System-View.md) | Provides information about the procedure being routed. This view is for internal use only. |
| [PROCEDURES](6-System-Views-Reference/6.01-System-Views/PROCEDURES-System-View.md) | Provides information about available stored procedures. |
| [PROJECTION_VIEW_COLUMN_SOURCES](6-System-Views-Reference/6.01-System-Views/PROJECTION_VIEW_COLUMN_SOURCES-System-View.md) | Provides information about available projection view columns. |
| [PSE_CERTIFICATES](6-System-Views-Reference/6.01-System-Views/PSE_CERTIFICATES-System-View.md) | Provides information about certificates used in PSEs. |
| [PSE_PURPOSE_OBJECTS](6-System-Views-Reference/6.01-System-Views/PSE_PURPOSE_OBJECTS-System-View.md) | Provides information about all PSEs and their assigned providers or hosts, referred to as purpose objects. |
| [PSES](6-System-Views-Reference/6.01-System-Views/PSES-System-View.md) | Provides information about personal security environments (PSE). |
| [QUERY_PLANS](6-System-Views-Reference/6.01-System-Views/QUERY_PLANS-System-View.md) | Plans how to handle query execution. |
| [REFERENTIAL_CONSTRAINTS](6-System-Views-Reference/6.01-System-Views/REFERENTIAL_CONSTRAINTS-System-View.md) | Provides information about referential constraints. |
| [REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS](6-System-Views-Reference/6.01-System-Views/REMOTE_SOURCE_OBJECT_COLUMN_CONSTRAINTS-System-View.md) | Provides remote source object column constraint information. |
| [REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS](6-System-Views-Reference/6.01-System-Views/REMOTE_SOURCE_OBJECT_COLUMN_DESCRIPTIONS-System-View.md) | Provides remote source object column description information. |
| [REMOTE_SOURCE_OBJECT_COLUMNS](6-System-Views-Reference/6.01-System-Views/REMOTE_SOURCE_OBJECT_COLUMNS-System-View.md) | Provides remote source object column information. |
| [REMOTE_SOURCE_OBJECT_DESCRIPTIONS](6-System-Views-Reference/6.01-System-Views/REMOTE_SOURCE_OBJECT_DESCRIPTIONS-System-View.md) | Provides remote source object description information. |
| [REMOTE_SOURCE_OBJECTS](6-System-Views-Reference/6.01-System-Views/REMOTE_SOURCE_OBJECTS-System-View.md) | Provides remote source object information. |
| [REMOTE_SOURCES](6-System-Views-Reference/6.01-System-Views/REMOTE_SOURCES-System-View.md) | Provides information about remote sources. |
| [REMOTE_SUBSCRIPTION_DATA_CONTAINERS](6-System-Views-Reference/6.01-System-Views/REMOTE_SUBSCRIPTION_DATA_CONTAINERS-System-View.md) | Provides information regarding remote subscription data. |
| [REMOTE_SUBSCRIPTION_EXCEPTIONS](6-System-Views-Reference/6.01-System-Views/REMOTE_SUBSCRIPTION_EXCEPTIONS-System-View.md) | Provides remote subscription exception information. |
| [REMOTE_SUBSCRIPTIONS](6-System-Views-Reference/6.01-System-Views/REMOTE_SUBSCRIPTIONS-System-View.md) | Lists all the remote subscriptions created for a remote source. |
| [REMOTE_USERS](6-System-Views-Reference/6.01-System-Views/REMOTE_USERS-System-View.md) | Provides information about user mappings for cross-database access. |
| [REORG_GENERATE_OVERVIEW](6-System-Views-Reference/6.01-System-Views/REORG_GENERATE_OVERVIEW-System-View.md) | Tracks automated and administrator calls to the REORG_GENERATE procedure. |
| [REORG_OVERVIEW](6-System-Views-Reference/6.01-System-Views/REORG_OVERVIEW-System-View.md) | Provides an overview of landscape redistributions. |
| [REORG_PLAN](6-System-Views-Reference/6.01-System-Views/REORG_PLAN-System-View.md) | Provides current plan information for landscape reorganization. |
| [REORG_PLAN_INFOS](6-System-Views-Reference/6.01-System-Views/REORG_PLAN_INFOS-System-View.md) | Provides additional information about the current landscape reorganization plan. |
| [REORG_STEPS](6-System-Views-Reference/6.01-System-Views/REORG_STEPS-System-View.md) | Contains the executed or to be executed table redistribution plan items. |
| [RESERVED_KEYWORDS](6-System-Views-Reference/6.01-System-Views/RESERVED_KEYWORDS-System-View.md) | Provides a list of reserved keywords that are not allowed to be used as a simple identifier. |
| [RESULT_CACHE](6-System-Views-Reference/6.01-System-Views/RESULT_CACHE-System-View.md) | Provides information about objects available to use the result cache. |
| [RESULT_CACHE_COLUMNS](6-System-Views-Reference/6.01-System-Views/RESULT_CACHE_COLUMNS-System-View.md) | Provides information about columns available to use the result cache. |
| [ROLE_LDAP_GROUPS](6-System-Views-Reference/6.01-System-Views/ROLE_LDAP_GROUPS-System-View.md) | Shows the mapping between SAP HANA roles and LDAP groups. |
| [ROLES](6-System-Views-Reference/6.01-System-Views/ROLES-System-View.md) | Shows available roles. |
| [SAML_PROVIDERS](6-System-Views-Reference/6.01-System-Views/SAML_PROVIDERS-System-View.md) | Shows available SAML providers. |
| [SAML_USER_MAPPINGS](6-System-Views-Reference/6.01-System-Views/SAML_USER_MAPPINGS-System-View.md) | Shows the SAML providers known for each user. |
| [SCHEMAS](6-System-Views-Reference/6.01-System-Views/SCHEMAS-System-View.md) | Shows available schemas. |
| [SEARCH_RULE_SET_CONDITIONS](6-System-Views-Reference/6.01-System-Views/SEARCH_RULE_SET_CONDITIONS-System-View.md) | Shows conditions to available search rule sets. |
| [SEARCH_RULE_SETS](6-System-Views-Reference/6.01-System-Views/SEARCH_RULE_SETS-System-View.md) | Shows information about available search rule sets. |
| [SEQUENCES](6-System-Views-Reference/6.01-System-Views/SEQUENCES-System-View.md) | Provides information about available sequences. |
| [SERIES_KEY_COLUMNS](6-System-Views-Reference/6.01-System-Views/SERIES_KEY_COLUMNS-System-View.md) | Provides information about series key columns for series tables. |
| [SERIES_TABLES](6-System-Views-Reference/6.01-System-Views/SERIES_TABLES-System-View.md) | Provides series definitions for tables. |
| [SESSION_COOKIES](6-System-Views-Reference/6.01-System-Views/SESSION_COOKIES-System-View.md) | Shows information about available session cookies. |
| [SQLSCRIPT_ANALYZER_RULES](6-System-Views-Reference/6.01-System-Views/SQLSCRIPT_ANALYZER_RULES-System-View.md) | Provides information regarding SQLScript Code Analyzer rules. |
| [SQLSCRIPT_VARIABLE_CACHE System view](6-System-Views-Reference/6.01-System-Views/SQLSCRIPT_VARIABLE_CACHE-System-view.md) | Provides information about procedures and functions that have variable caches defined. |
| [ST_GEOMETRY_COLUMNS](6-System-Views-Reference/6.01-System-Views/ST_GEOMETRY_COLUMNS-System-View.md) | Provides information about spatial columns. |
| [ST_SPATIAL_REFERENCE_SYSTEMS](6-System-Views-Reference/6.01-System-Views/ST_SPATIAL_REFERENCE_SYSTEMS-System-View.md) | Provides information about spatial reference systems. |
| [ST_UNITS_OF_MEASURE](6-System-Views-Reference/6.01-System-Views/ST_UNITS_OF_MEASURE-System-View.md) | Provides information about spatial units of measure. |
| [STATEMENT_HINTS](6-System-Views-Reference/6.01-System-Views/STATEMENT_HINTS-System-View.md) | Provides information about statement hints, including when they were last enabled and/or disabled and by whom. |
| [STRUCTURED_PRIVILEGES](6-System-Views-Reference/6.01-System-Views/STRUCTURED_PRIVILEGES-System-View.md) | Provides information about available structured (analytic) privileges. |
| [SYNONYMS](6-System-Views-Reference/6.01-System-Views/SYNONYMS-System-View.md) | Lists available synonyms. |
| [TABLE_COLUMNS](6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS-System-View.md) | Provides information about available table columns. |
| [TABLE_COLUMNS_ODBC](6-System-Views-Reference/6.01-System-Views/TABLE_COLUMNS_ODBC-System-View.md) | Provides information about available table columns. |
| [TABLE_GROUPS](6-System-Views-Reference/6.01-System-Views/TABLE_GROUPS-System-View.md) | Provides an overview of table group relationships. |
| [TABLE_PARTITIONS](6-System-Views-Reference/6.01-System-Views/TABLE_PARTITIONS-System-View.md) | Partitionspecific information for partitioned tables. |
| [TABLE_PLACEMENT](6-System-Views-Reference/6.01-System-Views/TABLE_PLACEMENT-System-View.md) | Provides table placement information. |
| [TABLE_PLACEMENT_LOCATIONS](6-System-Views-Reference/6.01-System-Views/TABLE_PLACEMENT_LOCATIONS-System-View.md) | Provides table placement location information. |
| [TABLE_REPLICAS](6-System-Views-Reference/6.01-System-Views/TABLE_REPLICAS-System-View.md) | Provides information about replicated tables and their replicas. |
| [TABLES](6-System-Views-Reference/6.01-System-Views/TABLES-System-View.md) | Provides information about tables in the database. |
| [TASK_PARAMETERS](6-System-Views-Reference/6.01-System-Views/TASK_PARAMETERS-System-View.md) | Provides task parameter information. |
| [TASKS](6-System-Views-Reference/6.01-System-Views/TASKS-System-View.md) | Provides information regarding table tasks. |
| [TEMPORAL_TABLES](6-System-Views-Reference/6.01-System-Views/TEMPORAL_TABLES-System-View.md) | Provides information about system-versioned tables, history tables, and application-time period tables. |
| [TEXT_CONFIGURATIONS](6-System-Views-Reference/6.01-System-Views/TEXT_CONFIGURATIONS-System-View.md) | Provides information about configurations and other resources for customizing text analysis and text mining. |
| [TIMEZONES](6-System-Views-Reference/6.01-System-Views/TIMEZONES-System-View.md) | Provides information about the timezones which are available together with their originating data set. |
| [TRANSACTION_HISTORY](6-System-Views-Reference/6.01-System-Views/TRANSACTION_HISTORY-System-View.md) | Provides information about committed transactions and their users. |
| [TRIGGER_ORDERS](6-System-Views-Reference/6.01-System-Views/TRIGGER_ORDERS-System-View.md) | Provides information about trigger order for triggers in the database. |
| [TRIGGERS](6-System-Views-Reference/6.01-System-Views/TRIGGERS-System-View.md) | Provides information about triggers that are defined for tables. |
| [USER_PARAMETERS](6-System-Views-Reference/6.01-System-Views/USER_PARAMETERS-System-View.md) | Lists all parameters and their values, which have been assigned to users in the system (using CREATE USER ... SET PARAMETER or ALTER USER ... SET PARAMETER). |
| [USERGROUP_PARAMETERS](6-System-Views-Reference/6.01-System-Views/USERGROUP_PARAMETERS-System-View.md) | Provides the list of parameter sets defined for usergroups. |
| [USERGROUPS](6-System-Views-Reference/6.01-System-Views/USERGROUPS-System-View.md) | Provides details on all user groups. |
| [USERS](6-System-Views-Reference/6.01-System-Views/USERS-System-View.md) | Lists all users. |
| [VIEW_COLUMNS](6-System-Views-Reference/6.01-System-Views/VIEW_COLUMNS-System-View.md) | Lists available view columns. |
| [VIEW_EXPRESSION_MACROS](6-System-Views-Reference/6.01-System-Views/VIEW_EXPRESSION_MACROS-System-View.md) | Describes the expression macros defined for views. |
| [VIEW_PARAMETERS](6-System-Views-Reference/6.01-System-Views/VIEW_PARAMETERS-System-View.md) | Provides information about view parameters. |
| [VIEWS](6-System-Views-Reference/6.01-System-Views/VIEWS-System-View.md) | Lists available views. |
| [VIRTUAL_COLUMN_PROPERTIES](6-System-Views-Reference/6.01-System-Views/VIRTUAL_COLUMN_PROPERTIES-System-View.md) | Provides the properties set on virtual table columns. |
| [VIRTUAL_COLUMNS](6-System-Views-Reference/6.01-System-Views/VIRTUAL_COLUMNS-System-View.md) | Provides information about virtual columns. |
| [VIRTUAL_FUNCTION_PACKAGES](6-System-Views-Reference/6.01-System-Views/VIRTUAL_FUNCTION_PACKAGES-System-View.md) | Provides information about virtual function packages. |
| [VIRTUAL_FUNCTIONS](6-System-Views-Reference/6.01-System-Views/VIRTUAL_FUNCTIONS-System-View.md) | Provides information about virtual functions. |
| [VIRTUAL_PACKAGES](6-System-Views-Reference/6.01-System-Views/VIRTUAL_PACKAGES-System-View.md) | Provides the list of virtual packages. |
| [VIRTUAL_PROCEDURES](6-System-Views-Reference/6.01-System-Views/VIRTUAL_PROCEDURES-System-View.md) | Provides the list of virtual procedures. |
| [VIRTUAL_TABLE_PARAMETERS](6-System-Views-Reference/6.01-System-Views/VIRTUAL_TABLE_PARAMETERS-System-View.md) | Provides a list of parameters of the virtual tables that refer to column views in a remote SAP HANA database. |
| [VIRTUAL_TABLE_PROPERTIES](6-System-Views-Reference/6.01-System-Views/VIRTUAL_TABLE_PROPERTIES-System-View.md) | Provides the properties set on virtual tables. |
| [VIRTUAL_TABLES](6-System-Views-Reference/6.01-System-Views/VIRTUAL_TABLES-System-View.md) | Provides information about virtual tables. |
| [WORKLOAD_CLASSES](6-System-Views-Reference/6.01-System-Views/WORKLOAD_CLASSES-System-View.md) | Provides information about available workload classes. |
| [WORKLOAD_MAPPINGS](6-System-Views-Reference/6.01-System-Views/WORKLOAD_MAPPINGS-System-View.md) | Provides information about available workload mappings. |
| [X509_PROVIDER_RULES](6-System-Views-Reference/6.01-System-Views/X509_PROVIDER_RULES-System-View.md) | Lists all of the matching rules for X.509 providers. |
| [X509_PROVIDERS](6-System-Views-Reference/6.01-System-Views/X509_PROVIDERS-System-View.md) | Lists all of the X.509 providers configured in the SAP HANA database. |
| [X509_USER_MAPPINGS](6-System-Views-Reference/6.01-System-Views/X509_USER_MAPPINGS-System-View.md) | Shows the X.509 certificates that are known for each user. |
| [XSA_AUDIT_LOG](6-System-Views-Reference/6.01-System-Views/XSA_AUDIT_LOG-System-View.md) | Provides information about XSA audit records. Database users with the AUDIT ADMIN, AUDIT OPERATOR, or AUDIT READ system privilege can view information in this system view. For all other database users, this view is… |
