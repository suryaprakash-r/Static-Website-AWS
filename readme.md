#!/bin/bash <br />
sudo yum -y update <br />
sudo yum -y install httpd <br />
sudo systemctl start httpd <br />
sudo systemctl enable httpd <br />
