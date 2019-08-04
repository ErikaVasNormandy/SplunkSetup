# Splunk Setup

Splunk isn't *that* hard to setup, but there are a couple of small details to keep in mind

##### Links:
- https://docs.splunk.com/Documentation/Splunk/7.3.0/Installation/DeployandrunSplunkEnterpriseinsideDockercontainers
- https://docs.splunk.com/Documentation/Splunk/7.3.1/SearchTutorial/Systemrequirements
- https://docs.splunk.com/Documentation/Splunk/7.3.0/Admin/Installalicense
- https://linoxide.com/linux-how-to/install-splunk-ubuntu/
- https://www.splunk.com/pdfs/technical-briefs/deploying-splunk-enterprise-on-amazon-web-services-technical-brief.pdf
- https://aws-quickstart.s3.amazonaws.com/quickstart-splunk-enterprise/doc/splunk-enterprise-on-the-aws-cloud.pdf
--- 

A list of notes on how to setup Splunk-Docker with a community license

### TLDR Steps
> 0. Request developer license
> 1. Spin up virtual host with right hardware and network requirements
> --> Make sure you apply the networking rules correctly to this, Splunk runs on port 8000, 8089, and 9997
> 2. Install Docker on Ubuntu
> 3. Install Splunk image
--- 

### 0. Request Developer License
https://www.splunk.com/page/sign_up/developer_license?redirecturl=http://dev.splunk.com/page/developer_license_sign_up/
This can take "1-3 business days but I got mine in a week after sending an inquiry to devinfo@splunk.com
"A 10GB for non-customers that goes through an approval process"

### 1. Spin Up Virtual Host 
For me I used AWS Instance **c5.18xlarge**, 144 GIB memory. AWS has dedicated documentation for Splunk ( https://aws-quickstart.s3.amazonaws.com/quickstart-splunk-enterprise/doc/splunk-enterprise-on-the-aws-cloud.pdf )

| Instance Type       | Daily Indexing Volume       | Users  |
| ------------- |:-------------:| -----:|
| c4.2xlarge   | <100 | <8? |
| c4.4xlarge    | 100-200    |   8? |
| c4.8xlarge | 200-300+     |    16? |

This was the table for **indexers**, but you can use them as a guidelines for ideas on what hardware requirements
###### Networking Rules



