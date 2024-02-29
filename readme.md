#!/bin/bash<br />
sudo yum -y update<br />
sudo yum -y install httpd<br />
sudo systemctl start httpd<br />
sudo systemctl enable httpd<br />

<b>Procedure to Host a Web Page in AWS </b>
Step-1: Created an S3 Bucket<br />
Step-2: Upload files like inded.html, style.css etc., After uploading files copy the S3 Bucket location.<br />
Step-3: Hereafter, create a role in IAM for accessing S3 Bucket in Instance<br />
Step-4: The role created for S3 full access<br />
Step-5: Then, create an EC2 Instance with their requirements and user data. If you want to know about the user data you can check on my GitHub Repo<br />
Step-6: Connect the instance using SSH connectivity or other methods.<br />
Step-7: Check the S3 buckets in usign the command "aws s3 ls" !If your not attached the IAM S3 role on instance the command will not be working.<br />
Step-8: Then, change the Directory to cd /var/www/html/<br />
Step-9: Copy the files from S3 Bucket to the current location using the command sudo aws s3 cp --recursive s3bucketlocation .<br />
Step-10: After the copying the files from S3 to the location go to the EC2 Instance and copy the Local IP and paste it in new tab<br />
