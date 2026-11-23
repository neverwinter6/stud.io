# stud.io

An AI study companion in a single HTML file. Turn a textbook chapter, a lecture
transcript or an article into structured notes, a study plan and practice exams.

**Live:** https://studio-sooty-omega.vercel.app

## Run it

No build step, no dependencies. Open `index.html` in a browser — or serve the
folder with anything, e.g. `npx serve .`.

## How it works

- **Courses first.** Starting a course asks for a title and your study budget
  (deadline, hours per day, days per week). Everything you add after that
  becomes sections of the same course.
- **Materials.** Paste book/PDF text, a YouTube transcript, or article text.
  Text is split into sections; notes are generated per section.
- **Notes, plan, exam, games** all read from the same course sections.
- **Data stays on the device.** Courses, notes, exams and study time live in
  `localStorage`. Nothing is sent anywhere except an optional Gemini call.
- **AI is optional.** Add a Gemini API key in Account settings to have notes
  written by AI. Without a key, notes are built on-device from your text.

Browsers cannot read a video's captions or another site's article across
origins, which is why the importers take pasted text (the URL is kept as the
source reference).

## Deploy

Static site, so Vercel serves it as-is:

```sh
vercel deploy --prod
```

Only `index.html` is published; `.vercelignore` keeps the rest of the working
folder out of deployments.
