# Light Up NYC — GitHub Pages Setup (free, no backend)
## ~10 minutes, completely free, no accounts other than GitHub

This version has **no database and no admin panel**. You edit one list of
names/amounts directly in the file, save it, and push to GitHub. That's it.

---

## Step 1 — Create a GitHub account (if you don't have one)

Go to **https://github.com** and sign up. Free.

---

## Step 2 — Create a new repository

1. Click the **+** in the top right → **New repository**
2. Name it something like `nyc-marathon` (this becomes part of your URL)
3. Set it to **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

---

## Step 3 — Upload index.html

1. In your new repo, click **Add file → Upload files**
2. Drag in the `index.html` file from this folder
3. Scroll down, click **Commit changes**

---

## Step 4 — Turn on GitHub Pages

1. In your repo, click **Settings** (top tab)
2. In the left sidebar, click **Pages**
3. Under "Build and deployment" → **Source**, choose **Deploy from a branch**
4. Branch: select **main**, folder: **/ (root)** → click **Save**
5. Wait ~1 minute, refresh the page — you'll see a link like:

   ```
   https://yourusername.github.io/nyc-marathon/
   ```

That's your permanent, free, shareable link. Send it to friends and family.

---

## Adding a new donor (do this every time someone gives)

1. Open your Excel and find the new row (order, name, amount)
2. Go to your GitHub repo → click on `index.html` → click the **pencil icon** (Edit)
3. Find this section near the top of the `<script>` tag:

```js
const DONORS = [
  // { order: 1, name: "Sarah K.", amount: 100 },
  // { order: 2, name: "Mike T.", amount: 50 },
];
```

4. Add a new line for the new donor (uncomment the format, remove the `//`):

```js
const DONORS = [
  { order: 1, name: "Sarah K.", amount: 100 },
  { order: 2, name: "Mike T.", amount: 50 },
];
```

5. Scroll down, click **Commit changes**
6. Wait about 30-60 seconds — GitHub Pages auto-rebuilds your site
7. Refresh your link — the new donor's windows are lit

You can batch-add multiple donors at once too — just add multiple lines
before committing.

---

## Tips

- **Order doesn't change anything visually** — it's just there so the list
  matches your Excel rows. Feel free to skip the `order` field entirely if
  you don't want to bother:
  ```js
  { name: "Sarah K.", amount: 100 },
  ```
- **Editing directly in GitHub's web editor is totally fine** — you never
  need to install git or any software. Everything happens in the browser.
- **Want to edit from your phone?** GitHub's mobile web editor works for this
  too, or use the GitHub mobile app.
- **Make a mistake?** Every edit is saved as a "commit" — you can always see
  history and revert under the repo's "Commits" tab.

---

## Customizing

- **Your name/story**: search for "I'm running 26.2" in index.html and edit
- **Your Pledge.to link**: search for `pledge.to` and replace the URL
- **The fundraising goal**: find `const GOAL = 5000;` and change the number
- **Donation tiers** (how many windows per dollar amount): edit the
  `TIER_MAP` object

---

## Need help?

Bring any error or weird behavior back to Claude with a screenshot or
description — it's a quick fix.
