# Data URI Image Viewer (Single-File HTML)

A self-contained, single-file HTML app that displays images embedded as base64 data URIs. The page is fully self-contained (no external dependencies) and ready to deploy. It includes features to download or copy the embedded data URIs and supports a light/dark theme toggle.

## Summary
This app renders images provided as base64 data URIs directly in the browser. It showcases two attachments included with the project:
- sample.png (a 1x1 PNG, embedded as a data URI)
- logo.svg (an SVG logo embedded as a data URI)

Users can view both images, download them, or copy their data URIs to the clipboard. The interface is responsive, accessible, and includes a theme toggle.

## Key Features
- Self-contained single HTML file (index.html) with inline CSS and JavaScript
- Display of two data URI images (sample.png and logo.svg)
- Per-image actions: Copy Data URI and Download
- Light/Dark theme toggle with persistent preference (localStorage)
- Responsive, accessible UI with clear captions
- No external dependencies required

## Setup Instructions
1. Save the provided content as index.html.
2. Open index.html in any modern web browser (Chrome, Firefox, Edge, Safari).

Optional:
- To customize the data URIs, edit the values in the HTML where the images are defined.

## Usage Instructions
- The page loads with two embedded images displayed in a responsive grid.
- For each image:
  - Copy URI: Copies the base64 data URI to your clipboard.
  - Download: Downloads the image using the embedded data URI.
- Use the theme toggle in the header to switch between light and dark modes. The selected theme is saved to localStorage and persists across reloads.

## Technical Details
- HTML: A single HTML document (index.html) that includes all markup for the header, image gallery, and actions.
- CSS: Inline CSS within a <style> tag. Implements a responsive grid, card-style containers, and a light/dark theme via data-theme attribute.
- JavaScript: Inline script handling:
  - Theme initialization and persistence
  - Copy-to-clipboard functionality for data URIs
  - Lightweight toast notifications for user feedback
- Accessibility: Proper semantic elements (header, sections, figure/figcaption), alt text for images, ARIA attributes for controls, and a visually-hidden label for the theme toggle.

## Deployment Info (GitHub Pages)
- Create a new GitHub repository (e.g., data-uri-viewer).
- Push this single index.html file to the repository (e.g., as main branch).
- In GitHub, enable GitHub Pages from the repository settings, selecting the main branch / root as the source.
- Access the site via https://<your-username>.github.io/<repository-name>/index.html

## License
MIT

## Generated
Date: 2025-10-16