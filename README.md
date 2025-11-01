# Test Calgary Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing the Test Calgary certification exam prep landing page.

---

## Table of Contents

1. [Overview](#overview)
2. [File Structure](#file-structure)
3. [Updating Text Content](#updating-text-content)
4. [Tailwind CSS Classes Explained](#tailwind-css-classes-explained)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Color Customization](#color-customization)
8. [Responsive Design Adjustments](#responsive-design-adjustments)
9. [Troubleshooting](#troubleshooting)
10. [Best Practices](#best-practices)

---

## Overview

The Test Calgary landing page is a modern, responsive website built with:

- **HTML5**: Semantic markup structure
- **Tailwind CSS**: Utility-first CSS framework (via CDN)
- **Font Awesome**: Icon library for visual elements
- **Vanilla JavaScript**: Mobile menu and smooth scrolling functionality

The page is designed to be easily customizable without requiring deep coding knowledge. All styling uses Tailwind CSS classes, making changes straightforward and maintainable.

### Key Features of This Landing Page

- **Sticky Navigation Header**: Remains visible while scrolling
- **Hero Section**: Eye-catching introduction with gradient effects
- **Features Section**: 6 feature cards with hover animations
- **Benefits Section**: 6 key benefits with icon indicators
- **Social Proof**: Statistics and testimonials
- **About Section**: Company information
- **Call-to-Action**: Multiple conversion opportunities
- **Responsive Design**: Works perfectly on mobile, tablet, and desktop
- **Mobile Menu**: Hamburger menu for smaller screens

---

## File Structure

Your project should be organized like this:

```
project-folder/
├── index.html                 (Main landing page)
├── privacy.html              (Privacy policy page)
├── terms.html                (Terms of service page)
├── blog.html                 (Blog page - optional)
├── css/
│   └── custom.css            (Optional custom styles)
└── images/
    └── (your image files)
```

**Note**: The current landing page uses Tailwind CSS via CDN, so you don't need a separate CSS file unless you want to add custom styles beyond Tailwind's capabilities.

---

## Updating Text Content

### Understanding the HTML Structure

Before making changes, understand how the page is organized:

```
<section id="features">        ← Each major section has an ID
    <h2>...</h2>              ← Main heading
    <p>...</p>                ← Paragraph text
    <h3>...</h3>              ← Subheadings
</section>
```

### 1. Updating the Hero Section (Main Headline)

**Location**: Lines 99-105

**Current Code**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6">
    <span class="gradient-text">Unlock Your Potential:</span> Ace Your Calgary Certification Exams
</h1>
```

**How to Update**:

1. Open `index.html` in a text editor (Notepad, VS Code, or any code editor)
2. Find the line starting with `<h1 class="text-4xl...`
3. Replace the text between `>` and `</h1>` with your new headline
4. Keep the `<span class="gradient-text">` tags around the part you want in purple gradient color

**Example**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight mb-6">
    <span class="gradient-text">Transform Your Future:</span> Master Your Professional Exams Today
</h1>
```

**What Changed**: The headline and the gradient-colored portion were updated while preserving all styling.

---

### 2. Updating the Hero Subtitle (Descriptive Paragraph)

**Location**: Lines 107-109

**Current Code**:
```html
<p class="text-lg md:text-xl text-gray-700 leading-relaxed mb-8">
    Stop feeling anxious and start feeling confident. We provide the proven resources and expert support you need to conquer any Calgary certification test. <span class="font-semibold text-purple-600">Guaranteed.</span>
</p>
```

**How to Update**:

1. Find the `<p>` tag that contains this text
2. Replace the text while keeping the HTML tags intact
3. To make specific words bold and purple, wrap them in: `<span class="font-semibold text-purple-600">YOUR TEXT</span>`

**Example**:
```html
<p class="text-lg md:text-xl text-gray-700 leading-relaxed mb-8">
    Join thousands of certified professionals who transformed their careers. We provide comprehensive study materials and expert guidance to help you succeed. <span class="font-semibold text-purple-600">100% Success Focused.</span>
</p>
```

---

### 3. Updating Feature Section Titles and Descriptions

**Location**: Lines 200-250 (Features Section)

Each feature card follows this structure:

```html
<div class="hover-lift bg-gradient-to-br from-white to-purple-50 rounded-2xl p-8 border border-purple-100">
    <div class="w-14 h-14 bg-gradient-to-br from-purple-600 to-pink-600 rounded-xl flex items-center justify-center mb-6">
        <i class="fas fa-chart-line text-white text-2xl"></i>
    </div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Personalized Study Plans</h3>
    <p class="text-gray-700 leading-relaxed mb-4">
        Our intelligent adaptive learning system...
    </p>
    <ul class="space-y-2 text-gray-600">
        <li class="flex items-start gap-2">
            <i class="fas fa-check text-green-500 mt-1 flex-shrink-0"></i>
            <span>AI-powered assessment technology</span>
        </li>
    </ul>
</div>
```

**How to Update a Feature Card**:

1. Find the feature card you want to update (each card starts with `<div class="hover-lift...`)
2. Update the `<h3>` text (the feature title)
3. Update the `<p>` text (the description)
4. Update each `<li>` item in the list (the bullet points)

**Example - Changing "Personalized Study Plans"**:

```html
<h3 class="text-2xl font-bold text-gray-900 mb-4">Customized Learning Paths</h3>
<p class="text-gray-700 leading-relaxed mb-4">
    Our advanced AI analyzes your learning style and creates a study plan tailored just for you.
</p>
<ul class="space-y-2 text-gray-600">
    <li class="flex items-start gap-2">
        <i class="fas fa-check text-green-500 mt-1 flex-shrink-0"></i>
        <span>Smart learning algorithms</span>
    </li>
    <li class="flex items-start gap-2">
        <i class="fas fa-check text-green-500 mt-1 flex-shrink-0"></i>
        <span>Adaptive difficulty scaling</span>
    </li>
    <li class="flex items-start gap-2">
        <i class="fas fa-check text-green-500 mt-1 flex-shrink-0"></i>
        <span>Live progress monitoring</span>
    </li>
</ul>
```

**Important**: Keep all the `class` attributes exactly as they are. Only change the text content.

---

### 4. Updating Testimonials

**Location**: Lines 400-450 (Testimonials Section)

Each testimonial card has this structure:

```html
<div class="hover-lift bg-white rounded-2xl p-8 border border-gray-200 shadow-md transition-all duration-300">
    <div class="flex items-center gap-1 mb-4">
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
        <i class="fas fa-star text-yellow-400"></i>
    </div>
    <p class="text-gray-700 leading-relaxed mb-6">
        "I was so overwhelmed by the amount of material..."
    </p>
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Sarah Chen</p>
        <p class="text-sm text-gray-600">Project Manager, ATCO Energy</p>
    </div>
</div>
```

**How to Update a Testimonial**:

1. Find the testimonial card you want to change
2. Update the quoted text (between the `<p>` tags)
3. Update the person's name (in the `<p class="font-bold...">` tag)
4. Update their title and company (in the `<p class="text-sm text-gray-600">` tag)

**Example**:

```html
<p class="text-gray-700 leading-relaxed mb-6">
    "Test Calgary's structured approach helped me prepare efficiently. I completed my certification in just 6 weeks and scored in the top 10%!"
</p>
<div class="border-t border-gray-200 pt-4">
    <p class="font-bold text-gray-900">Jessica Williams</p>
    <p class="text-sm text-gray-600">Business Analyst, Suncor Energy</p>
</div>
```

---

### 5. Updating Statistics (Trust Indicators)

**Location**: Lines 115-140 (Hero Section) and Lines 360-380 (Trust Section)

**Hero Section Stats**:
```html
<div class="flex items-center gap-3">
    <div class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center">
        <i class="fas fa-check text-green-600 text-xl"></i>
    </div>
    <div>
        <p class="font-bold text-lg text-gray-900">94% Pass Rate</p>
        <p class="text-sm text-gray-600">Our proven success rate</p>
    </div>
</div>
```

**How to Update**:

1. Change the percentage or number in the bold line
2. Update the description below it

**Example**:
```html
<p class="font-bold text-lg text-gray-900">96% Pass Rate</p>
<p class="text-sm text-gray-600">Industry-leading success rate</p>
```

---

### 6. Updating Meta Tags (SEO Information)

**Location**: Lines 5-8 (Head Section)

These tags help search engines understand your page:

```html
<meta name="description" content="Master Calgary certification exams with personalized study plans, expert-led tutorials, and proven success strategies. Join 94% of our users who pass on their first try.">
<meta name="keywords" content="Calgary certification, exam prep, study guides, certification exams, professional development">
<meta name="author" content="Test Calgary">
<title>Unlock Your Potential: Ace Your Calgary Certification Exams</title>
```

**How to Update**:

1. **Description**: Update the text to summarize your page (150-160 characters is ideal)
2. **Keywords**: Add relevant search terms separated by commas
3. **Author**: Change to your company name
4. **Title**: Update the browser tab title

**Example**:
```html
<meta name="description" content="Ace your professional certification with our comprehensive study platform. Expert instructors, practice exams, and personalized learning paths.">
<meta name="keywords" content="certification exam prep, professional development, study materials, exam practice">
<meta name="author" content="Your Company Name">
<title>Professional Certification Exam Prep - Expert Training</title>
```

---

## Tailwind CSS Classes Explained

### Understanding Tailwind CSS

Tailwind CSS uses utility classes to style elements. Instead of writing custom CSS, you combine predefined classes. Here are the most important ones used on this landing page:

### Text and Font Classes

| Class | Effect |
|-------|--------|
| `text-4xl` | Extra large text (48px) |
| `text-5xl` | Even larger text (64px) |
| `text-6xl` | Largest text (72px) |
| `text-lg` | Large text (18px) |
| `text-xl` | Extra large text (20px) |
| `font-bold` | Bold text |
| `font-semibold` | Semi-bold text |
| `text-gray-900` | Dark gray text |
| `text-gray-700` | Medium gray text |
| `text-gray-600` | Light gray text |
| `text-white` | White text |
| `text-purple-600` | Purple text |
| `text-pink-600` | Pink text |

**Example**: To make text larger and bold:
```html
<!-- Before -->
<p class="text-lg">Welcome to Test Calgary</p>

<!-- After -->
<p class="text-2xl font-bold">Welcome to Test Calgary</p>
```

### Spacing Classes

| Class | Effect |
|-------|--------|
| `mb-6` | Margin-bottom: 24px (space below element) |
| `mb-8` | Margin-bottom: 32px |
| `mt-6` | Margin-top: 24px (space above element) |
| `px-4` | Padding left and right: 16px (internal space) |
| `py-6` | Padding top and bottom: 24px |
| `gap-4` | Space between flex items: 16px |
| `space-y-2` | Space between stacked items: 8px |

**Example**: To add more space below a heading:
```html
<!-- Before: mb-4 (16px) -->
<h2 class="text-4xl font-bold mb-4">Features</h2>

<!-- After: mb-8 (32px) -->
<h2 class="text-4xl font-bold mb-8">Features</h2>
```

### Background and Color Classes

| Class | Effect |
|-------|--------|
| `bg-white` | White background |
| `bg-gray-900` | Dark gray background |
| `bg-purple-600` | Purple background |
| `bg-gradient-to-r` | Gradient from left to right |
| `from-purple-600` | Gradient starting color |
| `to-pink-600` | Gradient ending color |
| `bg-purple-50` | Very light purple background |

**Example**: To change a button's gradient color:
```html
<!-- Before: Purple to pink gradient -->
<a class="bg-gradient-to-r from-purple-600 to-pink-600">Get Started</a>

<!-- After: Blue to purple gradient -->
<a class="bg-gradient-to-r from-blue-600 to-purple-600">Get Started</a>
```

### Layout Classes

| Class | Effect |
|-------|--------|
| `grid` | Creates a grid layout |
| `grid-cols-1` | 1 column on mobile |
| `md:grid-cols-2` | 2 columns on medium screens |
| `lg:grid-cols-3` | 3 columns on large screens |
| `flex` | Creates a flexbox layout |
| `flex-col` | Stack items vertically |
| `items-center` | Center items vertically |
| `justify-between` | Space items apart horizontally |
| `max-w-7xl` | Maximum width container (1280px) |
| `mx-auto` | Center container horizontally |

**Example**: To change a 3-column grid to 2 columns:
```html
<!-- Before: 3 columns on large screens -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

<!-- After: 2 columns on large screens -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
```

### Hover and Transition Classes

| Class | Effect |
|-------|--------|
| `hover:text-purple-600` | Change to purple on hover |
| `hover:bg-purple-50` | Change background on hover |
| `hover:shadow-lg` | Add shadow on hover |
| `transition-all` | Smooth animation for all changes |
| `duration-300` | Animation takes 300ms |

**Example**: To change hover effect on a button:
```html
<!-- Before -->
<button class="hover:shadow-lg hover:scale-105 transition-all duration-300">

<!-- After: Slower animation -->
<button class="hover:shadow-lg hover:scale-110 transition-all duration-500">
```

### Responsive Classes (Mobile-First)

Tailwind uses prefixes to apply styles at different screen sizes:

| Prefix | Screen Size |
|--------|-------------|
| (none) | Mobile (all sizes) |
| `sm:` | Small: 640px and up |
| `md:` | Medium: 768px and up |
| `lg:` | Large: 1024px and up |
| `xl:` | Extra Large: 1280px and up |

**Example**: To hide something on mobile but show on larger screens:
```html
<!-- Hidden on mobile, shown on medium screens and up -->
<div class="hidden md:flex">This shows on tablets and desktops</div>

<!-- Text size changes based on screen -->
<h1 class="text-2xl md:text-4xl lg:text-6xl">Responsive Heading</h1>
```

### Practical Customization Examples

**Example 1: Making a Section Background Darker**
```html
<!-- Before: Light purple background -->
<section class="bg-gradient-to-br from-purple-50 via-white to-pink-50">

<!-- After: Darker purple background -->
<section class="bg-gradient-to-br from-purple-100 via-purple-50 to-pink-100">
```

**Example 2: Increasing Padding in Feature Cards**
```html
<!-- Before: p-8 (32px padding) -->
<div class="rounded-2xl p-8 border">

<!-- After: p-12 (48px padding) -->
<div class="rounded-2xl p-12 border">
```

**Example 3: Changing Text Size for Mobile**
```html
<!-- Before: Same size on all devices -->
<h2 class="text-4xl font-bold">Features</h2>

<!-- After: Smaller on mobile, larger on desktop -->
<h2 class="text-2xl md:text-4xl lg:text-5xl font-bold">Features</h2>
```

---

## Fixing and Managing Links

### Understanding Links in This Landing Page

The landing page contains several types of links:

1. **Navigation Links**: In the header (sticky at top)
2. **Call-to-Action Links**: Buttons throughout the page
3. **Footer Links**: Navigation and policy links at bottom
4. **Anchor Links**: Links that jump to sections on the same page

### Finding All Links

All links in HTML use the `<a>` tag. Search for `href=` to find every link:

```html
<a href="URL_HERE">Link Text</a>
```

### 1. Main Navigation Links (Header)

**Location**: Lines 46-52 (Desktop Menu) and Lines 58-66 (Mobile Menu)

**Current Code**:
```html
<!-- Desktop Navigation -->
<a href="#features" class="text-gray-700 hover:text-purple-600...">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-purple-600...">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-purple-600...">Testimonials</a>
<a href="#about" class="text-gray-700 hover:text-purple-600...">About</a>
<a href="https://example.com" class="px-6 py-2 bg-gradient...">Get Started</a>
```

**What These Links Do**:
- `#features` - Jumps to the Features section
- `#benefits` - Jumps to the Benefits section
- `#testimonials` - Jumps to the Testimonials section
- `#about` - Jumps to the About section
- `https://example.com` - **PLACEHOLDER** - Goes to your signup page

**How to Update the "Get Started" Button**:

The "Get Started" button appears in 4 places:

1. **Header Navigation** (Line 51)
2. **Hero Section** (Line 111)
3. **CTA Section** (Line 520)
4. **Footer** (Line 570)

**Step-by-Step: Update All "Get Started" Links**

1. Open `index.html`
2. Use Find & Replace (Ctrl+H or Cmd+H in most editors)
3. Find: `https://example.com`
4. Replace with: `https://yourwebsite.com/signup` (or your actual URL)
5. Click "Replace All"

**Example**:
```html
<!-- Before -->
<a href="https://example.com" class="px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600...">
    Get Started
</a>

<!-- After -->
<a href="https://yoursite.com/signup" class="px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600...">
    Get Started
</a>
```

**Verification**: After replacing, test each button to ensure they all link to the correct page.

---

### 2. Footer Links

**Location**: Lines 540-600 (Footer Section)

The footer contains several link sections:

**Quick Links Section** (Lines 555-562):
```html
<li><a href="#features" class="text-gray-400 hover:text-purple-400...">Features</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-purple-400...">Benefits</a></li>
<li><a href="#testimonials" class="text-gray-400 hover:text-purple-400...">Testimonials</a></li>
<li><a href="#about" class="text-gray-400 hover:text-purple-400...">About Us</a></li>
```

**These are already correct** - they link to sections on the same page.

**Resources Section** (Lines 565-572):
```html
<li><a href="blog.html" class="text-gray-400 hover:text-purple-400...">Blog</a></li>
<li><a href="privacy.html" class="text-gray-400 hover:text-purple-400...">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-purple-400...">Terms of Service</a></li>
<li><a href="#" class="text-gray-400 hover:text-purple-400...">Contact Support</a></li>
```

**What Needs to be Fixed**:
- `blog.html` - Link to your blog page
- `privacy.html` - **NEEDS TO BE CREATED** (see next section)
- `terms.html` - **NEEDS TO BE CREATED** (see next section)
- `#` (Contact Support) - Should link to contact form or email

**How to Update Footer Links**:

1. **Contact Support Link** - Change to email or contact form:
```html
<!-- Before -->
<li><a href="#" class="text-gray-400 hover:text-purple-400...">Contact Support</a></li>

<!-- After: Email link -->
<li><a href="mailto:support@yoursite.com" class="text-gray-400 hover:text-purple-400...">Contact Support</a></li>

<!-- Or: Link to contact form -->
<li><a href="contact.html" class="text-gray-400 hover:text-purple-400...">Contact Support</a></li>
```

2. **Blog Link** - If you don't have a blog yet:
```html
<!-- Option 1: Remove the link -->
<!-- Remove this entire line -->

<!-- Option 2: Link to external blog -->
<li><a href="https://medium.com/yourprofile" class="text-gray-400 hover:text-purple-400...">Blog</a></li>

<!-- Option 3: Link to your blog page -->
<li><a href="blog.html" class="text-gray-400 hover:text-purple-400...">Blog</a></li>
```

---

### 3. Email Link

**Location**: Line 580

```html
<p class="text-gray-400 mb-4">
    <i class="fas fa-envelope mr-2"></i>
    <a href="mailto:test@test.com" class="hover:text-purple-400...">test@test.com</a>
</p>
```

**How to Update**:

Replace `test@test.com` with your actual email address:

```html
<a href="mailto:support@yourcompany.com" class="hover:text-purple-400...">support@yourcompany.com</a>
```

---

### 4. Social Media Links

**Location**: Lines 583-600

```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full...">
    <i class="fab fa-facebook-f"></i>
</a>
```

**Current Status**: All social links use `href="#"` which means they don't go anywhere.

**How to Update**:

1. **Facebook**:
```html
<!-- Before -->
<a href="#" class="w-10 h-10 bg-gray-800...">

<!-- After -->
<a href="https://facebook.com/yourpage" class="w-10 h-10 bg-gray-800..." target="_blank">
```

2. **Twitter**:
```html
<a href="https://twitter.com/yourhandle" class="w-10 h-10 bg-gray-800..." target="_blank">
```

3. **LinkedIn**:
```html
<a href="https://linkedin.com/company/yourcompany" class="w-10 h-10 bg-gray-800..." target="_blank">
```

4. **Instagram**:
```html
<a href="https://instagram.com/yourprofile" class="w-10 h-10 bg-gray-800..." target="_blank">
```

**Important**: Always add `target="_blank"` to external links so they open in a new tab.

---

### 5. Bottom Footer Links

**Location**: Lines 605-615

```html
<a href="privacy.html" class="text-gray-400 hover:text-purple-400...">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-purple-400...">Terms of Service</a>
<a href="blog.html" class="text-gray-400 hover:text-purple-400...">Blog</a>
```

These are duplicates of the footer links above and will be fixed when you create the policy pages (see next section).

---

### Troubleshooting Links

**Problem**: Link doesn't work
**Solution**: 
- Check for typos in the URL
- For internal pages (like `privacy.html`), ensure the file exists in the same folder
- For external URLs, include `https://` at the beginning

**Problem**: Link opens in same tab instead of new tab
**Solution**:
- Add `target="_blank"` to external links
- Example: `<a href="https://example.com" target="_blank">Link</a>`

**Problem**: Anchor link doesn't scroll to section
**Solution**:
- Ensure the section has an `id` attribute matching the link
- Example: Link is `href="#features"` → Section should be `<section id="features">`

---

## Adding Privacy and Terms Pages

### Understanding Why These Pages Are Important

Privacy Policy and Terms of Service pages are:
- **Legally required** in most jurisdictions
- **Trust builders** for your users
- **SEO beneficial** for search engines
- **Already linked** in your footer

### Step 1: Create the Privacy Policy Page

**Create a new file** called `privacy.html` in the same folder as `index.html`.

**Copy this template**:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Test Calgary">
    <title>Privacy Policy - Test Calgary</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-graduation-cap text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold gradient-text">Test Calgary</a>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Testimonials</a>
                <a href="index.html#about" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">About</a>
                <a href="https://yoursite.com/signup" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg hover:shadow-lg hover:scale-105 transition-all duration-300 font-semibold">Get Started</a>
            </div>
            
            <button class="md:hidden mobile-menu-button p-2 text-gray-700 hover:text-purple-600 transition-colors duration-300">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 lg:py-32 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold mb-8 gradient-text">Privacy Policy</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2025</p>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Introduction</h2>
                <p>Test Calgary ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Information We Collect</h2>
                <p>We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>Personal Data:</strong> Name, email address, phone number, and other contact information you voluntarily provide.</li>
                    <li><strong>Account Information:</strong> Username, password, and profile information.</li>
                    <li><strong>Usage Data:</strong> Information about how you interact with our platform, including study progress and exam scores.</li>
                    <li><strong>Device Information:</strong> Browser type, IP address, and operating system.</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. How We Use Your Information</h2>
                <p>We use the information we collect in the following ways:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>To provide, maintain, and improve our services</li>
                    <li>To process transactions and send related information</li>
                    <li>To send promotional communications (with your consent)</li>
                    <li>To respond to your inquiries and support requests</li>
                    <li>To monitor and analyze usage patterns and trends</li>
                    <li>To comply with legal obligations</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Data Security</h2>
                <p>We implement appropriate technical and organizational measures to protect your personal data against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet is 100% secure.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Third-Party Links</h2>
                <p>Our website may contain links to third-party websites. We are not responsible for the privacy practices of other sites. We encourage you to review their privacy policies before providing any personal information.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Your Rights</h2>
                <p>Depending on your location, you may have certain rights regarding your personal data, including:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Right to access your data</li>
                    <li>Right to correct inaccurate data</li>
                    <li>Right to request deletion of your data</li>
                    <li>Right to opt-out of marketing communications</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">7. Contact Us</h2>
                <p>If you have questions about this Privacy Policy or our privacy practices, please contact us at:</p>
                <p class="ml-4">
                    <strong>Test Calgary</strong><br>
                    Email: privacy@testcalgary.com<br>
                    Address: Calgary, Alberta, Canada
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-6">
                        <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-graduation-cap text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-white">Test Calgary</span>
                    </div>
                    <p class="text-gray-400">Empowering professionals to achieve their certification goals.</p>
                </div>
                
                <div>
                    <h4 class="text-white font-bold text-lg mb-6">Quick Links</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Testimonials</a></li>
                        <li><a href="index.html#about" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">About Us</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold text-lg mb-6">Resources</h4>
                    <ul class="space-y-3">
                        <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Blog</a></li>
                        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
                        <li><a href="mailto:support@testcalgary.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Contact Support</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold text-lg mb-6">Connect With Us</h4>
                    <p class="text-gray-400 mb-4">
                        <i class="fas fa-envelope mr-2"></i>
                        <a href="mailto:support@testcalgary.com" class="hover:text-purple-400 transition-colors duration-300">support@testcalgary.com</a>
                    </p>
                    <div class="flex gap-4">
                        <a href="https://facebook.com" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300" target="_blank">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="https://twitter.com" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300" target="_blank">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="https://linkedin.com" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300" target="_blank">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="https://instagram.com" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300" target="_blank">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </div>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center gap-4">
                    <p class="text-gray-400 text-sm">
                        &copy; 2025 Test Calgary. All rights reserved.
                    </p>
                    <div class="flex gap-6">
                        <a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Privacy Policy</a>
                        <a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Terms of Service</a>
                        <a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Blog</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                });
            }
        });
    </script>
</body>
</html>
```

**Important Changes to Make**:

1. Update the email address:
```html
<!-- Change this -->
Email: privacy@testcalgary.com

<!-- To this -->
Email: your-actual-email@yourcompany.com
```

2. Update the physical address:
```html
<!-- Change this -->
Address: Calgary, Alberta, Canada

<!-- To this -->
Address: Your actual address
```

3. Update your company name if different:
```html
<!-- Change all instances of "Test Calgary" to your company name -->
```

---

### Step 2: Create the Terms of Service Page

**Create a new file** called `terms.html` in the same folder as `index.html`.

**Copy this template**:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Test Calgary">
    <title>Terms of Service - Test Calgary</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .gradient-text {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header Navigation (Same as index.html) -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center space-x-2">
                <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                    <i class="fas fa-graduation-cap text-white text-lg"></i>
                </div>
                <a href="index.html" class="text-xl font-bold gradient-text">Test Calgary</a>
            </div>
            
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html#features" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Features</a>
                <a href="index.html#benefits" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Benefits</a>
                <a href="index.html#testimonials" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">Testimonials</a>
                <a href="index.html#about" class="text-gray-700 hover:text-purple-600 transition-colors duration-300 font-medium">About</a>
                <a href="https://yoursite.com/signup" class="px-6 py-2 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-lg hover:shadow-lg hover:scale-105 transition-all duration-300 font-semibold">Get Started</a>
            </div>
            
            <button class="md:hidden mobile-menu-button p-2 text-gray-700 hover:text-purple-600 transition-colors duration-300">
                <i class="fas fa-bars text-2xl"></i>
            </button>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 lg:py-32 bg-white">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold mb-8 gradient-text">Terms of Service</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2025</p>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <h2 class="text-2xl font-bold text-gray-900 mt-8">1. Agreement to Terms</h2>
                <p>By accessing and using the Test Calgary website and services, you accept and agree to be bound by and comply with these Terms and Conditions. If you do not agree to abide by the above, please do not use this service.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">2. Use License</h2>
                <p>Permission is granted to temporarily download one copy of the materials (information or software) on Test Calgary for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:</p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the site</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                </ul>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">3. Disclaimer</h2>
                <p>The materials on Test Calgary are provided on an 'as is' basis. Test Calgary makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">4. Limitations</h2>
                <p>In no event shall Test Calgary or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on the site, even if Test Calgary or an authorized representative has been notified orally or in writing of the possibility of such damage.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">5. Accuracy of Materials</h2>
                <p>The materials appearing on Test Calgary could include technical, typographical, or photographic errors. Test Calgary does not warrant that any of the materials on its website are accurate, complete, or current. Test Calgary may make changes to the materials contained on its website at any time without notice.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">6. Links</h2>
                <p>Test Calgary has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Test Calgary of the site. Use of any such linked website is at the user's own risk.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">7. Modifications</h2>
                <p>Test Calgary may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">8. Governing Law</h2>
                <p>These terms and conditions are governed by and construed in accordance with the laws of Alberta, Canada, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">9. User Accounts</h2>
                <p>If you create an account on our website, you are responsible for maintaining the confidentiality of your account information and password and for restricting access to your computer. You agree to accept responsibility for all activities that occur under your account.</p>
                
                <h2 class="text-2xl font-bold text-gray-900 mt-8">10. Contact Information</h2>
                <p>If you have any questions about these Terms of Service, please contact us at:</p>
                <p class="ml-4">
                    <strong>Test Calgary</strong><br>
                    Email: support@testcalgary.com<br>
                    Address: Calgary, Alberta, Canada
                </p>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-12">
                <div>
                    <div class="flex items-center space-x-2 mb-6">
                        <div class="w-10 h-10 bg-gradient-to-br from-purple-600 to-pink-600 rounded-lg flex items-center justify-center">
                            <i class="fas fa-graduation-cap text-white text-lg"></i>
                        </div>
                        <span class="text-xl font-bold text-white">Test Calgary</span>
                    </div>
                    <p class="text-gray-400">Empowering professionals to achieve their certification goals.</p>
                </div>
                
                <div>
                    <h4 class="text-white font-bold text-lg mb-6">Quick Links</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="index.html#testimonials" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Testimonials</a></li>
                        <li><a href="index.html#about" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">About Us</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold text-lg mb-6">Resources</h4>
                    <ul class="space-y-3">
                        <li><a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Blog</a></li>
                        <li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
                        <li><a href="mailto:support@testcalgary.com" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Contact Support</a></li>
                    </ul>
                </div>
                
                <div>
                    <h4 class="text-white font-bold text-lg mb-6">Connect With Us</h4>
                    <p class="text-gray-400 mb-4">
                        <i class="fas fa-envelope mr-2"></i>
                        <a href="mailto:support@testcalgary.com" class="hover:text-purple-400 transition-colors duration-300">support@testcalgary.com</a>
                    </p>
                    <div class="flex gap-4">
                        <a href="https://facebook.com" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300" target="_blank">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="https://twitter.com" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300" target="_blank">
                            <i class="fab fa-twitter"></i>
                        </a>
                        <a href="https://linkedin.com" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300" target="_blank">
                            <i class="fab fa-linkedin-in"></i>
                        </a>
                        <a href="https://instagram.com" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center text-gray-400 hover:bg-purple-600 hover:text-white transition-all duration-300" target="_blank">
                            <i class="fab fa-instagram"></i>
                        </a>
                    </div>
                </div>
            </div>
            
            <div class="border-t border-gray-800 pt-8">
                <div class="flex flex-col md:flex-row justify-between items-center gap-4">
                    <p class="text-gray-400 text-sm">
                        &copy; 2025 Test Calgary. All rights reserved.
                    </p>
                    <div class="flex gap-6">
                        <a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Privacy Policy</a>
                        <a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Terms of Service</a>
                        <a href="blog.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300 text-sm">Blog</a>
                    </div>
                </div>
            </div>
        </div>
    </footer>

    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const mobileMenuButton = document.querySelector('header nav .mobile-menu-button');
            const mobileMenu = document.querySelector('header nav .mobile-menu');
            
            if (mobileMenuButton && mobileMenu) {
                mobileMenuButton.addEventListener('click', () => {
                    mobileMenu.classList.toggle('hidden');
                });
            }
        });
    </script>
</body>
</html>
```

**Important Changes to Make**:

1. Update the email address:
```html
Email: support@testcalgary.com
```

2. Update the physical address:
```html
Address: Your actual address
```

---

### Step 3: Verify Links Are Working

After creating both `privacy.html` and `terms.html` files:

1. **Open `index.html` in your browser**
2. **Scroll to the footer**
3. **Click on "Privacy Policy"** - Should open `privacy.html`
4. **Click on "Terms of Service"** - Should open `terms.html`
5. **Click the logo at the top** - Should return to `index.html`

**If links don't work**:
- Ensure files are in the same folder
- Check file names match exactly (including capitalization)
- Clear browser cache (Ctrl+Shift+Del)

---

### Step 4: Update Footer Links in index.html

Now that you have created the policy pages, verify these links in `index.html` are correct:

**Location**: Lines 565-572 (Footer Resources Section)

```html
<li><a href="blog.html" class="text-gray-400 hover:text-purple-400...">Blog</a></li>
<li><a href="privacy.html" class="text-gray-400 hover:text-purple-400...">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-purple-400...">Terms of Service</a></li>
```

These should now work correctly. If you don't have a blog yet, you can:

**Option 1: Remove the blog link**
```html
<!-- Delete this entire line -->
<li><a href="blog.html"...>Blog</a></li>
```

**Option 2: Link to external blog**
```html
<li><a href="https://medium.com/yourprofile" target="_blank" class="text-gray-400 hover:text-purple-400...">Blog</a></li>
```

---

### Step 5: Customize Policy Pages

The templates provided are generic. Customize them for your business:

**In privacy.html**, update:
- Contact email address
- Physical address
- Specific data collection practices
- Data retention policies

**In terms.html**, update:
- Contact email address
- Physical address
- Specific terms for your service
- Refund policies
- Liability limitations

---

## Color Customization

### Understanding the Color System

The landing page uses a purple-to-pink gradient as its primary color scheme. Here's how to change it:

### Primary Colors Used

```
Primary Purple: #667eea (from-purple-600)
Secondary Pink: #764ba2 (to-pink-600)
Accent Colors: Blue, Green, Yellow, Orange
```

### Where Colors Appear

1. **Gradient Text** - Headlines with gradient effect
2. **Buttons** - CTA buttons throughout
3. **Icons** - Feature card icons
4. **Borders** - Card borders
5. **Backgrounds** - Section backgrounds

### Changing the Primary Gradient

**Step 1: Identify Color Classes**

The gradient is created with these Tailwind classes:
- `from-purple-600` - Starting color
- `to-pink-600` - Ending color

**Step 2: Find All Instances**

Search for `from-purple-600 to-pink-600` in your file.

**Step 3: Replace with New Colors**

**Example: Change to Blue-to-Cyan**

```html
<!-- Before: Purple to Pink -->
<div class="bg-gradient-to-r from-purple-600 to-pink-600">

<!-- After: Blue to Cyan -->
<div class="bg-gradient-to-r from-blue-600 to-cyan-600">
```

### Available Tailwind Colors

```
Red:        from-red-600 to-pink-600
Orange:     from-orange-600 to-yellow-600
Green:      from-green-600 to-emerald-600
Blue:       from-blue-600 to-cyan-600
Purple:     from-purple-600 to-indigo-600
Pink:       from-pink-600 to-rose-600
```

### Changing All Gradient Colors at Once

**Using Find & Replace** (Ctrl+H or Cmd+H):

1. Find: `from-purple-600 to-pink-600`
2. Replace with: `from-blue-600 to-cyan-600`
3. Click "Replace All"

This will change:
- All gradient buttons
- All gradient text
- All gradient icons
- All gradient backgrounds

### Changing Individual Element Colors

**Example: Change only button colors**

```html
<!-- Before -->
<a class="bg-gradient-to-r from-purple-600 to-pink-600 text-white">Get Started</a>

<!-- After: Use blue gradient instead -->
<a class="bg-gradient-to-r from-blue-600 to-cyan-600 text-white">Get Started</a>
```

### Changing Hover States

Hover colors are defined with `hover:` prefix:

```html
<!-- Before: Hover to purple -->
<a href="#" class="text-gray-700 hover:text-purple-600">Link</a>

<!-- After: Hover to blue -->
<a href="#" class="text-gray-700 hover:text-blue-600">Link</a>
```

### Changing Background Tints

Feature cards have light background tints:

```html
<!-- Before: Light purple background -->
<div class="bg-gradient-to-br from-white to-purple-50">

<!-- After: Light blue background -->
<div class="bg-gradient-to-br from-white to-blue-50">
```

---

## Responsive Design Adjustments

### Understanding Responsive Breakpoints

The landing page uses Tailwind's responsive prefixes:

| Prefix | Screen Size | Device |
|--------|-------------|--------|
| (none) | 0px+ | Mobile |
| `sm:` | 640px+ | Small tablet |
| `md:` | 768px+ | Tablet |
| `lg:` | 1024px+ | Desktop |
| `xl:` | 1280px+ | Large desktop |

### How Responsive Classes Work

```html
<!-- Mobile: 1 column, Tablet: 2 columns, Desktop: 3 columns -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
    <div>Feature 1</div>
    <div>Feature 2</div>
    <div>Feature 3</div>
</div>
```

On mobile (0-767px): Shows 1 column
On tablet (768-1023px): Shows 2 columns
On desktop (1024px+): Shows 3 columns

### Common Responsive Adjustments

**Example 1: Change Number of Feature Columns**

**Location**: Line 200 (Features Section Grid)

```html
<!-- Before: 3 columns on large screens -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

<!-- After: 2 columns on large screens -->
<div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 gap-8">
```

**Example 2: Change Hero Text Size on Different Devices**

```html
<!-- Before: Smaller on mobile, larger on desktop -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">

<!-- After: Even larger on desktop -->
<h1 class="text-3xl md:text-5xl lg:text-7xl font-bold">
```

**Example 3: Hide/Show Elements Based on Screen Size**

```html
<!-- Hidden on mobile and tablet, shown on desktop -->
<div class="hidden lg:flex">This only shows on large screens</div>

<!-- Shown on mobile, hidden on desktop -->
<div class="block lg:hidden">This only shows on mobile</div>
```

### Testing Responsive Design

1. **Open your browser's developer tools** (F12 or Right-click → Inspect)
2. **Click the responsive design mode** (Ctrl+Shift+M)
3. **Test at different widths**:
   - Mobile: 375px
   - Tablet: 768px
   - Desktop: 1024px

### Making the Mobile Menu Work

The mobile menu is already implemented. Here's how it works:

**HTML Structure** (Lines 55-67):
```html
<button class="md:hidden mobile-menu-button">
    <i class="fas fa-bars text-2xl"></i>
</button>

<div class="mobile-menu hidden">
    <!-- Menu items -->
</div>
```

**JavaScript** (Lines 625-645):
```javascript
const mobileMenuButton = document.querySelector('.mobile-menu-button');
const mobileMenu = document.querySelector('.mobile-menu');

mobileMenuButton.addEventListener('click', () => {
    mobileMenu.classList.toggle('hidden');
});
```

**How it works**:
- `md:hidden` hides button on tablets and up
- When clicked, JavaScript toggles the `hidden` class
- Menu appears/disappears with animation

---

## Troubleshooting

### Common Issues and Solutions

#### Issue 1: Links Not Working

**Problem**: Clicking a link does nothing

**Solutions**:

1. **Check the URL is correct**:
```html
<!-- Wrong: Missing https:// -->
<a href="example.com">Link</a>

<!-- Correct -->
<a href="https://example.com">Link</a>
```

2. **For internal links, check file exists**:
```html
<!-- Make sure privacy.html exists in the same folder -->
<a href="privacy.html">Privacy</a>
```

3. **For anchor links, check the ID exists**:
```html
<!-- Link -->
<a href="#features">Features</a>

<!-- Section must have matching ID -->
<section id="features">...</section>
```

---

#### Issue 2: Text Not Showing or Overlapping

**Problem**: Text is invisible or overlapping other elements

**Possible Causes**:

1. **Text color matches background**:
```html
<!-- Before: White text on white background = invisible -->
<p class="text-white bg-white">Text</p>

<!-- After: White text on dark background -->
<p class="text-white bg-gray-900">Text</p>
```

2. **Missing text in element**:
```html
<!-- Before: Empty element -->
<h2 class="text-4xl font-bold"></h2>

<!-- After: Add text -->
<h2 class="text-4xl font-bold">Your Heading</h2>
```

3. **CSS class removed accidentally**:
```html
<!-- Before: Proper styling -->
<p class="text-lg text-gray-700">Text</p>

<!-- After: Accidentally removed classes -->
<p>Text</p>

<!-- Fix: Restore classes -->
<p class="text-lg text-gray-700">Text</p>
```

---

#### Issue 3: Images Not Showing

**Problem**: Image placeholder or broken image icon appears

**Solution**:

Check the image URL in the `src` attribute:

```html
<!-- Before: Broken URL -->
<img src="image.jpg" alt="Description">

<!-- After: Correct URL -->
<img src="https://images.unsplash.com/photo-1552664730-d307ca884978?w=600&h=600&fit=crop" alt="Description">
```

---

#### Issue 4: Mobile Menu Not Working

**Problem**: Hamburger menu doesn't open on mobile

**Solutions**:

1. **Check JavaScript is not broken**:
   - Open browser console (F12)
   - Look for red error messages
   - Fix any JavaScript syntax errors

2. **Verify mobile menu HTML is present**:
```html
<!-- Mobile menu should exist -->
<div class="mobile-menu hidden">
    <!-- Menu items -->
</div>
```

3. **Check breakpoint is correct**:
```html
<!-- md:hidden means hidden on medium screens and up -->
<button class="md:hidden">Menu</button>
```

---

#### Issue 5: Styling Not Applied

**Problem**: CSS classes don't seem to work

**Solutions**:

1. **Check Tailwind CDN is loading**:
   - Open browser console (F12)
   - Go to Network tab
   - Look for `https://cdn.tailwindcss.com`
   - Should show status 200 (successful)

2. **Verify class name is spelled correctly**:
```html
<!-- Before: Misspelled -->
<div class="text-4xl font-bold">Text</div>
<!-- Typo: "text-4xl" should work -->

<!-- After: Correct -->
<div class="text-4xl font-bold">Text</div>
```

3. **Check class name is a valid Tailwind class**:
```html
<!-- Before: Invalid class -->
<div class="text-huge">Text</div>

<!-- After: Valid Tailwind class -->
<div class="text-6xl">Text</div>
```

---

#### Issue 6: Gradient Text Not Showing

**Problem**: Gradient text appears as solid color or invisible

**Solution**:

Check the gradient-text custom CSS is in the style tag:

```html
<style>
    .gradient-text {
        background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        background-clip: text;
    }
</style>
```

If it's missing, add it back. The gradient-text class is custom CSS, not a Tailwind class.

---

#### Issue 7: Page Layout Broken on Mobile

**Problem**: Elements overlap or don't fit on mobile screen

**Solutions**:

1. **Check responsive classes are used**:
```html
<!-- Before: Same size on all devices -->
<div class="p-8 text-4xl">Text</div>

<!-- After: Responsive sizing -->
<div class="p-4 md:p-8 text-2xl md:text-4xl">Text</div>
```

2. **Verify max-width is set**:
```html
<!-- Before: No max width, may be too wide -->
<div class="mx-auto px-4">

<!-- After: Has max width -->
<div class="max-w-7xl mx-auto px-4">
```

---

### Browser Developer Tools (Essential for Debugging)

**How to open**:
- Windows: Press F12
- Mac: Press Cmd+Option+I
- Right-click any element → Inspect

**Useful tabs**:

1. **Elements/Inspector**: See HTML structure
2. **Console**: See JavaScript errors
3. **Network**: Check if resources load (images, CSS, JS)
4. **Responsive Design Mode**: Test mobile view (Ctrl+Shift+M)

**How to inspect an element**:
1. Right-click the element
2. Click "Inspect" or "Inspect Element"
3. See the HTML and CSS for that element

---

## Best Practices

### 1. Always Backup Before Making Changes

Before editing your HTML:

```
Original File: index.html
Backup File: index.html.backup
```

If something breaks, you can restore from backup.

---

### 2. Test Changes in Multiple Browsers

Test your changes in:
- Chrome
- Firefox
- Safari
- Edge

Different browsers may render slightly differently.

---

### 3. Test on Multiple Devices

Test responsive design on:
- Mobile phone (375px width)
- Tablet (768px width)
- Desktop (1024px+ width)

Use browser responsive design mode (Ctrl+Shift+M).

---

### 4. Keep Consistent Spacing

Use consistent spacing values:
- `mb-4`, `mb-6`, `mb-8` (avoid random values)
- `px-4`, `px-6`, `px-8` (avoid random values)
- `gap-4`, `gap-6`, `gap-8` (avoid random values)

This keeps the design cohesive.

---

### 5. Keep Consistent Colors

Stick to the defined color palette:
- Primary: Purple-600 to Pink-600
- Text: Gray-900, Gray-700, Gray-600
- Backgrounds: White, Gray-50, Purple-50

Don't add random new colors.

---

### 6. Use Semantic HTML

Use proper HTML tags for meaning:

```html
<!-- Before: Using div for everything -->
<div>Features</div>

<!-- After: Using proper heading -->
<h2>Features</h2>
```

Proper tags help:
- Search engines understand content
- Screen readers help visually impaired users
- Code is more maintainable

---

### 7. Keep External Links Consistent

All external links should:
- Include `https://` at the beginning
- Include `target="_blank"` to open in new tab
- Include `rel="noopener noreferrer"` for security

```html
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
    External Link
</a>
```

---

### 8. Validate HTML Regularly

Use an online HTML validator:
1. Go to https://validator.w3.org/
2. Paste your HTML
3. Fix any errors reported

This ensures your code is valid and will work in all browsers.

---

### 9. Keep Comments for Complex Sections

Add comments to explain complex code:

```html
<!-- Mobile Menu: Hidden on desktop, shown on mobile -->
<div class="mobile-menu hidden md:hidden">
    <!-- Menu items appear here -->
</div>
```

This helps future you remember why code is structured that way.

---

### 10. Test All Interactive Elements

After making changes, test:
- ✓ All navigation links
- ✓ All buttons and CTAs
- ✓ Mobile menu open/close
- ✓ Hover effects
- ✓ Responsive layouts at different screen sizes

---

## Quick Reference: Common Tasks

### Task: Change the main headline
**Location**: Line 99-105
**Change**: Text inside `<h1>` tags
**Keep**: All class attributes

### Task: Update a feature card
**Location**: Lines 200-250
**Change**: Title (`<h3>`), description (`<p>`), and bullet points (`<li>`)
**Keep**: All class attributes and icon classes

### Task: Update a testimonial
**Location**: Lines 400-450
**Change**: Quote text, person's name, and their title
**Keep**: All star ratings and class attributes

### Task: Change button link
**Find**: `href="https://example.com"`
**Replace**: `href="https://yoursite.com/signup"`

### Task: Change color scheme
**Find**: `from-purple-600 to-pink-600`
**Replace**: `from-blue-600 to-cyan-600` (or your colors)

### Task: Hide element on mobile
**Add**: `hidden md:block` to the element's class list
**Example**: `<div class="hidden md:block">Desktop only</div>`

### Task: Make text larger
**Find**: `text-lg` or `text-xl`
**Replace**: `text-2xl` or `text-3xl`

---

## Conclusion

You now have a comprehensive guide to maintaining and customizing the Test Calgary landing page. The key points to remember:

1. **Text Content**: Change only text between HTML tags, keep classes intact
2. **Links**: Always include `https://` for external links, use correct file names for internal links
3. **Colors**: Use Find & Replace for consistent color changes across the entire page
4. **Responsive Design**: Use `md:` and `lg:` prefixes for different screen sizes
5. **Testing**: Always test changes in multiple browsers and on mobile devices

For more help with Tailwind CSS, visit: https://tailwindcss.com/docs

Happy customizing! 🚀