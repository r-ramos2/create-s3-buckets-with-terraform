<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Create S3 Buckets with Terraform

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-devops-terraform1)

**Author:** R  


---

![Image](http://learn.nextwork.org/serene_teal_majestic_duck/uploads/aws-devops-terraform1_9i0j1k2l)

---

## Introducing Today's Project!

In this project, I will demonstrate how to use Terraform to automate the creation and management of an Amazon S3 bucket. The goal is to reduce manual work, minimize errors, and streamline cloud infrastructure deployment using Infrastructure as Code.

### Tools and concepts

Services I used were AWS S3, IAM, and Terraform. Key concepts I learned include infrastructure as code (IaC), how Terraform manages cloud resources declaratively, and the lifecycle of provisioning, verifying, and destroying infrastructure using terraform init, plan, apply, and destroy.

### Project reflection

This project took me approximately 1 hour to complete. The most challenging part was setting up AWS credentials correctly for Terraform to authenticate. It was most rewarding to see the S3 bucket created and managed entirely through code.

I did this project to gain hands-on experience with Terraform and cloud resource provisioning. This project met my goals by giving me practical exposure to IaC and deepening my understanding of how to automate AWS infrastructure securely and efficiently.

---

## Introducing Terraform

Terraform is an open-source tool that lets you define and provision cloud infrastructure using configuration files, automating deployment and reducing manual setup.

Terraform is one of the most popular tools used for infrastructure as code (IaC), which is a method of managing and provisioning infrastructure through code to ensure consistent, repeatable, and scalable deployments.

Terraform uses configuration files to define desired infrastructure states and manage deployments automatically. main.tf is the primary file where these definitions are written, serving as the blueprint for provisioning cloud resources.

![Image](http://learn.nextwork.org/serene_teal_majestic_duck/uploads/aws-devops-terraform1_9i0j1k2l)

---

## Configuration files

The configuration is structured in blocks, each defining a provider or resource. The advantage of doing this is clarity, modularity, and easier maintenance of cloud infrastructure.

### My main.tf configuration has three blocks

The first block indicates AWS as the provider. The second block provisions an S3 bucket. The third block manages public access settings for the bucket.

![Image](http://learn.nextwork.org/serene_teal_majestic_duck/uploads/aws-devops-terraform1_ljvh9876)

---

## Customizing my S3 Bucket

---

## Terraform commands

I ran 'terraform init' to set up my Terraform project by downloading required provider plugins, initializing the backend, and creating a lock file to ensure consistent infrastructure management.

Next, I ran 'terraform plan' to preview the changes Terraform will make to my AWS infrastructure, allowing me to review the resources it will create before applying them.

![Image](http://learn.nextwork.org/serene_teal_majestic_duck/uploads/aws-devops-terraform1_3g4h5i6j)

---

## AWS CLI and Access Keys

When I tried to plan my Terraform configuration, I received an error message that says “No valid credential sources found” because Terraform could not access my AWS account. This happens when the necessary AWS credentials are not yet configured on my machine.

To resolve my error, first I installed AWS CLI, which is a command-line tool that allows me to interact with AWS services directly from my terminal. It's essential for authenticating Terraform with my AWS account and managing infrastructure programmatically.

I set up AWS access keys to allow Terraform (via the AWS CLI) to authenticate with my AWS account and securely create and manage cloud resources programmatically from my local machine.

![Image](http://learn.nextwork.org/serene_teal_majestic_duck/uploads/aws-devops-terraform1_7j8k9l0m)

---

## Lanching the S3 Bucket

I ran 'terraform apply' to create the actual AWS resources I defined in my configuration. Running 'terraform apply' will affect my AWS account by provisioning an S3 bucket and its associated public access block, as specified in the main.tf file.

The sequence of running terraform init, plan, and apply is crucial because terraform init sets up the environment and installs necessary providers, terraform plan previews the changes Terraform will make, and terraform apply executes those changes. This order ensures predictable, controlled, and safe infrastructure deployment.

![Image](http://learn.nextwork.org/serene_teal_majestic_duck/uploads/aws-devops-terraform1_1q2w3e4r)

---

## Uploading an S3 Object

---

---
