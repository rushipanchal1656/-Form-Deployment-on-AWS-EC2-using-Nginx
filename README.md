# 🌐 Form Deployment on AWS EC2 using Nginx

This project demonstrates how to deploy a web form on an Amazon EC2 instance using **Nginx** as the web server. It includes step-by-step setup and configuration.

---

## Table of Contents

- [Project Structure](#-project-structure)
- [Deployment Steps](#-deployment-steps)
- [How to Make It Work](#-how-to-make-it-work)
- [All Steps](#all-steps)
- [Author](#-author)

---

## 📁 Project Structure

```bash

project-root/
├── assets/
│ ├── ec2-setup.png
├── home_page.html
├── login
├── README.md
```

---

# 🚀 Deployment Steps

### 1. Launch EC2 Instance

- Go to AWS Console → EC2 → Launch a new instance
- Choose Amazon Linux 2 AMI
- Allow HTTP (port 80) in the security group

<img src="./assets/EC2_image.png" alt="EC2 Setup" width="400"/>

---

### 2. Connect via SSH

```bash
ssh -i your-key.pem ec2-user@your-ec2-public-ip
```

---

### 3. Install Nginx on EC2

<details>
<summary>Click to expand detailed Nginx setup instructions</summary>

```bash
sudo yum update -y
sudo amazon-linux-extras enable nginx1
sudo yum install -y nginx
sudo systemctl start nginx
sudo systemctl enable nginx
```

</details>

<p float="left">
  <img src="./assets/step_1.png" width="400"/>
  <img src="./assets/step_2.png" width="400"/>
  <img src="./assets/step_3.png" width="400"/>
</p>

---

### 4. Deploy Your Form

Copy your index.html and any supporting files (CSS, JS) to the Nginx root:

```bash
sudo cp index.html /usr/share/nginx/html/
sudo cp style.css /usr/share/nginx/html/
```

---

### 5. Add Port number 90

<img src="./assets/add_90_port.png" alt="EC2 Setup" width="400"/>

<img src="./assets/90_port_added.png" alt="EC2 Setup" width="400"/>

### 5. View Your Form

Open your browser and go to:
<http://13.222.240.188:90>

<img src="./assets/about.png" alt="EC2 Setup" width="400"/>
<img src="./assets/login.png" alt="EC2 Setup" width="400"/>

---

### 6. Author

Rushikesh Panchal
LinkedIn | GitHub

---

### 📝 How to Make It Work

1. Save all images (`ec2-setup.png`, etc.) in a folder called `assets/` inside your project directory.
2. Save the above content as `README.md` in the root of your project.
3. When you push this to GitHub or another repo, the images will show up if they are in the correct relative path.

---

Let me know if you'd like to include form source code, live demo links, or auto-deployment steps (e.g., with a script or CI/CD).

### All Steps

#### 1st step

<img src="./assets/step_1.png" alt="step 1" width="400"/>

#### 2nd step

<img src="./assets/step_2.png" alt="step 2" width="400"/>

#### 3rd step

<img src="./assets/step_3.png" alt="step 3" width="400"/>

#### 4th step  

<img src="./assets/step_5.png" alt="step 4" width="400"/>

#### 5th step

<img src="./assets/step_6.png" alt="step 5" width="400"/>

#### 6th step

<img src="./assets/step_7.png" alt="step 6" width="400"/>

#### 7th step

<img src="./assets/step_8.png" alt="step 7" width="400"/>

#### 8th step

<img src="./assets/step_9.png" alt="step 8" width="400"/>

#### 9th step

<img src="./assets/step_10.png" alt="step 9" width="400"/>

#### 10th step

<img src="./assets/step_11.png" alt="step 10" width="400"/>

---

- **Live Demo:** [View Form](http://13.222.240.188:90)
- **Author:** [Rushikesh Panchal](https://www.linkedin.com/in/your-linkedin)
