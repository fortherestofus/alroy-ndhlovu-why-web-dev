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
- Portfolio section
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

**Spacing Challenge:** I encountered a spacing issue between "Desired Skillset" and "The whole idea..." headings. I fixed this by:

- Reducing bottom margin from `mb-5` to `mb-0`
- Adding controlled top padding `pt-3` to the row
- This brought the gap down from 48px to just 16px
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
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link
  href="https://fonts.googleapis.com/css2?family=Jost:wght@300;400;500;600;700&display=swap"
  rel="stylesheet"
/>
```

Applied globally in CSS:

```css
body {
  font-family:
    "Jost",
    -apple-system,
    BlinkMacSystemFont,
    "Segoe UI",
    sans-serif;
}
```

This gave the site a modern, clean aesthetic with multiple font weights (300-700) available.

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

### Bootstrap Integration

I learned how to effectively use Bootstrap's:

- Grid system (`container`, `row`, `col`)
- Utility classes (`mb-`, `pt-`, `pb-`, `d-flex`, etc.)
- Component classes (navbar, cards, buttons)
- Responsive breakpoints (`col-lg-`, `col-md-`, etc.)

### CSS Custom Properties

I used CSS variables for maintainable color management:

```css
:root {
  --brand-orange: #ff6b35;
  --brand-coral: #f7931e;
  /* etc. */
}
```

### Responsive Design

I ensured the site works across all devices by:

- Using Bootstrap's responsive grid
- Testing mobile-first approach
- Implementing responsive images with `img-fluid`
- Creating mobile-friendly navigation

### Accessibility

I maintained accessibility standards by:

- Using semantic HTML5 elements
- Adding proper `alt` text to images
- Including `aria-label` attributes
- Ensuring keyboard navigation works

## File Structure

```
Alroy Ndhlovu_Why Web Dev/
├── index.html          # Main HTML file
├── css/
│   └── style.css       # Custom CSS overrides
├── images/
│   ├── cropped-AN-Favicon.png
│   ├── alroy.png
│   ├── eggs-in-one-basket.webp
│   ├── pexels-pixabay-159299.jpg
│   └── specialist-vs-generalist.webp
└── README.md           # This file
```

## Design Decisions

1. **Color Palette:** I extracted colors directly from my logo to ensure brand consistency
2. **Typography:** Chose Jost for its modern, geometric aesthetic that matches my brand
3. **Spacing:** Used Bootstrap's spacing utilities with custom overrides where needed
4. **Interactions:** Added subtle hover effects to enhance user engagement
5. **Content:** Wrote authentic, first-person copy explaining my web dev journey

## Challenges & Solutions

### Challenge 1: Spacing Issues

**Problem:** Large gap between "Desired Skillset" heading and content below
**Solution:** Adjusted Bootstrap margin/padding classes from `mb-5` to `mb-0` and added `pt-3`

### Challenge 2: Making Cards Clickable

**Problem:** Blog cards weren't clickable
**Solution:** Wrapped entire card divs in anchor tags with `class="card-link"`

### Challenge 3: Brand Consistency

**Problem:** Default Bootstrap blue didn't match my brand
**Solution:** Created CSS custom properties and overrode Bootstrap's primary color with my gradient

### Challenge 4: Logo Integration

**Problem:** SVG placeholders in navbar and footer
**Solution:** Replaced with actual logo images using `<img>` tags with proper sizing

## Future Enhancements

- Add smooth scroll behavior for navigation links
- Implement dark mode toggle
- Add animation on scroll (AOS library)
- Create a contact form section
- Add more portfolio projects
- Implement a blog section with filtering

## Conclusion

This project taught me the fundamentals of combining Bootstrap's powerful framework with custom CSS to create a unique, branded website. I learned how to override framework defaults, maintain design consistency, and create responsive, accessible web pages. Most importantly, I gained confidence in my ability to build and customize modern websites from scratch.

---

**Built with ❤️ by Alroy Ndhlovu**  
_Learning to code, one project at a time._
