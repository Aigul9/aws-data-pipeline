### Variables

| Name             | Value                                                                                           |
|------------------|-------------------------------------------------------------------------------------------------|
| Bronze Bucket Name | yt-data-pipeline-bronze-us-east-1-sai                                                           |
| Silver Bucket Name | yt-data-pipeline-silver-us-east-1-sai                                                           |
| Gold Bucket Name | yt-data-pipeline-gold-us-east-1-sai                                                             |
| Scripts Bucket Name         | yt-data-pipeline-scripts-us-east-1-sai                                                          |
|SNS ARN | arn:aws:sns:us-east-1:282254623350:yt-data-pipeline-alerts:30ec1837-7ab8-4d74-beb8-8bf69acf13ec |
| Glue Bronze | yt_data_pipeline_bronze                                                                         |
| Glue Silver | yt_data_pipeline_silver                                                                         |
| Glue Gold | yt_data_pipeline_gold                                                                           |


### Params for bronze-to-silver glue job

--bronze_database yt_data_pipeline_bronze
--bronze_table raw_stats
--silver_bucket yt-data-pipeline-silver-us-east-1-sai
--silver_database yt_data_pipeline_silver
--silver_table clean_stats

### Params for silver-to-gold glue job
--silver_database yt_data_pipeline_silver
--gold_bucket yt-data-pipeline-gold-us-east-1-sai
--gold_database yt_data_pipeline_gold

### Useful Commands

```bash
aws help
aws configure

cat ~/.aws/credentials
cat ~/.aws/config

aws s3 ls
aws glue list-jobs --region us-east-1
aws lambda list-functions
```
