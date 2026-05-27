# Voices of the Creek — The Efik People of Nigeria
A premium, multi-page cultural showcase of the Efik people of Calabar, Cross River State, Nigeria. Prepared as part of the academic coursework for the Department of Communication and Language Arts (CLA 706: Indigenous Communication Systems) at the University of Ibadan.

This project has been refactored from a single monolithic file into a clean, modular multi-page static website to ensure ease of deployment, robust portability, and professional presentation.

---

## 📂 Project Architecture

```bash
Voices_of_the_creek/
├── index.html        # Landing page (Hero, Intro, Blog Card Deck, Quote Band, Footer)
├── post-1.html       # Part 1: Origins, Land, and Governance
├── post-2.html       # Part 2: Culinary Delights, Rhythmic Traditions, and Royal Leadership
├── post-3.html       # Part 3: Contemporary Challenges and Protecting Indigenous Cultures
├── styles.css        # Centralized stylesheet (all custom typography, layout grids, variables, and transitions)
├── README.md         # Project documentation (this file)
└── IMG-*.jpg         # Mapped visual media assets (12 files)
```

---

## 🛠️ Summary of Refactoring Steps Done

1. **Decoupled Monolithic Styling**:
   - Extracted all styling rules into an external, shared stylesheet: [styles.css](styles.css).
   - Cleaned the main pages of inline CSS blocks, reducing `index.html` from **1,384 lines** to a highly readable **178 lines**.
   - Preserved all curated typography imports (`Playfair Display`, `Lora`, `DM Sans`), CSS variables, responsive viewport rules, and transitions.

2. **Created Native Subpages**:
   - Split each of the three blog posts into individual, fully structured files (`post-1.html`, `post-2.html`, and `post-3.html`).
   - Integrated custom subpage navigation: links inside subpages (`Blog Posts`, `About`) correctly target the specific sections of the homepage using smooth URL anchors.
   - Built bottom-navigation rows in all articles for intuitive browsing (`Previous Article`, `Back to Home`, `Next Article`).

3. **Populated Visual Placeholders**:
   - Replaced all SVG dotted outlines across the cards and inline article figures with responsive image tags loading your provided local `.jpg` photos.
   - Swapped the post headers for Post 2 and Post 3 as requested to align the media assets with the subject matter.

4. **Optimized Scripts & Speed**:
   - Removed obsolete JS visibility toggles (`showHome` and `showPost`), allowing pages to render statically and instantly.
   - Preserved the clean **Intersection Observer** scroll-reveal animation script on the homepage for standard modern transitions.

---

## 📷 Image Specification Catalog
Below is the definitive mapping of the images in the website. Use this guide if you wish to swap these images with other assets of your choice in the future:

| Page / Section | Current Filename | Position & Purpose | Ideal Visual Theme / Subject | Aspect Ratio | Recommended Search Terms |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Home Page** | `IMG-20260526-WA0114.jpg` | Intro Section Image | Efik women in traditional beaded attire, wrappers, and coral beads. | **4:5** (Portrait) | `"Efik traditional attire"`, `"Efik wedding beads"`, `"Calabar women"` |
| **Part 1 (Blog Card & Hero)** | `IMG-20260526-WA0115.jpg` | Card 1 in `index.html` & Header in `post-1.html` | Aerial landscape of Calabar, Cross River coastline, or Calabar city scenery. | **16:10** (Card) & **Full-width** (Hero) | `"Calabar city aerial"`, `"Cross River Nigeria"`, `"Calabar waterways"` |
| **Part 1 (Figure 1)** | `IMG-20260526-WA0116.jpg` | Inline image in `post-1.html` (first body section) | Efik elders and men dressed in their elegant traditional attire. | **16:9** (Landscape) | `"Efik traditional attire"`, `"Efik elders Calabar"` |
| **Part 1 (Figure 2)** | `IMG-20260526-WA0117.jpg` | Inline image in `post-1.html` (second body section) | Vibrant performers in elaborate beaded costumes at the Calabar Carnival. | **16:9** (Landscape) | `"Calabar Carnival"`, `"Efik Ekpe masquerade"` |
| **Part 2 (Blog Card & Hero)** | `IMG-20260526-WA0121.jpg` | Card 2 in `index.html` & Header in `post-2.html` | A majestic view of Ekombi dance performers or a traditional royal Efik feast. | **16:10** (Card) & **Full-width** (Hero) | `"Ekombi dance"`, `"Calabar dance traditional"`, `"Efik palace"` |
| **Part 2 (Figure 3)** | `IMG-20260526-WA0119.jpg` | Inline image in `post-2.html` (first body section) | A premium bowl of Edikang Ikong soup served with pounded yam/eba. | **16:9** (Landscape) | `"Edikang Ikong soup"`, `"Nigerian traditional soup"`, `"Calabar food"` |
| **Part 2 (Figure 4)** | `IMG-20260526-WA0120.jpg` | Inline image in `post-2.html` (second body section) | Close-up of Ekombi dancers demonstrating wave-like movements in brass leg bangles. | **16:9** (Landscape) | `"Ekombi performers"`, `"Calabar traditional dance"` |
| **Part 3 (Blog Card & Hero)** | `IMG-20260526-WA0118.jpg` | Card 3 in `index.html` & Header in `post-3.html` | Scenery representing environmental impact along the Cross River coast or a community meeting. | **16:10** (Card) & **Full-width** (Hero) | `"Niger Delta river"`, `"Calabar coast pollution"`, `"Nigerian community gather"` |
| **Part 3 (Figure 5)** | `IMG-20260526-WA0122.jpg` | Inline image in `post-3.html` (first body section) | Mangrove waterway ecosystem showing local livelihood activities like fishing. | **16:9** (Landscape) | `"mangrove swamp Nigeria"`, `"creek fishing Nigeria"` |
| **Part 3 (Figure 6)** | `IMG-20260526-WA0123.jpg` | Inline image in `post-3.html` (second body section) | His Royal Majesty, the Obong of Calabar, addressing his people from the throne. | **16:9** (Landscape) | `"Obong of Calabar"`, `"Efik king throne"` |

---

## 🚀 How to Host on Vercel

Vercel is an excellent hosting platform for static websites. You can deploy this project to the web for free in just a few steps:

### Option A: Using the Vercel Dashboard (No Coding Required)
1. Sign up for a free account on [vercel.com](https://vercel.com).
2. Compress your project folder `Voices_of_the_creek` into a **.zip** file.
3. In the Vercel Dashboard, go to **Add New...** -> **Project**.
4. Scroll down to the **"Browse Templates"** / **"Import"** section and select the option to drag-and-drop or upload a folder/zip file.
5. Upload your folder. Vercel will automatically detect the static HTML/CSS files and deploy them instantly!

### Option B: Using GitHub (Recommended for Continuous Deployment)
1. Initialize a Git repository in your project folder, commit your changes, and push them to a new repository on GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   # Create a repository on GitHub, then link and push:
   git remote add origin <your-github-repo-url>
   git branch -M main
   git push -u origin main
   ```
2. Log in to [vercel.com](https://vercel.com) using your GitHub account.
3. Click **"Add New"** -> **"Project"** in Vercel.
4. Select your newly created GitHub repository from the list.
5. Click **"Deploy"**. Any changes you push to GitHub in the future will automatically update your live website!

### Option C: Using the Vercel Command-Line Interface (CLI)
If you have Node.js and the Vercel CLI installed on your local computer, open your terminal in the project directory and run:
```bash
vercel
```
Follow the interactive prompts to log in and set up your project. To deploy to production, run:
```bash
vercel --prod
```
