# 🚀 Static Website Deployment with CI/CD on AWS

This project demonstrates how to automate the deployment of a static website to AWS S3 using GitHub Actions, and accelerate its delivery via CloudFront. The goal is to eliminate manual deployment steps and enable faster, secure, production-ready updates.

> 🔗 **Read the full blog here:** [Medium Blog Post – Coming Soon](#)

---

## 📁 Project Structure

```

.
├── .github/workflows/
│   └── deploy.yml           # GitHub Actions CI/CD pipeline
├── site/
│   ├── index.html           # Main website file
│   └── (other assets)       # CSS, JS, images, etc.
├── README.md

```

---

## ⚙️ What This Project Does

✅ Automatically deploys static files in the `site/` folder to **AWS S3**

✅ Uses **GitHub Actions** to automate build and deployment workflows

✅ Configures **AWS CloudFront** for CDN-level speed and SSL support

✅ Implements **version control + rollback** by tying deployments to commits

✅ Supports **cache invalidation** after each deployment

---

## 🛠️ Tools & Services Used

| Tool            | Purpose                             |
|-----------------|-------------------------------------|
| AWS S3          | Host static website                 |
| AWS CloudFront  | Serve content globally (CDN + SSL)  |
| GitHub Actions  | Automate build and deployment       |
| IAM             | Secure permissions and credentials  |

---

## 🚀 How It Works (CI/CD Flow)

1. **Push code to GitHub**
2. **GitHub Actions** triggers the workflow defined in `.github/workflows/deploy.yml`
3. Website files in the `site/` folder are uploaded to **S3**
4. **CloudFront cache is invalidated** to reflect changes instantly

---

## 🔐 Secrets Required in GitHub

Set the following secrets under your repository settings → Secrets:

- `AWS_ACCESS_KEY_ID`
- `AWS_SECRET_ACCESS_KEY`
- `AWS_REGION` (e.g. `us-east-1`)
- `S3_BUCKET_NAME`
- `CLOUDFRONT_DISTRIBUTION_ID`

---

## 🌐 Live Demo

🔗 [https://d613pmwca2u3u.cloudfront.net](https://d613pmwca2u3u.cloudfront.net)

---

## 📚 Blog Post

> ✍️ A detailed walkthrough is available on Medium.  
> 📌 [**Read the full blog here**](#)

---

## 🤝 Contributing

Feel free to fork this repo and try it with your own AWS setup. Suggestions and PRs are welcome!

---

## 📩 Contact

Made with 💻 by Bhavika Chauhan | bhavika.engineered@gmail.com | bhavika-engineered.kit.com
