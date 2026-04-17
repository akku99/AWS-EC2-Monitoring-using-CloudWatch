# **AWS EC2 Monitoring with Cloudwatch | Monitor Memory Utilization using CloudWatch**

## Steps:

### Step 1: Create an IAM and Attach CloudWatch and SSM Full Access - EC2-CloudWatch-Role
### Step 2: Create a parameter in Systems Manger with the name "/alarm/AWS-CWAgentLinConfig" and store the value.
### Step 3: Create an EC2 Instance, Attach the role created in Step 1 and Add the commands in the Userdata Section.
