# How to Edit This Website — Plain English Guide

This guide shows you how to update common things on the website **without
needing to know HTML**. Each section has a copy-paste recipe.

---

## ✏️ Add a news item

**File:** `index.html`
**What to look for:** the section that starts with `<!-- ====== NEWS ====== -->`

Inside the `<ul class="news-list">`, **paste this block at the very top** (right after the `<ul>` line):

```html
<li>
  <span class="news-date">[2026-05]</span>
  Your news content here. You can include <a href="https://link.com" target="_blank" rel="noopener">links</a> and <em>italics</em>.
</li>
```

Change:
- `[2026-05]` → the date you want shown
- The text after it → your news

Save → done. The newest items go on top.

---

## 📄 Add a publication

**File:** `publications.html`

### If the paper is from a year already on the page:

Find that year's section (e.g., `<!-- ====== 2025 ====== -->`).
Inside the `<ul class="pub-list">`, paste this block:

```html
<li>
  <span class="pub-title">Your paper title here</span>
  <span class="pub-authors">A. One, <span class="self">C. Zhang</span>, B. Two</span>
  <span class="pub-venue">Venue Name 12 (3), 100-200, 2025
    <span class="pub-citations">12 citations</span>
  </span>
</li>
```

Change:
- The title text
- The authors (wrap Prof. Zhang's name with `<span class="self">C. Zhang</span>` to bold him)
- The venue, volume, pages, year
- The citation count (or remove the entire `<span class="pub-citations">` block if not needed)

### If the paper is from a NEW year not yet on the page:

Copy this entire block and paste it in the right spot (newest year at the top):

```html
<!-- ====== 2027 ====== -->
<section class="card">
  <div class="year-section">
    <h3>2027</h3>
    <ul class="pub-list">
      <li>
        <span class="pub-title">Paper title</span>
        <span class="pub-authors">Authors here, <span class="self">C. Zhang</span></span>
        <span class="pub-venue">Venue, 2027</span>
      </li>
    </ul>
  </div>
</section>
```

---

## 👥 Add a team member

**File:** `team.html`

First, **delete** the `<div class="coming-soon"> ... </div>` block (the "Coming Soon" message).

Then paste this in its place:

```html
<h3>Current PhD Students</h3>
<ul>
  <li><strong>Student Name 1</strong> — Research topic, started 2024</li>
  <li><strong>Student Name 2</strong> — Research topic, started 2023</li>
</ul>

<h3>Master's Students</h3>
<ul>
  <li><strong>Name</strong> — Topic</li>
</ul>

<h3>Alumni</h3>
<ul>
  <li><strong>Dr. Past Student</strong> — PhD 2023, now Assistant Professor at XYZ University</li>
</ul>
```

Add or remove `<li>...</li>` lines as needed.

---

## 🏆 Add awards

**File:** `awards.html`

Delete the `<div class="coming-soon">` block, paste this:

```html
<ul class="news-list">
  <li><span class="news-date">[2024]</span> Award name, granting body</li>
  <li><span class="news-date">[2022]</span> Best Paper Award, IEEE Conference XYZ</li>
  <li><span class="news-date">[2020]</span> Outstanding Researcher Award, Henan University</li>
</ul>
```

---

## 🎓 Add academic services

**File:** `services.html`

Delete the `<div class="coming-soon">` block, paste this:

```html
<h3>Editorial Boards</h3>
<ul>
  <li>Associate Editor, <em>Journal Name</em>, 2023–present</li>
</ul>

<h3>Conference Organization</h3>
<ul>
  <li>Area Chair, AAAI 2025</li>
  <li>Senior PC Member, IJCAI 2024</li>
</ul>

<h3>Reviewing</h3>
<p>
  Regular reviewer for <em>IEEE TPAMI</em>, <em>IEEE TNNLS</em>,
  <em>Pattern Recognition</em>, <em>AAAI</em>, <em>IJCAI</em>, <em>NeurIPS</em>,
  <em>CVPR</em>, <em>ICCV</em>, and <em>KDD</em>.
</p>
```

---

## 📷 Change the profile photo

1. Put your new photo into the `images` folder.
2. Either:
   - Rename it to `profile.gif`, OR
   - In `index.html`, find the line `<img src="images/profile.gif"` and change `profile.gif` to your new filename (e.g., `profile.jpg`).

---

## 🎨 Change the colors / theme

**File:** `css/style.css`
**Look at the top of the file** for `:root { ... }`. Each line is a color. Change the value (e.g., `#1a4ed8` → `#c0392b`) and **every page** updates.

Most useful ones to change:
- `--color-link` — the blue color of all links
- `--color-accent` — the gold color used for the underline under the active nav and section headers
- `--color-bg` — the page background
- `--color-card` — the white card background

---

## 📊 Update the citation stats on the homepage

**File:** `index.html`
**Look for:** `<div class="stats">`

Update the numbers (`2,096`, `18`, `27`, `70+`) every few months by checking [Google Scholar](https://scholar.google.com/citations?user=iCmyLZYAAAAJ&hl=en).

---

## 🔄 Update navigation links (if you add a new page)

If you create a new page (e.g., `teaching.html`), you need to add it to the **top navigation on every page**.

In each `.html` file, find the `<nav class="topnav">` block and add a new line:

```html
<span class="sep">·</span>
<a href="teaching.html">Teaching</a>
```

(You'll need to do this in all 6 HTML files so the nav stays consistent.)

---

## ⚠️ Common mistakes to avoid

1. **Don't delete the `<` or `>` symbols** — they tell the browser where each piece of code starts and ends.
2. **Always close your tags** — if you open `<li>`, close it with `</li>`.
3. **Save the file in UTF-8** — otherwise Chinese characters break.
4. **Test locally first** — double-click `index.html` on your computer to preview before uploading.

---

## 💡 Tips

- Use [GitHub's web editor](https://github.dev) for nicer editing right in the browser. Just press `.` (period) on your repo page.
- Keep a backup folder of the original files.
- If something breaks, GitHub remembers every version — go to "commits" and restore.

That's it! Happy editing. 🎓
