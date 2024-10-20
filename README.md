<p align="center">
<img src="https://imgur.com/2HDDgj5.jpeg" alt="AWS logo"/>
</p>

<h1>Lab - Create an AWS environment and configure IAM roles and policies.
 </h1>

- Simple Steps and Description:
  
In this project, I set up an AWS environment, focusing on creating IAM roles and users to manage secure access to resources like EC2 and S3. This forms the foundational cloud security needed for effective resource management and user access control. This project focuses on building foundational cloud security and user management skills by configuring Identity and Access Management (IAM) within an AWS environment, and setting up secure access controls for users and roles, which are essential for protecting resources and managing permissions effectively.

Project Goals:
- Create an IAM Role for EC2 instances to interact with S3.
- Configure IAM users with proper access policies.

Steps:
Create an AWS Account
Navigate to IAM
Understand Identity and Access Management.
Create IAM Roles
Example: EC2_S3_FullAccess_Role for secure access.
Create IAM Users
Example: AdminGroup and user assignment.
Best Practices
Set up MFA and least privilege.
Resource Cleanup

Tools:
- AWS Management Console
- IAM Dashboard
- Key Learnings:
- Effective cloud resource security management.
- Hands-on experience with IAM roles and user permissions.
  
Part 1: Create an AWS Account or Sign in 

- If you do not already have an AWS account, you’ll need to create one. If you have an account, log in to your AWS Management Console.
- Go to the AWS sign-up page and follow the instructions to create your account.
- You will need to provide a payment method, but most tasks are eligible under the AWS Free Tier, so you can avoid charges for basic usage.
- Once you’ve signed in to your AWS console, you can begin setting up your environment.


Part 2: Navigate to IAM (Identity and Access Management)

Identity and Access Management (IAM) is the AWS service that allows you to control access to AWS resources securely.

- From the AWS Management Console, type IAM in the search bar at the top and select IAM from the dropdown.
- This will open the IAM Dashboard, where you can manage users, groups, roles, and policies.
<img src="https://imgur.com/YmhWs72.jpeg" alt="AWS logo"/>

What is IAM?
- IAM helps you manage access to AWS services and resources securely. You create and manage AWS users, roles, and permissions to ensure that the right people have the right access to your cloud resources.
<img src="https://imgur.com/2b8q072.jpeg" alt="AWS logo"/>

Part 3: Create IAM Roles

IAM roles are critical when you need to grant AWS services permissions to interact with other services securely. For this project, we’ll create roles that allow specific services, like EC2, to interact with S3 buckets, for example.

Create a Role for EC2 Instances:
- In the IAM Dashboard, click on Roles on the left sidebar.
- Click Create Role.
- Select AWS Service under the "Trusted Entity Type."
- Choose EC2 from the list of services, as we will create a role that allows EC2 instances to interact with S3.
  <img src="https://imgur.com/GnzkwSb.jpeg" alt="AWS logo"/>
- Click Next: Permissions.

Attach a Policy to the Role:
- AWS will ask you to attach a policy to this role. For this project, search for and select the AmazonS3FullAccess policy. This policy gives the role full access to S3 buckets.
- Click Next: Tags. (Tags are optional, so you can skip this for now.)
- Click Next: Review.
- Name the role something descriptive, like EC2_S3_FullAccess_Role.
<img src="https://imgur.com/vUOkuMb.jpeg" alt="AWS logo"/>
- Click Create Role.

Your role is now ready and can be assigned to an EC2 instance. This allows the instance to access and manipulate S3 buckets without needing to store AWS credentials on the instance itself—improving security.

Step 4: Create IAM Users

IAM users are identities that allow individuals or systems to access your AWS resources. These users will be assigned specific permissions based on their roles or responsibilities.

Create a New User:
- Go back to the IAM dashboard, click on Users in the left-hand sidebar, then click Add User.
(Name your user something descriptive, like AdminUser or ReadOnlyUser, depending on what access they should have.)

- For Access Type, select Programmatic access if the user will be accessing AWS via the CLI or API, or AWS Management Console access if they will be using the web interface.
<img src="https://imgur.com/pbQ0dk9.jpeg" alt="AWS logo"/>

For this project, let’s select AWS Management Console access and set a custom password.
- Click Next: Permissions.

Assign User Permissions:
- You can assign permissions to the user in different ways. For this project, we’ll create a new group for easy permission management.
<img src="https://imgur.com/YwFy81b.jpeg" alt="AWS logo"/>
<img src="https://imgur.com/39sOOlm.jpeg" alt="AWS logo"/>

Click Create Group and name the group something appropriate, like AdminGroup or ReadOnlyGroup, depending on your user’s needs.

Attach a permission policy to the group. You can search for policies like:

- AdministratorAccess: Grants full access to all AWS resources.
- AmazonS3ReadOnlyAccess: Grants read-only access to all S3 buckets.
- Click Create Group.
<img src="https://imgur.com/hjtyZzP.jpeg" alt="AWS logo"/>
<img src="https://imgur.com/zt3aOMH.jpeg" alt="AWS logo"/>

Assign your user to the newly created group and click Next: Tags (you can skip this step).

- Click Next: Review and then Create User.

AWS will give you a summary with the user’s credentials, including an option to download them. You’ll need these credentials to log in as that user.

Step 5: Clean Up Resources
To avoid incurring costs after completing this project, remember to clean up the resources you’ve created.

- Terminate EC2 instances: Go to the EC2 Dashboard, select your running instances, and click Terminate.
- Delete IAM Users/Roles: If this was a test project, you can go to IAM > Users and IAM > Roles to delete the users and roles you created.
- Delete S3 Buckets: Go to the S3 Console and delete any test buckets you created.
<img src="https://imgur.com/TAiRuRk.jpeg" alt="AWS logo"/>

Summary of Project Outcomes
-By completing this project, you’ll gain practical experience in:

- Setting up and managing users, roles, and permissions in AWS using IAM.
- Assigning appropriate policies to users and roles.
- Configuring access controls for AWS services like EC2 and S3.
- Understanding the security benefits of IAM roles, especially when avoiding hardcoded credentials.
