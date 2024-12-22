# altschool-cloud-project

# public IP address: 34.242.216.26

# Screenshot of the HTML page in the browser

![image alt](https://github.com/Neduamagwu/AltSchoolCloudProject/blob/c42bacacff4927001cece6b5dbd9ba2f25619493/MyWebPage.JPG)

# Step-by-step documentation of Deploying/building a simple HTML page on a Linux Server with AWS as the cloud provider

# Step 1:
We need to build an Ec2 Instance
Once you click on it, next will be to click on Launch instance
- Select Ubuntu as the AMI (Amazon Machine Image) 
- Select the Instance type, in my case I used the t2.micro that has the *eligible for free tier* to it
- You can use default settings for configure instance details,
- Make sure to configure the security group, in my case I selected the SSH type Port 22 and I added another security group, selecting HTTP Type port 80
- then launch, make sure you keep the .pem file very safe, that's what we will use to SSH into the linux server created in the instance.

# Let's Connect to the Instance

We will use the key to ssh into the ubuntu server with the public ip, it will be like this:
*ssh -i the.pem-key.pem ubuntu@<public-ip>*

# Step 2:
Let's run some linux command after we have connected to the server
*sudo apt update
sudo apt upgrade -y
sudo apt install nginx -y*
After installing the nginx we will enable and start the nginx service:
*sudo systemctl start nginx
sudo systemctl enable nginx*

# Step 3:
Let's create the HTML file, it has been pushed to this repository
- First we will 