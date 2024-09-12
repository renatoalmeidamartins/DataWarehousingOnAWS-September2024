 DataWarehousing on AWS course links

Materials and learning content
- Lab environment --> https://us-east-1.student.classrooms.aws.training/class/3BytfMhcadY3CQjJwUhsLP
- AWS Learning repository Learning  -> https://skillbuilder.aws/


Day 1
- Sagemaker Serverless --> https://aws.amazon.com/about-aws/whats-new/2022/04/amazon-sagemaker-serverless-inference/
- OpenSearch Serverless --> https://aws.amazon.com/about-aws/whats-new/2023/01/amazon-opensearch-serverless-available/
- Well architected framework - Data analytics lens --> https://docs.aws.amazon.com/wellarchitected/latest/analytics-lens/well-architected-design-principles.html
- Mapping between PostgreSQL and Redshift --> https://docs.aws.amazon.com/redshift/latest/dg/c_redshift-and-postgres-sql.html
- Redshift provisioned, nodes, slices --> https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-clusters.html
- Functions that run only on the leader node --> https://docs.aws.amazon.com/redshift/latest/dg/c_sql-functions-leader-node.html
- Kimball's book --> https://www.amazon.com/Data-Warehouse-Toolkit-Definitive-Dimensional/dp/1118530802
- Supported data types --> https://docs.aws.amazon.com/redshift/latest/dg/c_Supported_data_types.html
- Data distribution styles --> https://docs.aws.amazon.com/redshift/latest/dg/c_choosing_dist_sort.html
- Spatial data --> https://docs.aws.amazon.com/redshift/latest/dg/geospatial-overview.html
- Primary key and foreign key contraints --> https://docs.aws.amazon.com/redshift/latest/dg/c_best-practices-defining-constraints.html
- Interleaved sorting --> https://aws.amazon.com/blogs/aws/quickly-filter-data-in-amazon-redshift-using-interleaved-sorting/
- Optimizing star schemas for interleaved sorting --> https://aws.amazon.com/blogs/big-data/optimizing-for-star-schemas-and-interleaved-sorting-on-amazon-redshift/
- Analyze compression --> https://docs.aws.amazon.com/redshift/latest/dg/r_ANALYZE_COMPRESSION.html
- Available compression encodings --> https://docs.aws.amazon.com/redshift/latest/dg/c_Compression_encodings.html
- Let COPY choose the compression --> https://docs.aws.amazon.com/redshift/latest/dg/c_best-practices-use-auto-compression.html
- Grant command in detail --> https://docs.aws.amazon.com/redshift/latest/dg/r_GRANT.html
   - attention to the default CREATE and USAGE permissions on the PUBLIC schema
   - nesting of roles is achieved by GRANTing a ROLE to another ROLE
   - with GRANT OPTION (allows granting the same permissions to another user/group/role)
   - with ADMIN OPTION, with with roles, provides the admin options for the granted roles
- System defined roles --> https://docs.aws.amazon.com/redshift/latest/dg/r_roles-default.html
- ASSUMEROLE permission (not to confuse with the ROLE inside Redshift) --> https://docs.aws.amazon.com/redshift/latest/dg/r_GRANT-usage-notes.html#r_GRANT-usage-notes-assumerole
   - ROLE in Redshift relates to Redshift-scoped objects
   - ASSUMEROLE relates to IAM roles, granting permissions to services/features outside of Redshift (think an S3 bucket, a Sagemaker model)
 - Database migration walkthroughs --> https://docs.aws.amazon.com/dms/latest/sbs/dms-sbs-welcome.html
 - UNLOAD command (dump query output to S3) --> https://docs.aws.amazon.com/redshift/latest/dg/r_UNLOAD.html
 - Error during COPY? Check the SYS_LOAD_ERROR_DETAIL table --> https://docs.aws.amazon.com/redshift/latest/dg/SYS_LOAD_ERROR_DETAIL.html
 - Loading encrypted data (either client or server-side encrypted) --> https://docs.aws.amazon.com/redshift/latest/dg/c_loading-encrypted-files.html
 - Auto copy (single command incremental ETL from S3) --> https://docs.aws.amazon.com/redshift/latest/dg/loading-data-copy-job.html
 - Some data lake "architectures" regarding the level of aggregation:
   - Hitchiker's guide to the data lake --> https://azure.github.io/Storage/docs/analytics/hitchhikers-guide-to-the-datalake/
   - Medallion architecture --> https://www.databricks.com/glossary/medallion-architecture
  - MERGE (does UPSERTs) --> https://docs.aws.amazon.com/redshift/latest/dg/r_MERGE.html

Day 2
- EMRFS (HDFS backed by S3) --> https://docs.aws.amazon.com/emr/latest/ReleaseGuide/emr-fs.html
- Good practices for loading data (file sizes, using copy, doing bulk or multi-row inserts, ...) --> https://docs.aws.amazon.com/redshift/latest/dg/c_loading-data-best-practices.html
- Zero-ETL integrations --> https://docs.aws.amazon.com/redshift/latest/mgmt/zero-etl-using.html
- Zero-ETL setup walkthrough --> https://aws.amazon.com/blogs/big-data/getting-started-guide-for-near-real-time-operational-analytics-using-amazon-aurora-zero-etl-integration-with-amazon-redshift/
- Kinesis Firehose now supports zero-buffer --> https://aws.amazon.com/about-aws/whats-new/2023/12/amazon-kinesis-data-firehose-zero-buffering/
- Kinesis Flink applications --> https://aws.amazon.com/blogs/big-data/get-started-with-flink-sql-apis-in-amazon-kinesis-data-analytics-studio/
- CREATE EXTERNAL SCHEMA (multiple sources available - Kinesis, MSK, Postgres, ...) --> https://docs.aws.amazon.com/redshift/latest/dg/r_CREATE_EXTERNAL_SCHEMA.html
- Step-by-step Redshift Spectrum configuration --> https://docs.aws.amazon.com/redshift/latest/dg/c-getting-started-using-spectrum.html#c-getting-started-using-spectrum-create-external-table
- Streaming ingestion into Redshift --> https://docs.aws.amazon.com/redshift/latest/dg/materialized-view-streaming-ingestion.html
- Materialized view concepts --> https://docs.aws.amazon.com/redshift/latest/dg/materialized-view-overview.html
- CREATE MATERIALIZED VIEW --> https://docs.aws.amazon.com/redshift/latest/dg/materialized-view-create-sql-command.html
- AutoMV --> https://docs.aws.amazon.com/redshift/latest/dg/materialized-view-auto-mv.html
- DMS with Redshift as a target --> https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Target.Redshift.html
- Fully managed Schema conversion on DMS --> https://aws.amazon.com/blogs/aws/new-a-fully-managed-schema-conversion-in-aws-database-migration-service/
- Schema conversion tool --> https://docs.aws.amazon.com/SchemaConversionTool/latest/userguide/CHAP_Welcome.html
- Using DMS for ongoing replicaton from RDS --> https://docs.aws.amazon.com/dms/latest/userguide/CHAP_Task.CDC.html
- COPY command copying from SSH --> https://docs.aws.amazon.com/redshift/latest/dg/copy-parameters-data-source-ssh.html
- EMR step-by-step pre-reqs to load data into Redshift --> https://docs.aws.amazon.com/redshift/latest/dg/loading-data-from-emr.html
- Connecting using Query Editor V2 --> https://docs.aws.amazon.com/redshift/latest/mgmt/query-editor-v2-connecting.html
- Scheduled queries --> https://docs.aws.amazon.com/redshift/latest/mgmt/query-editor-v2-schedule-query.html
- Shared queries --> https://docs.aws.amazon.com/redshift/latest/mgmt/query-editor-v2-query-share.html
- Querying the Glue catalog --> https://docs.aws.amazon.com/redshift/latest/mgmt/query-editor-v2-glue.html
- Custom crawlers in Glue (to support customer-specific file structures in S3)  --> https://docs.aws.amazon.com/glue/latest/dg/custom-classifier.html
- Auto-refreshing of materialized views --> https://docs.aws.amazon.com/redshift/latest/dg/materialized-view-refresh.html#materialized-view-auto-refresh
- Stored procedures --> https://docs.aws.amazon.com/redshift/latest/dg/stored-procedure-overview.html
- pgSQL commands supported for Stored Procedures on Redshift --> https://docs.aws.amazon.com/redshift/latest/dg/c_PLpgSQL-statements.html
- Aggregation extensions (Rollup, Cube, Grouping, ...) --> https://docs.aws.amazon.com/redshift/latest/dg/r_GROUP_BY_aggregation-extensions.html
- User-defined functions (UDF) --> https://docs.aws.amazon.com/redshift/latest/dg/user-defined-functions.html
- Repo with sample UDFs --> https://github.com/aws-samples/amazon-redshift-udfs/blob/master/README.md
- Multi-AZ for Redshift --> https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-multi-az.html
- Restore cluster from AWS Backup --> https://docs.aws.amazon.com/aws-backup/latest/devguide/redshift-restores.html
- Restoring cluster from CLI or Redshift console --> https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-snapshot-restore-cluster-from-snapshot.html
- Cluster relocation feature --> https://docs.aws.amazon.com/redshift/latest/mgmt/managing-cluster-recovery.html
- Snapshots --> https://docs.aws.amazon.com/redshift/latest/mgmt/working-with-snapshots.html
- VACUUM tables --> https://docs.aws.amazon.com/redshift/latest/dg/t_Reclaiming_storage_space202.html
- Analyze (updating statistics) --> https://docs.aws.amazon.com/en_us/redshift/latest/dg/r_ANALYZE.html
- EXPLAIN operators --> https://docs.aws.amazon.com/redshift/latest/dg/r_EXPLAIN.html
- DAta redistribution operators shown on EXPLAIN --> https://docs.aws.amazon.com/redshift/latest/dg/c_data_redistribution.html
- Query alerts --> https://docs.aws.amazon.com/redshift/latest/dg/c-reviewing-query-alerts.html
- AutoWLM paper --> https://assets.amazon.science/5a/9d/338478254f9a9dde672fa84da2b7/auto-wlm-machine-learning-enhanced-workload-management-in-amazon-redshif.pdf
- Concurrency scaling --> https://docs.aws.amazon.com/redshift/latest/dg/concurrency-scaling-queues.html
- Working with concurrency scaling --> https://docs.aws.amazon.com/redshift/latest/dg/concurrency-scaling.html
- Queue assignment rules --> https://docs.aws.amazon.com/redshift/latest/dg/cm-c-wlm-queue-assignment-rules.html
- Short Query Acceleration --> https://docs.aws.amazon.com/redshift/latest/dg/wlm-short-query-acceleration.html
- Query monitoring rules (deciding if a query going over a certain metric threshold, should be aborted, logged, hopped, ...) --> https://docs.aws.amazon.com/redshift/latest/dg/cm-c-wlm-query-monitoring-rules.html
- Redshift Advisor recommendations --> https://docs.aws.amazon.com/redshift/latest/dg/advisor-recommendations.html
- Cluster resize --> https://docs.aws.amazon.com/redshift/latest/mgmt/resizing-cluster.html
- Redshift metrics --> https://docs.aws.amazon.com/redshift/latest/mgmt/metrics-listing.html
- STL views for logging --> https://docs.aws.amazon.com/redshift/latest/dg/c_intro_STL_tables.html
- SYS views --> https://docs.aws.amazon.com/redshift/latest/dg/sys_view_migration.html
- Event notifications for provisioned clusters --> https://docs.aws.amazon.com/redshift/latest/mgmt/event-subscribe.html

Day 3
- Setting up an OIDC IdP --> https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_create_oidc.html#:~:text=You%20use%20an%20IAM%20OIDC%20identity%20provider%20when
- Temporary credentials --> https://docs.aws.amazon.com/redshift/latest/mgmt/generating-iam-credentials-steps.html
- Federated querying setup --> https://docs.aws.amazon.com/redshift/latest/dg/federated-overview.html
- Get session token (maximum session duration is 36 hours, defaulting to 12 hours) --> https://docs.aws.amazon.com/cli/latest/reference/sts/get-session-token.html
- Assume role (maximum role session duration is 12 hours) --> https://docs.aws.amazon.com/cli/latest/reference/sts/assume-role.html
- Row-Level security --> https://aws.amazon.com/blogs/big-data/achieve-fine-grained-data-security-with-row-level-access-control-in-amazon-redshift/
-  Dynamic data masking --> https://docs.aws.amazon.com/redshift/latest/dg/t_ddm.html
-  One example of using config to monitor and (optionally) remediate compliance --> https://docs.aws.amazon.com/config/latest/developerguide/redshift-require-tls-ssl.html
-  Amazon State Language (used in Step Functions) --> https://docs.aws.amazon.com/step-functions/latest/dg/concepts-amazon-states-language.html
-  State Functions Tasks --> https://docs.aws.amazon.com/step-functions/latest/dg/state-task.html



  
