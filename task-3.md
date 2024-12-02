# Task 3: Cloud Infrastructure Deployment (AWS)

## Objective:
Deploy a virtual machine instance on AWS with the following configurations:
- Linux-based OS
- SSH access
- Web server (Nginx) setup
- Firewall rules for HTTP traffic
- Static IP address

---

### Step 1: Create a Virtual Machine (EC2 Instance)

1. **Action**: Launch an EC2 instance with Ubuntu (or your preferred Linux distribution).
   - Go to the AWS EC2 dashboard.
   - Click **Launch Instance**.
   - Choose an AMI (Amazon Machine Image), for example, **Ubuntu Server 20.04 LTS**.
   - Select an instance type (e.g., `t2.micro` for testing purposes).
   - Configure the instance (leave default settings for now).
   - Add a security group (or configure existing) to allow SSH and HTTP (ports 22 and 80).
   - Review and launch the instance.

2. **Screenshot**:
   ![Create EC2 Instance](./Screenshots/VM%20Instance%20set%20up%20on%20AWS(EC2).PNG)
   *The screenshot shows the EC2 instance setup page with selected configurations.*

---

### Step 2: Set Up SSH Access

1. **Action**: Connect to your instance via SSH.
   - Retrieve the public IP address of your EC2 instance from the EC2 dashboard.
   - Use your SSH key to connect:
   ```bash
   ssh -i your-key.pem ubuntu@<your-ec2-public-ip>
