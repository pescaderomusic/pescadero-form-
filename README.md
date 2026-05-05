# Pescadero Music — Custom Form UI

## Folder Structure
```
pescadero-form/
├── index.html        ← The custom form UI
├── images/           ← Drop your PNG assets here
│   ├── logo.png      ← Your logo (referenced in header)
│   └── ...           ← Any other images you add
└── README.md
```

---

## Step 1: Wire the Google Form Entry IDs

The form currently uses placeholder names like `entry.FIRST_NAME`. You need to replace these with the real `entry.XXXXXXXXX` IDs from your Google Form.

### How to get your entry IDs:
1. Open your Google Form in Chrome
2. Right-click the page → **Inspect**
3. In the Elements panel, press `Ctrl+F` / `Cmd+F` and search for `entry.`
4. Each question's input will have `name="entry.XXXXXXXXX"`

### Where to replace in index.html:
Search for `entry.FIRST_NAME`, `entry.EMAIL`, etc. and swap each placeholder with the real ID.

The fields and their placeholder names are:

| Field                     | Placeholder to replace        |
|---------------------------|-------------------------------|
| First Name                | `entry.FIRST_NAME`            |
| Last Name                 | `entry.LAST_NAME`             |
| Email                     | `entry.EMAIL`                 |
| Phone                     | `entry.PHONE`                 |
| Organization              | `entry.ORGANIZATION`          |
| Event Name                | `entry.EVENT_NAME`            |
| Event Date                | `entry.EVENT_DATE`            |
| Event Time                | `entry.EVENT_TIME`            |
| Venue Name                | `entry.VENUE`                 |
| Venue Address             | `entry.VENUE_ADDRESS`         |
| Attendance                | `entry.ATTENDANCE`            |
| Event Type                | `entry.EVENT_TYPE`            |
| Event Details             | `entry.EVENT_DETAILS`         |
| # of Performers           | `entry.PERFORMERS`            |
| Stage Setup               | `entry.STAGE_SETUP`           |
| Indoor/Outdoor            | `entry.INDOOR_OUTDOOR`        |
| Has Existing Gear         | `entry.HAS_EXISTING_GEAR`     |
| Existing Gear Description | `entry.EXISTING_GEAR`         |
| Budget                    | `entry.BUDGET`                |
| Additional Questions      | `entry.ADDITIONAL_QUESTIONS`  |

> Each placeholder appears **twice** in index.html — once on the visible input, once on the hidden input in the submit form. Replace both.

---

## Step 2: Add Your Images

Drop PNG files into the `images/` folder. They are already referenced by filename:

- `images/logo.png` — your logo shown in the header circle

To add more images, reference them in index.html as:
```html
<img src="images/your-file.png" alt="description" />
```

---

## Step 3: Adjust Form Questions

The form is built from reasonable assumptions about your inquiry flow. If your actual Google Form has different questions, sections, or answer options, update the HTML to match exactly — then map the correct entry IDs.

---

## Step 4: Host It

This is a plain HTML file — no build step needed. You can host it on:
- **Netlify Drop** (drag and drop the folder) — free
- **GitHub Pages** — free
- **Your own web host / cPanel**
- **Google Sites** (embed via iframe)

---

## Color Reference
| Name          | Hex       |
|---------------|-----------|
| Navy          | `#0D1B2A` |
| Cream         | `#F5EFE0` |
| Candy Red     | `#D62828` |
| Robin Egg Blue| `#44BEC7` |
