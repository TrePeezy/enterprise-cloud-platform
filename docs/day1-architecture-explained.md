# Day 1 Architecture Explanation

## Overview
This architecture represents the initial design of a production style AWS cloud platform. The goal is to create a secure, scalable, and highly available foundation that can grow into a full enterprise environment.

## Region and Availability Zones
The design is deployed in a single AWS Region across two Availability Zones. This improves availability and reduces the risk of downtime if one AZ fails.

## VPC Design
The architecture is built inside a Virtual Private Cloud (VPC), which acts as the private network boundary for the platform. This gives control over networking, routing, and security.

## Public and Private Subnets
Public subnets are used for internet facing resources such as the Application Load Balancer. Private subnets are used for the application and database tiers to reduce exposure and improve security.

## Traffic Flow
User traffic comes in through the load balancer. The load balancer routes requests to the application tier. The application tier communicates with the database tier in the private network.

## Supporting Services
Amazon S3 is included for storage needs such as static assets or logs. CloudWatch is included for monitoring and observability.

## Future Expansion
This platform will later be expanded with:
- EC2 deployment
- RDS deployment
- Terraform
- Kubernetes
- CI/CD pipelines
- Monitoring dashboards
- AI powered cloud tools