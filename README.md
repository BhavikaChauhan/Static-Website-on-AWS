# Static Website Deployment with CI/CD on AWS

This project demonstrates how to automate the deployment of a static website to **AWS S3** using **GitHub Actions** as part of a **CI/CD pipeline**. The pipeline ensures that every time changes are pushed to the `main` branch, the latest version of the website is deployed to S3.

## 🚀 Features
- **Automated Deployment**: Every time code is pushed to the `main` branch, GitHub Actions automatically deploys the site to AWS S3.
- **AWS CloudFront Integration**: Content is delivered via **CloudFront** for faster and secure access.
- **Versioning and Rollback**: Versioning of files in S3 is enabled, ensuring safe deployments with rollback options in case of failures.

## 📦 Tech Stack
- **AWS S3**: For hosting static website files.
- **AWS CloudFront**: For content delivery with CDN.
- **GitHub Actions**: For automating the CI/CD pipeline.
- **HTML, CSS, JS**: For the static website content.

## 🛠️ Prerequisites
Before setting up the project, make sure you have the following:
- **AWS Account**: An active AWS account to create the S3 bucket and CloudFront distribution.
- **GitHub Account**: A GitHub account for creating the repository and configuring GitHub Actions.
- **AWS CLI**: For managing AWS services via command line (optional but useful).

## ⚙️ Setup Instructions

### 1. Clone the Repository
First, clone the repository to your local machine:
```bash
git clone https://github.com/BhavikaChauhan/static-website-ci-cd.git
cd static-website-ci-cd

### 2. Configure AWS S3 Bucket
Log in to your AWS account.

Create a new S3 bucket for hosting the static site.

Enable Static Website Hosting in the bucket settings.

Make the files publicly accessible by setting the appropriate permissions.

### 3. Set Up AWS CloudFront (Optional)
Create a CloudFront distribution to serve the website with a Content Delivery Network (CDN) for faster access and SSL support.

Note the S3 website endpoint and CloudFront domain for later.

### 4. Add AWS Credentials to GitHub
Go to your GitHub repository settings and add the following secrets:

AWS_ACCESS_KEY_ID: Your AWS Access Key ID.

AWS_SECRET_ACCESS_KEY: Your AWS Secret Access Key.

AWS_REGION: The AWS region where your S3 bucket is located (e.g., us-east-1).

S3_BUCKET_NAME: The name of your S3 bucket.

### 5. Configure GitHub Actions Workflow
The GitHub Actions workflow is defined in .github/workflows/deploy.yml. This will automatically deploy your site to AWS S3 when you push code to the main branch.

Key Steps in the Workflow:
Checkout Code: The workflow first checks out the latest code.

Configure AWS Credentials: It then configures AWS credentials using the secrets added in step 4.

Sync to S3: Finally, it syncs the files to your S3 bucket using the AWS CLI.

### 6. Push Code to GitHub
Once everything is set up, push your local changes to GitHub:
git add .
git commit -m "Initial website setup"
git push origin main
This will trigger the GitHub Actions workflow to deploy your site automatically.


🌐 Accessing the Website
Once the workflow runs successfully, your website will be accessible through the S3 endpoint or CloudFront distribution URL.


🧑‍💻 Contributing
If you want to contribute to this project, feel free to fork the repository and make your changes. Pull requests are welcome!
