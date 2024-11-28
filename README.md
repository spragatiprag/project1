# project1

Deploy a static React app (Use AWS S3 to deploy a static React app)
===================================================================
step 1 :Build your react app .Have a react project in  hand and go to the react project directory
        $ npm run build

step 2 :create an s3 bucket
step 3 :configure s3 , properties-static web hosting,index,error.html
step 4 :upload /build files to s3 bucket
step 5 :set public access permission tab 
        set policy 
          {
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::your-bucket-name/*"
    }
  ]
}

step 6 : Access react app by copying the url 

optional : Set Up a Custom Domain with Route 53 (or another DNS provider)
Optional : Use AWS CloudFront for Faster Global Delivery



Automation: Use Terraform to automate the deployment and set up AWS CloudFront for CDN.
======================================================================================
