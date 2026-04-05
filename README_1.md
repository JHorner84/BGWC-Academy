# BGWC Academy Arizona — Website

**Live site:** https://jhorner84.github.io/BGWC-Academy/

USA Wrestling chartered youth wrestling club in Waddell, Arizona.  
Charter No. 2300052502 | Est. 2005

---

## Site Structure

```
BGWC-Academy/
├── index.html              ← Homepage
├── README.md               ← This file (not visible to site visitors)
├── assets/
│   ├── site.css            ← Shared stylesheet (all pages use this)
│   ├── BGWC_Academy_Logo_600px.png
│   ├── BGWC_Academy_Logo_Transparent.png
│   ├── hero-wrestling.jpg      ← Add this image
│   └── little-lions-flyer.jpg  ← Add this image
├── about/index.html        ← Club history, mission, USA Wrestling charter
├── blog/index.html         ← News, tournament recaps, athlete spotlights
├── coaches/index.html      ← Coaching staff bios
├── community/index.html    ← Band app — official club communication
├── donate/index.html       ← Giving, Arizona tax credit, sponsorship tiers
├── forms/index.html        ← All Google Forms (registration, waivers, inquiry, contact)
├── gallery/index.html      ← Tabbed photo gallery
├── programs/index.html     ← Little Lions + Youth Wrestling detail
├── resources/index.html    ← Parent resources, rules, recognition
├── schedule/index.html     ← Practice schedule + Google Calendar embed
└── store/index.html        ← Merch store (Bonfire / Printful / Custom Ink)
```

---

## Navigation (all pages)

Home · Programs · About · Coaches · Schedule · Gallery · News · Store · Community · Resources · Donate · Register Now

---

## First-Time GitHub Pages Setup

### Step 1 — Clone the repo
```bash
git clone https://github.com/JHorner84/BGWC-Academy.git
cd BGWC-Academy
```

### Step 2 — Copy all site files in
Match the folder structure above exactly. The assets/ folder must contain site.css and both logo images or the site will not display correctly.

### Step 3 — Push to GitHub
```bash
git add .
git commit -m "Initial site build"
git push origin main
```

### Step 4 — Enable GitHub Pages
1. Go to your repo: https://github.com/JHorner84/BGWC-Academy
2. Click Settings → Pages
3. Source: Deploy from a branch
4. Branch: main | Folder: / (root)
5. Click Save

Live at: https://jhorner84.github.io/BGWC-Academy/
Takes about 60 seconds after pushing.

---

## Every Future Update

```bash
git add .
git commit -m "Describe what you changed"
git push origin main
```

GitHub Desktop users: copy changed files into the repo folder, type a summary, click Commit to main, then Push origin.

---

## Google Workspace Integration

All dynamic functionality uses Google's free tools. Nothing form-related lives in this repo.

### Google Forms — forms/index.html
Each tab (Registration, Waivers, Inquiry, Contact) has a placeholder with exact instructions.
1. Build each form at forms.google.com
2. Set response destination to a Google Sheet
3. Click Send → embed icon → copy the iframe
4. In forms/index.html, find the gform-placeholder div for that tab
5. Replace the entire placeholder div with the iframe
6. Commit and push

### Google Calendar — schedule/index.html
1. Create a club calendar at calendar.google.com
2. Three dots → Settings and sharing → Integrate calendar → copy Embed code
3. In schedule/index.html, replace the gcal-placeholder div with the iframe
4. Share the public calendar URL with families so they can subscribe

### Newsletter — blog/index.html
A Google Form with Name + Email fields, embedded in the blog sidebar.
1. Build the form at forms.google.com
2. Embed it in the sidebar placeholder in blog/index.html
3. Responses go to a Google Sheet — use that as your email list

### Google Photos — gallery/index.html
1. Create albums at photos.google.com (Practice, Tournaments, Little Lions, Recognition)
2. Share each album → Create link
3. Replace photo slot placeholders with real image tags or link to the shared album URL

---

## Band App — community/index.html

Band is the club's official communication app.

To activate the invite link:
1. Open Band on your phone
2. Go to your BGWC Academy group
3. Tap the three dots (top right) → Invite via link
4. Copy that URL
5. In community/index.html, find the two spots marked YOUR-INVITE-CODE
6. Replace both with your actual Band invite URL
7. Commit and push

---

## Merch Store — store/index.html

Three platform options are documented on the page. Bonfire is the fastest to set up.

To activate:
1. Set up your store on Bonfire (bonfire.com), Printful, or Custom Ink Fundraising
2. Get your store URL or embed code
3. In store/index.html, find the button with href="https://www.bonfire.com"
4. Replace that href with your actual store URL
5. Commit and push

---

## Adding Content

### Add a blog post
In blog/index.html, find #posts-list and copy one of the article.card.post-card blocks.
Paste it at the top of the list and update:
- data-cat attribute: news / tournament / spotlight / schedule
- Category badge class and label
- Post date, h2 title, p excerpt
- Image src if you have a photo (place it in assets/)

### Add coach photos
In coaches/index.html, find the coach-photo divs and replace with:
  <img src="../assets/coach-name.jpg" alt="Coach Name" />

### Add practice schedule
In schedule/index.html, find .day-placeholder divs and replace with:
  <div class="day-row">
    <span class="day-name">Monday</span>
    <span class="day-time">6:00 PM - 8:00 PM</span>
  </div>

### Add gallery photos
Place images in assets/, then in gallery/index.html replace each photo-slot div with:
  <div class="photo-slot">
    <img src="../assets/photo-name.jpg" alt="Description" />
  </div>

---

## What Lives Where

  Thing                  | Where it lives         | In this repo?
  HTML pages             | GitHub Pages           | Yes
  Stylesheet (site.css)  | GitHub Pages           | Yes
  Logo and images        | GitHub Pages (assets/) | Yes
  Google Forms           | Google's servers       | No
  Form submissions       | Google Sheets          | No
  Club calendar          | Google Calendar        | No
  Photo library          | Google Photos          | No
  Band group             | Band's servers         | No
  Merch store            | Bonfire / Printful     | No

---

## Colors & Design Reference

  Navy  #0F2340  Primary dark, headings
  Gold  #C9A44A  Accent, highlights, CTAs
  Red   #B2222E  Action buttons, badges
  Cream #F4EFE6  Background sections
  White #FFFFFF  Cards, forms

Fonts: Barlow Condensed (headings) + Lato (body)
Both load from Google Fonts — no font files needed in the repo.

---

## Club Info

BGWC Academy Arizona
17600 West Olive Ave, Waddell, AZ 85355
USA Wrestling Charter No. 2300052502
Est. 2005
