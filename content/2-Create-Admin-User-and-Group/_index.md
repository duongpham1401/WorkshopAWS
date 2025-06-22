---
title : "Create Admin Group and Admin User"
date : "2025-06-19T06:49:25.364"
weight : 2
chapter : false
pre : " <b> 2. </b> "
---
## Creating an Admin Group

1. **Log in to the Dashboard** on the [AWS Web Service page](https://aws.amazon.com/)
> **Note:** Before entering the exercise, we need to choose the region to do the practice exercise, here we should choose the Singapore region (because it will help us in the process of doing the exercise smoothly and without lag)

   ![AWS IAM](/images/01/11002.png?featherlight=false&width=90pc)

2. Click on the search bar on aws and search for **IAM Manage access to AWS resources**

   ![AWS IAM](/images/01/11001.png?featherlight=false&width=90pc)

3. In the left window, click on **User group** then select **create group**

   ![AWS IAM](/images/01/11003.png?featherlight=false&width=90pc)

4. Under **User group name**, enter the Group name (Example: *AdminGroup, GroupAdmin, AdminAWS,...*) and scroll down

   ![AWS IAM](/images/01/11004.png?featherlight=false&width=90pc)

5. In the **Attach permissions policies - Optional** section, type **AdministratorAccesss** in the search bar (as in step 1) and click **AdministratorAccesss**. Finally, select **Create user Group** (in step 2).

   ![AWS IAM](/images/01/11005.png?featherlight=false&width=90pc)

6. Finish creating **admin group**.

   ![AWS IAM](/images/01/11006.png?featherlight=false&width=90pc)


#### Create Admin User

1. In the left navigation bar, select **Users** then select **Add User**

   ![AWS IAM](/images/02/11007.png?featherlight=false&width=90pc)

2. Enter the User name (Example: *AdminUser*).
+ Click **Provide user access to the AWS Management Console - optional** *(As shown in step 2)*
+ A new window will appear and click **i want to create an IAM user***(As shown in step 3)*
+ Click **Custom password** then type a password of your choice (note: you must remember this password for future logins) Or you can leave the password random *(as shown in the default)*
+ Uncheck **User must create a new password...**.
+ Click **Next**.

   ![AWS IAM](/images/02/11008.png?featherlight=false&width=90pc)

> **Note:** By selecting **AWS Management Console access**, you have just allowed the IAM User to access AWS through the AWS web console. Unchecking the **User must create a new password...** option allows the user to log in to the IAM User for the first time without having to create a new password.

3. Click the **Add user to group** tab and click the **AdminGroup** that we created earlier.

   ![AWS IAM](/images/02/11009.png?featherlight=false&width=90pc)

4. Click **Next:Tags**

- Tags are an optional option to organize, track, or control user access, so you can add tags or not.

5. Click **Next:Review**.

   ![AWS IAM](/images/02/11009.png?featherlight=false&width=90pc)

6. Check the information and select **Create user**

   ![AWS IAM](/images/02/11010.png?featherlight=false&width=90pc)

7. After completing the user creation. You can download .csv to store the Access key.
   ![AWS IAM](/images/02/11011.png?featherlight=false&width=90pc)
*(You can download the Access key after creating **Admin user**)*
   ![AWS IAM](/images/02/11012.png?featherlight=false&width=90pc)

8. Successfully created admin user.

   ![AWS IAM](/images/02/11013.png?featherlight=false&width=90pc)

9. Check user details.

   ![AWS IAM](/images/02/11014.png?featherlight=false&width=90pc)

> **Note:** After creating a user, you will see a dialog box to download access key and secret key information. This information is used to perform **Programmatic access** to AWS resources via **AWS CLI** and **AWS SDK**. We will not use it for now.


#### Login to AdminUser

1. Return to the main AWS window, then select the IAM service again, and select **Users** on the left sidebar.

2. Click on the name of the IAM User you just selected.

3. In the **Summary** section, select the **Security credentials** tab. Look at the **Summary: Console sign-in link** line and copy the link next to it. This is the link you use to sign in to the IAM User.

   ![AWS IAM](/images/03/11015.png?featherlight=false&width=90pc)

4. Open an incognito tab of the browser you are using and paste the link into the search bar.

   ![AWS IAM](/images/03/11016.png?featherlight=false&width=90pc)

> **Note:** *Logging in with an anonymous tab allows you to log in to AWS with an IAM User without having to log out of the root user in the main tab.*

5. Enter the correct IAM User name and password that you entered in the **create IAM User** section above. Click **sign in**.

>**Tip:** *If you forget your account password, you can go back to the downloaded excel file named **download.csv** in the IAM user creation section*

   ![AWS IAM](/images/03/11017.png?featherlight=false&width=90pc)

6. After successfully accessing your account under the name of an IAM User **AdminUser**.

   ![AWS IAM](/images/03/11018.png?featherlight=false&width=90pc)


## Creating Access Key for AWS Root User

### Minimum Required Permissions

To perform the following steps, you need at least the following IAM (Identity and Access Management) permissions:

- You must log in as the root user of AWS, which does not require any additional IAM permissions. These steps cannot be performed as an IAM user or a role.

- Use the email address and password of your AWS account to sign in to the AWS Management Console as the root user.

- In the top-right corner of the console, select your account name or number, then choose "Security Credentials".

- Under "Access keys," select "Create access key." If this option is unavailable, it means you have the maximum number of access keys. You must delete one of the existing access keys before creating a new one. For more information, see IAM Object Quotas in the IAM User Guide.

- On the "Alternatives to root user access keys" page, consider security recommendations. To proceed, check the box and then select "Create access key."

- On the "Retrieve access key" page, your Access Key ID will be displayed.

- Under the "Secret access key" section, select "Show," then copy the Access Key ID and Secret Key from your browser window and paste them into a secure location. Alternatively, you can select "Download .csv file" to download a file named "rootkey.csv" containing the Access Key ID and Secret Key. Keep the file in a secure location.

- Select "Done." When you no longer need the access key, we recommend either deleting it or at least considering disabling it to prevent misuse.

> Note: These steps apply only to the root user account on AWS. For IAM users or roles, the process of creating and managing access keys may differ.

## Revoking Access Key for Root User on AWS

### Minimum Permissions
To perform the following steps, you must have at least the following IAM (Identity and Access Management) permissions:

- You must be logged in as the root user of your AWS account, this does not require any additional AWS Identity and Access Management (IAM) permissions. You cannot perform these steps as an IAM user or a role.
- Use the email address and password of your AWS account to sign in to the AWS Management Console as the root user.
- In the top-right corner of the console, select your account name or number, then choose **Security Credentials**.
- Under **Access keys**, select the access key you wish to delete, then in the **Actions** section, choose **Delete**.

> **Note**
> Alternatively, you can choose to **Deactivate** an access key instead of permanently deleting it. This allows you to continue using it in the future without changing both the key ID and secret key. While the key is deactivated, any requests using it in AWS API requests will fail with an "access denied" error.
>
> In the **Delete <access key ID>** dialog, select **Deactivate**, enter the access key ID to confirm your intention to delete it, then choose **Delete**.
