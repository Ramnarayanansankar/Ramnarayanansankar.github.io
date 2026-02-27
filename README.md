# Personal Portfolio

A frontend-only portfolio site for **Ramnarayanan Sankar**, built with **Angular 17** (no backend required).

## Run the project

```bash
cd frontend
npm install
npm start
```

Open [http://localhost:4200](http://localhost:4200) in your browser.

## Build for production

```bash
cd frontend
npm run build
```

Output is in `frontend/dist/frontend/browser/`. Serve that folder with any static host (e.g. Netlify, Vercel, GitHub Pages).

## Deploy to GitHub Pages

Your site will be available at **`https://ramnarayanansankar.github.io/`** (user site; repo name is `Ramnarayanansankar.github.io`).

### 1. Create the repo and push code

- Use your repo **`Ramnarayanansankar.github.io`** (already created).
- From your project folder:

```bash
git remote add origin https://github.com/Ramnarayanansankar/Ramnarayanansankar.github.io.git
git branch -M main
git push -u origin main
```

### 2. Turn on GitHub Pages

- In the repo: **Settings** → **Pages**.
- Under **Build and deployment**:
  - **Source**: **GitHub Actions** (not “Deploy from a branch”).
- Save. No need to create a `gh-pages` branch.

### 3. Deploy

- The workflow in `.github/workflows/deploy-pages.yml` runs on every push to `main`.
- It builds the Angular app with the correct base href (`/`) and deploys to GitHub Pages.
- After it finishes (Actions tab → “Deploy to GitHub Pages” run), open:

  **`https://ramnarayanansankar.github.io/`**

### Local build with same base href (optional)

To test the production build as it will appear on GitHub Pages:

```bash
cd frontend
npm run build -- --configuration production --base-href /
npx serve dist/frontend/browser -s
```

Then open the URL shown (e.g. `http://localhost:3000/`).

## Project structure

- **frontend/** — Angular app (About, Experience, Education, Projects, Skills, Contact)
- **backend/** — Optional; not used. You can delete the `backend` folder if you want a frontend-only repo.

## Tech stack

- Angular 17, SCSS, Angular Router
