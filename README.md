# 🎯 DigitalOcean App Platform — Deploy Apps Easily from GitHub

**DigitalOcean App Platform** is a modern Platform-as-a-Service (PaaS) that lets you build, deploy, and scale apps directly from your GitHub repo. It handles deployments, HTTPS, scaling, and more automatically.

---

## ✅ Features

* Deploy directly from GitHub, GitLab, or Bitbucket
* Supports static sites, Docker, and popular runtimes (Node.js, Python, PHP, Go, Ruby, etc.)
* Automatic HTTPS with Let’s Encrypt
* Zero-downtime deploys
* Auto scaling (vertical & horizontal)
* Built-in logs & monitoring
* Free tier for static sites

---

## 📦 Getting Started

### Prerequisite: Have your app in a GitHub repo

✅ Make sure your code is pushed to GitHub (or GitLab / Bitbucket).

---

## 🚀 Basic Usage

### 1️⃣ Create an App on DigitalOcean

1. Sign in at [cloud.digitalocean.com](https://cloud.digitalocean.com).
2. Click **Apps** in the sidebar.
3. Click **Create App**.

---

### 2️⃣ Connect your GitHub repo

* Authorize DigitalOcean to access your GitHub account.
* Select the repo and branch you want to deploy.

---

### 3️⃣ Configure your app

* App Platform auto-detects frameworks (Node, PHP, Python, static HTML, etc).
* Customize:

  * **Build command**, e.g.

    ```bash
    npm install
    npm run build
    ```
  * **Run command**, e.g.

    ```bash
    npm start
    ```
  * **Output directory** (for static sites), e.g. `dist` or `build`.

---

### 4️⃣ Set environment variables (optional)

Under **Settings → Environment Variables**, add your keys, API tokens, or config.

---

### 5️⃣ Deploy!

Click **Next → Launch Starter App**.

✅ DigitalOcean will:

* Clone your repo
* Build the app
* Deploy it
* Assign a free URL like:

  ```
  your-app.ondigitalocean.app
  ```
* Set up HTTPS automatically

---

## 🔄 Auto deploy on `git push`

Whenever you push to your configured branch (e.g. `main`), App Platform auto-rebuilds and redeploys.

---

## 🌍 Point your domain to DigitalOcean App

### 📝 Add your custom domain

1. In the App Platform dashboard, go to **Settings → Domains**.
2. Click **Add Domain**.
3. Enter your domain (like `mywebsite.com` or `app.mywebsite.com`).

---

### ⚙️ Update your DNS records

DigitalOcean will show DNS records to add at your domain registrar (e.g. Namecheap, GoDaddy, Cloudflare).

Most common:

| Type  | Name          | Value                                  |
| ----- | ------------- | -------------------------------------- |
| CNAME | www           | `your-app.ondigitalocean.app`          |
| A     | mywebsite.com | IP address or alias target shown by DO |

(For root domains, DigitalOcean may give you **ALIAS** or **A record**, for subdomains it’s typically **CNAME**.)

---

### 🔒 Automatic HTTPS

✅ Once DNS propagates (usually 5–30 min), DigitalOcean automatically provisions an SSL certificate via Let’s Encrypt.
Your dashboard will show:

```
SSL Certificate: Active
```

---

## ✅ Verify everything

Visit:

```bash
https://mywebsite.com
https://www.mywebsite.com
```

You should see your app with a 🔒 secure lock icon.

---

## 🧩 Tips

* Redirect root ↔ www via your DNS provider or by adding redirects in your app.
* Use **DigitalOcean → Logs** to debug build or runtime errors.
* Scale vertically (more RAM/CPU) or horizontally (more instances) anytime.

---

## 📚 More Info

* Docs: [https://docs.digitalocean.com/products/app-platform/](https://docs.digitalocean.com/products/app-platform/)
* Custom domains guide: [https://docs.digitalocean.com/products/app-platform/how-to/manage-domains/](https://docs.digitalocean.com/products/app-platform/how-to/manage-domains/)
* Pricing: [https://www.digitalocean.com/pricing/app-platform](https://www.digitalocean.com/pricing/app-platform)

---

✅ That’s it! You’re now ready to deploy apps from GitHub to DigitalOcean App Platform and run them on your own domain with HTTPS in minutes. 🚀
