# 🌐 sedky.net — AWS-Driven Portfolio Website

This is the source code behind [https://sedky.net](https://sedky.net) — a cloud-native portfolio built to showcase scalable AWS solutions and frontend integrations. It serves as a real-world demonstration of my capabilities in deploying secure, production-grade infrastructure using AWS best practices.

## 💡 Why This Project Exists

This site is part of a structured initiative to sharpen and demonstrate architectural thinking in the AWS ecosystem — beyond certifications or theory. Every service was selected and integrated with intent: performance, security, and maintainability. It reflects the same principles I apply in client-facing environments.

---

## 🔧 Technologies & Tools Used

- **HTML/CSS** — Custom static website design
- **Amazon S3** — Static website hosting
- **Amazon Route 53** — Custom domain registration and DNS management
- **Amazon CloudFront** — Global CDN with HTTPS support
- **AWS ACM** — Free SSL certificate
- **Microsoft 365 (E5)** — Custom domain email with SPF, DKIM, DMARC
- **GitHub + VS Code** — Source control and local development

---

## 🛠️ Step-by-Step Infrastructure Build

### 1. 🔐 IAM & Budgeting
- Created new AWS account
- Created IAM user with secure admin access
- Enabled billing dashboard visibility with monthly budget

### 2. 🌐 Domain & DNS
- Purchased `sedky.net` via Route 53
- Created hosted zone for DNS control

### 3. 🪣 Static Site Hosting
- Created public S3 bucket with website hosting enabled
- Uploaded HTML/CSS files
- Set permissions and policy to allow public read access

### 4. 🚀 CDN + HTTPS
- Created CloudFront distribution pointing to S3
- Issued SSL certificate with ACM (in `us-east-1`)
- Attached certificate to CloudFront
- Set cache behavior and custom error responses

### 5. 🔗 DNS Integration
- Added A/AAAA records in Route 53 pointing to CloudFront distribution
- Verified DNS propagation

### 6. 📧 Email + Deliverability
- Added Microsoft 365 mail exchanger records to Route 53
- Validated domain ownership in Microsoft 365 Admin Center
- Configured and validated:
  - ✅ SPF (`v=spf1 include:spf.protection.outlook.com -all`)
  - ✅ DKIM (2 CNAMEs)
  - ✅ DMARC (`v=DMARC1; p=quarantine; rua=mailto:dmarc@sedky.net`)
- Confirmed deliverability via [mail-tester.com](https://www.mail-tester.com/)

---

## 📱 UI Optimizations

- Mobile-friendly layout
- Responsive grid system
- Dark mode toggle via CSS
- FontAwesome icons
- External links with `target="_blank"` security

---

## 🧠 Key Insights Gained

- Hands-on DNS propagation troubleshooting
- DKIM validation errors resolved through precise CNAME matching
- SSL and S3/CloudFront regional configuration strategies
- Streamlined GitHub and VS Code version control setup
- Benefits of using CloudFront for caching, HTTPS, and edge performance

---

## 🔗 Live Website

[🌐 https://sedky.net](https://sedky.net)

---

## 💼 Next Steps

- Add new AWS projects
- Link GitHub project repos and technical breakdowns
- Add CI/CD pipeline for automated deployment (GitHub Actions + S3 sync)