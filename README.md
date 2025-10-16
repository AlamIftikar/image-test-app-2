# Data URI Image Viewer - Round 2

Project title
- Data URI Image Viewer - Round 2

Summary
- A self-contained single-file HTML app that renders images embedded as base64 data URIs. It includes features to copy the embedded data URIs to the clipboard, download the images, and toggle between light and dark themes. In Round 2, a heading above the image gallery was added, images are laid out side-by-side with spacing, and a dark background theme option is emphasized.

Key features
- Heading above the gallery: “My Image Gallery”
- Images laid out side-by-side with consistent spacing (responsive grid)
- Light/dark theme toggle with persistent preference
- Copy URI button to copy the embedded data URI to the clipboard
- Download button for each image
- Self-contained single-file HTML (no external dependencies)

Setup instructions
1. Create a new file named index.html.
2. Copy and paste the entire HTML content from the updated code.
3. Open index.html in a modern web browser.

Usage instructions
- Use the theme toggle in the header to switch between light and dark themes. The chosen theme is saved to localStorage and will persist on reloads.
- In the gallery:
  - Click “Copy URI” to copy the corresponding data URI to the clipboard.
  - Click “Download” to save the embedded image to your device.

Technical details
- HTML/CSS/JS are all contained in a single HTML file.
- Layout
  - A responsive grid (.gallery) uses grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); to place images side-by-side with spacing.
  - Each image is wrapped in a .card with a caption and toolbar containing action buttons.
- Data URIs
  - Images are embedded as base64 data URIs (PNG and SVG used in the sample gallery).
- Theme
  - CSS variables define light and dark themes.
  - A toggle control updates a data-theme attribute on the documentElement and stores the preference in localStorage.
- Interactions
  - A toast notification shows success/failure messages for clipboard Copy actions.
  - Copy to clipboard uses the Clipboard API with graceful fallback messaging.

Changes made in Round 2
- Added a visible heading above the image gallery: “My Image Gallery” (replacing the previous “Preview” heading).
- Ensured images are displayed side-by-side with consistent spacing by leveraging a responsive grid layout (repeat(auto-fit, minmax(260px, 1fr)) with a 16px gap).
- Clarified and stabilized the header by fixing a minor style property issue and reinforcing the dark background support via the existing theme system.
- Retained all existing features (Copy URI, Download, theme persistence, and toast notifications) with improved layout context for the gallery.

Deployment info (GitHub Pages)
- This is a single-file app suitable for hosting on GitHub Pages.
- Steps:
  1. Create a repository (e.g., yourname/data-uri-image-viewer).
  2. Add index.html with the updated contents.
  3. Commit and push to the main branch (or gh-pages depending on your setup).
  4. In the repository settings, enable GitHub Pages and select the branch (main) and root directory.
  5. Access the site at https://<username>.github.io/<repository>/

License
- MIT License

Notes
- The gallery uses two embedded data URIs in this example:
  - sample.png (1x1 PNG)
  - logo.svg (blue circle)
- You can replace or add more items by duplicating the .card blocks inside the gallery section and updating the data-uri attribute and image src accordingly.