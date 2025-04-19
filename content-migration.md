# Content Migration Guide

## Steps to Copy Content from Squarespace

1. **Access your Squarespace dashboard**
2. **For each page section on the Squarespace site:**
   - Copy the text content
   - Save any images to the `/img` folder
   - Add the content to the corresponding section in `index.html`

## Common Sections to Migrate
- About Us information
- Contact details
- Support initiatives
- Event information
- News/updates
- Resource links

## Image Migration
Save all images from Squarespace to the `/img` directory and update the HTML to reference them locally:

```html
<img src="img/image-name.jpg" alt="Description of image">
```