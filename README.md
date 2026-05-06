# Prof. Chongsheng Zhang — Academic Homepage

A clean, professional academic homepage built with plain HTML and CSS.
No build step. No frameworks. Just open the files and edit.

---

## 📁 What's in this folder

```
zhang-homepage/
├── index.html              ← Home page (photo, bio, news)
├── research.html           ← Research themes
├── publications.html       ← Paper list grouped by year
├── team.html               ← Lab members (placeholder)
├── services.html           ← Academic services (placeholder)
├── awards.html             ← Awards (placeholder)
├── css/
│   └── style.css           ← All styling lives here
├── images/
│   └── profile.gif         ← Profile photo
├── README.md               ← THIS FILE — deployment instructions
└── EDITING_GUIDE.md        ← How to update content easily
```

---

## 🚀 How to Deploy on GitHub Pages — Step by Step

This guide assumes you have **never used GitHub before**. Just follow each step.

### Step 1 — Create a GitHub account (skip if you have one)

1. Go to **https://github.com/signup**
2. Use your university email if possible (you get free Pro features as a student/teacher).
3. Verify your email.

### Step 2 — Create a new repository

The repository name **decides your website URL**, so this matters.

1. Click the **+** icon at the top-right of GitHub → **New repository**.
2. **Repository name:** type `YOUR-USERNAME.github.io`
   (replace `YOUR-USERNAME` with your actual GitHub username — for example, if your username is `czhang`, the repo name is `czhang.github.io`)
3. Set it to **Public** (required for free GitHub Pages).
4. ✅ Check **"Add a README file"**
5. Click **Create repository**.

> ⚠️ The name **must** be exactly `username.github.io` — that's what tells GitHub to publish it as a website automatically. If the username doesn't match, it will not work.

### Step 3 — Upload all the files

You have two options. **Option A is easier** — no command line needed.

#### Option A — Upload through the browser (recommended for beginners)

1. Inside your new repository, click **Add file** → **Upload files**.
2. Open the `zhang-homepage` folder on your computer.
3. Select **all the files and folders** (`index.html`, `research.html`, `publications.html`, `team.html`, `services.html`, `awards.html`, the `css` folder, the `images` folder, both `.md` files).
4. Drag them all into the upload box on GitHub.
5. Wait until they all finish uploading (you'll see green checkmarks).
6. Scroll down. In the **Commit changes** box, type something like `Initial homepage upload`.
7. Click **Commit changes**.

> 📌 If GitHub complains the folder is too big, upload the `css` folder first (commit), then the `images` folder (commit), then the HTML files (commit). It works fine in batches.

#### Option B — Use Git (if you're comfortable with the command line)

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
cd YOUR-USERNAME.github.io
# Copy all files from zhang-homepage/ into this folder
cp -r /path/to/zhang-homepage/* .
git add .
git commit -m "Initial homepage upload"
git push origin main
```

### Step 4 — Enable GitHub Pages

For repositories named `username.github.io`, this is usually automatic. To verify:

1. Go to your repository → **Settings** (top menu, far right).
2. In the left sidebar, click **Pages**.
3. Under **Source**, make sure it says **Deploy from a branch**.
4. Branch should be **main** and folder should be **`/ (root)`**.
5. Click **Save** if changes were needed.

### Step 5 — Visit your live website! 🎉

After **1–3 minutes**, your site will be live at:

> **https://YOUR-USERNAME.github.io**

For example: `https://czhang.github.io`

If you see the page — congratulations, it's live! Share the URL.

If you see a 404 error after 5 minutes:
- Make sure the file is named exactly `index.html` (not `Index.html` or `index.htm`)
- Check that the repository is **Public**, not Private
- Wait another few minutes — sometimes the first deploy is slow

---

## 🔄 How to Update the Website Later

Whenever you change anything, you have two options:

### Easy way (browser):
1. Go to your repo on GitHub.
2. Click on the file you want to edit (e.g., `index.html`).
3. Click the **pencil icon** (Edit this file).
4. Make changes.
5. Scroll down → click **Commit changes**.
6. The site updates within ~1 minute.

### To replace the photo:
1. Go into the `images` folder on GitHub.
2. Delete `profile.gif`.
3. Upload your new photo.
4. **Important:** rename your new photo to `profile.gif` (or update the `<img src="...">` line in `index.html` to match the new filename).

---

## 🌐 Optional: Use a custom domain

If your professor owns a domain like `chongshengzhang.com`:

1. In your repo → **Settings** → **Pages** → **Custom domain**, type the domain.
2. At your domain registrar (GoDaddy, Namecheap, etc.), add these DNS records:
   - Type: `A`, Name: `@`, Value: `185.199.108.153`
   - Type: `A`, Name: `@`, Value: `185.199.109.153`
   - Type: `A`, Name: `@`, Value: `185.199.110.153`
   - Type: `A`, Name: `@`, Value: `185.199.111.153`
   - Type: `CNAME`, Name: `www`, Value: `YOUR-USERNAME.github.io`
3. Wait up to 24 hours for DNS to propagate.
4. Tick **Enforce HTTPS** in GitHub Pages settings.

---

## ❓ FAQ

**Q: Can multiple people edit the site?**
A: Yes — go to repo → Settings → Collaborators → Add people.

**Q: How do I track changes / undo?**
A: GitHub keeps full history. Repo → "commits" tab shows everything; you can revert any change.

**Q: The Chinese characters look weird on someone's browser.**
A: They shouldn't — the site declares `<meta charset="UTF-8">`. If it happens, they're using a very old browser.

**Q: Where do I edit the colors / fonts?**
A: Open `css/style.css`. The top section called `:root { ... }` has all the colors. Change one value, all pages update.

---

## 📖 Now read EDITING_GUIDE.md

For step-by-step instructions on **adding publications, news, and team members**, open `EDITING_GUIDE.md`.
