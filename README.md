# Vedaprakash Kamaraj — Portfolio

A single-page portfolio website for **Vedaprakash Kamaraj**, network architect and creative technologist. Built with plain HTML, CSS and JavaScript, plus [three.js](https://threejs.org/) for the 3D scenes. No build step and no dependencies to install.

## Pages

The site is one file (`index.html`) with hash-based pages, e.g. `index.html#/about`:

| Page | What it shows |
| --- | --- |
| Home | Name, photo, spider-themed background, "slide for next page" slider |
| About | Background, teaching experience and interests |
| Network | Interactive 3D network topology (click devices to inspect) |
| World | 3D global network globe |
| Skills | Skills radar, strengths and filterable skill cards (Networking, Security, Cloud & Automation, Creative Dev, Linux & DevOps, Hardware) |
| Projects | Selected projects with details |
| Tech | Live "Latest Tech Radar" with a sweeping scan |
| Camera | Camera technology aspirations |
| Contact | Email form and social links |

Other features: draggable spider and swipe to change pages, AI-style web assistant (bottom-right button), and a responsive layout for phones and desktops.

## Project structure

```
.
├── index.html   # the whole site (HTML + CSS + JS, photo embedded)
├── README.md
├── .gitignore
└── .nojekyll    # tells GitHub Pages to serve the files as-is
```

## Run locally

Just open `index.html` in a browser. Or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

An internet connection is needed for three.js and Google Fonts, which load from a CDN.

## Deploy on GitHub Pages

1. Create a new repository on GitHub (for example `portfolio`).
2. Upload all files from this folder, or push them:
   ```bash
   git init
   git add .
   git commit -m "Add portfolio website"
   git branch -M main
   git remote add origin https://github.com/<your-username>/portfolio.git
   git push -u origin main
   ```
3. In the repository go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select **main** and **/ (root)**, then **Save**.
5. After a minute your site is live at `https://<your-username>.github.io/portfolio/`.

## Things to edit before publishing

Open `index.html` and search for these:

- `const EMAIL='veda@example.com'` — replace with your real email address (used by the Contact form).
- `const SOCIAL={github:..., linkedin:..., instagram:...}` — replace with your own profile URLs.
- WhatsApp link — find `wa.me` to update or remove it.
- Project, skill and tech-radar content — look for the `PROJ`, `TECH` and skills arrays in the script.

## Credits

- 3D graphics: [three.js](https://threejs.org/) r128
- Fonts: Inter, JetBrains Mono, Bangers (Google Fonts)
