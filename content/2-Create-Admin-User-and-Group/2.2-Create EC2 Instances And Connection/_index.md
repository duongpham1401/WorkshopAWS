---
title : "Create an EC2 Instances And Connection"
date : "2025-06-19T06:49:25.364"
weight : 2
chapter : false
pre : " <b> 2.2 </b> "
---

## Create a Security Group

1. **Log in to the Console** on the [AWS Web Service page](https://aws.amazon.com/)

2. Click on the search bar on aws and search for **VPC Isolated Cloud Resources**

    ![AWS SG](/images/2/12001.png?featherlight=false&width=90pc)

3. Look at the left window and select **Security group** in the **Security** section (*as shown in step 1*) and select **create Security group** (as shown in step 2)

    ![AWS VPC](/images/3/13002.png?featherlight=false&width=90pc)

4. Right below **Security group name**, name the security group: *(eg: SGR-workshop,SG-Public,....)*

   + Enter a description for security group
   + Select the VPC that you have created in previous articles (or recreate it on the [AWS Web Service page](https://ap-southeast-1.console.aws.amazon.com/vpcconsole/home?region=ap-southeast-1#vpcs:))
   + In the Inbound rules section, in **type** select **SSH** and **Source** select **My IP** (as in step 3)
   + Next, add a rule at the first **type** select **ALL ICMP-IPV4** and select **Source** as **Anywhere IPV4** (as in step 4)
   + Next, select to create **Security group**

    ![AWS SG](/images/3/13003.png?featherlight=false&width=90pc)

5. When successfully creating security public

    ![AWS SG](/images/3/13004.png?featherlight=false&width=90pc)

6. Continue like that to create another **Private security group**

   + Enter a description for the security group

   + Select the VPC that you have created in previous articles (or create it again on the [AWS Web Service page](https://ap-southeast-1.console.aws.amazon.com/vpcconsole/home?region=ap-southeast-1#vpcs:))
   + In the Inbound rules section, in **type** select **SSH** and **Source** select **Security group (created earlier)** (as in step 3)
   **Note:** **Source** in this step can be assigned directly to *Publicsubnet*

   + Next, add a rule at the first **type** select **ALL ICMP-IPV4** and select **Source** as **Anywhere IPV4** (as shown in step 4)
   + Next select create **Security group**

    ![AWS SG](/images/3/13005.png?featherlight=false&width=90pc)

7. After successfully creating another **Private security group**

    ![AWS SG](/images/3/13006.png?featherlight=false&width=90pc)

8. Complete creating a **Public security group** and **Private security group**

    ![AWS SG](/images/3/13007.png?featherlight=false&width=90pc)

## Create an EC2 server

1. **Log in to the Console** on the [AWS Web Service page](https://aws.amazon.com/)

2. Click on the search bar on aws and search for **EC2**

    ![AWS EC2](/images/3/13001.png?featherlight=false&width=90pc)

3. Look at the left window and select **Instances** in the **Instances** section (*as shown in step 1*) and select **Create Launch instances** (as shown in step 2)

    ![AWS EC2](/images/3/13008.png?featherlight=false&width=90pc)

4. Right below **Name and tag**, name the Launch instances: *(eg: EC2 Public,EC2 Private,....)*

   + Right at **Amazon Machine Image**, select **Amazon linux 2 AMI(HVM)**
   + Next create **Key Pair** name the keypair and use the keypair in .pem file format, then click create a keypair

   ![AWS SG](/images/3/13009.png?featherlight=false&width=90pc)
   ![AWS SG](/images/3/13010.png?featherlight=false&width=90pc)

5. Edit **Network settings** select VPC and Public subnet created before *(in step 1 and step 2)*

   + Check **Auto-assign public IP** in **Enable** status
   + Select **Security existing security group**, in **Common security group** select **Public security** *(as in step 3)*
   + Check again and select **create launch instance**

   ![AWS SG](/images/3/13011.png?featherlight=false&width=90pc)

6. When successfully creating EC2 public

    ![AWS SG](/images/3/13012.png?featherlight=false&width=90pc)

7. Continue like **Public EC2** to create another **EC2 Private**

    + Right below **Name and tag**, name the Launch instances: *(eg: EC2 Public,EC2 Private,....)*
    + Right at **Amazon Machine Image**, select **Amazon linux 2 AMI(HVM)**
    + Next, create **Key Pair**, name the keypair and use the keypair in .pem file format, then click create a keypair

    ![AWS SG](/images/3/13013.png?featherlight=false&width=90pc)
    ![AWS SG](/images/3/13010.png?featherlight=false&width=90pc)

8. Edit **Network settings** select VPC and Public subnet created before

   + Check **Auto-assign public IP** in **Disable** state
   **Note:** Because it is **Private EC2**, it must be in **Disable** state
   + Select **Security existing security group**, in **Common security group** select **Private security**
   + Check again and select **create launch instance**

    ![AWS SG](/images/3/13014.png?featherlight=false&width=90pc)

1. Create **Private EC2** successfully

    ![AWS SG](/images/3/13015.png?featherlight=false&width=90pc)

11. After creating and launching the two **EC2 Public** and **Private EC2** succeeded 

    ![AWS SG](/images/3/13016.png?featherlight=false&width=90pc)

12. Use **MobaXterm** to test the connection 

    ![AWS SG](/images/3/13018.png?featherlight=false&width=50pc) 
    ![AWS SG](/images/3/13019.png?featherlight=false&width=50pc)