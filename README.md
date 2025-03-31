# AWS---Portfolio-using-CI-CD

This repository contains the CI/CD pipeline for deploying a static AWS portfolio website using Amazon S3 and GitHub Actions.

## Live Demo
[Click here to view the live portfolio](http://portfolio-awsbucket-cicd-project.s3-website.ap-south-1.amazonaws.com)

## Overview
This project automates the deployment of a static portfolio website using AWS S3 and GitHub Actions. Whenever changes are pushed to the repository, GitHub Actions triggers the CI/CD pipeline, which updates the S3 bucket hosting the portfolio.

## Architecture Diagram
![CI/CD Flowchart](./path-to-your-diagram.png)  
*(Replace `path-to-your-diagram.png` with the actual image path in your repository.)*

## Tech Stack
- **AWS S3** – Hosts the static website
- **GitHub Actions** – Automates the deployment process
- **IAM Roles** – Manages access permissions for GitHub Actions

## Features
- Continuous Deployment (CD) with GitHub Actions
- Secure and scalable hosting using AWS S3
- Automated updates on every push

## How It Works
1. **Push Changes to GitHub**: The user commits and pushes updates to the repository.
2. **GitHub Actions Triggered**: A GitHub Actions workflow runs the CI/CD pipeline.
3. **Deployment to AWS S3**: The updated website files are synced with the S3 bucket.
4. **Live Website Updated**: The changes reflect instantly on the live portfolio site.

## Getting Started
### Prerequisites
- AWS account with an S3 bucket configured
- GitHub repository with appropriate permissions
- IAM role allowing GitHub Actions to access S3

### Deployment Setup
1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/AWS---Portfolio-using-CI-CD.git
   cd AWS---Portfolio-using-CI-CD
   ```
2. **Configure AWS Credentials** in GitHub Secrets:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_REGION`
   - `S3_BUCKET_NAME`

3. **Push changes to trigger deployment**
   ```bash
   git add .
   git commit -m "Update portfolio"
   git push origin main
   ```

## GitHub Actions Workflow
This repository includes a `.github/workflows/deploy.yml` file that:
- Installs dependencies (if any)
- Syncs files to S3 using AWS CLI
- Invalidates the CloudFront cache (if applicable)

## Contributing
Feel free to fork this repository and submit pull requests for improvements!

## License
This project is open-source and available under the [MIT License](LICENSE).
