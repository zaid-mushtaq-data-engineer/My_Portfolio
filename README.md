# Professional Portfolio Website

A fully responsive, modern portfolio website built with vanilla HTML, CSS, and JavaScript. All content is dynamically loaded from JSON files, making it easy to customize without touching the code.

## Features

- **Dynamic Content Loading** - All content loaded from JSON files
- **Responsive Design** - Mobile-first approach, works on all devices
- **Dark Mode Toggle** - With localStorage persistence
- **Project Showcase** - With search and tag filtering
- **Blog System** - With categories, search, and detailed views
- **Skills Section** - Animated progress bars
- **Certificates Display** - Professional certification showcase
- **Contact Form** - Ready for integration with form services
- **Smooth Scrolling** - Enhanced user experience
- **Lazy Loading** - Optimized image loading
- **SEO Friendly** - Semantic HTML structure

## Project Structure

```
portfolio-website/
├── index.html              # Main page
├── blog.html               # Blog detail page
├── css/
│   ├── main.css           # Main styles with CSS variables
│   └── responsive.css     # Responsive styles
├── js/
│   ├── utils.js           # Utility functions
│   ├── dataLoader.js      # JSON data loading
│   ├── renderer.js        # Reusable rendering functions
│   ├── navigation.js      # Navbar functionality
│   ├── hero.js            # Hero section
│   ├── about.js           # About section
│   ├── skills.js          # Skills section
│   ├── projects.js        # Projects section
│   ├── blogs.js           # Blog section
│   ├── certificates.js    # Certificates section
│   ├── contact.js         # Contact section
│   ├── blogDetail.js      # Blog detail page
│   └── main.js            # Main application
├── data/
│   ├── profile.json       # Profile information
│   ├── skills.json        # Skills data
│   ├── projects.json      # Projects data
│   ├── blogs.json         # Blog posts data
│   └── certificates.json  # Certificates data
├── images/                # Image assets
└── README.md             # This file
```

## Getting Started

### 1. Clone or Download

Download the project files to your local machine.

### 2. Customize Content

Edit the JSON files in the `data/` folder to add your own content:

#### profile.json
```json
{
  "name": "Your Name",
  "title": "Your Title",
  "description": "Your description",
  "profileImage": "images/your-photo.jpg",
  "resumeLink": "files/your-resume.pdf",
  "social": {
    "github": "https://github.com/yourusername",
    "linkedin": "https://linkedin.com/in/yourusername",
    "twitter": "https://twitter.com/yourusername"
  }
}
```

#### skills.json
```json
{
  "categories": [
    {
      "name": "Category Name",
      "icon": "icon-name",
      "skills": [
        { "name": "Skill Name", "percentage": 90 }
      ]
    }
  ]
}
```

#### projects.json
```json
{
  "projects": [
    {
      "id": "unique-id",
      "title": "Project Title",
      "description": "Project description",
      "image": "images/projects/project.jpg",
      "tags": ["JavaScript", "React"],
      "demoLink": "https://demo-link.com",
      "githubLink": "https://github.com/username/repo"
    }
  ]
}
```

#### blogs.json
```json
{
  "blogs": [
    {
      "id": "blog-post-id",
      "title": "Blog Title",
      "category": "Category",
      "description": "Short description",
      "image": "images/blogs/blog-image.jpg",
      "date": "2024-01-01",
      "readTime": "5 min read",
      "content": "<p>HTML content here</p>"
    }
  ]
}
```

#### certificates.json
```json
{
  "certificates": [
    {
      "id": "cert-id",
      "title": "Certificate Title",
      "issuer": "Issuing Organization",
      "image": "images/certificates/cert.jpg",
      "link": "https://verify-link.com"
    }
  ]
}
```

### 3. Add Your Images

Place your images in the `images/` folder:
- `profile.jpg` - Your profile photo
- `projects/` - Project screenshots
- `blogs/` - Blog featured images
- `certificates/` - Certificate images

### 4. Test Locally

Open `index.html` in your browser to test the website locally.

**Note:** For the JSON loading to work properly, you need to serve the files through a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then visit `http://localhost:8000`

## GitHub Pages Deployment

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository
2. Name it `yourusername.github.io` (for user site) or any name (for project site)

### Step 2: Push Your Code

```bash
# Initialize git (if not already done)
git init

# Add all files
git add .

# Commit
git commit -m "Initial portfolio website"

# Add remote repository
git remote add origin https://github.com/yourusername/yourusername.github.io.git

# Push to GitHub
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** section (or click Pages in sidebar)
4. Under **Source**, select **Deploy from a branch**
5. Select **main** branch and **/(root)** folder
6. Click **Save**

Your site will be live at `https://yourusername.github.io`

### Step 4: Custom Domain (Optional)

1. In the Pages settings, add your custom domain
2. Create a `CNAME` file in your repository with your domain name
3. Configure DNS settings with your domain provider

## Customization Guide

### Colors and Theme

Edit CSS variables in `css/main.css`:

```css
:root {
  --accent-primary: #3b82f6;    /* Primary color */
  --accent-secondary: #6366f1;  /* Secondary color */
}
```

### Fonts

The website uses Inter font from Google Fonts. To change:

1. Update the Google Fonts link in HTML files
2. Update the font-family in CSS:

```css
body {
  font-family: 'Your Font', sans-serif;
}
```

### Adding New Sections

1. Add HTML structure in `index.html`
2. Create a new JS file in `js/` folder
3. Import the JS file in `index.html`
4. Add styles in `css/main.css`

### Contact Form Integration

The contact form is ready for integration with services like:

#### Formspree
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

#### Netlify Forms
Add `netlify` attribute to the form:
```html
<form name="contact" method="POST" data-netlify="true">
```

#### EmailJS
Follow [EmailJS documentation](https://www.emailjs.com/docs/) to set up email sending.

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance Features

- Lazy loading for images
- Debounced search inputs
- Throttled scroll events
- CSS animations with GPU acceleration
- Minimal JavaScript footprint

## Accessibility

- Semantic HTML structure
- ARIA labels for interactive elements
- Keyboard navigation support
- Color contrast compliance
- Screen reader friendly

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

For issues or questions:
1. Check the browser console for errors
2. Verify JSON file syntax
3. Ensure all file paths are correct
4. Test with a local server

---

**Happy coding!** 🚀
