# Cloud-storage-setup

**COMPANY**:CODTECH IT SOLUTIONS

**NAME**:PARTH KULKARNI

**INTERN ID**:CTIS3903

**DOMAIN**:CLOUD COMPUTING

**DURATION**:16 WEEKS

**MENTOR**:NEELA SANTOSH

# DISCRIPTION OF TASK LIKE HOW YOU PERFORMED AND WHAT YOU HAVE DONE AND PASTE PICTURES OF OUTPUT 

**DISCRIPTION**: During my cloud computing internship, I successfully completed a core project focused on Cloud Storage Setup. The objective was to design, deploy, and secure a cloud storage environment using Amazon Web Services (AWS). This task involved not just the creation of a storage container (an S3 Bucket) but also the implementation of the Principle of Least Privilege through AWS Identity and Access Management (IAM).
Below is the detailed, step-by-step breakdown of how I executed this task, from initial setup to permission validation.
Phase 1: Setting Up the Amazon S3 Bucket
The first part of the project required creating a scalable storage location. Amazon S3 (Simple Storage Service) was chosen due to its reliability and industry-standard status.
Step 1: Accessing the Console
I began by navigating to the AWS Management Console. After logging in with my administrative credentials, I used the search bar to locate the S3 service. This dashboard serves as the central hub for managing all "buckets"—the fundamental containers for data in AWS.
Step 2: Bucket Configuration and Global Uniqueness
Upon clicking "Create bucket," I was prompted to provide a Bucket Name. A critical learning point here was that S3 bucket names must be globally unique across all AWS accounts worldwide. I chose a specific naming convention—intern-project-storage-2026-uniqueid—to ensure there were no conflicts. I also selected a Region (e.g., US East-1) to ensure the data was stored geographically close to the intended users for lower latency.
Step 3: Finalizing Creation
I kept the default settings for "Block Public Access" enabled. This is a security best practice that prevents the bucket from being accidentally exposed to the open internet. After reviewing the settings, I clicked "Create bucket." The bucket was now live and ready to host data.
Phase 2: Configuring IAM for Secure Access
Once the storage was ready, the next goal was to ensure that not everyone had full control over it. I needed to create a specific user with restricted access.
Step 4: Navigating to IAM
I searched for the IAM (Identity and Access Management) service in the AWS Console. This service is used to manage who can access what resources within the cloud environment.
Step 5: Creating a Restricted IAM User
In the IAM dashboard, I clicked on "Users" and then "Create user." I assigned a username (e.g., S3-Validator-User) and opted to provide the user with AWS Management Console access. I set a custom password and ensured that the user would be required to change this password upon their first login to maintain security integrity.
Step 6: Attaching Permission Policies
This was the most technical part of the setup. Instead of granting the user "Administrator" rights, I attached specific policies. To meet the task requirements, I used a combination of managed policies:
AmazonS3ReadOnlyAccess: This allows the user to view buckets and list the files inside them.
Custom Inline Policy: I added a specific permission (s3:CreateBucket) to allow the user to create new storage containers while explicitly excluding s3:DeleteObject permissions to prevent data loss.
Phase 3: Deployment and Verification
The final phase involved "testing" the setup to ensure the permissions were working exactly as intended.
Step 7: Testing the IAM User Access
I copied the unique IAM Sign-in URL provided in the user summary. I opened a private browser tab to avoid session conflicts and logged in as the new user.
Step 8: Validating the "Read-Only" and "Delete Protection"
To verify the configuration:
View Task: I successfully navigated to S3 and could see the bucket created in Phase 1.
Upload Task: I uploaded a sample text file to the bucket.
Delete Task (The Fail Test): I attempted to delete the file I just uploaded. As expected, the system returned an "Access Denied" error.
Conclusion of the Deliverable
The project concluded with a fully functional S3 bucket and a verified IAM user. This exercise demonstrated the importance of cloud security; even if a user has access to a service, their actions can be strictly governed to prevent unauthorized deletions or data breaches. This "ReadOnly" with "Create" privilege configuration ensures that an intern or junior developer can contribute to the infrastructure without the risk of accidentally destroying existing data.

**OUTPUT**

https://github.com/Parth-007-git/Cloud-storage-setup/issues/1
