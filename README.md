# NovaTech Alpha — Static Site

Static website for [novatechalpha.com](https://novatechalpha.com), hosted on GitHub Pages.

## Pages

| File | URL | Purpose |
|------|-----|---------|
| `index.html` | `/` | Homepage |
| `privacy.html` | `/privacy.html` | Privacy Policy (required for A2P 10DLC) |
| `terms.html` | `/terms.html` | Terms of Service (required for A2P 10DLC) |

## Deploying to GitHub Pages

### 1. Push to GitHub

```bash
git init
git add .
git commit -m "Initial site"
git remote add origin https://github.com/YOUR_USERNAME/novatechalpha.git
git push -u origin main
```

### 2. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages** (left sidebar)
3. Under **Source**, select **Deploy from a branch**
4. Set branch to `main` and folder to `/ (root)`
5. Click **Save**

### 3. Set Custom Domain

1. In **Settings → Pages**, enter `novatechalpha.com` in the **Custom domain** field
2. Click **Save** — GitHub will verify the `CNAME` file automatically

### 4. Configure DNS

Add these records at your domain registrar:

| Type | Name | Value |
|------|------|-------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `YOUR_USERNAME.github.io` |

DNS propagation can take up to 48 hours. GitHub Pages will automatically provision an HTTPS certificate via Let's Encrypt once DNS is verified.

### 5. Enforce HTTPS

After the certificate is issued, go to **Settings → Pages** and check **Enforce HTTPS**.

## Notes

- All pages are publicly accessible with no authentication — required for A2P 10DLC carrier vetting
- The `CNAME` file must remain in the repository root for the custom domain to work
- Contact email: contact@novatechalpha.com
