## Your ADT User Account
You will receive an onboarding email. You will find the following information within this email, which are needed to use ADT:

* Your email address, which is your account username.
* Temp password. Please change it after receiving your first access token.
* ADT app client ID, to request the Token for accessing the API
* External ID, which is used for the cross account role accessing. More about the [Cross Account Role Access](https://aws.amazon.com/blogs/apn/securely-accessing-customer-aws-accounts-with-cross-account-iam-roles/). 

## Generate Access Token and ID Token:
You will need an Access Token in order to change your password. You will need an ID Token for authenticating you requests in ADT.

Create file [auth.json](https://github.com/bosch-engineering/automotive_data_transformer_support/blob/main/auth.json) with the following content:
```
{"AuthParameters" : {"USERNAME" : "<your-email>", "PASSWORD" : "<password>"}, "AuthFlow" : "USER_PASSWORD_AUTH", "ClientId" : "<client-id>"}
```

Run the following command in the location for the file:
```sh
curl -X POST --data @auth.json \
-H 'X-Amz-Target: AWSCognitoIdentityProviderService.InitiateAuth' \
-H 'Content-Type: application/x-amz-json-1.1' \
https://cognito-idp.eu-central-1.amazonaws.com/
```

As a result you get the following output:
```json
{
  "AuthenticationResult": {
    "AccessToken": "YourAccesTokeneyJraWQiOiJsT2NEb0V6ZWpOdThlZ1wva1NUNXZSWUNBSG5lO",
    "ExpiresIn": 86400,
    "IdToken": "YourIdTokeneyJraWQiOiJqRkh5b05MeWpxakVxWWJUUnlicStVYkF",
    "RefreshToken": "YourRefreshTokeneyJjdHkiOiJKV1QiLCJlbmMiOiJ",
    "TokenType": "Bearer"
  },
  "ChallengeParameters": {}
}
```

## Change your password
Create a file named [change_password.json](https://github.com/bosch-engineering/automotive_data_transformer_support/blob/main/change_password.json) with the following content:
```
{ "AccessToken": "string", "PreviousPassword": "string", "ProposedPassword": "string" }
```

Run the following command in the location of the newly created file:
```sh
curl -X POST --data @change_password.json \
-H 'X-Amz-Target: AWSCognitoIdentityProviderService.ChangePassword' \
-H 'Content-Type: application/x-amz-json-1.1' \
https://cognito-idp.eu-central-1.amazonaws.com/
```
After the password is changed you need to generate a new ID Token again as the old one is invalid.
