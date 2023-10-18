❓ Does ID Token expire?<br>
An ID token is valid for 24 hours. You will get "Unauthorized" error if it goes invalid. You can request the new one based on your use-case very easily.

❓ How does the output look like?<br>
Based on your parsing options, the output formats could be csv, json or parquet. For each signal we will generate one output file, to keep the raw resolution of the signal. If you have other wishes, please let us know.

❓ How to grant multiple buckets to the ADT?<br>
Edit the Cross Account Role policy in your IAM.
https://github.com/TimBo2602/automotive_data_transformer_support/tree/Tim_Proposals/wiki
❓ Why do I get 502 Gateway timeout if I try to export all signals?<br>
This is an issue will be addressed in the next minor release. The signal will be exported successfully, despite it.

❓ What happened if your service is down?<br>
We have deployed our service with multi-region failover mechanism. The secondary region will be used automatically if the primary region is down. You will get an email to setup your user password for the new region. Just follow the email.

❓ What to do if I get the Error 407 (Error: tunneling socket could not be established, statusCode=407)?<br>
Check your proxy settings. Maybe you are using ADT behind a corporate proxy. 

❓ I still get "Internal Server Error" ☹️ <br>
Please double check attributes in your request. If everything looks correct, contact our support team by sending an Email to us automotive-data-transformer@bosch.com.
