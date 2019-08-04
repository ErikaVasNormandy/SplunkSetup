# SplunkSetup

Links:
> https://docs.splunk.com/Documentation/Splunk/7.3.0/Installation/DeployandrunSplunkEnterpriseinsideDockercontainers
> https://docs.splunk.com/Documentation/Splunk/7.3.1/SearchTutorial/Systemrequirements
> https://docs.splunk.com/Documentation/Splunk/7.3.0/Admin/Installalicense
> https://linoxide.com/linux-how-to/install-splunk-ubuntu/
> https://www.splunk.com/pdfs/technical-briefs/deploying-splunk-enterprise-on-amazon-web-services-technical-brief.pdf
> https://aws-quickstart.s3.amazonaws.com/quickstart-splunk-enterprise/doc/splunk-enterprise-on-the-aws-cloud.pdf


A list of notes on how to setup Splunk-Docker with a community license

##### TLDR Steps
> 0. Request developer license
> 1. Spin up virtual host with right hardware and network requirements
> --> Make sure you apply the networking rules correctly to this, Splunk runs on port 8000, 8089, and 9997
> 2. Install Docker on Ubuntu
> 3. Install Splunk image

# 1. Spin Up Virtual Host



