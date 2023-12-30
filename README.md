# Build and Launch a website on Amazon S3
![Blank diagram-4](https://github.com/julien-muke/static_website_aws/assets/110755734/1aeda0f8-11fb-47e2-b1c0-5165019d6195)


### [🌐 LIVE SITE](https://muke-demo-s3.s3.amazonaws.com/static_website_aws/index.html)

## Introduction
Let's build together! In this tutorial, we will be deploying a beginner-friendly static website on AWS.

Launching a website is one of the most important thing for a company either it is a startup or a well established company. Let’s see how you can host a website using AWS with some easy steps.

## Let's get started
Let’s see how you can host a website using AWS with some easy steps:

- Step 1: Gathering the Basics:
        The most basic step is to first have a working AWS account and your front end code (.html file) which will be the content of your website. 
        Open your terminal and run the following command to clone the repository:

   ```bash
   git clone https://github.com/julien-muke/static_website_aws.git
   ```

- Step 2: Create a S3 Bucket of your website
        To keep things simple we will be using only one AWS service to host our website that is AWS S3. AWS S3 in an storage service where all files are stored in S3 Buckets.

- Step 3: Uploading file into your S3 Bucket
        Once the bucket is created, now it’s time to upload the .html file onto it. For this click on blue Upload button on the top right.

- Step 4: Configure the settings of your S3 Bucket
        

Next click on Permission tab, Now you’ll need to click on the “Bucket Policy” subsection. Here, you’ll be prompted to create a JSON object that contains the details of your bucket’s access permission policy.

This part can be confusing. For now, I’ll just give you the JSON that will grant full public access to the files in your bucket. This will make the website publicly accessible.

Paste this into the bucket policy editor shown above:

    {   "Version":"2012-10-17",
            "Statement":
             [{
                "Sid":"PublicReadForGetBucketObjects",
                "Effect":"Allow","Principal":"*",
                "Action":"s3:GetObject",
                "Resource":"arn:aws:s3:::YOUR-BUCKET-NAME/*"
            }]
     }
    
        
- Step 5: Hosting your Website
          To access your site, go back to the “Overview” tab on S3 and click on your index document . You’ll get a slide-in menu with the link on your website.

### [🌐 LIVE SITE](https://muke-demo-s3.s3.amazonaws.com/static_website_aws/index.html)

        




