# 📱 Responsive Media Queries

This repository contains a collection of **reusable media query snippets** in both **CSS** and **SCSS**.  
Designed to simplify responsive design by offering ready-to-use breakpoints for a wide range of devices.

---

## 📐 Features

- Common breakpoints for mobile, tablet, desktop, and large screens
- Easy to copy and adapt
- SCSS mixins for streamlined development
- Works in any modern web project

---

## 🧰 Tech Stack

- **CSS3**
- **SCSS (Sass)**

---

## 🧪 Example Usage (SCSS)

```scss
@mixin respond-to($breakpoint) {
  @if $breakpoint == small {
    @media (max-width: 600px) { @content; }
  } @else if $breakpoint == medium {
    @media (min-width: 601px) and (max-width: 1024px) { @content; }
  } @else if $breakpoint == large {
    @media (min-width: 1025px) { @content; }
  }
}

// Usage:
.container {
  padding: 2rem;

  @include respond-to(small) {
    padding: 1rem;
  }
}
