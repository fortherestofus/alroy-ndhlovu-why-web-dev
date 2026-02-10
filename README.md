# Why Web Dev? - Personal Portfolio Site

## Project Overview

This is my personal portfolio website explaining why I decided to study web development. I built this site to showcase my journey into web development while demonstrating my growing skills in HTML, CSS, and Bootstrap.

## Technologies Used

- **HTML5** - Semantic markup and structure
- **Bootstrap 5.3.8** - Responsive grid system and components
- **Vanilla CSS** - Custom styling in `style.css`
- **Google Fonts** - Jost font family for modern typography

## Build Process

### 1. Initial Setup

I started by setting up the basic HTML structure with proper meta tags and linking to Bootstrap's CDN. I created a clean, semantic layout with clearly defined sections:

- Navbar
- Hero section
- Features section
- Blog section
- Footer

### 2. Navigation Bar

I implemented a responsive Bootstrap navbar with:
- My logo (`cropped-AN-Favicon.png`) replacing the text brand
- Navigation links to my website and portfolio
- Mobile-responsive hamburger menu

### 3. Hero Section

I created an eye-catching hero section using Bootstrap's grid system:
- Two-column layout (image on right, text on left on desktop)
- Responsive design that stacks on mobile
- My personal photo with fluid image sizing
- Compelling headline and description
- Call-to-action button

### 4. Features Section - Desired Skillset

I built a features grid showcasing my multidisciplinary skillset:
- Four skill cards: Digital Marketing, Branding & Design, Business Tech, and Development
- Custom icons with gradient backgrounds
- Two-column responsive layout
- Carefully adjusted spacing between the section title and content
- There are still some spacing issues that I need to fix

### 5. Blog Section - Blog Posts

I created clickable blog post cards featuring my top articles:
- Three blog post cards with background images
- Each card wrapped in an `<a>` tag for clickability
- Hover effects with smooth transitions
- Cards lift up 8px on hover with enhanced shadow
- Links open in new tabs

**Implementation:** I wrapped each `.card` div with:
```html
<a href="URL" class="card-link" target="_blank">
  <div class="card...">
    <!-- card content -->
  </div>
</a>
```

### 6. Footer

I built a professional footer with:
- Copyright notice
- Centered logo (clickable)
- Navigation links to my website, thought leadership, and portfolio
- Responsive three-column layout

### 7. Custom Branding & Colors

I extracted colors from my logo to create a cohesive brand identity:

**Brand Colors:**
- Orange: `#FF6B35`
- Coral: `#F7931E`
- Teal: `#2C5F5D`
- Dark Teal: `#1A3A3A`
- Brand Gradient: `linear-gradient(135deg, #FF6B35 0%, #F7931E 50%, #2C5F5D 100%)`

I applied these colors to:
- **Primary buttons** - Gradient background with hover lift effect
- **Feature icons** - Gradient backgrounds instead of plain blue
- **Navbar links** - Orange active state, coral hover state
- **All interactive elements** - Consistent brand colors throughout

### 8. Typography

I imported and implemented the **Jost** font from Google Fonts:

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Jost:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

Applied globally in CSS:
```css
body {
  font-family: 'Jost', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}
```

### 9. Custom CSS Overrides

In `style.css`, I created custom styles to enhance Bootstrap's defaults:

**Button Styles:**
- Primary buttons with gradient backgrounds
- Hover effects with translateY and box-shadow
- Smooth 0.3s transitions

**Card Hover Effects:**
```css
.card-link .card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.4) !important;
  cursor: pointer;
}
```

**Icon Styling:**
- Applied brand gradient to all feature icons
- Consistent sizing (3rem x 3rem)

**Navbar Customization:**
- Active link styling with brand orange
- Hover effects with brand coral

**Footer Spacing:**
- Added left and right margins (20px) for better alignment

**Section Headings:**
- Increased font size to 42px for `.pb-2` class

## Key Learning Points

- Combined Bootstrap components with custom CSS for a unique brand identity.
- Mastered CSS variables for easy color management.
- Implemented responsive design across all devices.
- Learned the importance of semantic HTML for accessibility and SEO.

---

**Built with ❤️ by Alroy Ndhlovu**
