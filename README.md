                                ASSIGNMENT FOR THE ASSESSMENT
This is a solution for Wordpress website. Highly available, resilient and secured architecure created in AWS CloudFormation.
Find the design's schema in launchpad-assessment-project.pdf

Instruction of deployment:
1. Add your AWS repository secrets to GitHub (ACCESS_KEY and ACCESS_KEY_SECRET)
2. Specify region where you want to deploy it in .github/workflows/deploy.yaml (line 30)
3. Provide SSL Certificate for Application Load Balancer in .github/workflows/deploy.yaml (line 106)
4. Provide SSL Certificate for CloudFront in .github/workflows/deploy.yaml (line 157)
5. Provide WPDomain parameter for instance-stack job in .github/workflows/deploy.yaml associated with previously provided certificate (line 110 and 156)
6. Provide your email address for SNS topic in instance.yaml (line 509)

Resources that will be created using this solution:
- VPC
- 2 Availability Zones
- 2 public and 4 private subnets
- Internet Gateway
- 2 Nat Gateways
- 2 Elastic IPs
- Routes and Route Tables
- Parameters and Secrets
- S3 bucket (to store static content)
- EFS (to be used by EC2 instances for Wordpress data)
- RDS and replica (to store Wordpress Database)
- Instance Role
- EC2 instances (ubuntu servers)
- AutoScaling Group
- Application Load Balancer
- SNS
- Security Groups
- CloudFront 
