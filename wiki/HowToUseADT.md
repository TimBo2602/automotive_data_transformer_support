# Quick Start

* [with cURL](https://github.com/bosch-engineering/automotive_data_transformer_support/wiki/How-to-use-ADT#with-curl)
* [with Postman](https://github.com/bosch-engineering/automotive_data_transformer_support/wiki/How-to-use-ADT#with-postman)


## With cURL

### Prepare
#### Get the ID Token at first
Please refer to the documentation, [how to get the ID Token](https://github.com/bosch-engineering/automotive_data_transformer_support/wiki/ADT-User-Account#generate-access-token-and-id-token)

### Get Channel List of a MF4 file
Download the request data template [curl_channel_list.json](https://github.com/bosch-engineering/automotive_data_transformer_support/blob/main/curl_channel_list.json).
```sh
curl -X POST --data @curl_channel_list.json \
-H "Content-Type: application/json" \
-H"Authorization: Bearer <IDToken>" \
https://api.automotive-data-transformer.com/v1/
```
You will get the signal list of the MF4 file. Which could be used for the export quick start tutorial.

### Export One Signal
Download the request data template [curl_export_one_signal.json](https://github.com/bosch-engineering/automotive_data_transformer_support/blob/main/curl_export_one_signal.json).

```sh
curl -X POST --data @curl_export_one_signal.json \
-H "Content-Type: application/json" \
-H"Authorization: Bearer <IDToken>" \
https://api.automotive-data-transformer.com/v1/
```

You will find the exported parquet file of the chosen signal in the output folder.


## With Postman
Download the Postman [Quick Start Collection](https://github.com/bosch-engineering/automotive_data_transformer_support/blob/main/adt_quick_start.postman_collection.json).

### Prepare
#### Get the ID Token at first
<!--
<img width="623" alt="image" src="https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/9d035c13-1235-4470-a4a9-fff4875ef793">
-->
<img width="600" alt="image" src="https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/bf6ff206-e4fe-4d34-820c-c8144d407c22">

You will find the ID Token in the `AuthenticationResult`.

#### Setup the ID Token in Postman Collection
<!--
![image](https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/8f265865-8f9d-4048-9149-7d0a26bba2ea)
-->
1. Click the collection name
2. Click `Variables` tab.
3. Input the ID Token.

<img width="600" alt="image" src="https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/3efddec4-bafe-4e3b-92eb-6188231da942">


### Get Channel List of a MF4 file
Open the request "Quick Start Get Channels". Fill the needed fields. The input bucket must be the bucket that the cross account role has the access to. And then click "Send".

<!--
<img width="700" alt="image" src="https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/c8b1c9b0-f186-442c-a9b0-b014b6252ec4">
-->

<img width="600" alt="image" src="https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/f6df3d0d-3c07-4853-b55e-9b0a87bf2e0f">


You will get the signal list of the MF4 file. Which could be used for the export quick start tutorial.


### Export one Signal
Open the request "Quick Start Export Signal". Fill the needed fields. The input and output bucket must be the buckets that the cross account role has the access to. And then click "Send".

<!--
<img width="697" alt="image" src="https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/a3fe179b-02f9-4528-a6d8-fbf73dd016da">
-->

<img width="600" alt="image" src="https://github.com/bosch-engineering/automotive_data_transformer_support/assets/54136241/2fde3329-f153-4bf7-91dc-7c811267b5f6">


You will find the exported parquet file of the chosen signal in the output folder.

## Want to know more about how to use ADT?
### Checkout our Postman Collection
https://github.com/bosch-engineering/automotive_data_transformer_support/blob/main/adt_v1.postman_collection.json

### OpenAPI Doc
https://github.com/bosch-engineering/automotive_data_transformer_support/blob/main/adt_openapi_v1.json
