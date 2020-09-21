# cloudformation-wordpress
A cloudformation template that launches a fully equipped wordpress site across two availability zones. 

Set Up

In order to use this cloudformation template, you're going to need to set up some things first.

1) AWS Account
-You will need an AWS account to launch and maintain your wordpress website. The account is free to make and easy to set up. Follow the instrunctions here: https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/

2) EC2 Key Pair
- This is used to SSH into your instance in case you need to access the server. The key pair includes a public and a private key. You will need to create and download the private key and the template will give the instance the public key associated with your private key. This key is required in order to access the backend of your server. This may not be necessary, but it is a good idea to hold on to it in case the need arrises.

To create your key pair. Go to your AWS account
