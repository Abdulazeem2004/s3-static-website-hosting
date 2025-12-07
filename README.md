# s3-static-website-hosting

🌐 Static Website Hosting on Amazon S3
This project demonstrates how I deployed a fully static website to Amazon S3 using S3 Website Hosting in the af-south-1 (Cape Town) region. It covers bucket setup, permissions, hosting configuration, and accessing content using the S3 website endpoint.

🚀 Live Website
URL: http://my-second-020405.s3-website.af-south-1.amazonaws.com
📁 Project Structure
/project-root
│── index.html
|──image folder
│──README.md

🧰 AWS Services Used
# Amazon S3
- Hosts static file (HTML)
- Provides a public website endpoint

#IAM
- Used to configure safe access permissions 
- Handles bucket policies and access rules  (I attached a JSON policy to control public access at the bucket level rather than using a ACL)
  
#S3 Website Hosting
- Generates a public endpoint
- Serves static content over HTTP
- Allows custom index and error documents

  ⚙️ Deployment Steps
1. Create S3 Bucket
Bucket name: my-second-020405
Region: af-south-1
Uncheck: “Block All Public Access”


2. Enable Static Website Hosting
In the bucket:
Properties → Static Website Hosting → Enable
Set:
Index Document: index.html
Error Document: error.html (optional)
This generates the website endpoint:
http://my-second-020405.s3-website.af-south-1.amazonaws.com

3. Upload Website Files
Upload:
index.html
images
Note: The HTML template used in this project was sourced from a publicly available YouTube tutorial strictly for learning purposes.

5. Configure Bucket Policy
Used to allow public access to objects

6. Test the Website
Open:
http://my-second-020405.s3-website.af-south-1.amazonaws.com

🧠 What I Learned
✔️ S3 Website Hosting

How to turn an S3 bucket into a public website

How static content is served from object storage

✔️ AWS Security & IAM

Understanding bucket policies

Public object access vs Block Public Access settings

Least privilege principles

✔️ Cloud Deployment Flow

From creating a bucket → configuring hosting → uploading files → testing endpoint.

🏗️ Architecture Diagram (Conceptual)
[User Browser]
       │
       ▼
[S3 Website Endpoint]
       │
       ▼
[S3 Bucket]
  index.html
  styles.css

🔮 Future Enhancements
Add CloudFront for:
HTTPS support
Global CDN delivery
Custom domain with Route 53
Add form handling using:
API Gateway
Lambda
DynamoDB
Add CI/CD deployment using GitHub Actions
Add Terraform or CloudFormation for Infrastructure as Code

In Conclusion
This project showcases how to deploy a static website on S3 while understanding AWS fundamentals such as bucket policies, permissions, and public hosting. It is a foundational cloud project that demonstrates real AWS hands-on experience.




