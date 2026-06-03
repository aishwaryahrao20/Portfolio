# Aishwarya portfolio starter (static site)

This is a lightweight, responsive portfolio website designed for deployment on **Vercel via GitHub**.

## What is included

- Dark / light mode toggle
- Clickable project list with dedicated detail pages
- Clickable experience list with dedicated detail page
- About section
- Contact section with email, phone, LinkedIn, and a quick email form
- Resume PDF included in `assets/resume/`

## Project structure

- `index.html` → homepage
- `projects/index.html` → projects list
- `projects/*/index.html` → project detail pages
- `experience/index.html` → experience list
- `experience/*/index.html` → experience detail page
- `assets/styles.css` → all styling
- `assets/script.js` → theme toggle, mobile menu, reveal animations, contact form helper

## Run locally

From the project folder:

```bash
python3 -m http.server 3000
```

Then open `http://localhost:3000` in your browser.

## Push to GitHub with GitHub CLI

```bash
git init
git add .
git commit -m "Initial portfolio site"
gh auth login
gh repo create aishwarya-portfolio --public --source=. --remote=origin --push
```

## Push to GitHub with plain Git

```bash
git init
git add .
git commit -m "Initial portfolio site"
git branch -M main
git remote add origin YOUR_GITHUB_REPO_URL
git push -u origin main
```

## Deploy to Vercel

### Recommended GitHub-connected flow

1. Sign in to Vercel.
2. Import the GitHub repository.
3. Deploy.
4. Every future push to GitHub will trigger a new deployment.

### CLI flow

```bash
npm i -g vercel
vercel
vercel --prod
```

## Fast edits you will probably make

- Update text in `index.html`
- Edit project detail pages in `projects/*/index.html`
- Edit experience detail page in `experience/project-intern-drdo-cair/index.html`
- Adjust colors and spacing in `assets/styles.css`
- Update contact links in the HTML files if needed

## Note about your phone number

The current contact section includes your phone number because it appears on your resume. If you prefer not to publish it publicly, remove the `tel:` link from `index.html`.
