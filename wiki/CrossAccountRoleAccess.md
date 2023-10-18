## About the Cross Account Role Access
For better understanding this process, please read about the cross account role access: <br>
https://aws.amazon.com/blogs/apn/securely-accessing-customer-aws-accounts-with-cross-account-iam-roles/<br>
https://docs.aws.amazon.com/IAM/latest/UserGuide/access_policies-cross-account-resource-access.html<br>
https://docs.aws.amazon.com/IAM/latest/UserGuide/tutorial_cross-account-with-roles.html

## Create Cross-Account Role to grant ADT Access to your S3 Bucket
1. Download the [CloudFormation Template](https://github.com/bosch-engineering/automotive_data_transformer_support/blob/main/cross_account_role.json) for the cross-account role.

2. Create a new CloudFormation Stack in AWS CloudFormation Service:

![image](https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/bf584a78-4ca9-466c-8de6-3814f9461396)


3. Fill the form for creating the stack:

![image](https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/899dbc98-df46-44be-9e31-62619063c531)

* You can find the external ID and the ADT account ID (MasterAccountName) in the onboarding email.

4. Build the stack.
