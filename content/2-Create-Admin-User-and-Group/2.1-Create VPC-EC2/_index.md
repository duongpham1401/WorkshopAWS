---
title : "Create VPC Resource Map"
date : "2025-06-19T06:49:25.364"
weight : 1
chapter : false
pre : " <b> 2.1 </b> "
---

## Create a VPC (Virtual Private Server)

1. **Log in to the Control Panel** on the [AWS Web Service page](https://aws.amazon.com/)

2. Click on the search bar on aws and search **VPC Isolated Cloud Resources**

![AWS VPC](/images/2/12001.png?featherlight=false&width=90pc)

3. Look at the left window and select **Yours VPS** (*as shown in step 1*) and select **Creat VPC** (as shown in step 2)

![AWS VPC](/images/2/12002.png?featherlight=false&width=90pc)

4. Select **VPC Only** in the first section

+ In the **Name tag** section we can name the VPC (*eg: VPC 1, VPC 2,...*) (in step 1 as shown in the image)
+ Then select IPV4 CIDR *(note that CIDR must be between /26 and /28)* (in step 2)
+ IPV6 CIDR leave it as default (not needed yet)
+ After the steps, click **Create VPC**

![AWS VPC](/images/2/12003.png?featherlight=false&width=90pc)

5. Virtual server creation successful
![AWS VPC](/images/2/12004.png?featherlight=false&width=90pc)

## Create Subnets

1. **Log in to the Control Panel** on the [AWS Web Service page](https://aws.amazon.com/)
2. Click on the search bar on aws and search for **VPC Isolated Cloud Resources**

![AWS Subnet](/images/2/12001.png?featherlight=false&width=90pc)

3. Look at the left window, select **Subnets** (*as shown in step 1*) and select **Create Subnets** (as shown in step 2)

![AWS Subnet](/images/2/12005.png?featherlight=false&width=90pc)
4. When creating a subnet, we must re-select the **VPC ID** we just created
+ Name the subnet *(eg: Public subnet 1, public subnet 2,...)*
+ Then we select **Availability Zone**
+ Based on IPV4 CIDR, we select IPV4 subnet CIDR
+ Next, select **Create subnet**

![AWS Subnet](/images/2/12006.png?featherlight=false&width=90pc)

5. After successfully creating **Public Subnets 1**

![AWS Subnet](/images/2/12007.png?featherlight=false&width=90pc)

6. Similarly create 1 more **Public Subnets 2**

![AWS Subnet](/images/2/12009.png?featherlight=false&width=90pc)

*Complete creating **Public sbunet 2***
![AWS Subnet](/images/2/12010.png?featherlight=false&width=90pc)

7. Similar to **Public subnet** we create 2 more **Private subnet**

*Private Subnet 1*
![AWS Subnet](/images/2/12009.png?featherlight=false&width=90pc)

*Private Subnet 2*
![AWS Subnet](/images/2/12010.png?featherlight=false&width=90pc)

8. After completing the creation of 4 subnets

![AWS Subnet](/images/2/12013.png?featherlight=false&width=90pc)

9. Next we will edit 2 **public subnet 1** and **public subnet 2**
+ First select **Public Subnet 1** to edit
+ Select **Action** and select **edit subnets settings**
+ Next select **Enable auto-assign public IPV4 address**
+ Then select **Save information**
> **Note:** Edit to automatically allocate ID address

![AWS Subnet](/images/2/12014.png?featherlight=false&width=90pc)
![AWS Subnet](/images/2/12016.png?featherlight=false&width=90pc)

11. After successful editing, there will be a green notification line

![AWS Subnet](/images/2/12013.png?featherlight=false&width=90pc)

12. Similarly, we edit with **Public subnet 2**

![AWS Subnet](/images/2/12017.png?featherlight=false&width=90pc)

*After successfully changing public subnet 2*

![AWS Subnet](/images/2/12018.png?featherlight=false&width=90pc)

## Create an Internet Gateway

1. **Log in to the Dashboard** on the [AWS Web Service page](https://aws.amazon.com/)

2. Click on the search bar on aws and search for **VPC Isolated Cloud Resources**

![AWS internet gateways](/images/2/12001.png?featherlight=false&width=90pc)

3. Look at the left window and select **Internet gateways** (*as shown in step 1*) and select **create internet gateways** (as shown in step 2)

![AWS internet gateways](/images/2/12019.png?featherlight=false&width=90pc)

4. Name the **internet gateways** *(eg: internet-gateways,internetGW!,....)*
+ Select create **internet gateways**

![AWS internet gateways](/images/2/12020.png?featherlight=false&width=90pc)

5. After successfully creating **internet gateway**

![AWS internet gateways](/images/2/12021.png?featherlight=false&width=90pc)

![AWS internet gateways](/images/2/12022.png?featherlight=false&width=90pc)

## Create a Router Table
1. **Log in to the Dashboard** on the [AWS Web Service page](https://aws.amazon.com/)
2. Click on the search bar on aws and search **VPC Isolated Cloud Resources**

![AWS Router Table](/images/2/12001.png?featherlight=false&width=90pc)

3. Look at the left window and select **Route Table** (*as shown in step 1*) and click **create route table** (as shown in step 2)

![AWS Router Table](/images/2/12023.png?featherlight=false&width=90pc)

4. After successfully creating, the screen will look like this:

![AWS Router Table](/images/2/12024.png?featherlight=false&width=90pc)

5. Edit route table
+ Select the route to edit
+ Select **local** and **Internet gateway** in the target section
+ Then select **Save changes**

![AWS Router Table](/images/2/12025.png?featherlight=false&width=90pc)