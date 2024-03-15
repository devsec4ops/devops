# Installation
### AWS Linux Instance Setup: Quick Guide

#### Step 1: Sign Up for AWS

-   If you don't already have an AWS account, go to the [AWS homepage](https://aws.amazon.com/) and sign up. You'll need to provide payment information, but the AWS Free Tier allows you to experiment with little to no cost.

#### Step 2: Create an EC2 Instance

1.  Log into the AWS Management Console after creating your account.
2.  Navigate to the EC2 Dashboard under Services.
3.  Click Launch Instances to start the instance setup process.

#### Step 3: Choose an Amazon Machine Image (AMI)

-   AWS provides various Linux AMIs, including Amazon Linux 2, Ubuntu, and CentOS. Select the one that suits your requirements.

#### Step 4: Select Instance Type

-   Choose `t2.micro` for the AWS Free Tier eligibility, or select another type based on your needs.
-   Click Next: Configure Instance Details.

#### Step 5: Configure Instance Details

-   Leave the default settings or customize as per your requirements, such as network and IAM roles.
-   Ensure Auto-assign Public IP is enabled for remote access.

#### Step 6: Add Storage

-   Adjust the size if needed; the default is usually sufficient for basic use cases.
-   Click Next: Add Tags.

#### Step 7: Add Tags (Optional)

-   You can tag your instance for easier management, e.g., Name: MyLinuxInstance.

#### Step 8: Configure Security Group

-   Create a new security group or select an existing one.
-   Ensure SSH access (port 22) is allowed from your IP address for security.

#### Step 9: Review and Launch

-   Review your instance configurations.
-   Click Launch, then select a key pair for SSH access. If you don't have a key pair, create a new one. Download and save it securely.
-   Click Launch Instances.

#### Step 10: Connect to Your Linux Instance

-   Once your instance state is "running," connect via SSH using the downloaded key pair:

    `ssh -i /path/to/your-key.pem ec2-user@<Instance-Public-DNS>`

-   Replace `/path/to/your-key.pem` with your actual key file path and `<Instance-Public-DNS>` with your instance's public DNS.

### Note

-   Security Best Practices: Regularly update your Linux instance with the latest security patches.
-   Cost Management: Monitor your usage to stay within the Free Tier limits, and stop or terminate your instance when it's not in use to avoid unnecessary charges.