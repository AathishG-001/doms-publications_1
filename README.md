# DoMS Publications Portal
**Department of Management Studies, NIT Trichy**

A free, self-hosted digital publications portal for magazines and newsletters.  
Zero cost. Zero branding. Publicly accessible forever via GitHub Pages.

---

## One-Time Setup (do this once)

### Step 1 — Create the GitHub repository
1. Go to [github.com](https://github.com) and log in
2. Click **New repository**
3. Name it: `doms-publications` (or anything you prefer)
4. Set it to **Public**
5. Click **Create repository**

### Step 2 — Upload the files
Upload these files to the root of the repository:
```
index.html
reader.html
publications.json
pdfs/           ← create this folder (upload any PDF inside to create it)
```

To create the `pdfs/` folder: upload your first PDF into a folder named `pdfs/`.

### Step 3 — Enable GitHub Pages
1. Go to your repository → **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Branch: `main` | Folder: `/ (root)`
4. Click **Save**

Your site will be live at:
```
https://YOUR-USERNAME.github.io/doms-publications/
```

(Takes 2–3 minutes the first time.)

---

## Adding a New Publication (every quarter / bi-monthly)

This is all you need to do every time you publish a new issue:

### Step 1 — Upload the PDF
1. Go to your repository on GitHub
2. Click on the `pdfs/` folder
3. Click **Add file → Upload files**
4. Upload your PDF
5. Use a clear filename, e.g.:
   - `nexus-vol2-2026.pdf`
   - `newsletter-1-2026.pdf`
6. Click **Commit changes**

### Step 2 — Update publications.json
1. Click on `publications.json` in the repository
2. Click the **pencil icon** (Edit this file)
3. Add a new entry at the **top** of the list:

```json
{
  "title": "NEXUS Management Review — Vol. II",
  "type": "magazine",
  "issue": "Vol. II · 2026",
  "date": "March 2026",
  "desc": "Brief description of this issue's theme.",
  "file": "pdfs/nexus-vol2-2026.pdf"
},
```

- `type` must be either `"magazine"` or `"newsletter"`
- `file` must exactly match the filename you uploaded
- The first item in the list appears as "Latest" on the portal

4. Click **Commit changes**

The portal updates automatically within seconds.

---

## Giving Others Upload Access

For multiple team members to upload:
1. Go to repository **Settings → Collaborators**
2. Click **Add people**
3. Add their GitHub username
4. They accept the invitation via email

They can then upload PDFs and edit `publications.json` directly from GitHub's web interface — no coding required.

---

## File Naming Convention (recommended)

| Type | Format | Example |
|---|---|---|
| Magazine | `nexus-volN-YYYY.pdf` | `nexus-vol2-2026.pdf` |
| Newsletter | `newsletter-N-YYYY.pdf` | `newsletter-3-2026.pdf` |

---

## Your Public URL

Once deployed:
```
https://YOUR-USERNAME.github.io/doms-publications/
```

Share this URL with students, faculty, alumni, and recruiters.  
No login required. No ads. No watermarks.

---

## Troubleshooting

**PDF not loading in reader?**  
→ Check that the filename in `publications.json` exactly matches the uploaded file (case-sensitive).

**Site not updating after edit?**  
→ GitHub Pages takes 1–3 minutes to rebuild. Hard-refresh the browser (Ctrl+Shift+R).

**Reader showing blank page?**  
→ The PDF may be corrupt or password-protected. Test it locally first.
