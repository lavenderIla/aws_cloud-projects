# **AWS Project: Public and Private IP adress**

This project demonstrates how I troubleshooted an AWS networking issue involving EC2 instances, VPCs, and IP addressing — identifying why one instance could access the internet while another could not.

The goal was to investigate the difference between public and private IPs, connect via SSH, and recommend best practices for AWS VPC IP design.


## **📚Scenario Overview**

As an AWS Cloud Support Engineer, I received a support ticket from a customer whose two EC2 instances (Instance A and B) were in the same VPC and subnet:

Instance A ❌ Could not reach the internet

Instance B ✅ Could reach the internet

## **📚Steps**

1. Open AWS Management Console → EC2 → Instances.
   
2. Click Launch Instance

  <img width="499" height="249" alt="Screenshot 2025-10-28 at 17 41 21" src="https://github.com/user-attachments/assets/ce542ebf-fd46-4cf4-b807-c9dae393fbcf" />

3. Checked the Networking tab for both instances.

Observed that:

Instance A had only a private IP address.

<img width="499" height="319" alt="Screenshot 2025-10-28 at 18 25 51" src="https://github.com/user-attachments/assets/67a59806-6162-49ea-8065-c937bc6e4afa" />



Instance B had a public IP address assigned.

<img width="499" height="319" alt="Screenshot 2025-10-28 at 18 26 08" src="https://github.com/user-attachments/assets/962cca38-9922-46bd-a4af-b7016f3092ad" />

💡 Finding:
Only instances with public IPs can access the internet through the Internet Gateway.


## **✅ Test Connectivity via SSH**

Used SSH to connect to both instances from the terminal:**

- chmod 400 labsuser.pem
ssh -i labsuser.pem ec2-user@<Public-IP>

<img width="499" height="179" alt="Screenshot 2025-10-28 at 18 29 41" src="https://github.com/user-attachments/assets/cde58f2f-c955-4eb1-8466-5dd1a1b8e585" />

<img width="572" height="178" alt="Screenshot 2025-10-28 at 18 29 56" src="https://github.com/user-attachments/assets/8173df3e-f4b9-44bc-88cd-b35a49f032b6" />

Could connect to Instance B (has public IP).

Could not connect to Instance A (only private IP).

💡 Conclusion:
Instance A is isolated within the VPC since private IPs are not routable over the internet.
chmod 400 KeyPair.pem  

✅ **Customer Response**

As the support engineer, I explained to the customer that:

- The issue was due to Instance A lacking a public IP.

- To fix it, assign a public IP.

  
## 🧠 **Outcome**

- Diagnosed and resolved EC2 connectivity issue.

- Demonstrated understanding of IP addressing, AWS networking and troubleshooting.



## **✍️ Author**

Made with 💻 by  Lavender Ila

🔗  [LinkedIn](https://www.linkedin.com/in/lavender-ila-1981142b0/)
