Website Deployment on AWS using Elastic Beanstalk

This project demonstrates how to deploy a website using **AWS Elastic Beanstalk** with the **Default Sample Application**. It is designed as a beginner-friendly introduction to cloud deployment without writing or uploading custom code.

---

##  Project Overview

Elastic Beanstalk is a fully managed service provided by AWS that allows easy deployment and scaling of web applications. In this project, we use AWS’s built-in sample application to explore and understand the deployment pipeline, environment setup, and infrastructure management.

---

##  Key Features

- No coding required
- One-click deployment using sample app
- Automatic setup of servers (EC2), networking, and scaling
- Publicly accessible URL
- Beginner-friendly and fast setup

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

![Sample Elastic Beanstalk Welcome Page](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/images/elasticbeanstalk-sample-applicatio
