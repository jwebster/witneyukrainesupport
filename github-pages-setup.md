# GitHub Pages Setup Guide

## 1. Create a new GitHub repository
1. Go to https://github.com/new
2. Name your repository (e.g., `ukraine-support-website`)
3. Choose public visibility
4. Click "Create repository"

## 2. Push your local repository
Run these commands in your terminal:

```bash
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git branch -M main
git push -u origin main
```

## 3. Enable GitHub Pages
1. Go to your repository on GitHub
2. Click "Settings"
3. Scroll down to "GitHub Pages" section
4. Under "Source", select "main" branch
5. Click "Save"
6. Wait a few minutes for your site to be published

## 4. Set up a custom domain
1. In GitHub repository settings, under GitHub Pages, enter your domain: witneyukrainesupport.org
2. GitHub will verify the domain
3. Once verified, GitHub Pages will use your custom domain

## 5. Update DNS settings
With your domain registrar, create these DNS records:

### If using an apex domain (witneyukrainesupport.org):
Create these A records pointing to GitHub's servers:
- A: 185.199.108.153
- A: 185.199.109.153
- A: 185.199.110.153
- A: 185.199.111.153

### If using www subdomain:
Create a CNAME record:
- CNAME: www → YOUR-USERNAME.github.io

Wait for DNS changes to propagate (can take up to 24 hours).