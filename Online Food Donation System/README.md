# Online Food Donation System

A simple, static web project to connect food donors with recipients/NGOs. Includes a donation form that emails submissions via EmailJS and an embedded live map. Built with plain HTML and CSS—no backend server required.

## Features
- **Home page**: Branding, hero image, inspirational quote, and a floating "Donate Now" button.
- **Donate page**: Form collects name, email, phone, address, food details, quantity, comments, and terms consent.
- **Email notifications**: Submissions are sent via EmailJS (`emailjs-com` CDN). Requires your own EmailJS keys.
- **Live map**: Embedded Google Maps iframe on the donate page.
- **About page**: Project motivation with a local demo video.
- **Contact page**: Contact details and a styled (non-functional) contact form with a simple chat input placeholder.
- **Profile page**: Static example profile and donation history table (no authentication/backend).

## Tech Stack
- **Frontend**: HTML5, CSS3
- **Libraries/Services**:
  - EmailJS (CDN: `https://cdn.jsdelivr.net/npm/emailjs-com@2.6.4/dist/email.min.js`)
  - Google Maps Embed (iframe)

## Project Structure
```
Online Food Donation System/
├─ about.html
├─ contact.html
├─ donate.html
├─ index.html
├─ profile.html
├─ style.css
└─ Food donation system motivation video.mp4
```

## Getting Started
### Option 1: Open locally
1. Download/clone the repository.
2. Open `index.html` in your web browser.

### Option 2: Use a local dev server (recommended)
- With VS Code, install the "Live Server" extension.
- Right-click `index.html` → "Open with Live Server".

## Configure EmailJS
The donate form uses EmailJS to send submissions. Replace placeholder IDs with your own.
- In `donate.html`, update:
  - Public Key in `emailjs.init("YOUR_PUBLIC_KEY")`
  - Service ID and Template ID in `emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', event.target)`
- In your EmailJS template, ensure fields match input `name` attributes:
  - `name`, `email`, `phone`, `address`, `foodDetails`, `quantity`, `comments`, `terms`

## Usage
- Navigate to `index.html` for the home page.
- Click "Donate Now" or open `donate.html` to submit the donation form.
- View the live map below the form.
- See project info in `about.html` and contact details in `contact.html`.
- `profile.html` shows a static example profile and donation history.

## Deployment
Since the site is static, you can host it easily:
- **GitHub Pages**: Push to a repo and enable Pages for the `main` branch root.
- **Netlify / Vercel**: Drag-and-drop the folder or connect your repo. No build step required.
- **Any static host**: Serve the files as-is.

## Security & Privacy Notes
- Do not commit real EmailJS keys to public repos.
- The contact form is static and not wired to send messages—avoid entering sensitive data.

## Future Improvements
- Real authentication and user profiles.
- Persisted donation submissions with a backend or serverless functions.
- Admin/NGO dashboard to accept/track donations.
- Validation and success/error UI states for forms.

## License
Add your license of choice (e.g., MIT) in a `LICENSE` file.

## Acknowledgements
- EmailJS for client-side email service.
- Google Maps for embedded map.
