# Editing Your Blog — A Friendly Guide 🧪

Hi! This is a short guide to running your website. It's built on a template
called **al-folio**, but you don't need to know anything about that. This site
has been trimmed down to just what you need. Right now the menu at the top has
**four** things:

| Menu item       | What it is                                         | The file you edit             |
| --------------- | -------------------------------------------------- | ----------------------------- |
| **(your name)** | The home / **about** page (top-left, links to `/`) | `_pages/about.md`             |
| **blog**        | The list of all your posts                         | files in the `_posts/` folder |
| **CV**          | Your CV / résumé page                              | `_data/cv.yml`                |
| **submenus**    | A little **drop-down menu** (see the last section) | `_pages/dropdown.md`          |

Everything else that came with the template (publications, projects, teaching,
etc.) has just been **hidden from the menu** — the files are still there, but no
one sees them. You can ignore them.

> 💡 **Golden rule:** the parts between the two `---` lines at the very top of a
> file are _settings_ (called "front matter"). Change the words after the `:`,
> but keep the layout of colons and dashes the same. Everything **below** the
> second `---` is your actual writing.

---

## 0. First: make it yours (name, tagline, photo)

**Your name and site title** live in `_config.yml` (near the top):

```yaml
title: Blog
first_name: Augustine
middle_name:
last_name: Louvrier
```

Change these to your name. `title` is what shows in the browser tab.

**Your profile photo:** save your picture as `prof_pic.jpg` and drop it into the
`assets/img/` folder (replacing the one that's there). Keep the name exactly
`prof_pic.jpg` and it will appear automatically on the about page.

**Your social links** (Instagram, email, etc.) live in `_data/socials.yml`.
Fill in your usernames next to the ones you want, and delete or leave blank the
ones you don't.

---

## 1. The **about** page (your homepage)

Open **`_pages/about.md`**.

**The settings at the top** control the layout:

```yaml
subtitle: Chemistry student at Imperial College London # the line under your name
profile:
  align: right
  image: prof_pic.jpg # your photo (see section 0)
  image_circular: false # true = round photo, false = square
  more_info: >
    <p>Department of Chemistry</p>
    <p>Imperial College London</p>
social: true # true = show your social icons at the bottom
```

- Change `subtitle` to describe yourself (e.g. _"Chemistry undergrad who likes
  reactions that change colour"_).
- Edit the `more_info` lines to whatever you want under your photo, or delete
  them.

**Your actual bio** is everything _below_ the second `---`. Just delete the
placeholder text and write about yourself in plain English. You can use links
like this: `[the RSC](https://www.rsc.org)`.

There are two extra boxes on the homepage you can leave on or turn off:

```yaml
announcements:
  enabled: true # a "news" feed — set to false to hide it
latest_posts:
  enabled: true # shows your 3 newest blog posts — nice to keep on!
```

---

## 2. The **blog** — writing posts

This is the main event. **Each post is one file** in the **`_posts/`** folder.

### Step 1 — Name the file correctly

The filename **must** follow this pattern:

```
YEAR-MONTH-DAY-a-short-title-with-dashes.md
```

For example: `2026-07-05-why-flames-are-different-colours.md`

- Use dashes, not spaces.
- The date at the front is what sorts your posts.

### Step 2 — Copy this template into the new file

```markdown
---
layout: post
title: Why flames are different colours
date: 2026-07-05 10:00:00
description: A quick look at flame tests and why they're so pretty
tags: flame-tests inorganic fun
categories: chemistry
---

Start writing here! This is normal text.

## You can add headings like this

You can make words **bold** or _italic_, and add
[links](https://www.rsc.org) like that.

- bullet points
- work too

> And you can quote things like this.
```

- `title` — what shows up as the post's headline.
- `date` — should match the date in the filename.
- `description` — a one-line summary (shows in the blog list).
- `tags` / `categories` — words to group posts. Separate several with spaces.

### Step 3 — Adding a picture to a post

Put the image in `assets/img/`, then in your post write:

```markdown
![A blue flame](/blog/assets/img/your-image.jpg)
```

(The `/blog/` at the start is important — it's the site's address.)

### Where to find examples

The `_posts/` folder is **full of example posts** that came with the template.
They double as a cheat-sheet — e.g. open `2015-03-15-formatting-and-links.md` to
see formatting tricks, or `2015-05-15-images.md` for images. Once you're
comfortable, you can delete the example posts you don't want.

---

## 3. The **CV** page

Your CV is **not** written as normal text — it's filled in as a neat list in
**`_data/cv.yml`**. This keeps it looking tidy automatically.

Open `_data/cv.yml` and replace the placeholder (Albert Einstein!) details:

```yaml
cv:
  name: Augustine Louvrier
  label: Chemistry Student
  email: you@example.com
  location: London, UK
  summary: Undergraduate chemist interested in ...

  sections:
    Education:
      - institution: Imperial College London
        location: London, UK
        area: Chemistry
        studyType: MSci
        start_date: 2024
        end_date: 2028
        highlights:
          - Relevant module or achievement
          - Another one
```

**How to read the indentation:** the spaces at the start of each line matter a
lot in this file. The easiest way to add a new entry is to **copy an existing
block** (from one `- institution:` down to its last `highlights` line) and edit
the copy. Keep the dashes and spacing lined up exactly like the ones already
there.

You can add other sections too (Experience, Skills, Awards…) — just follow the
same pattern as the sections already in the file.

**The "Download CV" (PDF) button:** the page has a button to download a PDF. To
use your own, save your CV PDF into `assets/pdf/` and update this line at the
top of `_pages/cv.md`:

```yaml
cv_pdf: /assets/pdf/your-cv.pdf
```

If you don't want that button at all, just delete that line.

---

## 4. The **submenus** drop-down (the "idk what it does" one)

The **submenus** item in the menu is a **drop-down** — when you hover/click it, a
little list of extra links appears. It's handy for grouping things you don't
want cluttering the main menu.

It's controlled by **`_pages/dropdown.md`**:

```yaml
title: submenus # the word shown in the menu bar
dropdown: true
children:
  - title: bookshelf # a link inside the drop-down
    permalink: /books/
  - title: divider # draws a thin separating line
  - title: blog
    permalink: /blog/
```

- Change `title:` at the top to rename the menu button (e.g. `more`).
- Each `- title:` / `permalink:` pair is one link in the drop-down.
- `- title: divider` just draws a dividing line — no link.

**Ideas for you:** you could point it at a "bookshelf" of chemistry books you've
enjoyed (that page already exists — edit `_books/` and `_pages/books.md`), or a
page of favourite resources. If you don't want a drop-down at all, open
`_pages/dropdown.md` and change `nav: true` to `nav: false` to hide it.

---

## 5. Seeing your changes & publishing

- **To preview locally** (on your own laptop), a developer can run
  `bundle exec jekyll serve` and open the address it prints. There's more detail
  in `README.md` and `CLAUDE.md` if someone technical is helping you set that up.
- **To publish:** save your files, then commit and push them with git. The site
  rebuilds itself online automatically after you push.

If in doubt: **you can't really break anything permanently.** Every change is
saved in git history, so a wrong edit can always be undone. Experiment freely 🙂

Happy blogging! 🧪✨
