# CS-4843-Assignment-1
Joseph Miller
jfw445

Some very basic HTML for an S3 bucket and cloudfront pages through AWS.
https://d1m2gt2zuskano.cloudfront.net

Files:
index.html:
  This file is my main page, it contains some text and Links to my other 4 pages
about.html:
  This page contains a little blurb about me, and a link back to the index.html page
contact.html:
  This contains my contact information and a link back to the index.html page
media.html:
  This page contains my image and video required for the assignment. It also contains a link back to index.html
assignment_1.html:
  This page contains information relevant to assignment_1 and a link back to index.html

The two media objects are supposed to be in the following files
Folders 
image/
  trollface.jpg
 video
  playback.mp4

Bucket Policy
{
    "Version": "2008-10-17",
    "Id": "PolicyForCloudFrontPrivateContent",
    "Statement": [
        {
            "Sid": "1",
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:iam::cloudfront:user/CloudFront Origin Access Identity E2CTFP379DQ325"
            },
            "Action": "s3:GetObject",
            "Resource": "arn:aws:s3:::my-cs-4843-webserver/*"
        }
    ]
}



