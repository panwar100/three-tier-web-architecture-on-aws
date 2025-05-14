# three-tier-web-architecture-on-aws
# - s3 bucket
![Screenshot from 2025-05-13 18-24-24](https://github.com/user-attachments/assets/3403b959-e88d-4a6f-a62c-02a91221ee25)

---

# - IAM role
![Screenshot from 2025-05-13 18-27-54](https://github.com/user-attachments/assets/74102910-913c-41e5-8092-3b1bc23f4d72)
![Screenshot from 2025-05-13 18-31-01](https://github.com/user-attachments/assets/7689ab4f-9a85-4153-b21a-17f439d8af7e)

---

# - VPC
![Screenshot from 2025-05-13 18-33-32](https://github.com/user-attachments/assets/69ae06cf-06e9-4fb7-a387-5e0afafdde79)

---

# - Subnet
![Screenshot from 2025-05-13 18-39-07](https://github.com/user-attachments/assets/260858a7-b27b-4c9e-9352-b625551106ad)
![Screenshot from 2025-05-13 18-39-50](https://github.com/user-attachments/assets/232300c1-95ac-4b34-a384-fbb57f0eb208)
![Screenshot from 2025-05-13 18-40-34](https://github.com/user-attachments/assets/5243bdd5-d7f2-47f8-a19f-5332290be37c)
![Screenshot from 2025-05-13 18-41-40](https://github.com/user-attachments/assets/fdcd7058-3d84-49ad-8371-8c461e415f36)
![Screenshot from 2025-05-13 18-42-40](https://github.com/user-attachments/assets/c72f5aa4-ce68-4322-b56c-b7c45dbafadd)
![Screenshot from 2025-05-13 18-43-35](https://github.com/user-attachments/assets/ac0e0bce-c479-4eed-bd4a-d295fec5db9b)

 ### subnet is created
![Screenshot from 2025-05-13 18-44-49](https://github.com/user-attachments/assets/1e2e5b75-859a-4716-a8bb-b338f9deeaa4)

----

# - Inertnet gateway
![Screenshot from 2025-05-13 18-46-03](https://github.com/user-attachments/assets/9f5b0913-b616-41b0-9540-f9d766fe423d)

### attach vpc to internet gateway
![Screenshot from 2025-05-13 18-46-19](https://github.com/user-attachments/assets/f640ed80-dfe4-45b3-a0b9-9258ea25de57)
![Screenshot from 2025-05-13 18-46-33](https://github.com/user-attachments/assets/cc160aab-5e5c-4328-a935-d570f86f1cca)

---

# - NAT gateway
![Screenshot from 2025-05-13 18-47-41](https://github.com/user-attachments/assets/a26eaed6-3d18-4e59-aaf3-7b97ba47bec3)
![Screenshot from 2025-05-13 18-48-45](https://github.com/user-attachments/assets/9a1b3292-9372-4ab9-9705-2e4f43914829)

### NAT gateway is created
![Screenshot from 2025-05-13 18-50-36](https://github.com/user-attachments/assets/59b74394-016d-458f-94bf-4cd9ae98f13f)

---

# - Route Table
create two route one public one private
### For Publice Route table 
![Screenshot from 2025-05-13 18-51-25](https://github.com/user-attachments/assets/dae20d43-fae4-4f3b-9316-002d231f87f7)

### edit route
![Screenshot from 2025-05-13 18-51-55](https://github.com/user-attachments/assets/a43439d0-8c36-4a99-8554-f24995653e8e)
![Screenshot from 2025-05-13 18-52-20](https://github.com/user-attachments/assets/0902f1a0-70bd-4ea6-a2b3-78c678aa6e3c)

### edit subnet Associations
![Screenshot from 2025-05-13 18-52-36](https://github.com/user-attachments/assets/e9c40163-0323-4f32-a8c3-af23a0c5537d)
![Screenshot from 2025-05-13 18-52-56](https://github.com/user-attachments/assets/26b04914-0f01-4adb-a8c5-4929c49bf831)

![Screenshot from 2025-05-13 18-53-25](https://github.com/user-attachments/assets/59ee0c43-c6a4-48dd-955f-7efd30b82366)

### for Private Route table
![Screenshot from 2025-05-13 18-56-02](https://github.com/user-attachments/assets/c4b4e13e-d6b9-4b8d-a4b2-effeec8dbcfb)

### edit route
![Screenshot from 2025-05-13 18-56-38](https://github.com/user-attachments/assets/58cec3b9-6c65-466a-8dd3-add5bea9b61d)

### edit subnet Associations
![Screenshot from 2025-05-13 18-57-24](https://github.com/user-attachments/assets/8e402d5c-3e09-44ee-825d-efa12352becd)
![Screenshot from 2025-05-13 18-57-40](https://github.com/user-attachments/assets/1efa7ab7-c260-4cc5-9f6b-32db3a68ad01)

### route table is  created
![Screenshot from 2025-05-13 18-59-57](https://github.com/user-attachments/assets/13a42376-9b66-4b3f-b7af-d133cc8f7d3a)

# - Security group 
### create 5 security group
### InernetFacing
![Screenshot from 2025-05-13 19-06-00](https://github.com/user-attachments/assets/27a4da10-41b1-47c9-8b6f-9015025f13db)
![Screenshot from 2025-05-13 19-06-33](https://github.com/user-attachments/assets/ed752f41-6acc-41dc-9605-84a0870a2fb4)

### webTier
![Screenshot from 2025-05-13 19-11-16](https://github.com/user-attachments/assets/d9d45ad1-a769-4c72-8759-44ce1493317b)
![Screenshot from 2025-05-13 19-12-07](https://github.com/user-attachments/assets/2c3eb491-011b-4405-a060-dd8590d575d7)
![Screenshot from 2025-05-13 19-13-10](https://github.com/user-attachments/assets/159985fc-8ea8-4b5e-aa0b-91172aaf91ab)

### Inernal-lb-sg
![Screenshot from 2025-05-13 19-22-17](https://github.com/user-attachments/assets/7736f9ca-689f-44fd-98f9-0d6a503c96e0)

### PrivateInstance
![Screenshot from 2025-05-13 19-21-49](https://github.com/user-attachments/assets/6146e44d-32a4-4420-8e36-c3145319a041)

### DB-sg
![Screenshot from 2025-05-13 19-24-06](https://github.com/user-attachments/assets/82181904-9de7-4e10-9276-c7072af3eb15)

### security group is created
![Screenshot from 2025-05-13 19-39-29](https://github.com/user-attachments/assets/921d6d39-7920-4029-98e6-f1c040c570df)

# - RDS
### create subnet groups in rds
![Screenshot from 2025-05-13 19-26-59](https://github.com/user-attachments/assets/654d95eb-8838-4612-bd19-1fa8169958fa)

### create database
![Screenshot from 2025-05-13 19-30-23](https://github.com/user-attachments/assets/d74147c6-9aad-49db-a674-dc8c54208edf)
![Screenshot from 2025-05-13 19-32-19](https://github.com/user-attachments/assets/b723b4ee-b9d6-4bc4-b4c8-b174631c2120)
![Screenshot from 2025-05-13 19-33-26](https://github.com/user-attachments/assets/f344f7ee-c7f6-4a4f-b8e4-eaf673cb7ca7)


# - EC2 
# - for AppServer
### launch instance 
![Screenshot from 2025-05-13 19-40-29](https://github.com/user-attachments/assets/a4ebe9df-7e70-483f-81ba-4730e9228161)
![Screenshot from 2025-05-13 19-44-50](https://github.com/user-attachments/assets/85ed5173-a401-4957-8eb9-2187b05216c8)
![Screenshot from 2025-05-13 19-45-23](https://github.com/user-attachments/assets/f82a2ce3-c82b-4370-97f1-3212593bddf2)
![Screenshot from 2025-05-13 19-46-15](https://github.com/user-attachments/assets/73dfd8cc-a852-496b-9fdd-922de015e946)

select instance click on connect then  select smm and connect
![Screenshot from 2025-05-13 21-32-17](https://github.com/user-attachments/assets/aad2051e-92ad-4730-a561-3573eed8cff5)
![Screenshot from 2025-05-13 21-32-35](https://github.com/user-attachments/assets/45497fde-58bf-41e2-a8a8-1fe6f4b9317a)
![Screenshot from 2025-05-13 21-32-50](https://github.com/user-attachments/assets/b8bd0cac-dbef-48af-bd50-e8c8a4f9c119)
![Screenshot from 2025-05-13 21-33-05](https://github.com/user-attachments/assets/e1412075-4b82-4967-abc2-ccf7da3b70c7)

copy endpoint of database
![Screenshot from 2025-05-13 21-33-37](https://github.com/user-attachments/assets/cfa0898f-a928-424b-bae7-42c47c5c3735)

paste in this command like this
![Screenshot from 2025-05-13 21-33-18](https://github.com/user-attachments/assets/112b4219-0e84-498c-b135-dedaa33d6b1f)


![Screenshot from 2025-05-13 21-39-02](https://github.com/user-attachments/assets/d00707b0-5931-4891-a78e-8dfa4f985f3b)





