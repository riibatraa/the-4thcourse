# The waitlist → Google Sheet

**Status: connected and verified.** Signups from 4thcourse.in land in the
"The 4thCourse — Waitlist" form's response sheet.

| | |
|---|---|
| Form id | `1FAIpQLSdu9SQK17bWBdipu70HMCAwAhcJ1xlZqltYjGEpVGfI39mJ5w` |
| Name | `entry.807980480` |
| Email | `entry.988966014` |
| WhatsApp number | `entry.940632605` |

These live in `index.html`, in the block commented `WAITLIST → GOOGLE SHEET`.

Two test rows were submitted during setup — **TEST — please delete** and
**BROWSERTEST — please delete**. Remove them from the sheet.

The instructions below are kept for reference, in case the form is ever
rebuilt or replaced.

---

## 1. Make the Google Form

1. Go to <https://forms.new>
2. Title it **the 4thCourse — waitlist**
3. Add **three** questions, all of type **Short answer**, in exactly this order:

   | # | Question title    |
   |---|-------------------|
   | 1 | First name        |
   | 2 | Email             |
   | 3 | WhatsApp number   |

   The titles can say anything you like — only the **order** matters.

4. Click **Responses** → the green **Sheets** icon → **Create new spreadsheet**.
   That is the spreadsheet you'll mail from later.

---

## 2. Get the form id

Click **Send** → the **link** tab (🔗) → copy the link. It looks like:

```
https://docs.google.com/forms/d/e/1FAIpQLSdXXXXXXXXXXXXXXXXXXXXXXXXXXXX/viewform
```

The form id is the long piece between `/e/` and `/viewform`:

```
1FAIpQLSdXXXXXXXXXXXXXXXXXXXXXXXXXXXX
```

---

## 3. Get the three entry ids

1. Open the form editor, click the **⋮** menu (top right) → **Get pre-filled link**
2. Type any junk into the three boxes — `a`, `b`, `c` will do
3. Click **Get link**, then **Copy link**
4. Paste it somewhere you can read it. It looks like:

```
...viewform?usp=pp_url&entry.1111111111=a&entry.2222222222=b&entry.3333333333=c
```

Those three `entry.NNNNNNNNNN` values, **in that order**, are your name, email
and phone ids.

---

## 4. Send me the four values

Paste them to me like this and I'll wire them in:

```
FORM_ID = 1FAIpQLSd...
name    = entry.1111111111
email   = entry.2222222222
phone   = entry.3333333333
```

Or edit them yourself — they live in `index.html`, in the block commented
`WAITLIST → GOOGLE SHEET` near the bottom of the file.

---

## Worth knowing

- **Keep the form accepting responses.** If you close it in Google Forms,
  signups fail silently on the site.
- **The browser can't confirm the save.** Google Forms doesn't allow the page
  to read its reply, so the site shows success once the request is sent. Post a
  test signup yourself after wiring it up and check the row lands in the sheet.
- **Don't reorder or delete the questions** later — that changes the entry ids
  and breaks the form. Adding new questions at the end is safe.
- **This collects personal data.** You're storing names, emails and phone
  numbers and telling people you'll message them. The footer's Privacy link
  currently goes nowhere; it should point at a real page before you drive any
  real traffic here.
