# **AWS Project: Host a Static Website on Amazon S3**

This project demonstrates how I hosted a simple HTML/CSS website using Amazon S3, allowing it to be accessed publicly on the internet.

 

## **📚 Step 1 -- Prepare Your Website Files**
You will need:

•	index.html → your homepage

•	style.css → for styling

 <img width="808" height="375" alt="Screenshot 2025-10-11 at 10 15 33" src="https://github.com/user-attachments/assets/aea16a4a-49c3-4b75-a9b8-ba00698ecf9e" />
<img width="808" height="375" alt="Screenshot 2025-10-11 at 10 16 17" src="https://github.com/user-attachments/assets/a977d8e0-c3c2-4f15-bbff-1926694731b1" />





## **📚 Step 2 -- Create an S3 Bucket**
1.	Log in to your AWS Management Console
2.	Search for S3 and open it
3.	Click Create bucket
   <img width="1437" height="747" alt="create" src="https://github.com/user-attachments/assets/a354dd8e-b099-440b-9e7b-66d27cbe1138" />

5.	Bucket name: lavie-cloud-portfolio
7.	Uncheck “Block all public access” so your website can be viewed by everyone
<img width="1437" height="747" alt="uncheck block" src="https://github.com/user-attachments/assets/e8789ddd-24ef-4c92-beac-97482adf383f" />
<img width="1437" height="747" alt="Screenshot 2025-10-11 at 10 18 56" src="https://github.com/user-attachments/assets/9e74e146-e753-4cfb-bf27-065c9733a3bd" />



9.	Confirm and click Create bucket

 <img width="1437" height="602" alt="create bucket" src="https://github.com/user-attachments/assets/16ef8ae1-582b-4797-b145-1f2452a6d8f0" />

 



## **📚 Step 3 -- Upload Your Website Files**
1.	Open your bucket
2.	Click Upload → Add files
3.	Add your index.html and style.css
4.	Click Upload
<img width="1425" height="475" alt="uploaded-files" src="https://github.com/user-attachments/assets/116b85f5-f30a-4ffe-8ec8-7f50d1133254" />

 
 


## **📚 Step 4 -- Enable Static Website Hosting**
1.	Go to the Properties tab
2.	Scroll to Static website hosting
3.	Click Edit, then:
o	Choose Enable
o	Select Host a static website
o	Type index.html under Index document
4.	Save changes
You will see a Website endpoint URL — that’s your live link!
Example: http://lavie-cloud-portfolio.s3-website-us-west-2.amazonaws.com/
<img width="1425" height="671" alt="static-hosting" src="https://github.com/user-attachments/assets/6796ca6c-cd53-4ec0-9858-a6c8019939a3" />

 
 

## **📚 Step 5 -- Make the Files Public**
1.	Go to the Permissions tab
2.	Scroll to Bucket policy → Edit
3.	Paste this JSON (replace your-bucket-name with your real bucket name):


   
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": ["s3:GetObject"],
      "Resource": ["arn:aws:s3::: your-bucket-name/*"]
    }
  ]
}


<img width="1425" height="710" alt="bucket-policy" src="https://github.com/user-attachments/assets/63065545-3372-49a7-8b79-d88958d8c911" />



4. Save changes — now your website is publicly accessible!

 <img width="1425" height="710" alt="bucket-policy" src="https://github.com/user-attachments/assets/4e88723b-f515-41a1-8542-2af67ccc7575" />

 

 
 ## **Website hosted preview**
 <img width="1425" height="435" alt="website-preview" src="https://github.com/user-attachments/assets/1288120c-2795-45f3-a6b7-fa65c0cfb97e" />


 
## **🧠 What I Learned**

•	How to create and configure an S3 bucket for static website hosting

•	How to upload and manage files in S3

•	How to write and apply bucket policies for public access

•	How to test and deploy a static site in the AWS Sandbox

•	Basics of IAM permissions and cloud security
 
## **🏁 Summary**

This project taught me the fundamentals of cloud storage, hosting, and permissions using Amazon S3.
It’s a foundational step toward mastering AWS Cloud Practitioner concepts and deploying production-ready web apps.

 
## **✍️ Author**

Made with 💻 by  Lavender Ila

🔗  [LinkedIn](https://www.linkedin.com/in/lavender-ila-1981142b0/)



 
