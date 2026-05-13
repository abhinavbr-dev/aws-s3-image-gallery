# AWS S3 Image Gallery Website

A cloud-based image gallery web application developed using **HTML, CSS, JavaScript, Amazon S3, AWS EC2, and Apache Web Server**.

This project allows users to upload images to an AWS S3 bucket and dynamically display them in a responsive gallery interface.

---

# Project Overview

The main objective of this project is to create a scalable and cloud-hosted gallery website using Amazon Web Services (AWS). The application demonstrates integration between front-end web technologies and AWS cloud storage services.

The project includes:
- Image upload interface
- Dynamic image gallery
- AWS S3 cloud storage integration
- EC2 hosting environment
- Apache web server configuration

---

# Features

- Upload images directly to AWS S3
- Display uploaded images automatically
- Responsive gallery layout
- Cloud-based image storage
- Simple and clean UI
- Dynamic image rendering using JavaScript
- Hosted using AWS EC2 and Apache

---

# Technologies Used

- HTML5
- CSS3
- JavaScript
- AWS SDK for JavaScript
- Amazon S3
- AWS EC2
- Apache HTTP Server
- Ubuntu Linux

---

# Architecture

User → Browser → EC2 Apache Server → AWS S3 Bucket

---

# Project Structure

```bash
project-folder/
│
├── documentation/
│   └── Image gallery report.pdf
│
├── screenshots/
│   ├── Screenshot (14).png
│   └── Screenshot (40).png
│
├── source-code/
│   ├── gallery/
│   │   └── gallery.html
│   │
│   └── image-upload/
│       └── image_upload.html
│
└── README.md
```

---

# AWS Services Used

## Amazon EC2
Used for hosting the website using an Ubuntu-based virtual server.

## Amazon S3
Used for storing uploaded images securely in cloud storage.

## AWS Cognito / IAM
Used for authentication and secure access to AWS resources.

---

# Setup Instructions

## 1. Create an S3 Bucket

- Open AWS S3 Console
- Create a new bucket
- Enable public access if required
- Add bucket policy for image access

---

## 2. Configure AWS Credentials

Replace the following values in the HTML files:

```javascript
AWS.config.region = 'your-region';

IdentityPoolId: 'YOUR_IDENTITY_POOL_ID'

const bucketName = 'your-bucket-name';
```

Example:

```javascript
AWS.config.region = 'ap-south-1';

IdentityPoolId: 'ap-south-1:xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx'

const bucketName = 'my-gallery-bucket';
```

---

## 3. Install Apache on EC2

```bash
sudo apt update
sudo apt install apache2 -y
```

---

## 4. Move Project Files

```bash
sudo cp -r project-folder/* /var/www/html/
```

---

## 5. Restart Apache

```bash
sudo systemctl restart apache2
```

---

# Running the Project

Open the browser and visit:

```bash
http://YOUR_PUBLIC_IP/
```

Gallery Page:

```bash
http://YOUR_PUBLIC_IP/source-code/gallery/gallery.html
```

Upload Page:

```bash
http://YOUR_PUBLIC_IP/source-code/image-upload/image_upload.html
```

---

# Challenges Faced

- Configuring S3 bucket permissions
- Managing CORS policies
- Handling public image access
- AWS authentication setup
- Dynamic image rendering

---

# Learning Outcomes

Through this project, practical experience was gained in:
- Cloud computing
- AWS infrastructure
- Web hosting
- Apache server configuration
- S3 bucket management
- Front-end web development
- Dynamic JavaScript integration

---

# Screenshots

## Upload Interface

![Upload Page](screenshots/Screenshot%20(14).png)

## Gallery Interface

![Gallery Page](screenshots/Screenshot%20(40).png)

---

# Documentation

The complete project report is available inside the `documentation` folder.

```bash
documentation/Image gallery report.pdf
```

---

# Future Enhancements

- User authentication system
- Database integration
- Image categories and tags
- Admin dashboard
- Drag-and-drop uploads
- Image compression and optimization
- Search functionality

---

# Author

**Abhinav BR**  
BCA Student  
Cloud & Web Development Project

---

# License

This project is developed for educational and internship purposes.
