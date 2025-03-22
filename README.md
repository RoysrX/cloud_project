# cloud_project

Step 1: Create a Simple Blogging Website
Since we're using only HTML and CSS, we’ll create a basic blog with a homepage and individual posts.

Step 2: Upload Website to AWS S3
2.1 Create an S3 Bucket
Go to AWS S3 Console
Click Create Bucket.
Give it a unique name (e.g., my-html-blog).
Disable Block Public Access (since CloudFront will serve it).
2.2 Upload the Website Files
Open your S3 bucket.
Go to Objects → Click Upload.
Upload index.html, post1.html, and style.css.
2.3 Enable Static Website Hosting
In S3, go to Properties → Static Website Hosting.
Enable Static Website Hosting.
Set index document as index.html.
Note the S3 website endpoint URL.

Step 3: Set Up CloudFront
3.1 Create a CloudFront Distribution
Open AWS CloudFront Console
Click Create Distribution.
In Origin Settings:
Origin Domain Name: Select your S3 bucket.
Viewer Protocol Policy: Choose Redirect HTTP to HTTPS.
Set Default Root Object to index.html.
Click Create Distribution.


Step 4: Access Your Blog
Once CloudFront finishes deploying (~5-10 mins).
Open the CloudFront Domain Name (e.g., d123xyz.cloudfront.net).
🎉 Your blog is now live!
