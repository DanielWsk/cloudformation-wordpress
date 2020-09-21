# cloudformation-wordpress
A cloudformation template that launches a fully equipped wordpress site across two availability zones. 

SET UP

In order to use this cloudformation template, you're going to need to set up some things first.

1) AWS Account
- You will need an AWS account to launch and maintain your wordpress website. The account is free to make and easy to set up. Follow the instrunctions here: https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/

2) EC2 Key Pair
- This is used to SSH into your instance in case you need to access the server. The key pair includes a public and a private key. You will need to create and download the private key and the template will give the instance the public key associated with your private key. This key is required in order to access the backend of your server. This may not be necessary, but it is a good idea to hold on to it in case the need arrises.

- To create your key pair. Go to your AWS account and under services, go to EC2. On the left side menu, you will see the option for Key Pairs. Go there and create key pair. Name it whatever you like and it will automatically download onto your computer. You will input this later when you launch your website.

3) DNS/Route 53
- If you'd like your website to have a name instead of just an ip address, you're going to need to purchase a DNS hosted zone. This will cost you some money, but you will now own this DNS name.  

- To create a DNS Hosted Zone, go to your AWS Account and under services go to Route 53. On the left side menu go to Hosted Zones and create a hosted zone. Choose wisely because this will be the name of your website.

4) S3 Bucket
- We will be using cloudformation to launch your website. Cloudformation will take the template from a file on your AWS account. S3 is object storage that you can use for free on AWS. You will need to put the files from this repo into a "bucket" so cloudformation can find it.

- Go to your AWS account and under services go to S3. You will need to create a bucket. Name it whatever you like, it won't matter. Download the files from this repo and then upload them into your bucket.

USING THE TEMPLATE

Go to cloudformation under services. Create a stack. Name the stack whatever you like. For the template source, choose S3 and then copy and paste the URL for the master stack. To find this URL, go to your S3 bucket, click on the master stack file, and the URL should be displayed there.
Follow the instructions on the parameters page. Make sure that whichever option you choose for the VPC CIDR, all the subnets use the same CIDR scheme. Also don't forget to change the MasterUserName and MasterPassword to your own personal username and password. You can leave the rest of the settings on default and launch the stack. 
The stack will take a little while to finish launching. Give it 15 minutes.

Once the stack is fully launched, it should say Create Complete next to the master stack. 
Now you can access your wordpress website. Go to the website you created. You should be prompted for your username and password.
