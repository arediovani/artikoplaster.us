# SS Finishes - Venetian Plaster Website

A modern, elegant Hugo website for SS Finishes, a New York-based Venetian plaster specialist company.

## Features

- **Elegant Design**: Refined aesthetic with custom typography (Cormorant Garamond & Montserrat)
- **Fully Responsive**: Beautiful on all devices from mobile to desktop
- **Smooth Animations**: Fade-in effects, hover states, and scroll-triggered animations
- **Image Gallery**: Interactive gallery with modal lightbox for project photos
- **Contact Form**: Built-in contact form (requires backend integration)
- **Tailwind CSS**: Modern utility-first CSS framework via CDN
- **Performance Optimized**: Lazy loading images, separate gallery page, optimized for bandwidth

### Performance Optimizations

- **Homepage Gallery**: Shows only 4 latest projects to reduce initial load
- **Full Gallery Page**: All 40+ projects available at `/gallery` route
- **Samples Page**: Dedicated page at `/samples` for sample work
- **Lazy Loading**: All images use native lazy loading for better performance
- **Bandwidth Friendly**: Minimizes server load while maintaining beautiful presentation

## Design Philosophy

The design emphasizes:
- **Craftsmanship**: Elegant serif typography and refined spacing
- **Texture**: Subtle noise overlays and layered backgrounds
- **Sophistication**: Muted color palette inspired by natural materials
- **Professionalism**: Clean, uncluttered layouts with purposeful animations

### Color Palette

- Cream (`#F5F1E8`) - Primary background
- Stone (`#A8998C`) - Secondary text
- Charcoal (`#2C2C2C`) - Primary text and accents
- Marble (`#E8DFD3`) - Card backgrounds
- Bronze (`#B87333`) - Accent color
- Sage (`#9CA88C`) - Decorative elements

## Setup Instructions

### Prerequisites

- Hugo Extended (v0.115.0 or later)
- Your project images

### Installation

1. **Install Hugo**
   ```bash
   # macOS
   brew install hugo
   
   # Windows (with Chocolatey)
   choco install hugo-extended
   
   # Linux (Debian/Ubuntu)
   sudo apt-get install hugo
   ```

2. **Clone or download this template**

3. **Add your images**
   
   Place all your project images in the `static/images/` directory. The template is configured to use these images:
   
   ```
   static/images/
   ├── Brooklyn NY.jpeg
   ├── Brooklyn.jpeg
   ├── Downtown Manhattan.jpeg
   ├── Downtown Manhattan 2.jpeg
   ├── Fifth Avenue Manhattan.jpeg
   ├── Fifth Avenue Manhattan 2.jpeg
   ├── Hudson Yard NYC (1).jpeg
   ├── Hudson Yard NYC (2).jpeg
   └── ... (all other images)
   ```

4. **Add your logo** (optional)
   
   Place `LOGO.jpeg` in `static/images/` to use it in the design

5. **Run the development server**
   ```bash
   hugo server -D
   ```
   
   Your site will be available at `http://localhost:1313`

6. **Build for production**
   ```bash
   hugo
   ```
   
   The built site will be in the `public/` directory

## Customization

### Update Company Information

Edit `hugo.toml` to update:
- Phone number
- Email address
- Social media links

### Modify Content

The main content is in `layouts/index.html`. You can edit:
- Mission statement
- Services list
- Business hours
- Project descriptions in the gallery

### Change Colors

Update the CSS variables in `layouts/_default/baseof.html`:

```css
:root {
    --color-cream: #F5F1E8;
    --color-stone: #A8998C;
    --color-charcoal: #2C2C2C;
    --color-marble: #E8DFD3;
    --color-bronze: #B87333;
    --color-sage: #9CA88C;
}
```

### Contact Form Integration

The contact form currently shows an alert. To make it functional, integrate with:

- **Formspree**: Add `action="https://formspree.io/f/YOUR_FORM_ID"` to the form
- **Netlify Forms**: Add `netlify` attribute to the form
- **Custom Backend**: Send form data to your API endpoint

Example with Formspree:
```html
<form id="contactForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

## Deployment

### Netlify

1. Connect your Git repository to Netlify
2. Build command: `hugo`
3. Publish directory: `public`

### Vercel

1. Import your Git repository
2. Framework preset: Hugo
3. Build command: `hugo`
4. Output directory: `public`

### GitHub Pages

1. Build your site: `hugo`
2. Push the `public/` directory to your `gh-pages` branch

## Browser Support

- Chrome/Edge (latest)
- Firefox (latest)
- Safari (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance

- Images use lazy loading
- CSS animations are hardware-accelerated
- Minimal JavaScript for optimal performance
- Tailwind CDN (for production, consider building with Hugo Pipes)

## Structure

```
ss-finishes-hugo/
├── hugo.toml              # Site configuration
├── layouts/
│   ├── _default/
│   │   └── baseof.html    # Base template with head, scripts
│   ├── index.html         # Homepage content
│   ├── gallery.html       # Full gallery page (all projects)
│   └── samples.html       # Samples page (sample work)
├── static/
│   └── images/            # Project images (add your images here)
├── content/
│   ├── _index.md          # Homepage metadata
│   ├── gallery.md         # Gallery page metadata
│   └── samples.md         # Samples page metadata
└── README.md              # Documentation
```

## Pages

- **Homepage** (`/`) - Hero, About, Services (with "View Samples" button), Recent Projects (4 items), Contact
- **Full Gallery** (`/gallery`) - All 40+ project photos
- **Samples** (`/samples`) - Sample work and finishes

## Support

For questions or issues with the template, please contact the developer.

## License

This template is proprietary to SS Finishes.

---

**SS Finishes** - Venetian Plaster Specialists
Serving New York and beyond with handcrafted excellence.
