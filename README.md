
# S3 Static Website Hosting Project

## Files
- index.html : Home page
- error.html : Error page
- css/style.css : Styling
- js/script.js : JavaScript

## Steps to Host on AWS S3
1. Create an S3 bucket (unique name)
2. Disable 'Block all public access'
3. Enable Static Website Hosting
4. Upload all files
5. Add Bucket Policy for public access

## Bucket Policy Example
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}
