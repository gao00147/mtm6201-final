# MTM6201 Final Project – Web Portfolio

**Student:** Yijia Gao  
**Course:** MTM6201  
**GitHub Pages URL:** https://gao00147.github.io/mtm6201-final/

---

## About This Project

This project is a three-page responsive website for a fictional digital agency called **DevAgency**. The site includes a home page, a blog page, and an about page. It was built using HTML, CSS, and the Bootstrap 5 framework, following a set of provided design mockups at mobile (375px), tablet (768px), and desktop (1440px) screen sizes.

---

## My Process

I started by reviewing the design mockups carefully before writing any code. I set up the project folder structure first, then built the HTML for all three pages using semantic elements. After that, I linked Bootstrap 5 and wrote the custom CSS in `style.css` using CSS variables for colours and fonts.

I worked mobile-first, writing base styles for small screens and then adding media queries for tablet and desktop breakpoints. I used Bootstrap's grid system (`col-12`, `col-md-4`, `col-md-6`) to handle the column layouts and made sure the navbar collapsed into a hamburger menu on mobile.

---

## Challenges I Faced

**Responsive images:** Getting the `<picture>` element to work correctly with `srcset`, `sizes`, and `media` attributes took some trial and error. I had to understand the difference between using `media` to switch image files versus using `srcset` with width descriptors for the browser to choose automatically.

**Navbar overlay on hero image:** Making the navbar sit on top of the hero image (instead of pushing it down) required using `position: absolute` on the navbar, which was new to me. I had to make sure the hero section had `position: relative` so the navbar would be positioned relative to it.

**CSS specificity:** When I tried to apply different background colours to each "What We Provide" card using `:nth-child`, I ran into a selector specificity problem. I learned that I needed to target the parent column (`.col-md-4:nth-child(n)`) rather than the card itself, because each card is always the first child of its own column div.

**Equal-height cards:** Making blog and team cards in the same grid row equal in height required `height: 100%`, `display: flex`, and `flex-direction: column` on the card, with `flex: 1` on the card body to fill remaining space.

---

## What I Learned

- How to use CSS custom properties (variables) to keep colours and fonts consistent and easy to change across a project.
- How the Bootstrap grid system works and how to combine it with custom CSS without conflicts.
- How `position: absolute` and `position: relative` work together to layer elements on top of each other.
- How the `<picture>` element, `srcset`, `sizes`, and `media` attributes work to serve responsive images.
- The importance of semantic HTML elements (`<nav>`, `<main>`, `<section>`, `<footer>`) and ARIA attributes for accessibility.
- How CSS Grid can be used to reliably overlay text on top of an image without relying on absolute positioning.

---

## Assets and Resources Used

### Frameworks and Libraries
- [Bootstrap 5.3.3](https://getbootstrap.com/) – CSS and JS framework for layout and components
- [Google Fonts](https://fonts.google.com/) – Web fonts used: **Nunito** (headings) and **Mulish** (body text)

### Stock Images
All images used in this project are stock images obtained from free-to-use sources. They are not original photographs taken by the student.

- **Home page hero image** (`home-header-img-*.png`) – illustration from design template
- **Home page project card images** (`home-ourpro-*.png`) – mockup screenshots from design template
- **Home page experience section images** (`home-provide-*.png`) – illustrations from design template
- **Home page star rating images** (`home-*-4.5stars.png`) – from design template
- **Blog / About hero background** (`blog-bg-header-*.png`) – from design template
- **About page person photo** (`about-know-more-about-*.jpg`) – stock photo
- **About page team member photos** (`about-members-*.jpg`) – stock photos
- **Blog post images** (`blog-1.jpg` through `blog-6.jpg`) – stock photos
- **Logo** (`logo-*.png`) – from design template

### Design Reference
- [Figma design mockups](https://www.figma.com/design/C3LXB4pUeH7dsoVTAFgBsX/mtm6201-final?m=dev&t=ortgtBgnAyUZtP4j-1) provided as part of the course assignment (designed by instructor/course materials)

---

## Accessibility Features

- Skip link (`<a class="skip-link">`) for keyboard users to bypass navigation
- Semantic HTML5 elements throughout all pages
- `aria-label` attributes on `<nav>`, `<main>`, `<section>`, and `<footer>` elements
- Schema.org markup (`itemscope`, `itemtype`) on main content areas
- `alt` text on all images
- Sufficient colour contrast between text and backgrounds
- Keyboard-accessible navigation using Bootstrap's built-in toggler

---

## File Structure

```
mtm6201-final/
├── index.html
├── blog.html
├── about.html
├── style.css
├── README.md
└── images/
    ├── blog-bg-header-mobile.png
    ├── blog-bg-header-tablet.png
    ├── home-header-img-mobile.png
    ├── home-header-img-tablet.png
    ├── home-ourpro-mobile-1.png
    ├── home-ourpro-tablet-1.png
    ├── home-ourpro-mobile-2.png
    ├── home-ourpro-tablet-2.png
    ├── home-provide-mobile-1.png
    ├── home-provide-tablet-1.png
    ├── home-provide-mobile-2.png
    ├── home-provide-tablet-2.png
    ├── home-mobile-4.5stars.png
    ├── home-tablet-4.5stars.png
    ├── about-know-more-about-mobile.jpg
    ├── about-know-more-about-tablet.jpg
    ├── about-members-fs-mobile.jpg
    ├── about-members-fs-tablet.jpg
    ├── about-members-cb-mobile.jpg
    ├── about-members-cb-tablet.jpg
    ├── about-members-gw-mobile.jpg
    ├── about-members-gw-tablet.jpg
    ├── blog-1.jpg
    ├── blog-2.jpg
    ├── blog-3.jpg
    ├── blog-4.jpg
    ├── blog-5.jpg
    ├── blog-6.jpg
    ├── logo-mobile-header.png
    ├── logo-tablet-header.png
    ├── logo-mobile-footer.png
    └── logo-tablet-footer.png
```
