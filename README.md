# 🌐 Custom Domain Setup for GitHub Pages and DigitalOcean

## Project URLs

- https://roadmap.sh/projects/custom-domain-setup  
- https://roadmap.sh/projects/github-actions-deployment-workflow  
- https://roadmap.sh/projects/basic-dns  

---

## 📌 Project Overview

This project demonstrates how to configure a **custom domain name** for:

1. **GitHub Pages** hosted via **GitHub Actions**
2. A **DigitalOcean Droplet** serving a static website

It also reinforces **basic DNS concepts** such as A records, CNAME records, and DNS propagation as covered in the *Basic DNS* project.

---

## 🎯 Project Goals

- Understand how domain names and DNS records work
- Configure a custom domain for GitHub Pages
- Point a custom domain or subdomain to a DigitalOcean Droplet
- Learn real-world DNS troubleshooting and validation

---

## 🔑 Prerequisites

Before starting, ensure you have:

- A registered **custom domain**  
  (Cloudflare, Namecheap, GoDaddy, etc.)
- A **GitHub Pages site** deployed using GitHub Actions
- A **DigitalOcean Droplet** serving a static site with NGINX
- Basic understanding of DNS (A, CNAME, TTL)

---

## 🧩 Task 1: Custom Domain for GitHub Pages

### Steps Followed

1. Enabled **GitHub Pages** from repository settings  
   Deployment source set to **GitHub Actions**

2. Added a custom domain in  
   `Settings → Pages`

   Example:
   ```
   www.piratekingdevops.xyz
   ```

3. Configured DNS records at the domain provider:

   **A Records (apex domain):**
   ```
   piratekingdevops.xyz → GitHub Pages IPs
   ```

   **CNAME Record (www subdomain):**
   ```
   www → piratekingDevOps.github.io
   ```

4. Waited for DNS propagation and enabled **HTTPS**

### Result

✅ GitHub Pages site accessible via:

```
https://www.piratekingdevops.xyz
```

---

## 🧩 Task 2: Custom Domain for DigitalOcean Droplet

### Steps Followed

1. Created a DigitalOcean Droplet
2. Installed and configured **NGINX**
3. Served a static site from `/usr/share/nginx/html`
4. Added an **A record** pointing to the Droplet’s public IP:

   ```
   server.piratekingdevops.xyz → <DROPLET_PUBLIC_IP>
   ```

5. Updated NGINX server block to use the custom domain
6. Restarted NGINX and verified in browser

### Result

✅ DigitalOcean static site accessible via:

```
http://server.piratekingdevops.xyz
```

---

## 📚 DNS Concepts Applied (Basic DNS)

- A Records vs CNAME Records
- DNS propagation delay
- Apex domain vs subdomain
- Domain validation and resolution
- Common DNS misconfiguration errors

---

## 🛠 Technologies Used

- GitHub Pages
- GitHub Actions
- DigitalOcean
- NGINX
- DNS (A & CNAME records)
- HTML

---

## ✅ Final Outcome

After completing this project, you should be confident in:

- Setting up custom domains for static sites
- Managing DNS records across providers
- Deploying production-ready static websites
- Debugging DNS and hosting issues

🏴‍☠️ Project completed as part of roadmap.sh DevOps journey.
