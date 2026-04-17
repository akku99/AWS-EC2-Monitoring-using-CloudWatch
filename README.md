# AWS-EC2-Monitoring-using-CloudWatch

Steps:

Step 1: Create an IAM and Attach CloudWatch and SSM Full Access - EC2-CloudWatch-Role

Step 2: Create a parameter in Systems Manger with the name "/alarm/AWS-CWAgentLinConfig" and store the value.

Step 3: Create an EC2 Instance, Attach the role created in Step 1 and Add the commands in the Userdata

Commands that needs to be added in Userdata Section:

<picture>
 <source media="(prefers-color-scheme: dark)" srcset="YOUR-DARKMODE-IMAGE">
 <source media="(prefers-color-scheme: light)" srcset="YOUR-LIGHTMODE-IMAGE">
 <img alt="YOUR-ALT-TEXT" src="YOUR-DEFAULT-IMAGE">
</picture>


#!/bin/bash
wget https://s3.amazonaws.com/amazoncloudwatch-agent/linux/amd64/latest/AmazonCloudWatchAgent.zip
unzip AmazonCloudWatchAgent.zip
sudo ./install.sh
sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -a fetch-config -m ec2 -c ssm:/alarm/AWS-CWAgentLinConfig -s
