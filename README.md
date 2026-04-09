# cloud-project-no-2-
Highly secure , scalable web server created under aws resources 

Innovation alwasy starts with some sorts of issues . Its been done to reduce the pain for someone .

In todays time hosting a web server on own infrastructure is a hard job . it requires people with great experience , workbase etc . To make things easy for clinets cloud services came into effect . Today i have tried too create a web server with high availability , security and scalability 


For the architectural project , i have used AWS . It is one of worlds leading cloud service provider with a wide variety of services for easy working 

Services under AWS that are being used in the project --
1. AWS EC2 (elastic cloud compute)
2. route 53
3. Application load balancer
4. Amazon certification manager
5. Auto scalling groups
6. Cloud watch
7. Amazon SNS service


Every resources that i have used here have their own characteristics or functions .

Here, for this project i bought a public domain to show things in real life architectural level .

A question that may arise how its better than on premise, cloud provides more scalability, cost efficient , durability , proper resource utilisation compare to the on-premise .

# what problem this cloud web server solves 
1. Efiicient resource utilisation
2. Scalling up down resources when needed
3. Cost optimization
4. high availability
5. Automated monitoring and alerting

# System Archiecture 
User -----> domain(route 53) -------> Application load balancer (HTTPS via ACM) --------> EC2 instance ---------> Cloudwatch Monitoring ---------> SNS alerts.



# Working of the system 
1. user access the application using a domain name
2. Route 53 resolves the domain to the ALB
3. ALB recieves HTTPS request and decrypts it
4. Traffic is forwarded to EC2 instances
5. EC2 processes the request and returns response
6. CloudWatch monitors metrics continuously
7. If threshholds are crossed, SNS sends alerts

# what are the steps to attain this web service 

 # Implementation Steps

 1. Launched EC2 instance and configured web server (Apache)
 2. Created hosted zone in Route 53 and updated nameservers
 3. Requested SSL certificate using AWS Certificate Manager (ACM)
 4. Created Application Load Balancer and attached target group
 5. Configured HTTPS listener using ACM certificate
 6. Connected domain to ALB using Route 53 (A record - Alias)
 7. Set up CloudWatch alarms for CPU utilization
 8. Configured SNS for email notifications
 9. Implemented Auto Scaling Group with target tracking policy


<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/9a6bd77a-9d37-4dd4-b143-d1178cb01769" />
Browser screenshot: since i dont have any app in it i have implemented a small message in the cloud shell 

<img width="940" height="479" alt="image" src="https://github.com/user-attachments/assets/1520a9c8-e36e-4c4b-a977-adb1c1545a39" />
Hosted zones and records 

<img width="940" height="447" alt="image" src="https://github.com/user-attachments/assets/f8b20a0a-79d5-492c-b3ef-0aa55e2b0370" />
ACM certificate

<img width="940" height="478" alt="image" src="https://github.com/user-attachments/assets/631639ea-e5ee-48a7-a409-faf417889dbb" />
Target group with healthy monitoring 

<img width="940" height="446" alt="image" src="https://github.com/user-attachments/assets/e238afb9-e4a6-4f70-90e2-852f8c0a0003" />
Load balancer 

<img width="940" height="477" alt="image" src="https://github.com/user-attachments/assets/48a876e7-d65e-4595-9216-91e13f096f9a" />
cloudwatch creation 

<img width="940" height="501" alt="image" src="https://github.com/user-attachments/assets/ffa6d180-9b75-4a47-ba22-b562bd9be4ef" />
AWS SNS confirmation 

<img width="940" height="479" alt="image" src="https://github.com/user-attachments/assets/85d36b50-b7f2-4c9c-b242-03e089630351" />
resource threshhold exceeds 


<img width="940" height="478" alt="image" src="https://github.com/user-attachments/assets/5016f3a1-68e2-4402-8d81-fd4b04ac379b" />
Auto-scalling group template


<img width="940" height="477" alt="image" src="https://github.com/user-attachments/assets/fb2fa1d2-ed0e-45bb-87d7-d5560eea1c01" />
After injecting stress increase in instances 


<img width="940" height="478" alt="image" src="https://github.com/user-attachments/assets/f577133a-8397-4e53-b88b-0d3587990346" />
Terminal running stress

