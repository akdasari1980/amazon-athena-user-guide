# Amazon Athena User Guide

-----
*****Copyright &copy; 2020 Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What is Amazon Athena?](what-is.md)
   + [When should I use Athena?](when-should-i-use-ate.md)
   + [Accessing Athena](accessing-ate.md)
   + [Understanding Tables, Databases, and the Data Catalog](understanding-tables-databases-and-the-data-catalog.md)
   + [AWS Service Integrations with Athena](athena-aws-service-integrations.md)
+ [Setting Up](setting-up.md)
+ [Getting Started](getting-started.md)
+ [Accessing Amazon Athena](accessing-Athena.md)
+ [Creating Tables and Databases](work-with-data.md)
   + [Tables and Databases Creation Process in Athena](creating-tables.md)
   + [Names for Tables, Databases, and Columns](tables-databases-columns-names.md)
   + [Reserved Keywords](reserved-words.md)
   + [Table Location in Amazon S3](tables-location-format.md)
   + [Partitioning Data](partitions.md)
   + [Columnar Storage Formats](columnar-storage.md)
   + [Converting to Columnar Formats](convert-to-columnar.md)
+ [Connecting to Data Sources](work-with-data-stores.md)
   + [Integration with AWS Glue](glue-athena.md)
      + [Using AWS Glue to Connect to Data Sources in Amazon S3](data-sources-glue.md)
      + [Best Practices When Using Athena with AWS Glue](glue-best-practices.md)
      + [Upgrading to the AWS Glue Data Catalog Step-by-Step](glue-upgrade.md)
      + [FAQ: Upgrading to the AWS Glue Data Catalog](glue-faq.md)
   + [Using Athena Data Connector for External Hive Metastore (Preview)](connect-to-data-source-hive.md)
   + [Using Amazon Athena Federated Query (Preview)](connect-to-a-data-source.md)
      + [Deploying a Connector and Connecting to a Data Source](connect-to-a-data-source-lambda.md)
      + [Using the AWS Serverless Application Repository to Deploy a Data Source Connector](connect-data-source-serverless-app-repo.md)
      + [Using Athena Data Source Connectors](athena-prebuilt-data-connectors.md)
         + [Athena AWS CMDB Connector](athena-prebuilt-data-connectors-cmdb.md)
         + [Amazon Athena CloudWatch Connector](athena-prebuilt-data-connectors-cwlogs.md)
         + [Amazon Athena CloudWatch Metrics Connector](athena-prebuilt-data-connectors-cwmetrics.md)
         + [Amazon Athena DocumentDB Connector](athena-prebuilt-data-connectors-docdb.md)
         + [Amazon Athena DynamoDB Connector](athena-prebuilt-data-connectors-dynamodb.md)
         + [Amazon Athena HBase Connector](athena-prebuilt-data-connectors-hbase.md)
         + [Amazon Athena Connector for JDBC-Compliant Data Sources](athena-prebuilt-data-connectors-jdbc.md)
         + [Amazon Athena Redis Connector](athena-prebuilt-data-connectors-redis.md)
         + [Amazon Athena TPC Benchmark DS (TPC-DS) Connector](athena-prebuilt-data-connectors-tpcds.md)
      + [Writing Federated Queries](writing-federated-queries.md)
      + [Writing a Data Source Connector Using the Athena Query Federation SDK](connect-data-source-federation-sdk.md)
      + [Managing Data Sources](data-sources-managing.md)
   + [Connecting to Amazon Athena with ODBC and JDBC Drivers](athena-bi-tools-jdbc-odbc.md)
      + [Using Athena with the JDBC Driver](connect-with-jdbc.md)
      + [Connecting to Amazon Athena with ODBC](connect-with-odbc.md)
+ [Running SQL Queries Using Amazon Athena](querying-athena-tables.md)
   + [Working with Query Results, Output Files, and Query History](querying.md)
   + [Working with Views](views.md)
   + [Creating a Table from Query Results (CTAS)](ctas.md)
      + [Considerations and Limitations for CTAS Queries](considerations-ctas.md)
      + [Running CTAS Queries in the Console](ctas-console.md)
      + [Bucketing vs Partitioning](bucketing-vs-partitioning.md)
      + [Examples of CTAS Queries](ctas-examples.md)
      + [Using CTAS and INSERT INTO for ETL and Data Analysis](ctas-insert-into-etl.md)
      + [Using CTAS and INSERT INTO to Create a Table with More Than 100 Partitions](ctas-insert-into.md)
   + [Handling Schema Updates](handling-schema-updates-chapter.md)
      + [Types of Updates](types-of-updates.md)
      + [Updates in Tables with Partitions](updates-and-partitions.md)
   + [Querying Arrays](querying-arrays.md)
      + [Creating Arrays](creating-arrays.md)
      + [Concatenating Arrays](concatenating-arrays.md)
      + [Converting Array Data Types](converting-array-data-types.md)
      + [Finding Lengths](finding-lengths.md)
      + [Accessing Array Elements](accessing-array-elements.md)
      + [Flattening Nested Arrays](flattening-arrays.md)
      + [Creating Arrays from Subqueries](creating-arrays-from-subqueries.md)
      + [Filtering Arrays](filtering-arrays.md)
      + [Sorting Arrays](sorting-arrays.md)
      + [Using Aggregation Functions with Arrays](arrays-and-aggregation.md)
      + [Converting Arrays to Strings](converting-arrays-to-strings.md)
      + [Using Arrays to Create Maps](maps.md)
      + [Querying Arrays with Complex Types and Nested Structures](rows-and-structs.md)
   + [Querying JSON](querying-JSON.md)
      + [Best Practices for Reading JSON Data](parsing-JSON.md)
      + [Extracting Data from JSON](extracting-data-from-JSON.md)
      + [Searching for Values in JSON Arrays](searching-for-values.md)
      + [Obtaining Length and Size of JSON Arrays](length-and-size.md)
   + [Querying Geospatial Data](querying-geospatial-data.md)
      + [What is a Geospatial Query?](geospatial-query-what-is.md)
      + [Input Data Formats and Geometry Data Types](geospatial-input-data-formats-supported-geometry-types.md)
      + [List of Supported Geospatial Functions](geospatial-functions-list.md)
      + [Examples: Geospatial Queries](geospatial-example-queries.md)
   + [Using Machine Learning (ML) with Amazon Athena (Preview)](querying-mlmodel.md)
   + [Querying with User Defined Functions (Preview)](querying-udf.md)
   + [Querying AWS Service Logs](querying-AWS-service-logs.md)
      + [Querying Application Load Balancer Logs](application-load-balancer-logs.md)
      + [Querying Classic Load Balancer Logs](elasticloadbalancer-classic-logs.md)
      + [Querying Amazon CloudFront Logs](cloudfront-logs.md)
      + [Querying AWS CloudTrail Logs](cloudtrail-logs.md)
      + [Querying Amazon EMR Logs](emr-logs.md)
      + [Querying AWS Global Accelerator Flow Logs](querying-global-accelerator-flow-logs.md)
      + [Querying Network Load Balancer Logs](networkloadbalancer-classic-logs.md)
      + [Querying Amazon VPC Flow Logs](vpc-flow-logs.md)
      + [Querying AWS WAF Logs](waf-logs.md)
   + [Querying AWS Glue Data Catalog](querying-glue-catalog.md)
+ [Amazon Athena Security](security.md)
   + [Data Protection in Athena](data-protection.md)
      + [Encryption at Rest](encryption.md)
      + [Encryption in Transit](encryption-in-transit.md)
      + [Key Management](key-management.md)
      + [Internetwork Traffic Privacy](internetwork-traffic-privacy.md)
   + [Identity and Access Management in Athena](identity-and-access-management-in-athena.md)
      + [Managed Policies for User Access](managed-policies.md)
         + [AmazonAthenaFullAccess Managed Policy](amazonathenafullaccess-managed-policy.md)
         + [AWSQuicksightAthenaAccess Managed Policy](awsquicksightathenaaccess-managed-policy.md)
      + [Access through JDBC and ODBC Connections](policy-actions.md)
      + [Access to Amazon S3](s3-permissions.md)
      + [Fine-Grained Access to Databases and Tables in the AWS Glue Data Catalog](fine-grained-access-to-glue-resources.md)
      + [Access to Encrypted Metadata in the AWS Glue Data Catalog](access-encrypted-data-glue-data-catalog.md)
      + [Cross-account Access](cross-account-permissions.md)
      + [Access to Workgroups and Tags](workgroups-access.md)
      + [Allow Access to an Athena Data Connector for External Hive Metastore (Preview)](hive-metastore-iam-access.md)
      + [Example IAM Permissions Policies to Allow Athena Federated Query (Preview)](federated-query-iam-access.md)
      + [Example IAM Permissions Policies to Allow Amazon Athena User Defined Functions (UDF)](udf-iam-access.md)
      + [Allowing Access for ML with Athena (Preview)](machine-learning-iam-access.md)
      + [Enabling Federated Access to the Athena API](access-federation-saml.md)
   + [Logging and Monitoring in Athena](incident-response.md)
   + [Compliance Validation for Amazon Athena](athena-compliance.md)
   + [Resilience in Athena](disaster-recovery-resiliency.md)
   + [Infrastructure Security in Athena](infrastructure-security.md)
      + [Connect to Amazon Athena Using an Interface VPC Endpoint](interface-vpc-endpoint.md)
   + [Configuration and Vulnerability Analysis in Athena](vulnerability-analysis-and-management.md)
   + [Using Athena to Query Data Registered With AWS Lake Formation](lake-formation-athena.md)
      + [How Athena Accesses Data Registered With Lake Formation](lf-athena-access.md)
      + [Considerations and Limitations When Using Athena to Query Data Registered With Lake Formation](lf-athena-limitations.md)
      + [Managing Lake Formation and Athena User Permissions](lf-athena-user-permissions.md)
      + [Applying Lake Formation Permissions to Existing Databases and Tables](lf-athena-removing-permissions.md)
+ [Using Workgroups to Control Query Access and Costs](manage-queries-control-costs-with-workgroups.md)
   + [Using Workgroups for Running Queries](workgroups.md)
      + [Benefits of Using Workgroups](workgroups-benefits.md)
      + [How Workgroups Work](user-created-workgroups.md)
      + [Setting up Workgroups](workgroups-procedure.md)
      + [IAM Policies for Accessing Workgroups](workgroups-iam-policy.md)
      + [Workgroup Example Policies](example-policies-workgroup.md)
      + [Workgroup Settings](workgroups-settings.md)
         + [Workgroup Settings Override Client-Side Settings](workgroups-settings-override.md)
      + [Managing Workgroups](workgroups-create-update-delete.md)
      + [Athena Workgroup APIs](workgroups-api-list.md)
      + [Troubleshooting Workgroups](workgroups-troubleshooting.md)
   + [Controlling Costs and Monitoring Queries with CloudWatch Metrics and Events](control-limits.md)
      + [Enabling CloudWatch Query Metrics](athena-cloudwatch-metrics-enable.md)
      + [Monitoring Athena Queries with CloudWatch Metrics](query-metrics-viewing.md)
      + [Monitoring Athena Queries with CloudWatch Events](athena-cloudwatch-events.md)
      + [Setting Data Usage Control Limits](workgroups-setting-control-limits-cloudwatch.md)
+ [Tagging Workgroups](tags.md)
   + [Working with Tags Using the Console](tags-console.md)
   + [Working with Tags Using the API Actions](tags-api.md)
   + [Tag-Based IAM Access Control Policies](tags-access-control.md)
+ [Monitoring Logs and Troubleshooting](monitor-logs-and-troubleshoot.md)
   + [Logging Amazon Athena API Calls with AWS CloudTrail](monitor-with-cloudtrail.md)
   + [Troubleshooting](troubleshooting.md)
+ [SerDe Reference](serde-reference.md)
   + [Using a SerDe](serde-about.md)
   + [Supported SerDes and Data Formats](supported-format.md)
      + [Avro SerDe](avro.md)
      + [RegexSerDe for Processing Apache Web Server Logs](apache.md)
      + [CloudTrail SerDe](cloudtrail.md)
      + [OpenCSVSerDe for Processing CSV](csv.md)
      + [Grok SerDe](grok.md)
      + [JSON SerDe Libraries](json.md)
      + [LazySimpleSerDe for CSV, TSV, and Custom-Delimited Files](lazy-simple-serde.md)
      + [ORC SerDe](orc.md)
      + [Parquet SerDe](parquet.md)
   + [Compression Formats](compression-formats.md)
+ [SQL Reference for Amazon Athena](ddl-sql-reference.md)
   + [Data Types Supported by Amazon Athena](data-types.md)
   + [DML Queries, Functions, and Operators](functions-operators-reference-section.md)
      + [SELECT](select.md)
      + [INSERT INTO](insert-into.md)
      + [Presto Functions in Amazon Athena](presto-functions.md)
   + [DDL Statements](language-reference.md)
      + [Unsupported DDL](unsupported-ddl.md)
      + [ALTER DATABASE SET DBPROPERTIES](alter-database-set-dbproperties.md)
      + [ALTER TABLE ADD PARTITION](alter-table-add-partition.md)
      + [ALTER TABLE DROP PARTITION](alter-table-drop-partition.md)
      + [ALTER TABLE RENAME PARTITION](alter-table-rename-partition.md)
      + [ALTER TABLE SET LOCATION](alter-table-set-location.md)
      + [ALTER TABLE SET TBLPROPERTIES](alter-table-set-tblproperties.md)
      + [CREATE DATABASE](create-database.md)
      + [CREATE TABLE](create-table.md)
      + [CREATE TABLE AS](create-table-as.md)
      + [CREATE VIEW](create-view.md)
      + [DESCRIBE TABLE](describe-table.md)
      + [DESCRIBE VIEW](describe-view.md)
      + [DROP DATABASE](drop-database.md)
      + [DROP TABLE](drop-table.md)
      + [DROP VIEW](drop-view.md)
      + [MSCK REPAIR TABLE](msck-repair-table.md)
      + [SHOW COLUMNS](show-columns.md)
      + [SHOW CREATE TABLE](show-create-table.md)
      + [SHOW CREATE VIEW](show-create-view.md)
      + [SHOW DATABASES](show-databases.md)
      + [SHOW PARTITIONS](show-partitions.md)
      + [SHOW TABLES](show-tables.md)
      + [SHOW TBLPROPERTIES](show-tblproperties.md)
      + [SHOW VIEWS](show-views.md)
   + [Considerations and Limitations for SQL Queries in Amazon Athena](other-notable-limitations.md)
+ [Code Samples, Service Quotas, and Previous JDBC Driver](reference.md)
   + [Code Samples](code-samples.md)
   + [Using Earlier Version JDBC Drivers](connect-with-previous-jdbc.md)
   + [Service Quotas](service-limits.md)
+ [Release Notes](release-notes.md)
   + [March 11, 2020](release-note-2020-03-11.md)
   + [March 6, 2020](release-note-2020-03-06.md)
   + [November 26, 2019](release-note-2019-11-26.md)
   + [November 12, 2019](release-note-2019-11-12.md)
   + [November 8, 2019](release-note-2019-11-08.md)
   + [October 8, 2019](release-note-2019-10-08.md)
   + [September 19, 2019](release-note-2019-09-19.md)
   + [September 12, 2019](release-note-2019-09-12.md)
   + [August 16, 2019](release-note-2019-08-16.md)
   + [August 9, 2019](release-note-2019-08-09.md)
   + [June 26, 2019](release-note-2019-06-26.md)
   + [May 24, 2019](release-note-2019-05-24.md)
   + [March 05, 2019](release-note-2019-03-05.md)
   + [February 22, 2019](release-note-2019-02-22.md)
   + [February 18, 2019](release-note-2019-02-18.md)
   + [November 20, 2018](release-note-2018-11-20.md)
   + [October 15, 2018](release-note-2018-10-15.md)
   + [October 10, 2018](release-note-2018-10-10.md)
   + [September 6, 2018](release-note-2018-09-06.md)
   + [August 23, 2018](release-note-2018-08-23.md)
   + [August 16, 2018](release-note-2018-08-16.md)
   + [August 7, 2018](release-note-2018-08-07.md)
   + [June 5, 2018](release-note-2018-06-05.md)
   + [May 17, 2018](release-note-2018-05-17.md)
   + [April 19, 2018](release-note-2018-04-19.md)
   + [April 6, 2018](release-note-2018-04-06.md)
   + [March 15, 2018](release-note-2018-03-15.md)
   + [February 2, 2018](release-note-2018-02-12.md)
   + [January 19, 2018](release-note-2018-01-19.md)
   + [November 13, 2017](release-note-2017-11-13.md)
   + [November 1, 2017](release-note-2017-11-01.md)
   + [October 19, 2017](release-note-2017-10-19.md)
   + [October 3, 2017](release-note-2017-10-03.md)
   + [September 25, 2017](release-note-2017-09-25.md)
   + [August 14, 2017](release-note-2017-08-14.md)
   + [August 4, 2017](release-note-2017-08-04.md)
   + [June 22, 2017](release-note-2017-06-22.md)
   + [June 8, 2017](release-note-2017-06-08.md)
   + [May 19, 2017](release-note-2017-05-19.md)
   + [April 4, 2017](release-note-2017-04-04.md)
   + [March 24, 2017](release-note-2017-03-24.md)
   + [February 20, 2017](release-note-2017-02-20.md)
+ [Document History](DocHistory.md)
+ [AWS Glossary](glossary.md)