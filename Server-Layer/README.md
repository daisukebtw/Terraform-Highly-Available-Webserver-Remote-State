
# Terraform AWS Web Highly Available Infrastructure

This Terraform code is used to create a highly available web infrastructure with zero downtime and green/blue deployment. The infrastructure includes a launch configuration for an autoscaling group, an autoscaling group attached to an elastic load balancer, an elastic load balancer attached to subnets from the network layer, and a security group for the web server. The backend uses an S3 bucket to connect to remote state for easy editing of the project.

## Prerequisites

- An AWS account
- AWS CLI
- Terraform CLI

## Usage

1. Clone this repository:

    git clone https://github.com/daisukebtw/Highly-Available-Remote-State-Webserver-with-VPC

2. Change into the cloned directory

3. Initialize the backend:

    terraform init

4. Apply the code:

    terraform apply

5. Destroy the infrastructure when finished:

    terraform destroy

## Components

### Provider

The AWS provider is used to define the AWS region to create the infrastructure.


### Backend

The backend configuration uses an S3 bucket to connect to remote state for the project.


### Launch Configuration

The launch configuration creates an instance template used by the autoscaling group.


### Autoscaling Group

The autoscaling group automatically scales up or down based on demand, with a minimum size of two instances.


### Elastic Load Balancer

The elastic load balancer distributes incoming traffic to the instances in the autoscaling group.


### Security Group

The security group allows access to specific ports, with the option to define custom ports.



## Author

Made by Vitali Aleksandrov on April 28, 2023.
