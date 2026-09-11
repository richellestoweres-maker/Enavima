# Changing the words on the site

No software to install, nothing to break permanently. Everything happens in the browser,
and GitHub keeps every previous version, so any change can be undone.

---

## The 60-second version

1. Click the file you want to change (e.g. `parents.html`).
2. Click the **pencil icon** at the top right of the file.
3. Find the sentence you want to change and type over it.
4. Scroll down, write one line about what you changed, click **Commit changes**.

That's it. The live site updates itself within a minute or two.

---

## Which file is which page

| If you want to change… | Edit this file |
|---|---|
| The front page | `index.html` |
| The explainer about congenital CMV | `congenital-cmv.html` |
| The page for parents | `parents.html` |
| The page for clinicians | `clinicians.html` |
| The page for hospitals and labs | `labs.html` |
| The page about the test itself | `test.html` |
| The team, collaborators and contact details | `about.html` |

Some things appear on **every** page: the menu at the top, and the whole footer including the
address, phone number and the regulatory statement. Those have to be changed in all seven files.
Use **Ctrl+F** (or **Cmd+F**) in the editor to find the text, and repeat for each file.

---

## Reading the file without getting lost

The top third of each file is a long block of style rules. **Ignore all of it.** The actual
page content starts after a line that reads:

```
<main>
```

Everything a visitor reads lives between `<main>` and `</main>`.

Text sits between angle-bracket tags. To change a sentence, change only the words, and leave the
tags alone:

```html
<h2>The newborn hearing screen is not a CMV test.</h2>
     ↑ change these words          ↑ but not this
```

```html
<p>Hearing loss is the most common long-term effect.</p>
```

---

## Four rules that keep it from breaking

**1. Never delete a tag.** If you delete `</p>` the rest of the page can collapse. Change the
words between the tags, not the tags themselves.

**2. Tags come in pairs.** `<p>` opens, `</p>` closes. `<strong>` opens, `</strong>` closes.
Whatever you do to one, do to the other.

**3. Some characters have to be written the long way.**

| You want | Type this |
|---|---|
| an apostrophe, as in *baby's* | `&rsquo;` |
| an ampersand | `&amp;` |
| ~ (approximately) | `~` is fine as-is |

The site does not use dashes as punctuation anywhere. Use a comma, a period, or the
words "such as" instead.

A plain `'` will usually work too; `&rsquo;` just looks better.

**4. Don't touch anything inside `<style>` or `<script>`.** That's the layout and the menu.
The same goes for anything starting with `<img`, which is how the logo is placed.

---

## Common edits

**Change the phone number or address.** Search for `409-935-6700` or `903 Texas Avenue`.
Both appear in the footer of all seven files, and again on `about.html`.

**Change the regulatory statement.** Search for `have not been cleared or approved`.
It appears in the footer of all seven files, and once more in the middle of `test.html`.
This is the one edit most worth getting exactly right.

**Add a team member.** Open `about.html`, search for `Dr. Maryam Hussain`, and copy the whole
block from `<div class="card">` down to the matching `</div>`. Paste it directly underneath and
change the name, title and description.

**Update the state screening counts.** Search for `Universal screening` in `index.html`.
The numbers and the state name lists are right there. `labs.html` also mentions
"Twenty-three states" in a drop-down answer near the bottom.

---

## Previewing before you publish

At the top of the editor there are two tabs: **Edit** and **Preview**.

GitHub's Preview tab will *not* show you the finished page, it shows the raw code. To see the
real page, make the change, commit it, and look at the live site a minute later. If it looks
wrong, use the undo instructions below.

---

## Undoing a change

Every version is kept forever.

1. Click **Commits** (or the clock icon) at the top of the file list.
2. Find the change you want to reverse.
3. Click the **…** menu on it and choose **Revert**.

Nothing is ever really lost, so it is safe to experiment.

---

## When to ask rather than edit

Editing the words is safe. These are worth asking about first, because they touch the layout:

- adding a whole new page
- changing colors, fonts or spacing
- adding photographs, or changing the logo
- adding a working contact form (the current ones just open an email program)
