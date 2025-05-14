# three-tier-web-architecture-on-aws
This project documents my step-by-step implementation of the [AWS Three-Tier Web Architecture Workshop](https://catalog.us-east-1.prod.workshops.aws/workshops/85cd2bb2-7f79-4e96-bdee-8078e469752a/en-US),done independently for learning and hands-on practice.

---

## 📁 Repository Structure

```
three-tier-web-architecture-on-aws/
├── app-tier/         # Application layer code (backend)
├── web-tier/         # Web server layer code (frontend)
├── nginx.conf        # NGINX config used in web tier
├── README.md         # Documentation of this project
└── LICENSE           # Project license
```
---

# 🚀 Project Steps
## 🔽 Part 0: Setup
- ### ✅ Git Clone  
![Screenshot from 2025-05-14 15-58-14](https://github.com/user-attachments/assets/7f061ead-5d42-41ea-8162-7bd9eb7d163f)
![Screenshot from 2025-05-14 15-58-48](https://github.com/user-attachments/assets/5b2ad1d0-4b8b-4dfb-a37b-c710dba4782e)

- ### ✅ S3 Bucket Creation  
![Screenshot from 2025-05-13 18-24-24](https://github.com/user-attachments/assets/3403b959-e88d-4a6f-a62c-02a91221ee25)

- ### ✅ IAM Role  
![Screenshot from 2025-05-13 18-27-54](https://github.com/user-attachments/assets/74102910-913c-41e5-8092-3b1bc23f4d72)
![Screenshot from 2025-05-13 18-31-01](https://github.com/user-attachments/assets/7689ab4f-9a85-4153-b21a-17f439d8af7e)

---
## 🌐 Part 1: Networking & Security
### ✅ VPC & Subnets  
![Screenshot from 2025-05-13 18-33-32](https://github.com/user-attachments/assets/69ae06cf-06e9-4fb7-a387-5e0afafdde79)
 ...
 
### ✅ Subnets 
![Screenshot from 2025-05-13 18-39-07](https://github.com/user-attachments/assets/260858a7-b27b-4c9e-9352-b625551106ad)
![Screenshot from 2025-05-13 18-39-50](https://github.com/user-attachments/assets/232300c1-95ac-4b34-a384-fbb57f0eb208)
![Screenshot from 2025-05-13 18-40-34](https://github.com/user-attachments/assets/5243bdd5-d7f2-47f8-a19f-5332290be37c)
![Screenshot from 2025-05-13 18-41-40](https://github.com/user-attachments/assets/fdcd7058-3d84-49ad-8371-8c461e415f36)
![Screenshot from 2025-05-13 18-42-40](https://github.com/user-attachments/assets/c72f5aa4-ce68-4322-b56c-b7c45dbafadd)
![Screenshot from 2025-05-13 18-43-35](https://github.com/user-attachments/assets/ac0e0bce-c479-4eed-bd4a-d295fec5db9b)

#### subnet is created
![Screenshot from 2025-05-13 18-44-49](https://github.com/user-attachments/assets/1e2e5b75-859a-4716-a8bb-b338f9deeaa4)

### ✅ Internet Gateway 

![Screenshot from 2025-05-13 18-46-03](https://github.com/user-attachments/assets/9f5b0913-b616-41b0-9540-f9d766fe423d)

#### attach vpc to internet gateway
![Screenshot from 2025-05-13 18-46-19](https://github.com/user-attachments/assets/f640ed80-dfe4-45b3-a0b9-9258ea25de57)
![Screenshot from 2025-05-13 18-46-33](https://github.com/user-attachments/assets/cc160aab-5e5c-4328-a935-d570f86f1cca)

### ✅ NAT Gateway  

![Screenshot from 2025-05-13 18-47-41](https://github.com/user-attachments/assets/a26eaed6-3d18-4e59-aaf3-7b97ba47bec3)
![Screenshot from 2025-05-13 18-48-45](https://github.com/user-attachments/assets/9a1b3292-9372-4ab9-9705-2e4f43914829)

#### NAT gateway is created
![Screenshot from 2025-05-13 18-50-36](https://github.com/user-attachments/assets/59b74394-016d-458f-94bf-4cd9ae98f13f)

### ✅ Route Tables (Public & Private)  
create two route one public one private
- #### Publice Route table 
![Screenshot from 2025-05-13 18-51-25](https://github.com/user-attachments/assets/dae20d43-fae4-4f3b-9316-002d231f87f7)

#### edit route
![Screenshot from 2025-05-13 18-51-55](https://github.com/user-attachments/assets/a43439d0-8c36-4a99-8554-f24995653e8e)
![Screenshot from 2025-05-13 18-52-20](https://github.com/user-attachments/assets/0902f1a0-70bd-4ea6-a2b3-78c678aa6e3c)

#### edit subnet Associations
![Screenshot from 2025-05-13 18-52-36](https://github.com/user-attachments/assets/e9c40163-0323-4f32-a8c3-af23a0c5537d)
![Screenshot from 2025-05-13 18-52-56](https://github.com/user-attachments/assets/26b04914-0f01-4adb-a8c5-4929c49bf831)

![Screenshot from 2025-05-13 18-53-25](https://github.com/user-attachments/assets/59ee0c43-c6a4-48dd-955f-7efd30b82366)

- #### Private Route table
![Screenshot from 2025-05-13 18-56-02](https://github.com/user-attachments/assets/c4b4e13e-d6b9-4b8d-a4b2-effeec8dbcfb)

#### edit route
![Screenshot from 2025-05-13 18-56-38](https://github.com/user-attachments/assets/58cec3b9-6c65-466a-8dd3-add5bea9b61d)

#### edit subnet Associations
![Screenshot from 2025-05-13 18-57-24](https://github.com/user-attachments/assets/8e402d5c-3e09-44ee-825d-efa12352becd)
![Screenshot from 2025-05-13 18-57-40](https://github.com/user-attachments/assets/1efa7ab7-c260-4cc5-9f6b-32db3a68ad01)

#### route table is  created
![Screenshot from 2025-05-13 18-59-57](https://github.com/user-attachments/assets/13a42376-9b66-4b3f-b7af-d133cc8f7d3a)

----

### ✅ Security Groups  
#### create 5 security group
- InternetFacing  
- WebTier  
- Internal Load Balancer  
- PrivateInstance  
- DB-SG

#### InernetFacing
![Screenshot from 2025-05-13 19-06-00](https://github.com/user-attachments/assets/27a4da10-41b1-47c9-8b6f-9015025f13db)
![Screenshot from 2025-05-13 19-06-33](https://github.com/user-attachments/assets/ed752f41-6acc-41dc-9605-84a0870a2fb4)

#### webTier
![Screenshot from 2025-05-13 19-11-16](https://github.com/user-attachments/assets/d9d45ad1-a769-4c72-8759-44ce1493317b)
![Screenshot from 2025-05-13 19-12-07](https://github.com/user-attachments/assets/2c3eb491-011b-4405-a060-dd8590d575d7)
![Screenshot from 2025-05-13 19-13-10](https://github.com/user-attachments/assets/159985fc-8ea8-4b5e-aa0b-91172aaf91ab)

#### Inernal-lb-sg
![Screenshot from 2025-05-13 19-22-17](https://github.com/user-attachments/assets/7736f9ca-689f-44fd-98f9-0d6a503c96e0)

#### PrivateInstance
![Screenshot from 2025-05-13 19-21-49](https://github.com/user-attachments/assets/6146e44d-32a4-4420-8e36-c3145319a041)

#### DB-sg
![Screenshot from 2025-05-13 19-24-06](https://github.com/user-attachments/assets/82181904-9de7-4e10-9276-c7072af3eb15)

#### security group is created
![Screenshot from 2025-05-13 19-39-29](https://github.com/user-attachments/assets/921d6d39-7920-4029-98e6-f1c040c570df)

---

## 🗄️ Part 2: RDS (Database Tier)
- Subnet Group  
- MySQL DB Instance

### ✅ create subnet groups
![Screenshot from 2025-05-13 19-26-59](https://github.com/user-attachments/assets/654d95eb-8838-4612-bd19-1fa8169958fa)

### ✅ create database
![Screenshot from 2025-05-13 19-30-23](https://github.com/user-attachments/assets/d74147c6-9aad-49db-a674-dc8c54208edf)
![Screenshot from 2025-05-13 19-32-19](https://github.com/user-attachments/assets/b723b4ee-b9d6-4bc4-b4c8-b174631c2120)
![Screenshot from 2025-05-13 19-33-26](https://github.com/user-attachments/assets/f344f7ee-c7f6-4a4f-b8e4-eaf673cb7ca7)

---

## ⚙️ Part 3: App Tier
- EC2 Launch for AppServer  
- SSM Connect  
- Configure DB connection  
- Upload `app-tier` folder to S3
- Test App
- Create AMI, Target Group, Load Balancer, Launch Template & Auto Scaling  
 
### ✅ Launch instance for AppServer
![Screenshot from 2025-05-13 19-40-29](https://github.com/user-attachments/assets/a4ebe9df-7e70-483f-81ba-4730e9228161)
![Screenshot from 2025-05-13 19-44-50](https://github.com/user-attachments/assets/85ed5173-a401-4957-8eb9-2187b05216c8)
![Screenshot from 2025-05-13 19-45-23](https://github.com/user-attachments/assets/f82a2ce3-c82b-4370-97f1-3212593bddf2)
![Screenshot from 2025-05-13 19-46-15](https://github.com/user-attachments/assets/73dfd8cc-a852-496b-9fdd-922de015e946)

### ✅ Configure DB connection
##### select instance click on connect
![Screenshot from 2025-05-14 16-46-33](https://github.com/user-attachments/assets/5c6a8173-3104-479b-ae94-bd719e0fc719)

![Screenshot from 2025-05-13 21-32-17](https://github.com/user-attachments/assets/aad2051e-92ad-4730-a561-3573eed8cff5)
![Screenshot from 2025-05-13 21-32-35](https://github.com/user-attachments/assets/45497fde-58bf-41e2-a8a8-1fe6f4b9317a)
![Screenshot from 2025-05-13 21-32-50](https://github.com/user-attachments/assets/b8bd0cac-dbef-48af-bd50-e8c8a4f9c119)
![Screenshot from 2025-05-13 21-33-05](https://github.com/user-attachments/assets/e1412075-4b82-4967-abc2-ccf7da3b70c7)

##### copy endpoint of database
![Screenshot from 2025-05-13 21-33-37](https://github.com/user-attachments/assets/cfa0898f-a928-424b-bae7-42c47c5c3735)

##### paste in this command like this
![Screenshot from 2025-05-13 21-33-18](https://github.com/user-attachments/assets/112b4219-0e84-498c-b135-dedaa33d6b1f)


![Screenshot from 2025-05-13 21-39-02](https://github.com/user-attachments/assets/d00707b0-5931-4891-a78e-8dfa4f985f3b)
![Screenshot from 2025-05-13 21-49-55](https://github.com/user-attachments/assets/320e1f49-30c1-4d10-9544-16da0ea86c2f)
![Screenshot from 2025-05-13 21-50-34](https://github.com/user-attachments/assets/adbb18e2-877b-48af-bc5b-545181fdcc33)
![Screenshot from 2025-05-13 21-50-48](https://github.com/user-attachments/assets/d7f19174-fcfa-42ec-a71b-86c02e503525)

### ✅ Upload `app-tier` folder to S3  
![Screenshot from 2025-05-13 21-43-23](https://github.com/user-attachments/assets/b8a673ab-9721-4c54-bf04-b3ca7c352287)

then
![Screenshot from 2025-05-13 21-51-35](https://github.com/user-attachments/assets/28bde097-9537-4211-bb85-3ea0771b4b02)
![Screenshot from 2025-05-13 21-52-06](https://github.com/user-attachments/assets/a0fc9b62-a918-4f1e-98a1-97e3a0abea08)
![Screenshot from 2025-05-13 21-52-39](https://github.com/user-attachments/assets/751729e7-dcae-4880-b09c-68bd4c595916)
![Screenshot from 2025-05-13 21-52-59](https://github.com/user-attachments/assets/40450cb8-e820-4766-8813-d3f8025d52db)

### ✅ Test App
![Screenshot from 2025-05-13 21-58-40](https://github.com/user-attachments/assets/4d78ad01-b028-4a34-8ea1-6cd78ba0e76e)

Test App — fix `DbConfig.js`  
![Screenshot from 2025-05-13 22-04-54](https://github.com/user-attachments/assets/c2da5303-ed76-4a6c-8932-8fb76f3c4e70)
![Screenshot from 2025-05-13 22-01-26](https://github.com/user-attachments/assets/781c6521-37ce-4494-a1d9-394c2fb23a51)

### ✅ Create AMI, Target Group, Load Balancer, Launch Template & Auto Scaling  
#### create an image from instance
![Screenshot from 2025-05-13 22-09-51](https://github.com/user-attachments/assets/08a4a633-4e06-4d9d-9b11-994f6251c62e)
![Screenshot from 2025-05-13 22-10-44](https://github.com/user-attachments/assets/5fc8a98f-5343-4198-8ccd-3c7eb00910d1)

#### create target group
![Screenshot from 2025-05-13 22-12-15](https://github.com/user-attachments/assets/94f2eb2b-9e6f-4558-8459-20160280f098)
![Screenshot from 2025-05-13 22-12-55](https://github.com/user-attachments/assets/0deb261f-4d54-44f5-97fd-bc5aa106f9f2)
![Screenshot from 2025-05-13 22-13-26](https://github.com/user-attachments/assets/a11828a8-a527-4fc0-a2f6-09dd387baffd)
![Screenshot from 2025-05-13 22-14-23](https://github.com/user-attachments/assets/fa0c7693-3881-4461-b111-8e9c88ceecab)

#### create loadbalancer
![Screenshot from 2025-05-13 22-14-44](https://github.com/user-attachments/assets/351ed940-3f75-4381-b067-44bf406b821c)
![Screenshot from 2025-05-13 22-15-50](https://github.com/user-attachments/assets/c208e6b0-3efc-422f-a49e-7e87c0c3d0bf)
![Screenshot from 2025-05-13 22-16-59](https://github.com/user-attachments/assets/171ea54d-1572-4206-90ec-bad09a86a08e)
![Screenshot from 2025-05-13 22-17-31](https://github.com/user-attachments/assets/ae259f8b-411b-4b79-8c55-bc718898efd2)

#### launch template
![Screenshot from 2025-05-13 22-19-57](https://github.com/user-attachments/assets/55378bbc-ba06-4865-b8c0-0bc90c5f3cd2)
![Screenshot from 2025-05-13 22-20-45](https://github.com/user-attachments/assets/e1f7c6e0-b2cf-496a-a086-297fa738bd3b)
![Screenshot from 2025-05-13 22-21-18](https://github.com/user-attachments/assets/535cf67d-b818-4df9-9686-7e8f03f9c30c)
![Screenshot from 2025-05-13 22-21-44](https://github.com/user-attachments/assets/bb314c59-dcb3-4e42-b1c8-77a13751c1f6)

#### create autoscaling
![Screenshot from 2025-05-13 22-22-51](https://github.com/user-attachments/assets/cffb8f55-afec-44f1-9bec-2f24fe00da33)
![Screenshot from 2025-05-13 22-23-30](https://github.com/user-attachments/assets/92b63937-ce28-4a4d-b47d-d2b1de3d96c5)
![Screenshot from 2025-05-13 22-24-06](https://github.com/user-attachments/assets/f3effc2e-9fbb-40be-9792-41bebe576e18)
![Screenshot from 2025-05-13 22-24-48](https://github.com/user-attachments/assets/1119aa98-2fcc-4614-9257-a12d2f21c553)

---

## 🌐 Part 4: Web Tier
- Configure `nginx.conf` with App LB DNS  
- Upload `web-tier` and `nginx.conf` to S3  
- Launch EC2 for WebServer  
- Connect via SSM and test in browser
- Create AMI, Target Group, Load Balancer, Launch Template & Auto Scaling  
- Final Test  

### ✅ Configure `nginx.conf` with App LB DNS
##### now copy the dns and paste on nginx.conf file like 58 line

![Screenshot from 2025-05-13 22-30-44](https://github.com/user-attachments/assets/6589fcab-c7e0-4506-9807-00c230153324)
![Screenshot from 2025-05-13 22-31-46](https://github.com/user-attachments/assets/46c530de-cc9c-421f-bf5b-24623e577311)

### ✅ Upload `web-tier` and `nginx.conf` to S3  
![Screenshot from 2025-05-13 22-33-18](https://github.com/user-attachments/assets/db7033cd-d973-433f-bf20-95c642aa19ab)
![Screenshot from 2025-05-13 22-35-15](https://github.com/user-attachments/assets/db0d91fe-36f6-4c03-982f-5c1815c40930)

### ✅ Launch instance for WebServer
![Screenshot from 2025-05-13 22-44-35](https://github.com/user-attachments/assets/c4c3b883-188a-4af9-b0de-e6f572784aa7)
![Screenshot from 2025-05-13 22-44-25](https://github.com/user-attachments/assets/0b4b1274-9b00-4bb9-9327-32fad9a7bb48)
![Screenshot from 2025-05-13 22-38-11](https://github.com/user-attachments/assets/16a6d990-c25c-4c6a-bc69-d3d823167905)

##### select instance click on connect then
### ✅ Connect via SSM and test in browser
#### Connect via SSM
![Screenshot from 2025-05-14 16-46-33](https://github.com/user-attachments/assets/40adf5c8-ea69-4677-9392-af375372e026)

![Screenshot from 2025-05-13 22-49-35](https://github.com/user-attachments/assets/17ef5791-e81c-4ce8-a51c-2a1b0e7ff7ad)
![Screenshot from 2025-05-13 22-51-39](https://github.com/user-attachments/assets/068849c7-7510-4c1a-b2bd-96975a7df9ba)
![Screenshot from 2025-05-13 22-52-04](https://github.com/user-attachments/assets/616eed13-5af9-49f8-ab22-ec3885716b41)
![Screenshot from 2025-05-13 22-53-24](https://github.com/user-attachments/assets/8f26ee25-6a8d-4375-8be1-bb57f9ec8503)
![Screenshot from 2025-05-13 22-54-48](https://github.com/user-attachments/assets/2c612986-74e1-454e-9153-394133af053e)
![Screenshot from 2025-05-13 22-55-47](https://github.com/user-attachments/assets/8e02ee4d-47c1-49de-b553-d7675ce66c25)
![Screenshot from 2025-05-13 22-58-16](https://github.com/user-attachments/assets/6ffc14f2-4341-4788-9339-437c01f0d7c5)
![Screenshot from 2025-05-13 23-02-04](https://github.com/user-attachments/assets/1c9ae1c8-8c9b-40ce-9062-9de5865b5529)
![Screenshot from 2025-05-13 23-03-07](https://github.com/user-attachments/assets/300d56c3-3ae3-44d1-a45f-a608377e6f0c)

#### Test in browser
##### copy the ip of your intance and paste on your web browser
![Screenshot from 2025-05-13 23-04-17](https://github.com/user-attachments/assets/f3435958-62d3-417a-8f22-b6dd06c5a4a2)


### ✅ Create AMI, Target Group, Load Balancer, Launch Template & Auto Scaling  

#### create an image from instance
![Screenshot from 2025-05-13 23-06-17](https://github.com/user-attachments/assets/f19d0a82-4108-410e-9a84-acd823575494)
![Screenshot from 2025-05-13 23-07-00](https://github.com/user-attachments/assets/900fdd49-6289-42b7-8f60-3227e16f6202)

#### create target group
![Screenshot from 2025-05-13 23-09-27](https://github.com/user-attachments/assets/f913d90a-89ae-4681-9b69-7aed304edf7f)
![Screenshot from 2025-05-13 23-09-44](https://github.com/user-attachments/assets/fec3b1a3-bcb4-4e34-a265-91dc5c643a02)

#### create loadbalancer
![Screenshot from 2025-05-13 23-11-06](https://github.com/user-attachments/assets/f2b3b0fd-a4a2-40b1-807c-fcc5bda0316a)
![Screenshot from 2025-05-13 23-12-09](https://github.com/user-attachments/assets/df011f00-ced0-4587-bf8e-79c89d9164e4)

#### launch template
![Screenshot from 2025-05-13 23-14-18](https://github.com/user-attachments/assets/25732be3-456a-41fa-815a-d5dd88738cb1)
![Screenshot from 2025-05-13 23-14-41](https://github.com/user-attachments/assets/5f4a0f39-585f-49cd-b3dd-ffbf033a53ce)
![Screenshot from 2025-05-13 23-15-16](https://github.com/user-attachments/assets/981cbfa8-00ee-40e6-b03b-5a44afd0d732)
![Screenshot from 2025-05-13 23-15-36](https://github.com/user-attachments/assets/aeb3f782-bd48-4f4f-9b39-eee785029552)

#### create autoscaling
![Screenshot from 2025-05-13 23-16-36](https://github.com/user-attachments/assets/2270a9db-03cf-4b7e-817a-b305b08d9e74)
![Screenshot from 2025-05-13 23-17-32](https://github.com/user-attachments/assets/4480f69e-874e-4746-a54f-a11826c209bf)
![Screenshot from 2025-05-13 23-21-17](https://github.com/user-attachments/assets/044dbe2d-83d4-43aa-9a19-3b07605ff1ca)
![Screenshot from 2025-05-13 23-21-44](https://github.com/user-attachments/assets/cd33961e-003d-4bc2-8214-fcfb76984266)

### ✅ Final Test  
now copy the dns of loadbalancer and paste on your web browser
![Screenshot from 2025-05-13 23-22-44](https://github.com/user-attachments/assets/ff092191-7f61-4d2e-b134-1511d2f42e8a)

---

## 🧠 Learnings

- Building multi-tier architecture with AWS best practices
- Role-based access, NAT & IGW usage
- Auto scaling with load balancers
- Configuring backend/frontend interaction securely
- Real-world deployment flow using EC2 and RDS

## 🧹 Clean-Up

After completing the project:
- Terminate EC2s
- Delete Load Balancers
- Delete NAT Gateways (to avoid billing)
- Delete RDS (optional: take snapshot)
- Delete VPC and associated components
- Remove S3 contents

---

## 🔗 Workshop Reference

[AWS Official Workshop Link](https://catalog.us-east-1.prod.workshops.aws/workshops/85cd2bb2-7f79-4e96-bdee-8078e469752a/en-US)

