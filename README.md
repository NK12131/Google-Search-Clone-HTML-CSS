# 🔍 Google Search Clone

> A front-end recreation of Google's search interface in plain HTML and CSS. It has three pages: web search, image search and advanced search. Each page sends your query straight to Google, with no JavaScript and no backend.

---

## ✨ Features

| Page | File | What it does |
|------|------|--------------|
| **Google Search** | `index.html` | The classic homepage: the multicolour logo, a centred search bar, and the **Google Search** and **I'm Feeling Lucky** buttons |
| **Image Search** | `image.html` | A search bar that sends your query to Google Images |
| **Advanced Search** | `Adv_search.html` | A form with four fields: *all these words*, *this exact word or phrase*, *any of these words* and *none of these words* |

- Links in the top corner move between the three pages
- **I'm Feeling Lucky** goes straight to the first result
- Plain HTML forms, with no frameworks and no build step

---

## ⚙️ How It Works

Each page is an HTML `<form>` whose `action` points at a Google endpoint. When you submit the form, the browser builds the URL from the input names and Google returns the results.

| Form | Action | Parameters |
|------|--------|-----------|
| Web search | `https://google.com/search` | `q` = query, `btnI` = I'm Feeling Lucky |
| Image search | `https://google.com/images` | `q` = query |
| Advanced search | `https://google.com/search` | `as_q` = all words, `as_epq` = exact phrase, `as_oq` = any words, `as_eq` = excluded words |

For example, typing `cats` in the exact-phrase field and `dogs` in the none-of-these-words field submits to:

```
https://google.com/search?as_q=&as_epq=cats&as_oq=&as_eq=dogs
```

---

## 🧰 Tech Stack

- **HTML5** for page structure and forms
- **CSS3** for layout and the Google-style look (`style.css`)

---

## 📁 Project Structure

```
Google-search-clone/
├── index.html        # Web search (homepage)
├── image.html        # Image search
├── Adv_search.html   # Advanced search
└── style.css         # Shared styles
```

---

## 🚀 Getting Started

No installation is needed.

1. **Clone the repo**
   ```bash
   git clone https://github.com/<your-username>/Google-search-clone.git
   cd Google-search-clone
   ```
2. **Open `index.html` in your browser.** You can double-click the file, or use a local server such as the VS Code **Live Server** extension.

### Optional: host it on GitHub Pages
In the repository, go to **Settings → Pages**, choose the `main` branch and the root folder, and save. The site is published at `https://<your-username>.github.io/Google-search-clone/`.

---

## 🎯 What I Learned

- How HTML forms build GET requests from input `name` attributes
- How Google's search URL parameters work (`q`, `btnI`, `as_q`, `as_epq`, `as_oq`, `as_eq`)
- How to lay out and style pages to closely match an existing UI with CSS alone

---

## 🛣️ Possible Improvements

- [ ] Responsive layout for mobile
- [ ] More advanced-search filters (language, region, file type, date)
- [ ] A search icon and a microphone icon in the search bar
- [ ] Dark mode

---

## ⚠️ Disclaimer

This is an educational project and is not affiliated with Google. "Google" is a trademark of Google LLC.
