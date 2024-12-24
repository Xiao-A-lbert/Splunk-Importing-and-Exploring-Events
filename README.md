# Splunk Importing and Exploring Events

<h2>Description</h2>
In this SIEM task, I install and deployed a splunk instance. uploaded multiple indexes, and performed basic SPL (Search Programming Language) to filter within the access.log file.  


<h2>Languages and Utilities Used</h2>

- <b>linux CLI</b>

<h2>Environments Used </h2>

- <b>Splunk</b>
- <b>Unbuntu</b> 

<br />
<br />
Starting my splunk instance from the /opt/splunk directory. 

![1) starting splunk instance](https://github.com/user-attachments/assets/485485ec-e7f3-43ef-a2db-1ffc60f04ce8)

<br />
<br />
Uploading a sample pcap of 12 events into sample_index. 

![2) uploading log source and send to indexer](https://github.com/user-attachments/assets/72dca489-4be1-46b0-a9b1-6eca6b7f7ebf)

<br />
<br />  
In new search, i use "index="sample_index" to view the logs. 

![3) searching sample_index](https://github.com/user-attachments/assets/501f765c-2dce-4ee8-ac89-ca21a078328c)

<br />
<br />
Uploading access.log http pcap into http_sample index. 

![4) uploading more complexe log files](https://github.com/user-attachments/assets/bf80df8c-6977-49d0-ba03-1271ead248d9)

<br />
<br />
Using "index=http_sample" to query the index.

![5) index http_sample](https://github.com/user-attachments/assets/c3df536a-50c2-45a3-8da9-e81a9f94142e)

<br />
<br />
Looking in the patterns tab, it shows 2 patterns for GET/POST request with user-agent hydra. 

![6) patterns already show get and post request](https://github.com/user-attachments/assets/2249aed2-68ad-4b29-ba25-b02aef24a042)

<br />
<br />
Filtering for filetypes to not include "login.php" narrows down the logs from 3000+ to 160 events. 

![7) filtering for not login php shows 160 results](https://github.com/user-attachments/assets/d4939433-d123-478e-b203-33b3c4c2e42a)

<br />
<br />  
Filtering for a status code greater than 200 narrows the logs down to 25 events. 

![8) http status  200](https://github.com/user-attachments/assets/802038ee-4337-4d2b-96fe-3ef1095fcb1c)

<br />
<br />
Filtering in Splunk with AND, NOT and OR operators within parenthesis. 

![9) using boolean operators and order of operators](https://github.com/user-attachments/assets/573716f7-7f26-4b15-97e1-9d5f466fb0a6)

<br />
<br />
Filtering the clientip to with wildcards. 

![10) using wildcards](https://github.com/user-attachments/assets/a65a847d-416f-4dc8-9827-14da9f78583f)

<br />
<br />
Filtering the http_sample with earliest and latest absolute timestamps. 

![11) using absolute time to filter](https://github.com/user-attachments/assets/6bfe122f-7c04-4327-9fba-2b0d34811771)

<br />
<br />
