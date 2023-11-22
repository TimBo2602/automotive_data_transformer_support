## Public Cloud
The Automotive Data Transformer is tested for and runs completely on AWS infrastructure, therefore please make sure to also use AWS.

## AWS Services
The Automotive Data Transformer currently supports opening and saving files from S3 buckets. AWS databases are currently not supported.

## Access Permissions
To access the Automotive Data Transformer you need: 
a) the following information, which is provided to you by onboarding mail from <[automotive-data-transformer@bosch.com](mailto:automotive-data-transformer@bosch.com)>: 
1. user name and initial password, which needs to be changed directly
2. a customer ID, which is your AWS Marketplace account ID
3. a client ID, which is needed for authentication and creation of your access token
b) to give our Automotive Data Transformer access rights to your S3 storage, which can be revoked any time by you. For further information please check [here](https://github.com/bosch-engineering/automotive_data_transformer_support/wiki/Cross-Account-Role-Access)

## Programming Languages & SDKs
For further integration with your services we mainly use Python code and are happy to help. Please feel free to contact us under <[automotive-data-transformer@bosch.com](mailto:automotive-data-transformer@bosch.com)>
To get started quickly we provide a [postman collection](https://github.com/bosch-engineering/automotive_data_transformer_support/wiki/How-to-use-ADT). 

## Dependencies
Shall we add something here e.g. ASAMMDF?

## Data Types & Formats
a) Input Type:
MDF Generation: The ADT only supports MDF 4.x and we keep on updating it, if new updates are published. Please be aware that older MDF generations e.g. MDF 3.x might work, but we not actively support and test them.
MDF Provider: The ADT only supports MDF files from ETAS and Vector. We continuously work on extending support, but because all providers use the MDF standard slightly different, we cannot guarantee error-free functioning for all of them.
b) 
Output Type: The ADT supports export of 
1. metadata into JSON responses and files 
2. signal data into Parquet, CSV or JSON files

## Endpoint URL
You can access the production environment of ADT on: 

## Request & Response Limits
Max supported data size is
There is a limit of x requests per hour
If these are surpassed then ...

## Monitoring and Logging
You can monitor your API usage and performance by

## Error Handling
We support the following error codes and recommend:

## Support and Contact information
For technical questions please feel free to check out the supportive information [here](https://github.com/bosch-engineering/automotive_data_transformer_support/wiki/Questions) or create a new issue with your question and our support team will reply it asap.

For commercial questions or new feature ideas please feel free to contact us via <[automotive-data-transformer@bosch.com](mailto:automotive-data-transformer@bosch.com)>
