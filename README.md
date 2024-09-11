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


  
