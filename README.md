<div align="center">
 
  <h1>  Vertical Scaling of EBS Volume for a Linux VM </h1>

</div>
 
<div align="left">
 
  ### `Description:` Your company is experiencing business growth where solution deployment is happening with limited resources. In this case, the vertical scalability feature of AWS can be used to create a cost-optimised architecture. 

  ### `Tools required:` AWS account
  ### `Prerequisites:` A running EC2 Instance
</div>

#


### Steps to be followed:
 1. Creating an EC2 Instance
 2. Identifying the EBS volume that is created
 3. Creating a snapshot
 4. Creating a new volume
 5. Detaching the existing volume from the EC2 Instance
 6. Attaching a new volume to the EC2 Instance

## Step 1: Creating an EC2 Instance

  <li> 1.1  Navigate to the AWS Management Console, search for EC2, and click on Launch Instances as shown in the below screenshots:</li>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m1.png"></img>
  <li> 1.2 Enter a name for the Instance. </li> 

  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m2.png"></img>
  
