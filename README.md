#  Scalable Web Application Using AWS EC2, ALB & Auto Scaling

#  Project Overview

This project focuses on deploying a scalable and highly available web application using Amazon Web Services (AWS).
The application uses Amazon EC2 instances to host a website, an Application Load Balancer (ALB) to distribute incoming traffic, and an Auto Scaling Group (ASG) to automatically manage EC2 instances based on demand.
The architecture is designed to provide high availability, fault tolerance, and scalability across multiple Availability Zones.

# System Architecture

![AWS Scalable Web Application Architecture](docs/aws-architecture.png)

# Architecture Flow

```text
                  Internet Users
                        |
                        |
               Application Load Balancer
                        |
                   Target Group
                        |
              ---------------------
              |                   |
         Availability Zone A  Availability Zone B
              |                   |
           EC2-Instance 1      EC2-Instance 2
              |                   |
            Apache              Apache
              |                   |
            HTML App            HTML App
              |                   |
              ---------------------
                        |
                 Auto Scaling Group
                        |
                    CloudWatch
```

# AWS Services Used

| AWS Service | Purpose |
|---|---|
| Amazon EC2 | Hosts the web application |
| Application Load Balancer | Distributes incoming traffic |
| Target Group | Registers and monitors EC2 instances |
| Auto Scaling Group | Automatically manages EC2 capacity |
| Launch Template | Defines EC2 instance configuration |
| Amazon VPC | Provides network infrastructure |
| Security Groups | Controls inbound and outbound traffic |
| Amazon CloudWatch | Monitors resource utilization |

# Technologies Used

- AWS Cloud
- Amazon Linux 2023
- Linux
- Apache Web Server
- HTML
- EC2
- Application Load Balancer
- Auto Scaling
- CloudWatch

# Project Implementation

# 1. VPC Configuration
- Created a Virtual Private Cloud (VPC).
- Configured public subnets across multiple Availability Zones.
- Configured Internet Gateway and Route Tables.

# 2. Security Group Configuration
- Created separate security groups for ALB and EC2.
- Allowed HTTP traffic through the load balancer.
- Restricted SSH access to my IP address.

# 3. EC2 Configuration
- Launched an Amazon Linux 2023 EC2 instance.
- Installed and configured Apache Web Server.
- Created a custom HTML web application.

# 4. AMI Creation
- Created an Amazon Machine Image (AMI) from the configured EC2 instance.
- Used the AMI as the base image for additional instances.

# 5. Target Group Configuration
- Created a target group.
- Configured HTTP health checks.
- Registered EC2 instances.

# 6. Application Load Balancer
- Created an internet-facing Application Load Balancer.
- Configured listeners and target groups.
- Distributed incoming requests across healthy EC2 instances.

# 7. Auto Scaling Group
- Created a Launch Template.
- Configured minimum, desired, and maximum instance capacity.
- Integrated the Auto Scaling Group with the ALB Target Group.
- Configured scaling policies based on CPU utilization.

# 8. Monitoring
- Used Amazon CloudWatch to monitor EC2 CPU utilization.
- Configured automatic scaling based on demand.

# Key Features

- High Availability across multiple Availability Zones.
- Automatic EC2 instance scaling.
- Load balancing and traffic distribution.
- Health checks for EC2 instances.
- Fault tolerance and instance recovery.
- Centralized monitoring using CloudWatch.

# Project Screenshots

<img width="1892" height="916" alt="Screenshot 2026-11-09 160305" src="https://github.com/user-attachments/assets/ce0e9ede-9cb3-4c49-bd11-c3166e033484" />
<img width="1892" height="918" alt="Screenshot 2026-11-09 160419" src="https://github.com/user-attachments/assets/707362e2-6ad9-42d4-bcf1-4238e1ceacf0" />
<img width="1892" height="967" alt="Screenshot 2026-11-09 160225" src="https://github.com/user-attachments/assets/f9e578d8-6056-486f-b2ba-de930df794e5" />
<img width="1913" height="967" alt="Screenshot 2026-11-09 160235" src="https://github.com/user-attachments/assets/bd565b1e-c199-4173-abb6-b6433c4580b0" />
<img width="1897" height="953" alt="Screenshot 2026-11-09 160246" src="https://github.com/user-attachments/assets/31881fe1-b1e4-46ef-88cc-2f4b7ce0e205" />
<img width="1908" height="896" alt="Screenshot 2026-11-09 161153" src="https://github.com/user-attachments/assets/3084345c-a209-4435-b4cf-894daebaf89b" />
<img width="1916" height="952" alt="Screenshot 2026-11-09 160636" src="https://github.com/user-attachments/assets/c3173cb2-1bea-4752-9388-88a4eb49d5ff" />
<img width="1917" height="891" alt="Screenshot 2026-11-09 160647" src="https://github.com/user-attachments/assets/ba823a58-92d5-497e-b9e7-1284bf25fd53" />
<img width="1910" height="947" alt="Screenshot 2026-11-09 162056" src="https://github.com/user-attachments/assets/8d3a6b03-faa0-4d80-815a-58ea6b6ee122" />


## 🎯 Learning Outcomes

Through this project, I gained practical experience in:

- AWS networking and VPC configuration.
- EC2 instance management.
- Apache web server configuration.
- Application Load Balancer setup.
- Auto Scaling implementation.
- Cloud infrastructure monitoring.
- High availability and fault tolerance concepts.

## 👨‍💻 Author

**Kedarnath Shastry**

Aspiring Cloud & DevOps Engineer

Skills: AWS | Linux | Git | GitHub | Docker | Kubernetes | Jenkins | CI/CD

---

⭐ If you find this project useful, feel free to explore the repository!
