# YourOrg Advocacy Site

A clean, cozy advocacy site built with Bulma CSS + a custom design system.

**Colors:** Anchor Purple + Soft White  
**Fonts:** Lora (headings) + DM Sans (body)  
**Hosting:** GitHub Pages  

---

## 📁 File Structure

```
advocacy-site/
├── index.html              ← Homepage
├── about.html              ← About page
├── issues.html             ← Issues/campaigns page (build next)
├── resources.html          ← Resources page (build next)
├── contact.html            ← Contact page (build next)
├── team.html               ← Team page (build next)
├── blog/
│   ├── index.html          ← Blog listing page
│   ├── post-template.html  ← Copy this for every new post ← ← ←
│   └── [your-post].html    ← Actual blog posts go here
├── assets/
│   ├── css/style.css       ← All design system styles (edit here)
│   └── js/main.js          ← Nav + scroll behavior
└── _templates/
    └── PAGE_TEMPLATE.html  ← Copy this for every new page ← ← ←
```

---

## 🚀 Deploying to GitHub Pages

1. Create a new repo on GitHub (e.g. `yourorg-site`)
2. Push all these files to the `main` branch
3. Go to **Settings → Pages → Source: main branch / root**
4. Your site is live at `https://yourusername.github.io/yourorg-site`

**With Claude Code:**
```
git init
git add .
git commit -m "Initial site"
git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

---

## ✏️ How to Add a New Page

1. **Copy** `_templates/PAGE_TEMPLATE.html`
2. **Rename** it (e.g. `team.html`)
3. **Edit** the `<title>` and `<meta name="description">`
4. **Replace** the content placeholder with your content
5. **Add** the page link to the navbar in ALL pages (or ask Claude Code to do it)

**Ask Claude Code:**
> "Create a new page called `team.html` based on `_templates/PAGE_TEMPLATE.html`. Add a grid of 4 team member cards using the `.card-cozy` style. Add the page to the navbar in all HTML files."

---

## 📝 How to Add a New Blog Post

1. **Copy** `blog/post-template.html`
2. **Rename** it (e.g. `blog/housing-bill-2025.html`)
3. **Edit** the title, tag, author, date, and content
4. **Replace** the featured diagram placeholder with an SVG diagram
5. **Add** a card for it in `blog/index.html` and on `index.html` (latest posts section)

**Ask Claude Code:**
> "Create a new blog post at `blog/housing-bill-2025.html` based on `blog/post-template.html`. Title: 'What the new housing bill means for renters'. Tag: Housing. Write 400 words of plain-language content explaining the bill. Add an SVG bar chart diagram. Then add a card for this post at the top of `blog/index.html`."

---

## 🎨 Customizing the Design

All colors, fonts, and spacing live in `assets/css/style.css` at the top:

```css
:root {
  --purple-anchor:  #5440a4;   ← Main brand color
  --purple-deep:    #3b2a6e;   ← Dark headings
  --purple-blush:   #ede9f9;   ← Background tints
  --white-warm:     #faf9f6;   ← Page background
  /* ... */
}
```

**Ask Claude Code:**
> "Change the main brand color from #5440a4 to #6b4fa8 throughout the site."

---

## 🧩 Component Reference (CSS Classes)

| Class | Use |
|---|---|
| `.card-cozy` | Standard content card with dotted border |
| `.btn-primary` | Filled purple button |
| `.btn-outline` | Dotted border button |
| `.diagram-wrap` | Container for an SVG/image with dotted frame |
| `.diagram-placeholder` | Empty diagram slot (replace with real content) |
| `.callout-cozy` | Pull quote or highlighted callout |
| `.stat-box` | Large number + label stat box |
| `.blog-tag` | Small pill category tag |
| `.two-col` | 50/50 two-column layout |
| `.grid-2/3/4` | Responsive grid layouts |
| `.prose` | Long-form article text formatting |
| `.section-cozy` | Standard section with padding |
| `.page-hero` | Inner page header with breadcrumb |
| `.fade-up` | Fade-in-on-scroll animation |

---

## 💬 Useful Claude Code Prompts

**Update navbar across all pages:**
> "Add a new nav link for `faq.html` labeled 'FAQ' to the navbar in every HTML file in this project."

**Build a new section:**
> "Add a 'Meet the Team' section to `about.html` using `.grid-3` and `.card-cozy` cards. Each card should have a name, role, and short bio. Use the existing design system styles."

**Update footer across all pages:**
> "Update the footer copyright year to 2025 in every HTML file."

**Add a new issue card to issues.html:**
> "Add a fourth issue card to `issues.html` about mental health advocacy. Use the `.card-cozy` style with a 🧠 icon."
