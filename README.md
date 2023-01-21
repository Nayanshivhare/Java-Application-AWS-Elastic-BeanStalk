# Re- Architecting and Integrating Java based Web-App on AWS Cloud Native
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)

# 💻 Tech Stack
![Apache Tomcat](https://img.shields.io/badge/WebServer-%20Apache%20Tomcat-23D42029.svg?style=for-the-badge&logo=apache&logoColor=white) ![Elastic Beanstalk](https://img.shields.io/badge/Compute-%20Elastic%20Beanstalk-23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![RDS Instance](https://img.shields.io/badge/Database-%20RDS%20Instance-23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Amazon ElastiCache](https://img.shields.io/badge/Caching-%20Amazon%20ElastiCache%20Memcached-C71A36?style=for-the-badge&logo=amazon-aws&logoColor&logoColor=blue) ![Amazon MQ](https://img.shields.io/badge/MessageBroker-%20Amazon%20MQ-C71A36?style=for-the-badge&logo=amazon-aws&logoColor&logoColor=blue) ![Route53](https://img.shields.io/badge/DNS-%20Route53-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Cloud Front](https://img.shields.io/badge/Content%20Delivery%20Network-%20Route53-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white) ![Apache Maven](https://img.shields.io/badge/Apache%20Maven-C71A36?style=for-the-badge&logo=Apache%20Maven&logoColor=white) ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=java&logoColor=white) ![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E) ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white) ![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)

# 🔭 Objective
To increase scalability, availability, and cost-efficiency while leveraging the full set of AWS services, I am re-architecting web application from an on-premises infrastructure to a cloud-native architecture on AWS. I used memcached for caching, RDS instances for database management, Route53 for DNS management, and CloudFront for content delivery in addition to Amazon MQ for messaging and queuing. 
This re-architecture will help us with following benefits:
  1. Increase the scalability of our application.
  2. decrease downtime and improve reliability by utilizing AWS's built-in redundancy and failover features.
  3. Cut costs by utilizing the pay-as-you-go pricing model of AWS services.


# ☁️ Architecutre Diagram 
  ![image](https://user-images.githubusercontent.com/66699491/213844644-1368b9a7-7d96-450f-ae52-8b95a351c248.png)

# 🎯 Steps for Implementation

  1.  Login to AWS Account
  2.  Create following services in AWS:
      - Key pair
      - Secuirty Group- For Backend Services 
      - Amazon Elastic Cache- Memcached
      - Amazon Active MQ
  3.  Create Elastic Beanstalk Environemnt
  4.  Update Security group to allow traffic from Elastic Beanstalk Security Group
  4.  Update Security group to allow traffic from internal traffic
  5.  Launch Ec2 to intialize Database
  6.  Login to Ec2 and login to database
  7.  Initialize database
  8.  Change healthcheck on Elastic Beanstalk to our application /login
  9.  Add 445 https Listener to ELB
  10. Build Artifact with Backend Information
  11. Deploy Artifact to Beanstalk
  11. Create CDN with ssl cert
  12. Update entry in DNS
  13. Test the url
  
  
  # Screenshots on Implementation
  ## Create Elastic Beanstalk Environemnt
  <img src="https://user-images.githubusercontent.com/66699491/213845414-ed84e4ad-4ed4-42a9-8ce7-daa975d85a41.png" width="800" height="400">
   <img src="https://user-images.githubusercontent.com/66699491/213845414-ed84e4ad-4ed4-42a9-8ce7-daa975d85a41.png" width="800" height="400">
  <img src="https://user-images.githubusercontent.com/66699491/213845423-aedeee78-661a-4a9b-ba05-1a1e06787ab6.png" width="800" height="600">
  <img src="https://user-images.githubusercontent.com/66699491/213845441-9c2aa349-1f7b-465d-98ad-7b8a85dd4cee.png" width="800" height="600">
  <img src="https://user-images.githubusercontent.com/66699491/213845449-d72b85b6-17c5-4c7a-b2c9-17fd623b53ee.png" width="800" height="400">
   <img src="https://user-images.githubusercontent.com/66699491/213845464-a44bf511-8b19-4a61-8dc8-bee8a1bd3080.png" width="800" height="400">
   
   <img src="https://user-images.githubusercontent.com/66699491/213845469-14b29a5a-8b30-42b0-bdd7-3a9a2482dd49.png" width="800" height="400">
   <img src="https://user-images.githubusercontent.com/66699491/213845477-2ab25a78-94af-432d-8100-db68b39f2250.png" width="800" height="400">
   <img src="https://user-images.githubusercontent.com/66699491/213845478-69b8fa10-55d4-485f-b8d7-e6a4dcd40780.png" width="800" height="400">
   <img src="https://user-images.githubusercontent.com/66699491/213845482-22ab6a22-efee-49ff-b6e2-2bb52091cb4f.png" width="800" height="400">







  ## Security Group Configuration
  
  ## Creating RDS
  <img src="https://user-images.githubusercontent.com/66699491/213846037-092f11d3-68ea-47f0-ad6e-2dc8f6bd0961.png" width="550" height="400">
  <img src="https://user-images.githubusercontent.com/66699491/213846039-e920da58-1768-4945-becd-ee7d3cefe2d2.png" width="550" height="400">
  <img src="https://user-images.githubusercontent.com/66699491/213846045-e7d3dda1-c2dd-4ff4-8678-5677625055b4.png" width="550" height="550">
  <img src="https://user-images.githubusercontent.com/66699491/213846053-441e00a9-7955-4e91-af4b-d1b3471113cc.png" width="550" height="550">
 
  ![image](https://user-images.githubusercontent.com/66699491/213846059-726bcadd-3a73-4fdf-a942-ee03805d5c56.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846293-6bfa59e0-009f-417a-8d3d-cb04984bc982.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846317-78052053-e675-4f6d-a327-0c2c59cc9773.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846323-2016ae04-7e82-4519-8408-122c9bf392fc.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846498-8d847289-7fb6-4250-82d5-28fffc482bb7.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846377-ca601c76-bd8a-4f75-b77a-84640338ee78.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846393-513e81c0-e918-49f1-b07b-fb37f9ead20a.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846402-58fb3035-0fdc-49aa-b642-8644e5b08078.png)

  ## Intializing Database from Ec2 instance
  ![image](https://user-images.githubusercontent.com/66699491/213846184-92d802fe-4dfc-4d84-81ee-3d49dd16babc.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846196-74eeb0c5-c36b-4562-89e4-5febbed94ba0.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846233-ed02686f-0fe0-4608-91b8-08b713e9fe3d.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846433-f7da6d15-c200-4a5e-aaff-69eb2d57f8c7.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846447-80ebce59-4853-4de3-8304-045c4e812b28.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846501-82e36d88-8be5-424f-87fd-424eb21192ce.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846510-016310b0-654a-499b-9f85-3aa032d5e141.png)
  
  ![image](https://user-images.githubusercontent.com/66699491/213846515-ed3251f5-79ab-4409-a4fd-788d17e34ce4.png)
  
  ![image](https://user-images.githubusercontent.com/66699491/213846523-3f2f23e4-c5c2-45a6-9201-20073a92e300.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846528-41ca6cdd-de17-495c-97b2-7e2298780c23.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846533-a9a5f925-f923-415a-855b-a7113daa0bd0.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846537-2f3bee51-cdfd-4daf-a19d-eecb24fb08cb.png)

  ## Creating Amazon Active MQ
  ![image](https://user-images.githubusercontent.com/66699491/213846589-0eb359b5-3b0e-44f8-8b2c-ebfa1193c21b.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846590-609957d4-7539-408a-a892-61e894befcdb.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846594-2a426e5d-a0dc-4123-8111-ca01ebeae236.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846598-e45ce9cb-43df-4988-9b35-851bfcdadb0e.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846602-f12adc0e-6fb0-4327-872b-14db1a7ebadd.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846709-cf9e9f3a-0d41-416d-992f-021f55479b8e.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846786-aa3aa520-2db7-49ca-ac25-69281457b116.png)

  ## Creating ElasticCache Memcached
  ![image](https://user-images.githubusercontent.com/66699491/213846827-04d8945b-8e17-4aa4-b898-b30d2e76d742.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846833-eab743c4-0e6b-4c93-9e07-8c5f23476e2c.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846850-fd60d3c8-5f9d-44fe-a316-da3b6a6c3a32.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846856-9c8784c3-409e-46d6-bbfd-c9f5be8ab797.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846861-0a13aa67-8613-456b-a560-640465e8f7a8.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846931-0171d9d0-9f17-40e6-8038-d07513334fe3.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846968-af2f626d-6f3d-4224-b039-2ef027f0c34e.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846990-aa9bcb42-b0cd-42a2-bb29-91e0d739f1ff.png)
  ![image](https://user-images.githubusercontent.com/66699491/213846978-35416714-c839-4213-97f1-244a23f375a2.png)

  ## Building Stage
  ### Our application code is residing in Github repository. We will clone it, build it on our machine and deploy the artifect on elastic beanstalk.
  ### Open your git bash
  ### Use git clone in your current directory
  ### Git clone https://github.com/devopshydclub/vprofile-project.git
  
![image](https://user-images.githubusercontent.com/66699491/213847295-61c0d5ba-edf4-49ee-b6ff-0a58eca13ad4.png)

![image](https://user-images.githubusercontent.com/66699491/213847304-936b1863-d272-47c5-959f-8e73bb552d92.png)

![image](https://user-images.githubusercontent.com/66699491/213847307-1b08b38c-6e6f-4e3f-80c7-028ca50f8cef.png)

![image](https://user-images.githubusercontent.com/66699491/213847310-4bc8830b-47cb-4bd1-a4f3-bce52fb9627a.png)

![image](https://user-images.githubusercontent.com/66699491/213847315-e9f94d89-bde3-4051-b52c-2b2787fee2a5.png)

![image](https://user-images.githubusercontent.com/66699491/213847319-b239fa44-b478-446b-a387-cc597213a8c0.png)

![image](https://user-images.githubusercontent.com/66699491/213847323-a1657892-adf1-44c2-8ab3-63d1e74f88e4.png)

![image](https://user-images.githubusercontent.com/66699491/213847331-50e8c515-ea58-4a9d-b969-96fa6eeac8a5.png)
### Enter details of endpoints, username, & password
![image](https://user-images.githubusercontent.com/66699491/213847396-564fafa5-023c-43d8-8013-b5304e8d1271.png)
### esc
### :wq
### cd ../../..

## Using Maven to build my application artifacts
![image](https://user-images.githubusercontent.com/66699491/213847467-d798f0d5-da33-4cd7-9b17-3742b6363c59.png)
![image](https://user-images.githubusercontent.com/66699491/213847472-febd5aa2-5b6a-4cf9-81be-28cc54b8636f.png)
![image](https://user-images.githubusercontent.com/66699491/213847496-46c55ab8-3286-4707-8723-ed7bf71107a2.png)
![image](https://user-images.githubusercontent.com/66699491/213847499-bfa77c87-f896-4eac-8910-79c59dc223ce.png)
![image](https://user-images.githubusercontent.com/66699491/213847505-9b115f07-59e1-407e-98c4-2a8f97c6004e.png)

### Use your Elasticbeanstalk link to connect to your deployed application
![image](https://user-images.githubusercontent.com/66699491/213847522-d5c100e0-ea1e-40ae-a248-0e74c4a2e524.png)
![image](https://user-images.githubusercontent.com/66699491/213847588-f6261965-101b-4cd0-8d11-d255ab05e05a.png)


## Using DNS to create CNAME and configure Application Load Balancer
![image](https://user-images.githubusercontent.com/66699491/213847812-ffd93fa7-eda2-4a7d-9cd5-0a5d1a3e980b.png)
![image](https://user-images.githubusercontent.com/66699491/213847825-23999d29-9258-438f-9e93-5dd64085540f.png)
![image](https://user-images.githubusercontent.com/66699491/213847828-55bc8070-a53e-4bb4-9dfa-a87e32c149fb.png)
![image](https://user-images.githubusercontent.com/66699491/213847832-e538842d-4e81-4e0a-b7e0-59de6f2d6151.png)
### Click to apply

## Route53 to create CNAME record

![image](https://user-images.githubusercontent.com/66699491/213847865-b492116c-bcb9-4e18-b631-dc3d0eb72def.png)
![image](https://user-images.githubusercontent.com/66699491/213847868-206f9ab8-c791-4a8b-9dec-e41ce44e084c.png)
![image](https://user-images.githubusercontent.com/66699491/213847986-cd5cd03d-cb52-4d3c-94bc-32b7d7ed5605.png)
![image](https://user-images.githubusercontent.com/66699491/213847875-5f2e36b0-b4a4-4af9-be21-c4606a89509b.png)


##  Setting Cloud Front

![image](https://user-images.githubusercontent.com/66699491/213847901-562070dd-3464-4d1a-a556-4e6a63fed9b5.png)
![image](https://user-images.githubusercontent.com/66699491/213847905-935f688e-d369-4cf3-bf56-f4813e6df2f0.png)
![image](https://user-images.githubusercontent.com/66699491/213847909-46b22fe0-1474-476d-a23d-5e50afde1127.png)
![image](https://user-images.githubusercontent.com/66699491/213847917-5dd52062-6ffc-439c-8d36-2bfaf19c968f.png)
![image](https://user-images.githubusercontent.com/66699491/213847926-eaa70198-8c73-44ad-8cc7-a02191b159a8.png)
![image](https://user-images.githubusercontent.com/66699491/213847931-797d81ac-f8f1-4c49-87c0-7a205602e261.png)
![image](https://user-images.githubusercontent.com/66699491/213847936-bc9e5235-4809-4bee-9e32-f43a8188bde3.png)
![image](https://user-images.githubusercontent.com/66699491/213847940-853066a2-efb8-4378-ad70-6fc370c6eaeb.png)
![image](https://user-images.githubusercontent.com/66699491/213847944-c2304e1f-0bdc-4001-b039-7678fa8aaff7.png)
![image](https://user-images.githubusercontent.com/66699491/213847949-75d1a535-b273-415c-bba6-a86bf634417c.png)























  
  
















  






  



    
