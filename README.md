# Scalable and Secure E-Commerce Platform on AWS

## Overview
This project involves the design, development, and deployment of a scalable e-commerce platform on AWS. The platform is built to handle fluctuating user traffic, secure sensitive customer data, and optimize content delivery globally. Utilizing key AWS services such as Auto Scaling, RDS, WAF, CloudFront, and encryption methodologies, the project demonstrates the deployment of a secure and efficient application in a cloud environment.

---

## Table of Contents
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Project Phases](#project-phases)
  - [Phase 1: Infrastructure Setup](#phase-1-infrastructure-setup)
  - [Phase 2: Securing the Application](#phase-2-securing-the-application)
  - [Phase 3: Content Delivery and Performance Optimization](#phase-3-content-delivery-and-performance-optimization)
  - [Phase 4: Testing and Monitoring](#phase-4-testing-and-monitoring)
- [References](#references)

---

## Technologies Used
- **AWS Services**:
  - EC2 (Elastic Compute Cloud)
  - RDS (Relational Database Service)
  - WAF (Web Application Firewall)
  - CloudFront (Content Delivery Network)
  - S3 (Simple Storage Service)
  - IAM, ACM, and KMS for security
  - CloudWatch, CloudTrail, and AWS Config for monitoring
- **Tools**:
  - Apache JMeter for stress testing
  - GitHub for version control
  - MySQL for database operations

---

## Features
- Scalable EC2 instances with Auto Scaling and load balancing.
- Secure database management with RDS, encryption, and SSL.
- WAF for protection against common web attacks.
- Accelerated content delivery using CloudFront and S3.
- Monitoring and cost optimization with CloudWatch, CloudTrail, and Cost Explorer.

---

## Project Phases

### Phase 1: Infrastructure Setup
- **VPC and Subnets**:
  - Created a VPC with a CIDR block of `10.0.0.0/16`.
  - Configured public and private subnets across two availability zones.
- **EC2 and Auto Scaling**:
  - Deployed EC2 instances with a predefined AMI and custom `UserData` for application setup.
  - Configured an Auto Scaling Group with scaling policies based on CPU utilization.
- **Load Balancer**:
  - Set up an Application Load Balancer (ALB) to distribute incoming traffic.
- **RDS**:
  - Configured a MySQL RDS instance with Multi-AZ deployment and encryption at rest.
- **Deliverables**:
  - Fully functional EC2 instances with a load balancer.
  - CRUD operations on the database via the e-commerce platform.

### Phase 2: Securing the Application
- **Web Application Firewall (WAF)**:
  - Configured WAF with managed rules (SQL Injection, Common Vulnerabilities).
  - Monitored WAF logs via CloudWatch.
- **Encryption**:
  - Issued SSL/TLS certificates using ACM for secure HTTPS communication.
  - Enabled SSL for connections between EC2 and RDS.
- **Deliverables**:
  - WAF blocking malicious traffic.
  - Secure HTTPS communication and encrypted database connections.

### Phase 3: Content Delivery and Performance Optimization
- **CloudFront CDN**:
  - Configured CloudFront for caching static assets globally.
  - Integrated S3 buckets for static content delivery.
- **Performance Tuning**:
  - Enabled GZIP compression for assets to reduce load times.
  - Monitored latency and request rates using CloudWatch.
- **Deliverables**:
  - Optimized content delivery using CloudFront and S3.
  - Performance metrics for latency and cache hits.

### Phase 4: Testing and Monitoring
- **Stress Testing**:
  - Used Apache JMeter to simulate 1 million requests and validate Auto Scaling behavior.
- **Monitoring Setup**:
  - Configured CloudWatch dashboards for metrics like CPU utilization, database connections, and request rates.
  - Enabled CloudTrail and AWS Config for auditing and compliance.
- **Cost Optimization**:
  - Analyzed resource costs using AWS Cost Explorer.
  - Recommended Reserved Instances and Savings Plans.
- **Deliverables**:
  - Stress test results demonstrating Auto Scaling effectiveness.
  - CloudWatch dashboards and cost optimization recommendations.

---

## References
- [AWS VPC Documentation](https://docs.aws.amazon.com/vpc/)
- [Amazon RDS Documentation](https://docs.aws.amazon.com/rds/)
- [AWS WAF Documentation](https://docs.aws.amazon.com/waf/)
- [Amazon CloudFront Documentation](https://docs.aws.amazon.com/cloudfront/)
- [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/)

---
