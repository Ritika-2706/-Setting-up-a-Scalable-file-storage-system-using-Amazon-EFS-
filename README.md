 # SETTING UP A SCALABLE FILE STORAGE SYSTEM USING AMAZON ELASTIC FILE SYSTEM
## AIM
To  setting up a scalable file storage system using Amazon Elastic File System (EFS) for two EC2 instances in different availability zones. 
## PROBLEM STATEMENT
This experiment demonstrates how to configure Amazon EFS to provide a shared storage solution for two Linux EC2 instances across different availability zones, enabling easy data sharing. The aim is to ensure both instances can mount and access the EFS file system and validate data consistency across instances.

## ALGORITHM
 ### Steps 1: 
 Create two EC2 instances in different availability zones.
 ### Steps 2: 
 Set up a security group that allows necessary communication between the instances and EFS.
 ### Steps 3: 
 Create an EFS file system and mount it to both EC2 instances.
 ### Steps 4: 
 Ensure that the EC2 instances can access the file system and share data between them.

## COMMANDS
### EC2 Instance 1
     sudo su
     yum install httpd -y
     yum install -y amazon-efs-utils
     mount -t efs -o tls fs-064645ac116a12816:/ /var/www/html
     cd /var/www/html
     vi file  # Create a file and add some text
### EC2 Instance 2
    sudo su
    yum install httpd -y
    yum install -y amazon-efs-utils
     mount -t efs -o tls fs-064645ac116a12816:/ /var/www/html
     cd /var/www/html
      ls
      cat file  # Verify shared access by reading content created in Instance 1

## OUTPUT
### REG NUMBER: 212221240046
### NAME: Ritika S
 
![p1](https://github.com/user-attachments/assets/20d2d5c0-8583-48ea-bbce-c536a1ed8579)
![p2](https://github.com/user-attachments/assets/fba8cbb7-7963-478f-b927-9f30568aed14)
![Screenshot (10)](https://github.com/user-attachments/assets/bc750429-614f-4437-b0ed-0eaa904ff951)
![Screenshot (9)](https://github.com/user-attachments/assets/32a0b827-95ee-4313-89c4-9df5e6e57ba5)

## RESULT
Successfully set up a scalable file storage system using Amazon EFS shared between two Linux EC2 instances in different availability zones, enabling consistent data sharing.

  


