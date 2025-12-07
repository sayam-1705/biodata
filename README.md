# Curriculum Vitae - Portfolio Website

A modern, responsive CV/portfolio website for Sayam Mondal, built with semantic HTML5 and advanced CSS3 animations.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [HTML Elements](#html-elements)
- [CSS Features](#css-features)
- [Responsive Design](#responsive-design)
- [File Structure](#file-structure)
- [Setup & Usage](#setup--usage)

## 🎯 Overview

This project is a professional curriculum vitae website showcasing academic details, technical skills, projects, and social media links. The design emphasizes user experience with smooth animations, hover effects, and full responsiveness across all device sizes.

## ✨ Features

- **Fully Responsive Design**: Optimized for devices from 359px to 1920px+ width
- **Modern UI/UX**: Clean, professional design with smooth animations
- **Accessibility**: Semantic HTML5, ARIA labels, and screen reader support
- **Interactive Elements**: Hover effects, transitions, and animations
- **Cross-browser Compatible**: Works on all modern browsers
- **Performance Optimized**: Lightweight CSS with efficient animations

## 🛠 Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Advanced styling and animations
- **No JavaScript**: Pure CSS interactions
- **No External Libraries**: Vanilla code only

## 📝 HTML Elements

### Semantic Elements

| Element              | Purpose          | Location                                             |
| -------------------- | ---------------- | ---------------------------------------------------- |
| `<header>`           | Main page header | Contains CV title                                    |
| `<section>`          | Content sections | Career objective, academic details, skills, projects |
| `<nav>`              | Navigation       | Social media links                                   |
| `<figure>`           | Photo container  | Profile photograph                                   |
| `<table>`            | Tabular data     | Academic qualifications                              |
| `<thead>`, `<tbody>` | Table structure  | Academic details table                               |
| `<ul>`, `<ol>`       | Lists            | Technical skills (unordered), Projects (ordered)     |
| `<caption>`          | Table caption    | Screen reader accessible table description           |

### Meta Tags & SEO

```html
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta
  name="description"
  content="Curriculum Vitae of Sayam Mondal - B.Tech ECSE Student"
/>
```

### Accessibility Features

- **ARIA Labels**: All social media links have `aria-label` attributes
- **Screen Reader Only Class**: `.sr-only` for table captions
- **Semantic HTML**: Proper heading hierarchy (h1, h2)
- **Alt Text**: Image has descriptive alt attribute
- **Keyboard Navigation**: All interactive elements are accessible

### Link Attributes

- `target="_blank"`: Opens links in new tab
- `rel="noopener noreferrer"`: Security best practice for external links
- `href="mailto:"` and `href="tel:"`: Direct contact methods

## 🎨 CSS Features

### Main Stylesheet (styles.css)

#### 1. **Animations**

| Animation Name   | Purpose             | Duration | Timing Function |
| ---------------- | ------------------- | -------- | --------------- |
| `fadeIn`         | Body entrance       | 0.8s     | ease-in         |
| `fadeInUp`       | Section entrance    | 0.8s     | ease-out        |
| `fadeInLeft`     | Left-side elements  | 0.8s     | ease-out        |
| `fadeInRight`    | Right-side elements | 0.8s     | ease-out        |
| `slideDown`      | Title animation     | 0.6s     | ease-out        |
| `slideInProject` | Project items       | 0.6s     | ease-out        |
| `shimmer`        | Shimmer effect      | -        | -               |

#### 2. **Color Palette**

```css
Primary Dark: #2c3e50
Secondary Dark: #2d3748
Tertiary Dark: #1a202c
Light Gray: #4a5568
Background: #f4f6f9
White: #ffffff
Border: #e2e8f0
```

#### 3. **Typography**

- **Font Family**: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif
- **Heading Sizes**:
  - H1: 36px (mobile: 18-20px)
  - H2: 20px (mobile: 13-15px)
- **Body Text**: 14-15px
- **Line Height**: 1.6-1.8
- **Letter Spacing**: 0.5-2px (headings)

#### 4. **Layout Components**

**Container**:

```css
.cv-container {
  max-width: 850px;
  padding: 50px 60px;
  border-radius: 12px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
}
```

**Top Section** (Flexbox):

```css
.top-section {
  display: flex;
  justify-content: space-between;
}
```

#### 5. **Interactive Effects**

**Hover Transformations**:

- `.cv-container:hover`: Lift effect with shadow
- `.photo-box:hover`: Scale and rotate
- `tr:hover`: Table row highlight
- `th:hover`: Header shimmer effect
- `.social-links a:hover`: Button transformation

**Transition Properties**:

- Color transitions: 0.3s ease
- Transform transitions: 0.3-0.4s ease
- Shadow transitions: 0.3s ease

#### 6. **Pseudo-elements**

| Selector                     | Purpose                      |
| ---------------------------- | ---------------------------- |
| `.cv-container::before`      | Top accent border            |
| `h1::after`                  | Shimmer effect on hover      |
| `.section-title::before`     | Left accent line             |
| `.section-title::after`      | Animated underline           |
| `th::before`                 | Header shimmer effect        |
| `li::before`                 | Hover indicator              |
| `.social-links a::before`    | Button fill animation        |
| `.live-preview-link::before` | Button background transition |
| `.photo-box::before`         | Radial gradient overlay      |

#### 7. **Special Components**

**Profile Photo Box**:

- Fixed dimensions: 155px × 155px
- Border: 2px solid #2c3e50
- Border-radius: 8px
- Hover: Scale(1.06) + rotate(1deg)
- Box shadow with gradient overlay

**Project Links**:

- Flexbox layout with gap
- Inline-flex buttons
- Arrow animation on hover
- Background slide transition

**Social Links**:

- Pill-shaped buttons (border-radius: 25px)
- Slide-in background effect
- Lift animation on hover
- Color inversion

### Responsive Stylesheet (responsive-styles.css)

#### Breakpoint Strategy

| Breakpoint     | Width Range     | Target Devices                   |
| -------------- | --------------- | -------------------------------- |
| Extra Large    | 1920px+         | Large desktops, 4K monitors      |
| Large Desktop  | 1440px - 1919px | Standard desktops                |
| Medium Desktop | 1200px - 1439px | Laptops                          |
| Small Desktop  | 992px - 1199px  | Small laptops                    |
| Tablet         | 768px - 991px   | Tablets (landscape)              |
| Large Mobile   | 576px - 767px   | Tablets (portrait), large phones |
| Medium Mobile  | 480px - 575px   | Standard smartphones             |
| Small Mobile   | 360px - 479px   | Smaller smartphones              |
| Extra Small    | < 360px         | Very small devices               |

#### Responsive Adjustments

**Extra Large Screens (1920px+)**:

- Container: 1200px max-width
- H1: 42px
- Section titles: 22px
- Enhanced padding: 60px 80px

**Tablet (768px - 991px)**:

- Stacked layout (column direction)
- Centered alignment
- Reduced padding: 40px 45px
- Smaller table fonts: 12px

**Mobile (< 576px)**:

- Single column layout
- Flexible photo sizing: 90px - 120px
- Horizontal scrolling tables
- Wrapped social links
- Stacked project items
- Touch-friendly buttons

**Typography Scaling**:

```css
/* Desktop */
h1: 36px → Tablet: 28px → Mobile: 18px

/* Body */
p: 15px → Tablet: 13px → Mobile: 11px
```

#### Mobile Optimizations

1. **Touch Targets**: Minimum 44px × 44px tap areas
2. **Horizontal Scroll**: Tables scroll horizontally on small screens
3. **Flexible Images**: Photo box scales proportionally
4. **Readable Text**: Minimum 11px font size
5. **Spacing**: Reduced margins and padding
6. **Word Breaking**: `word-break: break-word` for long URLs

## 📱 Responsive Design

### Layout Changes by Screen Size

**Desktop (> 992px)**:

- Horizontal flex layout
- Photo on the right
- Full-width tables
- Inline social links

**Tablet (768px - 991px)**:

- Vertical stacked layout
- Centered photo
- Reduced padding
- Wrapped content

**Mobile (< 768px)**:

- Single column
- Full-width elements
- Stacked project layout
- 2-column social links grid
- Compact spacing

## 📁 File Structure

```
AD Lab/
├── index.html                 # Main HTML structure
├── styles.css                 # Core styles and animations
├── responsive-styles.css      # Media queries and responsive design
├── FrontFace.jpg             # Profile photograph
└── README.md                  # This documentation
```

## 🚀 Setup & Usage

### Clone the Repository

```bash
# Clone this repository
git clone https://github.com/sayam-1705/biodata.git

# Navigate to the project directory
cd biodata
```

### Local Development

1. **Open the project**:

   - Simply double-click `index.html` to open in your default browser
   - OR right-click `index.html` → Open with → Choose your browser

2. **Using Live Server** (Recommended for development):

   - Install [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code
   - Right-click on `index.html` and select "Open with Live Server"
   - The website will open at `http://127.0.0.1:5500`

3. **No build process required** - pure HTML/CSS, ready to use!

### Customization

#### Update Personal Information:

Edit the content in `index.html`:

- Name, contact details, and links
- Academic qualifications
- Technical skills
- Projects
- Social media links

#### Modify Colors:

Change color variables in `styles.css`:

```css
/* Primary colors */
#2c3e50  /* Dark blue-gray */
#2d3748  /* Text dark */
#f4f6f9  /* Background */
```

#### Adjust Breakpoints:

Modify media queries in `responsive-styles.css` to fit your needs.

## 📄 License

This project is open source and available for personal use.

## 👤 Author

**Sayam Mondal**

- Email: sayam2022mondal@gmail.com
- GitHub: [@sayam-1705](https://github.com/sayam-1705)
- LinkedIn: [mondalsayam](https://www.linkedin.com/in/mondalsayam/)

## 🙏 Acknowledgments

- Design inspired by modern CV templates
- Built with semantic HTML5 best practices
- Responsive design following mobile-first principles

---

**Last Updated**: December 2024
**Version**: 1.0.0
