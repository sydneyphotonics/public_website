# Sydney Photonics Website

Static website for Sydney Photonics, ready for GitHub Pages deployment.

## Quick Deploy to GitHub Pages

### Option A: Using GitHub Web Interface

1. Create a new repository on GitHub (e.g., `sydneyphotonics.github.io` for a user/org site, or any name for a project site)
2. Upload all files from this folder to the repository
3. Go to **Settings > Pages**
4. Under "Source", select **Deploy from a branch**
5. Select the **main** branch and **/ (root)** folder
6. Click **Save**
7. Your site will be live at `https://yourusername.github.io/repositoryname/` within a few minutes

### Option B: Using Git Command Line

```bash
# Initialise git in this folder
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit"

# Add your GitHub repository as remote
git remote add origin https://github.com/yourusername/your-repo-name.git

# Push to GitHub
git branch -M main
git push -u origin main
```

Then enable GitHub Pages in your repository settings as described above.

## Custom Domain (Optional)

To use a custom domain like `sydneyphotonics.com.au`:

1. In your repository, create a file called `CNAME` containing just your domain:
   ```
   sydneyphotonics.com.au
   ```

2. Configure your domain's DNS:
   - For apex domain (sydneyphotonics.com.au), add these A records:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```
   - For www subdomain, add a CNAME record pointing to `yourusername.github.io`

3. In GitHub Pages settings, enter your custom domain and enable "Enforce HTTPS"

## File Structure

```
├── index.html          # Single-page website with all sections
├── css/
│   └── style.css       # Main stylesheet
├── assets/
│   └── logo.png        # Logo (you need to add this)
└── README.md           # This file
```

## Sections

The single-page site includes these sections with anchor links:
- `#hero` - Hero with animated lantern diagram
- `#products` - Product cards (PL-3, PL-7, PL-19)
- `#technology` - How photonic lanterns work
- `#applications` - Use cases
- `#about` - Company story and founder
- `#contact` - Contact details and quote request info

## Before Going Live

1. **Add your logo**: Place your `logo.png` file in the `assets/` folder
2. **Update email**: The contact email is set to `info@sydneyphotonics.com` - update if different
3. **Test all links**: Click through every page and link
4. **Test on mobile**: Check the site works well on phones
5. **Update meta descriptions**: Each page has a meta description you may want to customise

## Making Changes

Simply edit the HTML files and push to GitHub. Changes will deploy automatically within a few minutes.

For major changes, consider testing locally first by opening `index.html` in your browser.

## Adding a Contact Form

GitHub Pages is static-only, so for a contact form you have two options:

1. **Formspree** (free tier available): Add a form that posts to `https://formspree.io/f/yourformid`
2. **Netlify Forms**: If you deploy to Netlify instead of GitHub Pages
3. **Email link**: The current setup uses a mailto: link which opens the user's email client

## Support

For website issues, the source files can be edited directly. For photonic lantern enquiries, contact info@sydneyphotonics.com.
