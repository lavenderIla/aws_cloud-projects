# **AWS Project: Deploy a Web Server on Amazon EC2**

This project demonstrates how I launched and configured an Amazon EC2 instance to host a simple web page using the Apache web server, and how I accessed and managed it via the Command Line (Terminal).


## **📚Steps - Launch an EC2 Instance**

1. Open the AWS Management Console → EC2

2. Click Launch Instance

3. Name: Web Server

AMI: Amazon Linux 2 AMI (Free tier eligible)
<img width="967" height="625" alt="Screenshot 2025-10-11 at 11 44 59" src="https://github.com/user-attachments/assets/3f35cadd-ba4a-44f7-9f96-9a64eeac35b1" />

4. Create or select an existing key pair

<img width="598" height="625" alt="Screenshot 2025-10-11 at 11 46 11" src="https://github.com/user-attachments/assets/55e2460a-19a8-4319-b6c8-3ea26a47204f" />

5. Under Network Settings, allow:

- SSH (22) — for remote login (Command Line Terminal)

- HTTP (80) — for website access

<img width="953" height="625" alt="Screenshot 2025-10-11 at 11 47 09" src="https://github.com/user-attachments/assets/9d520309-54c6-4739-bf59-c8e85c64126a" />

6. Under Advanced Settings → User Data, paste this script to auto-install Apache:

7. Click Launch Instance
<img width="1428" height="241" alt="Screenshot 2025-10-11 at 11 48 29" src="https://github.com/user-attachments/assets/01e23677-81da-4652-9666-0235db31f5df" />


# **You can access the EC2 instance via:**

## **✅ 1: Access via Command Line (Local Terminal)**

- If you prefer using your own terminal (on Mac, Linux, or Windows PowerShell):

- Download your key pair (e.g. KeyPair.pem)

- Move it to your working directory, then run:

Copy paste the command below but replace <public-ip-address> with your IP adress:

cd ~/Downloads

chmod 400 KeyPair.pem  

ssh -i KeyPair.pem ec2-user@<public-ip-address>


✅ You’re now connected to your EC2 instance from your own computer

<img width="567" height="367" alt="Screenshot 2025-10-11 at 12 00 04" src="https://github.com/user-attachments/assets/c3900bba-fbba-4b20-9dca-4ba7e19f6038" />



## **✅ 2: Test Your Web Server**

- Copy your EC2 Public IPv4 address

- Open your browser and paste it


<img width="1428" height="582" alt="Screenshot 2025-10-11 at 11 49 01" src="https://github.com/user-attachments/assets/3ca10f62-42fc-421d-9056-77c33a7e0e08" />

You’ll see your custom web page!
<img width="1153" height="582" alt="Screenshot 2025-10-11 at 11 49 42" src="https://github.com/user-attachments/assets/37bc1f10-27b8-4a16-987e-8849cc900e32" />


## **🧠 What I Learned**

- How to launch and configure EC2 instances

- How to use Apache web server

- How to connect via SSH from browser and terminal

- How to open ports using Security Groups

- How to automate setup with User Data scripts


## **✍️ Author**

Made with 💻 by  Lavender Ila

🔗  [LinkedIn](https://www.linkedin.com/in/lavender-ila-1981142b0/)

