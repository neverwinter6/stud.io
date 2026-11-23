# stud.io

An AI study companion in one HTML file. Add a course, paste your material, and
get notes, a study plan and practice exams.

**Live:** https://studio-sooty-omega.vercel.app

**Run:** open `index.html` in a browser. No build, no dependencies.

- **Courses first** — name the course and set your study time, then add a book,
  a video transcript or an article; everything joins that course as sections.
- **AI is optional** — add a Gemini API key in Account settings for AI notes.
  Without a key, notes are built on-device from your text.
- **Everything stays local** — courses, notes and exam scores live in
  `localStorage`. The only network call is the optional Gemini request.

Deploy: `vercel deploy --prod` (static; only `index.html` is published).
