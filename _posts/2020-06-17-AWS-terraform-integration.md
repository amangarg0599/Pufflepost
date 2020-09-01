---
layout: post
title:  "Integration Of AWS with Terraform"
author: Aman
categories: [ AWS, terraform ]
image: assets/images/terraformaws.webp
comments: false
---

Amazon web services  (AWS) is from  Amazon and is a major player in the cloud industry. Today they have many major clients that trusts AWS as their cloud provider, some of the services such as EC2 , S3 are very famous.

Terraform's an open source  IAC ( infrastructure as software) tool that allow us to manage multiple cloud infrastructure in cloud. Its a very smart tool to manage everything at one place instead of using different services of cloud. it uses it own high level language called **Hashicorp Configuration Language**. Its a very simple to use tool that uses modules to work with different platform.

Terraform also provides details documents for the services that it support so that we don't have to learn any command/code to perform any task . It can be found [here](https://www.terraform.io/docs/) 

Now before proceeding we have we have to make sure that these software are installed with their *PATH* set. 

- AWS CLI V2 
- Terraform  

To set the path just go to System Properties -> Advanced -> Environment Variables.. -> In system Variables find `PATH`  and click on Edit. 

![Environment Variable]({{ site.baseurl}}/assets/images/Environment variable.webp)

Then Add the path for terraform CLI as shown-

![edit path]({{ site.baseurl }}\assets\images\edit path.webp)

Now before starting we have to understand a basic thing that in real life we may work in environment where we don't want to expose our login credentials, so we will use terraform using the profile  that we will create from AWS CLI that can be seen in the screenshot, either we can use default profile for CLI or create our own profile. 

![CLI command to create profile]({{ site.baseurl }}/assets/images/profilesetup.webp)
Now we have created the method to authenticate we will create terraform workspace. A workspace is nothing but folder where we store our code, for better management of code its preferable to put code in a folder. Now we will create code to launch the instance in AWS 

`Note - The extension to store terraform file is my_file.tf`` 

Now we will create terraform code to launch ec2 instance

```terraform
provider "aws" {
  region     = "us-east-1"
  profile    = "default"
}
resource "aws_instance" "myinstance" {
  ami           = "ami-09d95fab7fff3776c"
  instance_type = "t2.micro"
  key_name      = "Mywebserverkey"
  security_groups = [ "MyWebServer" ]

  tags = {
    Name = "HttpdServer"
  }
}
```

This code will launch the ec2 instance in the AWS using the profile 'default' . Now we will explain each syntax line by line- 

`provider "aws" ` means that we will be using the AWS infrastructure in which we will use the region `us-east-1`  that is N. Virginia.

 `resource "aws_instance" "myinstance"` means that we will be launching the resource ec2 instance that is named `myinstance`  with the parameters such as  

-  AMI  -  Amazon machine image, here we will be using the AM 2 that is amazon's own machine image with id that we have provided .
- instance_type - Specifies type of instance that we want to launch 
- Key_name - Used to access the instance locally, here we are using the key `Mywebserverkey` that we created to access  access CLI.
- security_group - Its like firewall for the instance, here we are using the `MyWebServer` SG that we created earlier.

These all are required components specified by [Terraform docs](https://www.terraform.io/docs/providers/aws/index.html) to launch instance in cloud. Tag parameter will allow the easy access to this instance later on in terraform.

Save this file as myfile.tf in the desired workspace and open the command prompt to the location and write command `terraform init` this command is so smart that it will check the .tf file and download the required modules to run the file.

![]({{ site.baseurl }}\assets\images\terraform init.webp)
![]({{ site.baseurl }}\assets\images\terraform apply.webp)

After that we will write `terraform apply` in the same command prompt in location where we have initialized the workspace and type `yes` when asked. The instance will launched in AWS as seen in dashboard 



![AWS instance]({{ site.baseurl }}\assets\images\terraform launch.webp)
![AWS instance]({{ site.baseurl }}\assets\images\instance.webp)



