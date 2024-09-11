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
