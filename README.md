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

###


