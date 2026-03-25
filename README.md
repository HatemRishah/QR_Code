# Frontend Mentor - QR code component solution

## Overview
This is a solution to the QR code component challenge on Frontend Mentor. It is just a simple QR Code website built to practice responsive design and clean layout techniques.

### Links
- **GitHub Repository:** [https://github.com/HatemRishah/QR_Code.git]
- **Live Site URL:** [https://hatemqrcode.netlify.app/]

---

## My process

### Built with
- Semantic HTML5 markup
- CSS Custom Properties (Variables)
- Desktop-first workflow

### What I learned
In this project, I focused on security and performance. Here are two key things I implemented:

1. **Security with `rel="noopener"`**:
I learned that when using `target="_blank"` for external links, it's a best practice to add `rel="noopener"`. This prevents the new page from being able to access my window object via `window.opener`, which is a crucial security measure.

2. **GPU-Accelerated Animations**:
To make the hover effects and transitions as smooth as possible, I used properties that the GPU can handle efficiently (like `transform` and `opacity`) instead of properties that trigger a layout re-flow.

```css
/* Example of a smooth, GPU-friendly transition */
.card {
  transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  will-change: transform; /* Hinting the browser for GPU optimization */
}
.card:hover {
  transform: scale(1.03);
}