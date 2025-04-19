# Website Migration Steps

## 1. Content Migration

### Text Content
Copy text content from each Squarespace page to the corresponding section in your new static site:

- Home page content → index.html
- About page content → Create about.html using the index.html template
- Help & Advice → Create help-advice.html using the index.html template
- Contact page → Update contact section in index.html
- News page → Create news.html using the index.html template

### Images
1. Save all images from the Squarespace site to the `/img` folder
2. Create/obtain the following key images:
   - Logo image: save as `/img/logo.png`
   - Hero background: save as `/img/hero-bg.jpg`
   - Any other images referenced in the content

## 2. Final Setup & Testing

1. Update menu links in all HTML files to point to the correct pages
2. Test all internal links to ensure they work correctly
3. Test the site on multiple devices and browsers
4. Make any necessary adjustments to the CSS for proper mobile display

## 3. GitHub Pages Setup

1. Create a GitHub repository
   ```
   git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   git branch -M main
   git push -u origin main
   ```

2. Configure GitHub Pages
   - Go to repository Settings → Pages
   - Source: select "main" branch
   - Save

3. Set up custom domain
   - In GitHub Pages settings, enter: witneyukrainesupport.org
   - Create a CNAME file (already done)
   - Update DNS with your registrar:
     
     A records pointing to GitHub's IP addresses:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
     
     Or CNAME record:
     ```
     www → YOUR-USERNAME.github.io
     ```

## 4. DNS Migration

1. Before changing DNS, make sure the GitHub Pages site is working properly with the GitHub domain
2. Update TTL (Time To Live) on existing DNS records to a short period (e.g., 300 seconds)
3. Obtain DNS information from Squarespace (Support → Advanced → DNS Settings)
4. Update your domain registrar's DNS settings to point to GitHub's servers
5. Wait for DNS propagation (can take up to 24-48 hours)
6. Test accessing your site at witneyukrainesupport.org

## 5. Post-Migration

1. Verify all pages are working correctly
2. Set up Google Analytics or other analytics if needed
3. Consider setting up a contact form using a service like Formspree.io
4. Document the update process for future changes

## External Links

Update any external links that were on the original site, such as:
- Link to the Take Action external form: https://app.sheepcrm.com/witney-ukraine-response/form/627d4cd5eb69263172332b3e/