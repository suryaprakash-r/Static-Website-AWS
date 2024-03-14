<b>Procedure to Host a Static Web Page in AWS </b><br />
<b>Create an IAM Role for S3</b>
![Screenshot 2024-03-14 130518](https://github.com/suryaprakash-r/Static-Website-AWS/assets/129744688/18594e40-eb2b-45d1-b4d8-7ee1528fc7eb)
<b>Create an S3 Bucket for file upload like index.html</b>
![Screenshot 2024-03-14 130559](https://github.com/suryaprakash-r/Static-Website-AWS/assets/129744688/63b34812-8828-48f0-80b6-5e6732deff9f)
![Screenshot 2024-03-14 130623](https://github.com/suryaprakash-r/Static-Website-AWS/assets/129744688/1ed94f01-cbb0-456a-91d3-42a183165883)
<b>Create an EC2 Instance and attach IAM Role created for S3 access</b>
![Screenshot 2024-03-14 130645](https://github.com/suryaprakash-r/Static-Website-AWS/assets/129744688/821e27b4-519a-4c17-9bed-ad6dd77d6c43)
<br/><br/>
<b>Add user data while creating an EC2 Intance</b><br/>
<br/>
#!/bin/bash<br />
sudo yum -y update<br />
sudo yum -y install httpd<br />
sudo systemctl start httpd<br />
sudo systemctl enable httpd<br />
<br/>
<b>Connect instance with SSH or Web</b>
<b>Here is the command to copy the file from S3 Bucket to host a static web page</b>
![Screenshot 2024-03-14 130720](https://github.com/suryaprakash-r/Static-Website-AWS/assets/129744688/f6881832-8802-4eeb-abcb-30d945cbe37a)
<b>The final output for Static web site </b>
![Screenshot 2024-03-14 130822](https://github.com/suryaprakash-r/Static-Website-AWS/assets/129744688/65943320-7686-4251-a564-12119f4886b2)
