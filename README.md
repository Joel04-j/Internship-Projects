Projec 1: Website Deployment on AWS
Website Deployment on AWS using Elastic Beanstalk

This project demonstrates how to deploy a website using **AWS Elastic Beanstalk** with the **Default Sample Application**. It is designed as a beginner-friendly introduction to cloud deployment without writing or uploading custom code.

---

##  Project Overview

Elastic Beanstalk is a fully managed service provided by AWS that allows easy deployment and scaling of web applications. In this project, we use AWS’s built-in sample application to explore and understand the deployment pipeline, environment setup, and infrastructure management.

---

##  Services Used

| AWS Service         | Description                                              |
|---------------------|----------------------------------------------------------|
| **Elastic Beanstalk** | Main service used for deploying the web application     |
| **Amazon EC2**        | Virtual server that hosts the website                   |
| **Amazon S3**         | Used internally by Beanstalk to store versions & logs   |
| **IAM**               | Manages roles and permissions for secure access         |
| **Amazon Route 53**   | Provides DNS routing to the deployed application (behind the scenes) |

---

##  Uses and Applications

- Learning cloud deployment without writing code
- Demonstrating cloud deployment in presentations or college projects
- Testing AWS infrastructure and permissions
- Preparing for real app deployment with Flask, Node.js, or other platforms
- Creating portfolio or resume projects showing cloud skills

---

##  Deployment Steps

1. **Create AWS Account**  
   Sign up at [https://aws.amazon.com](https://aws.amazon.com) and access the AWS Console.

2. **Open Elastic Beanstalk Service**  
   Search for "Elastic Beanstalk" in the AWS Console.

3. **Create New Application**  
   - Click “Create Application”
   - Enter an application name
   - Choose platform (e.g., Python)
   - Select **“Sample Application”** for code

4. **Create Environment**  
   Click **“Create environment”**. AWS provisions resources automatically.

5. **Access Your Website**  
   After a few minutes, AWS provides a public URL.  
   Click the URL to see your live website running the sample application.

---

##  Sample Output

![Sample Elastic Beanstalk Welcome Page](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/images/elasticbeanstalk-sample-application


# Project 2: Server-less Application using AWS Lambda and API Gateway

## Project Overview

This project demonstrates the development of a server-less application using **AWS Lambda** and **Amazon API Gateway**. The goal is to create a backend service that performs a specific task (e.g., reversing a string) without maintaining any servers.

AWS Lambda executes code in response to HTTP requests triggered through API Gateway. This allows you to build a lightweight, cost-efficient, and scalable backend application.

---

## Key Features

- Server-less architecture with zero server maintenance
- Automatic scaling and event-driven execution
- Minimal cost (pay only per invocation)
- Fast deployment of backend services
- Easily extendable for complex microservices

---

## Services Used

| AWS Service         | Description                                       |
|---------------------|---------------------------------------------------|
| AWS Lambda          | Runs the backend logic (Python function)          |
| Amazon API Gateway  | Triggers Lambda functions via REST API endpoints |
| IAM (Identity Access Management) | Manages secure access to Lambda        |
| CloudWatch          | Monitors logs and function execution stats        |

---

## Step-by-Step Implementation

### 1 Choose a Use Case

We select a basic data processing example: **Text Reversal API**.

The user sends a string via an API request, and the Lambda function responds with the reversed string.

---

### 2 Write the Lambda Function (Python)

1. Go to the AWS Console → **Lambda → Create Function**
2. Select “Author from scratch”
3. Runtime: **Python 3.9**

def lambda_handler(event, context):
    input_text = event['queryStringParameters']['text']
    reversed_text = input_text[::-1]
    return {
        'statusCode': 200,
        'body': f"Reversed text: {reversed_text}"
    }

### 3 Set up API Gateway
Navigate to API Gateway → Create API

Choose HTTP API

Select Build

Connect the Lambda function as an integration

Create a route like: GET /reverse

Deploy the API and copy the Invoke URL
 ### 4 Test the API

#Project 3:  Static Website Hosting using Amazon S3 and File Upload and Download using Amazon S3

This project demonstrates how to host a **static website** using **Amazon S3 (Simple Storage Service)**. A static website contains fixed content like HTML, CSS, and images, and is ideal for personal portfolios, landing pages, or documentation sites.

---

## Project Overview

Amazon S3 allows users to store and retrieve any amount of data. In this task, an S3 bucket is configured for **public static website hosting**, enabling users to access the site via a web browser. This is one of the simplest and most cost-effective ways to deploy static web content to the internet.

---

## Key Features

- Fast and low-cost hosting for static files  
- No servers or backend code needed  
- Easy to configure with custom domain support  
- Auto-scalable and highly available  
- Public access configuration for web hosting

---

## AWS Services Used

| Service      | Description                                     |
|--------------|-------------------------------------------------|
| **Amazon S3**   | Stores and serves static website files        |
| **IAM**         | Configures user permissions and roles         |
| **Amazon CloudFront** (optional) | Provides CDN and HTTPS support |

---

## Uses and Applications

- Hosting personal portfolios or resumes  
- Creating landing pages for products  
- Serving documentation or project pages  
- Learning web hosting and AWS fundamentals  
- Deploying frontend projects (HTML/CSS/JS)

---

## Step-by-Step Instructions

1. **Login to AWS Console**  
   Go to [https://console.aws.amazon.com](https://console.aws.amazon.com)

2. **Create an S3 Bucket**  
   - Choose a unique name  
   - Enable public access only if necessary  
   - Choose the appropriate region

3. **Upload Files**  
   - Use the AWS Console to drag-and-drop files into the bucket  
   - Set permissions (public or private)

4. **Download Files**  
   - Click on the file in the bucket  
   - Use the **Object URL** to download via browser

5. **(Optional) Add a Folder Structure**  
   - Organize files using folder names inside the bucket  
   - Helps in managing documents or media files

---

## Sample Output

> A fully functioning static website visible on a public S3 URL, accessible globally.

---
#Project 4: Cloud Cost Optimization Analysis

##  Project Overview

This project involves analyzing cloud infrastructure costs and identifying areas where resources can be optimized to reduce overall expenditure. Using tools available in AWS, such as the **Cost Explorer** and **Budgets**, we gain insight into the most cost-intensive services and propose strategies to optimize resource usage while maintaining performance.

The main objective is to understand cloud billing patterns, eliminate waste, and recommend best practices for cost-effective infrastructure management.

---

##  Key Features

- Real-time cost tracking and usage analysis
- Identification of high-cost services and underutilized resources
- Strategic cost-saving recommendations
- Monitoring cost improvements after implementation

---

##  Services Used

| AWS Service              | Purpose                                                  |
|--------------------------|----------------------------------------------------------|
| AWS Cost Explorer        | Visualize usage patterns and trends                      |
| AWS Budgets              | Set and track usage/cost thresholds                      |
| AWS CloudWatch           | Monitor instance/resource activity and utilization       |
| AWS Compute Optimizer    | Receive recommendations for EC2 instance sizing          |
| AWS Trusted Advisor      | Identify idle resources and underutilized services       |
| Amazon EC2/S3/RDS        | Example services analyzed for optimization               |

---

##  Step-by-Step Implementation

### 1️ Access Cloud Cost and Usage Reports

- Go to **AWS Billing Dashboard**
- Open **Cost Explorer**
- Enable it if not already done
- Set time range to **Last 30 days**
- Filter by service (e.g., EC2, S3, RDS) and region

---

### 2 Identify Cost-Intensive Resources

- Sort services by **Unblended Cost**
- Spot unusually high usage or spikes in billing
- Cross-check EC2 and RDS instances for uptime vs. performance
- Identify storage buckets or resources that are infrequently accessed

---

### 3 Recommend Cost-Saving Measures

Examples of common recommendations:
- **EC2 Instance Optimization**: Downgrade oversized instances based on CPU/memory usage
- **Spot Instances**: Use spot pricing for non-critical workloads
- **Auto Scaling**: Implement auto-scaling groups to avoid idle resources
- **S3 Lifecycle Rules**: Transition old data to infrequent access or Glacier storage
- **Terminate Idle Resources**: Delete unused EBS volumes, snapshots, and unattached IPs

---

### 4 Monitor Cost Savings

- Set up **AWS Budgets** to monitor cost after optimization
- Enable **Alerts** to notify when the threshold is reached
- Regularly check **Cost Explorer** for drops in service-level spending
- Document changes and compare **Before vs. After** costs
