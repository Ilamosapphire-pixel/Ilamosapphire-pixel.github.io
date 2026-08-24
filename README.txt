HOW TO ADD PHOTOS TO YOUR PORTFOLIO GALLERY
=============================================

1. Copy your photo files into this "images" folder
   (e.g. herskills-day1.jpg, empowerher-iseyin.jpg).

2. Open "manifest.json" in this same folder in any text editor.
   It's a simple list — add one line per photo, like this:

   [
     { "file": "herskills-day1.jpg", "caption": "HerSkills Cohort 1 orientation" },
     { "file": "empowerher-iseyin.jpg", "caption": "EmpowerHER session, Iseyin" }
   ]

   - "file" must exactly match the photo's filename in this folder.
   - "caption" is optional — you can leave it as "" if you don't want one.
   - Don't forget the comma between entries, and no comma after the last one.

3. Save manifest.json and refresh the portfolio page — your photo will appear
   in the gallery automatically.

IMPORTANT: Because this is a plain folder of files (not a live app), the
portfolio page can't "see" what's inside the images folder on its own — the
manifest.json list is what tells it which photos to show. Adding a photo
without adding it to manifest.json means it won't appear.

Also note: some browsers block a page from reading local files (like
manifest.json) when you just double-click the HTML file to open it. If the
gallery doesn't load, try either of these:
- Host the whole folder (portfolio.html + images/) on something like Netlify
  or GitHub Pages — it'll work immediately there.
- Or run a tiny local server from this folder, e.g. open a terminal here and
  run: python3 -m http.server, then visit http://localhost:8000 in your browser.
