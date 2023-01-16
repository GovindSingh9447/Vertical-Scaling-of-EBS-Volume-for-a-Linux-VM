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

  <li> Navigate to the AWS Management Console, search for EC2, and click on Launch Instances as shown in the below screenshots:</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m1.png"></img>
  <br>
  <li> Enter a name for the Instance. </li> 
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m2.png"></img>
  <br>
  <li> Select an Amazon Linux VM.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m3.png"></img>
  <br>
  <li> Select the instance type.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m4.png"></img>
  <br>
  <li> Create a key pair if one has not been created already.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m5.png"></img>
  <br>
  <li> The EC2 Instance has been successfully launched.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m6.png"></img>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m7.png"></img>
  
  
## Step 2: Identifying the EBS volume that is createde

  <li>	Navigate to the Elastic Block Store and click on Volumes.</li>
  <br>
  <img  width="50%" height="50%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m8.png"></img>
  <br> 
   <li>	Identify the Volume and edit the Volume name as shown in the below screenshot:</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m9.png"></img>
  <br> 
   
 
 ## Step 3: Creating a snapshot

  <li>	Create a snapshot by clicking on the Actions tab of Old volume.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m10.png"></img>
  <br> 
   <li>	Enter a description and click on Create snapshot.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m11.png"></img>
  <br> 
   <li>	The snapshot has been successfully created.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m12.png"></img>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m13.png"></img>
  <br> 
  
  ## Step 4: Creating a new volume

  <li>	Create a new volume by clicking on Create volume.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m14.png"></img>
  <br> 
   <li>	Enter the details as shown in the below screenshot:</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m15.png"></img>
  <br> 
  <h2>Note: The Availability Zone should be provided as the same as the EC2 instance created.</h2>
  <br> 
   <li>	Click on Create volume.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m16.png"></img>
  <br>
  <li>	Edit the name as New Volume as the volume has been successfully created.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m17.png"></img>
  <br>
  <li>	Connect to the AWS Linux VM by selecting the Instance and clicking on the Connect button.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m18.png"></img>
  <br>
  <li>	Click on Connect.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m19.png"></img>
  <br>
  <li>	Enter the below command to view the EBS volumes created:</li>
  ```lsblk```
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m20.png"></img>
  <br>
  
  ## Step 5: Detaching the existing volume from the EC2 Instance

  <li>	Navigate to the instance my-ebs-volume and select Stop instance from the Instance state tab.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m21.png"></img>
  <br> 
   <li>	Click on Stop.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m22.png"></img>
  <br> 
  <li>	Select the Old volume, and under the Actions tab, click on Detach volume.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m23.png"></img>
  <br>
  <li>	Click on Detach.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m24.png"></img>
  <br>
  <li>	The Old volume has been successfully detached.</li>
  <br>
  <img  width="100%" height="100%" src="https://github.com/GovindSingh9447/DevOps/blob/main/Images/m25.png"></img>
  <br>
