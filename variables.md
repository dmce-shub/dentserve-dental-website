# Quick Start

1. Open this project folder in VS Code (or another code editor).
2. Run `npm install`, then `npm run dev` to preview the site.
3. For the fastest rebrand, start in `src/data/site.ts` and replace the values inside quotes.
4. Update the service list in `src/data/services.ts`; image placeholders are marked clearly until real photos are added.

This template keeps most reusable client data in `src/data/site.ts` and `src/data/services.ts`. Edit those files first. The scattered locations below are included as a reference and warning for values that are displayed or generated in other files.

### Business Info Clinic/business name
- Current value: DentServe Dental Clinic (short wordmark: DentServe)
- File location: `src/data/site.ts`; displayed through `src/main.tsx`; browser title in `index.html`
- Where in file: `site.name`, `site.shortName`; search for `DentServe` to find the visible legal placeholders and page copy
- How to change: Replace the two quoted name values in `site.ts`, then search the project for `DentServe` and update any sentence that is intentionally written into page copy or legal placeholder text.

### Business Info Tagline / slogan
- Current value: Comfortable care for every smile.
- File location: `src/data/site.ts`
- Where in file: `site.tagline`
- How to change: Replace the words inside the `tagline` quotes. Add the tagline to any new section by reading it from `site.tagline`.

### Business Info Phone number
- Current value: +91 80977 40288; dial link: +918097740288
- File location: `src/data/site.ts`; dial behavior is centralized in `src/main.tsx`
- Where in file: `site.phone`, `site.tel`, and the `CallNow` function; search for `CallNow`
- How to change: Replace `phone` with the display version and `tel` with the same number containing only digits and the country code. Do not add spaces to `tel`. Every call action uses `CallNow`, which explicitly sends the browser/device to the `tel:` dialer link.

### Business Info Email address
- Current value: No email is used; the email row is intentionally omitted.
- File location: `src/data/site.ts` / `src/main.tsx`
- Where in file: No email field exists; search for `mailto` to confirm
- How to change: Add an `email` value to `site.ts`, then add an email link to the utility/header/footer only if the new clinic supplies one.

### Business Info Physical address
- Current value: Shop No. 3, Om Sai Prasad, Opp. TMC Garden, Naka, Kharegaon, Kalwa, Thane, Maharashtra 400605
- File location: `src/data/site.ts`; rendered in footer, Contact page, and FAQ
- Where in file: `site.address`; search for `site.address`
- How to change: Replace the full address inside the `address` quotes. The footer, map card, and FAQ answer will use it automatically.

### Business Info Business hours
- Current value: Monday to Saturday, 9:30 AM–1 PM and 5–9 PM
- File location: `src/data/site.ts`; rendered in header, trust strip, footer, Contact page, and FAQ
- Where in file: `site.hours`; search for `site.hours`
- How to change: Replace the hours text inside the `hours` quotes. Also check the small header line `Mon–Sat · 9:30 AM–1 PM & 5–9 PM` in `src/main.tsx` if the schedule format changes.

### Branding & Media Logo file(s)
- Current value: No external logo file; the DentServe wordmark and blue-to-teal plus are built in the `Logo` function.
- File location: `src/main.tsx`, `src/styles.css`
- Where in file: Search for `function Logo`, `.logo`, `.logo-mark`
- How to change: Replace the text in the `Logo` function and adjust `.logo-mark` colors or dimensions in the stylesheet. Recommended future logo file: SVG, at least 240 × 80 px, with a transparent background.

### Branding & Media Favicon
- Current value: No favicon file has been supplied.
- File location: `index.html`
- Where in file: Search for `favicon`
- How to change: Add a small square SVG or PNG to `public/`, then add a `<link rel="icon" href="/your-file.svg">` inside the `<head>` in `index.html`.

### Branding & Media Hero/banner images
- Current value: `src/assets/coverpage.jpg`; displayed in the homepage hero/cover image.
- File location: `src/assets/coverpage.jpg`; imported in `src/main.tsx`
- Where in file: Search for `coverPage` and `hero-image`
- How to change: Replace the JPG with the approved hero photo using the same filename, or change the import path. Recommended image: 1600 × 1400 px or larger.

### Branding & Media Doctor/staff photos
- Current value: Dr. Amita — `src/assets/doctor.jpg`; no other doctors are rendered.
- File location: `src/assets/doctor.jpg`; displayed in the `Doctor` function in `src/main.tsx`
- Where in file: Search for `doctorPhoto` and `Dr. Amita`
- How to change: Replace the JPG with an approved portrait using the same filename, then update the credential placeholders and bio in `src/main.tsx`. Additional doctor cards can be added to the existing `Doctor` section.

### Branding & Media Clinic interior/exterior photos
- Current value: Four supplied images: `gallery1.jpg`, `gallery2.jpg`, `gallery3.jpg`, and `gallery4.jpg`.
- File location: `src/assets/gallery1.jpg` through `src/assets/gallery4.jpg`; displayed in `GalleryStrip` and `Gallery` in `src/main.tsx`
- Where in file: Search for `gallery1`, `gallery2`, `gallery3`, and `gallery4`
- How to change: Replace any image with a new approved clinic photo using the same filename, or change the corresponding import and alt text. Keep the image descriptions accurate.

### Branding & Media Before/after images
- Current value: Case 1 uses `before1.jpg` → `after1.jpg`; Case 2 uses `before2.jpg` → `after2.jpg`.
- File location: `src/assets/before1.jpg`, `src/assets/after1.jpg`, `src/assets/before2.jpg`, `src/assets/after2.jpg`; rendered in `Gallery` in `src/main.tsx`
- Where in file: Search for `before1`, `after1`, `before2`, and `after2`
- How to change: Replace each file with the approved patient image for that case, keep the before/after order, and confirm written patient consent before publishing.

### Branding & Media Stock images used as placeholders
- Current value: None. All visual placeholders are local styled blocks; no stock photo URLs are used.
- File location: `src/main.tsx`
- Where in file: Search for `https://` and `Placeholder`
- How to change: When real images are available, replace only the matching placeholder blocks. Do not paste stock-image URLs unless the clinic has approved the license.

### Location & Maps Google Maps embed
- Current value: `https://www.google.com/maps?q=DentServe%20Dental%20Clinic%20Kalwa%20Thane&output=embed`
- File location: `src/data/site.ts`; used by Contact page iframe
- Where in file: `site.mapEmbed`; search for `mapEmbed`
- How to change: Replace the full quoted URL with the clinic’s verified Google Maps embed URL. Keep the visible Directions link separate.

### Location & Maps Latitude/longitude
- Current value: Not used in schema because coordinates were not supplied.
- File location: None
- Where in file: Search for `latitude`, `longitude`, and `schema`
- How to change: If verified coordinates are supplied later, add them to `site.ts` and add a JSON-LD LocalBusiness block in `index.html` or a shared React SEO helper.

### Location & Maps Directions link
- Current value: `https://maps.app.goo.gl/KFiQ8y6Le7Xdpiur5`
- File location: `src/data/site.ts`; used in footer and Contact page
- Where in file: `site.directions`; search for `site.directions`
- How to change: Replace the quoted share URL with the new verified Google Maps share link.

### Content Blocks About Us / bio text
- Current value: Warm DentServe story in `AboutBlock` plus `site.description`.
- File location: `src/data/site.ts`, `src/main.tsx`
- Where in file: Search for `Welcome to DentServe` and `modern dental clinic in Kalwa`
- How to change: Update `site.description` first, then edit the two story paragraphs in `AboutBlock` if the clinic story changes.

### Content Blocks Doctor bio and credentials
- Current value: Dr. Amita; role, qualification, specialization, years, and bio are explicit `[INSERT ...]` placeholders.
- File location: `src/main.tsx`
- Where in file: Search for `INSERT ROLE`, `INSERT QUALIFICATION`, `INSERT SPECIALIZATION`, `INSERT YEARS`, and `INSERT 2–3`
- How to change: Replace each bracketed phrase with the confirmed credential or bio. Do not guess years, qualifications, or awards.

### Content Blocks Services list
- Current value: Eight services, each with name, slug, short description, longer description, intended audience, benefits, visit steps, and icon; no prices.
- File location: `src/data/services.ts`
- Where in file: Search for `export const services`
- How to change: Edit, add, or remove an object in the services array. Keep `slug` lowercase with hyphens because it is used in page links. Update `description`, `bestFor`, `benefits`, and `steps` to change the detailed service page.

### Content Blocks Pricing
- Current value: No pricing is displayed or stored.
- File location: `src/data/services.ts`, `src/main.tsx`
- Where in file: Search for `price`, `pricing`, and `starting_price`
- How to change: If the clinic later approves prices, add a field to the service data and deliberately add it to the relevant layout; do not assume a price is current.

### Content Blocks Testimonials/reviews
- Current value: Three real patient testimonials from Sanket Padwal, Bhaskar Ganguly, and Sunit Srivastava; each is shown with five stars. Google aggregate is 4.9 stars from 470+ reviews.
- File location: `src/data/site.ts`; rendered in `src/main.tsx`
- Where in file: `testimonials`, `googleRating`, and `googleReviewCount`; search for `testimonials`
- How to change: Edit the name and review text inside the `testimonials` array. Update the aggregate rating and review count in the shared site data when the verified Google profile changes.

### Content Blocks Patient count
- Current value: 500+ patients
- File location: `src/data/site.ts`; displayed in the homepage hero trust card
- Where in file: `site.patientCount`; search for `patientCount`
- How to change: Replace the quoted count only when the clinic confirms a new verified figure.

### Content Blocks FAQ questions & answers
- Current value: Eight questions and answers, centralized in `src/data/site.ts`.
- File location: `src/data/site.ts`; rendered on Home and FAQ pages
- Where in file: `export const faqs`
- How to change: Edit the question/answer pairs in the `faqs` list. Both pages will update automatically.

### Links & Social Social media URLs
- Current value: None supplied; no social icons or dead links are rendered.
- File location: `src/main.tsx`
- Where in file: Search for `instagram`, `facebook`, and `social`
- How to change: Add verified profile URLs to `site.ts`, then add icons/links to the first footer column.

### Links & Social Booking / form action URL
- Current value: The appointment form is a front-end placeholder with no external submission endpoint; it prevents default submit.
- File location: `src/main.tsx`
- Where in file: `AppointmentForm`, search for `onSubmit`
- How to change: Connect the form to the clinic’s approved email/API service in the submit handler, then replace the `preventDefault` placeholder behavior.

### Links & Social WhatsApp link
- Current value: `https://wa.me/918097740288`
- File location: `src/data/site.ts`; used by floating button, Contact CTA, and any `site.whatsapp` reference
- Where in file: `site.whatsapp`; search for `site.whatsapp`
- How to change: Replace the digits in the URL with the new WhatsApp number, including country code and no plus sign or spaces.

### SEO & Metadata Page titles
- Current value: Unique titles are set for Home, About, Services, Gallery, FAQ, Contact, and a service-detail fallback; the base title is in `index.html`.
- File location: `src/main.tsx`; fallback in `index.html`
- Where in file: Search for `const titles` inside `Seo`; search for `<title>` in `index.html`
- How to change: Edit the matching title inside the `titles` object. Update the base title in `index.html` as a fallback for the first page load.

### SEO & Metadata Meta description
- Current value: `DentServe Dental Clinic offers comfortable, modern dental care in Kalwa, Thane.`
- File location: `index.html`
- Where in file: Search for `meta name="description"`
- How to change: Replace the `content` text with the clinic’s preferred SEO description, ideally under about 160 characters.

### SEO & Metadata Open Graph image and text
- Current value: No Open Graph tags or image are used because no approved social image was supplied.
- File location: `index.html`
- Where in file: Search for `og:`
- How to change: Add `og:title`, `og:description`, `og:type`, and `og:image` tags inside `<head>` after an approved image is available.

### SEO & Metadata Schema.org structured data
- Current value: A `Dentist` JSON-LD block is generated from the verified clinic name, address, phone, hours, and current site URL.
- File location: `src/main.tsx`
- Where in file: Search for `dentserve-schema` inside `Seo`
- How to change: Update the source values in `src/data/site.ts`. If verified coordinates become available, add them to the schema object in `Seo`.

### Forms Submission destination
- Current value: No email/API endpoint; front-end form only.
- File location: `src/main.tsx`
- Where in file: Search for `AppointmentForm` and `onSubmit`
- How to change: Replace the placeholder submit handler with the approved form service endpoint and add a success message that is approved by the clinic.

### Forms Hardcoded confirmation text
- Current value: `We’ll confirm your preferred time by phone. No online payment required.`; no business name in a confirmation state.
- File location: `src/main.tsx`
- Where in file: Search for `We’ll confirm`
- How to change: Edit the sentence under the form if the clinic’s response process changes.

### Colors/Theme Primary brand colors
- Current value: Navy `#0b1f3a`, blue `#2563eb`, teal `#15b8a6`, pale background `#f5f9fc`.
- File location: `src/styles.css`
- Where in file: Search for `:root` and the variable names `--navy`, `--blue`, `--teal`, `--pale`
- How to change: Replace the hex values in `:root`. The entire site uses these variables, so this is the preferred re-theme location.
