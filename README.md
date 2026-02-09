<h1># Static Website Hosting on AWS S3 using Terraform</h1><br>

## 📌 Project Overview
This project demonstrates how to **provision and host a static website on AWS S3 using Terraform**.<br>
The entire infrastructure is created and managed using **Infrastructure as Code (IaC)**, without any manual configuration in the AWS Console.<br>

The website supports:<br>
* Static HTML pages<br>
* CSS for styling<br>
* JavaScript for client-side logic<br>

## 🗂 Project Structure<br>
The repository follows a **clean, modular, and industry-standard structure**:<br>

```
staticterraform/
│
├── main.tf
├── variables.tf
├── outputs.tf
├── terraform.tfvars
├── provider.tf
│
├── index.html
├── error.html
│
├── style.css
│
├── script.js
│
├── .gitignore
└── README.md
```

## 📄 File & Folder Explanation

### 🔹 Terraform Configuration Files

* **provider.tf**
  Defines the AWS provider and the region where resources will be created.

* **variables.tf**
  Declares input variables such as the S3 bucket name and AWS region.

* **terraform.tfvars**
  Stores actual values for the variables (e.g., bucket name, region).

* **main.tf**
  Core Terraform file that:

  * Creates an S3 bucket
  * Configures public access
  * Attaches a bucket policy
  * Enables static website hosting
  * Uploads HTML, CSS, and JavaScript files to S3

* **outputs.tf**
  Displays the S3 static website endpoint after successful deployment.

---

### 🔹 Website Files

* **index.html**
  Main entry point of the website.

* **error.html**
  Custom error page for the website.

* **css/style.css**
  Contains all website styling.

* **js/script.js**
  Contains JavaScript logic for the website.

---

### 🔹 Supporting Files

* **.gitignore**
  Prevents Terraform cache and state files from being pushed to GitHub:

  * `.terraform/`
  * `terraform.tfstate`

* **README.md**
  Project documentation for GitHub.

---

## ⚙️ How It Works

1. Terraform provisions an **AWS S3 bucket**.
2. Public access is configured for static website hosting.
3. A bucket policy allows public read access to website files.
4. Website configuration is enabled with `index.html` and `error.html`.
5. HTML, CSS, and JavaScript files are uploaded automatically to S3.
6. Terraform outputs a **public website URL**.

---

## 🚀 Deployment Steps

### Prerequisites

* AWS CLI configured (`aws configure`)
* Terraform installed

### Commands

```bash
terraform init
terraform apply
```

After deployment, Terraform outputs the **S3 static website URL**, which can be accessed directly from a browser.

---

## 🛡 Best Practices Followed

* Infrastructure as Code (IaC)
* No manual AWS Console changes
* Sensitive and large files excluded using `.gitignore`
* Clean and modular Terraform structure
* GitHub-ready repository

---

## 🧰 Technologies Used

* **Terraform**
* **AWS S3**
* **HTML, CSS, JavaScript**
* **Git & GitHub**

---

## 🎯 Key Takeaway

This project showcases how to **automate static website hosting on AWS** using Terraform in a **professional, scalable, and interview-ready manner**.

---

If you want next-level upgrades, this project can be extended with:
* CloudFront + HTTPS
* Custom domain (Route 53)
* CI/CD using GitHub Actions

