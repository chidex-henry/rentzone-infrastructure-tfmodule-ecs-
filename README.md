***Building AWS infrastructures with Terraform Modules***

### Overview
This project demonstrates the deployment of the Rentzone application on Amazon Web Services (AWS) infrastructure using Terraform modules. By utilizing Terraform modules, the project efficiently packages and deploys AWS resources, ensuring the scalability, reliability, and security of the application.

### Project Components

1. **AWS Provider Configuration**
   - Configured the AWS provider in `provider.tf` to establish a secure connection between Terraform and AWS resources.

2. **Terraform State Management**
   - Stored the Terraform state file in Amazon S3 and locked it with DynamoDB, ensuring the integrity and concurrency control of the infrastructure.

3. **AWS Resource Provisioning**
   - Leveraged Terraform modules to provision various AWS services including:
     - **Virtual Private Cloud (VPC):**
       - Created a VPC with public and private subnets across multiple availability zones to enhance fault tolerance and reliability.
     - **Internet Gateway:**
       - Facilitated connectivity between VPC instances and the wider Internet.
     - **Security Groups:**
       - Implemented as a network firewall mechanism to control inbound and outbound traffic.
     - **AWS RDS Instance:**
       - Launched an RDS instance to store the SQL file.
     - **Amazon ECS (Elastic Container Service):**
       - Configured task execution role, ECS cluster, task definition, and service to deploy, manage, and scale the application in containers.
     - **Application Load Balancer (ALB) and Auto Scaling:**
       - Utilized ALB and target group for evenly distributing web traffic to an Auto Scaling Group of EC2 instances across multiple availability zones.
       - Employed Auto Scaling Group to manage EC2 instances automatically, ensuring website availability, scalability, fault tolerance, and elasticity.
     - **GitHub Integration:**
       - Stored web files on GitHub for version control and collaboration.
     - **Certificate Manager:**
       - Secured application communication using SSL/TLS certificates.
     - **Simple Notification Service (SNS):**
       - Configured SNS to alert about activities within the Auto Scaling Group.
     - **Route 53:**
       - Registered the domain name and set up DNS records for the application.

### Usage
1. Clone the repository containing the Terraform configurations.
2. Configure AWS credentials and region.
3. Initialize Terraform with `terraform init`.
4. Review and modify variables in the Terraform files as necessary.
5. Apply the Terraform configuration with `terraform apply`.
6. Monitor the deployment process and ensure successful provisioning of resources.
7. Access the Rentzone application using the provided domain name.

### Conclusion
This project showcases the power of Terraform modules in simplifying the deployment and management of AWS infrastructures for complex applications like Rentzone. By encapsulating resource configurations into reusable modules, developers can streamline the provisioning process while maintaining scalability, reliability, and security.

This README provides an overview of the Rentzone application deployment using Terraform modules on AWS. It outlines the project components, and usage instructions, and highlights the benefits of using Terraform for infrastructure as code (IaC) deployments.

<img width="468" alt="image" src="https://github.com/chidex-henry/rentzone-infrastructure-tfmodule-ecs-/assets/77998377/bd8efa3e-1b93-4946-ab93-c79501146a9c">
