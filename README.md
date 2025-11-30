<<<<<<< HEAD
# newcleanshotx
=======
# cleanshotx-free

A static site to be hosted on GitHub Pages. This README explains two simple ways to deploy:

## Quick setup
1. Create a GitHub repository (e.g. `https://github.com/USERNAME/REPO`).
2. Add this repo as `origin` in your local repo:

```bash
cd /Users/macbook/Downloads/cleanshotx-free
git remote add origin https://github.com/USERNAME/REPO.git
git branch -M main

A static site to be hosted on GitHub Pages. This README explains two simple ways to deploy:

git push -u origin main
```

3. Update `package.json` `homepage` to match your GitHub Pages URL:
```json
"homepage":"https://USERNAME.github.io/REPO"
```

### Option A — Deploy with `gh-pages` (automated)
- This repo already includes a `deploy` script which uses `gh-pages` to publish the `docs` folder (or root) to the `gh-pages` branch.

```bash
# ensure the remote exists and you're on main
git push origin main
npm run deploy
```


### Option B — Use `main` branch, `docs/` folder (no extra package)
- The `docs` folder already contains the site's static files. If you prefer to let GitHub Pages serve from the repository main branch's `docs/` folder:

1. Push the branch with `docs/` to GitHub:
```bash
git push origin main
```

2. In your GitHub repository, go to Settings → Pages → Build and Deployment → Branch: select `main` and folder `/docs`, then click Save.
Your site will usually be served at `https://USERNAME.github.io/REPO` within a few minutes.

### Additional notes
- If you have not created the repo yet, visit https://github.com/new and create it, then add it as `origin`.
- The `deploy` script requires write access to your repo. Make sure you can push.
- If your repo is a user site (e.g., `USERNAME.github.io`), set `homepage` to `https://USERNAME.github.io` and deploy either the `main` branch or the `gh-pages` branch accordingly.

If you'd like, I can:
1. Set your `homepage` automatically (just tell me your GitHub username and repo name);
2. Attempt to push the repo and run `npm run deploy` (you will need to provide or configure remote access/credentials);
3. Turn this into a Vite project and publish a build instead (HMR for dev & optimized build for GitHub Pages).
