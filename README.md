# 🎡 What Should I Eat or Bring to a Potluck?

A tiny spinning app for friends who never know what to bring, for those who cannot decide on what to eat, and even for those who want to try something new!
Press **SPIN** and three columns roll like a slot machine. You get:

1. a **cuisine** (like Japanese),
2. a **flavour** (like spicy and tangy),
3. a **time of day** (like lunch).

Then tap **Find recipes** to search Google for ideas, or **See photos** to see what it looks like.

It is one file. No installs, no accounts, no cost.

---

## What is in this folder?

| File | What it is |
|---|---|
| `index.html` | **The app.** This is the one you publish. |
| `index-countries-test.html` | An experiment: adds every country in the world to the cuisine column (199 choices). |
| `meal-wheel-rings.html` | The old round-wheel version. Kept as a backup. |
| `README.md` | This page. |

---

## How to use it

1. Open `index.html` (double-click it) or visit your website.
2. Press **SPIN**.
3. Wait a few seconds. The columns stop one after another, left to right.
4. Your three answers appear underneath as colored pills.
5. Tap **Find recipes** or **See photos**.

---

## How to change the choices

Open `index.html` in any text editor (Notepad works). Find the part that says `const REELS`.
You will see three lists of words in quotes, for example:

```
items:['Breakfast','Lunch','Dinner']
```

- **Add** a word: type a comma, then the word in quotes, like `'Midnight snack'`.
- **Remove** a word: delete it and its comma.
- Keep the quotes and commas exactly as they are.

Each list also has a `max` number, which is the most words it can hold.
If you go over it, the app will stop and tell you which list is too long.
Raise the `max` number if you need more room.

The `dur` number is how long that column spins, in milliseconds. 1000 means 1 second.

---

## How to check that it works

Open the app, then press **F12** to open the browser console. Type:

```
runTests()
```

You should see **PASS**. It pretends to spin 1,000 times and checks the right word always
lands in the middle.

Shortcut: add `?test` to the end of the web address and it runs by itself.

---

## How to put it online for free (GitHub Pages)

1. Go to **github.com** and click **+ → New repository**.
2. Name it `meal-wheel`, choose **Public**, and click **Create repository**.
3. Click **uploading an existing file**. Drag in `index.html` (and this `README.md`).
4. Click **Commit changes**.
5. Go to **Settings → Pages**. Under **Source** choose **Deploy from a branch**,
   then branch **main** and folder **/ (root)**, and click **Save**.
6. Wait 1 to 2 minutes. Your link is:
   `https://YOUR-USERNAME.github.io/meal-wheel/`

To update the app later, upload the new `index.html` the same way and commit.

> The file **must** be named `index.html` and sit at the top level of the repository.

---

## Good to know

- **Privacy:** the app collects nothing. It loads one font from Google Fonts, and the recipe
  buttons open Google in a new tab. Nothing else leaves your device.
- **Phones:** built phone-first. The spin button is big and full width.
- **Less motion:** if a phone is set to reduce motion, the spin is quick and gentle.
- **Dark mode:** the app follows the phone's light or dark setting.
- **No secrets:** never paste a password or API key into `index.html`. Anyone visiting the
  site can read the file.

---

## Idea for later

Right now the recipe buttons just search Google. A future version could use an AI service
to suggest a real dish name (like "spicy katsu curry"). That needs a small server to keep an
API key private, so it is a separate step.

---

## If something goes wrong

| Problem | Try this |
|---|---|
| Nothing happens when I press SPIN | Refresh the page and try again. |
| The page is blank on GitHub | Check the file is named `index.html` and the repository is **Public**. |
| My changes do not show up | Wait a minute and do a hard refresh (Ctrl + Shift + R). |
| "exceeds max" error | A list has too many words. Remove some or raise its `max`. |
