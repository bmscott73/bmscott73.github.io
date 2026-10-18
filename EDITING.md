# Editing your academic website

This site keeps the AcademicPages sidebar and the simple flow of Onat Gungor's website: a homepage followed by Publications, Mentoring, and a direct CV download.

## Start here

1. Replace every visible `[placeholder]` in `_pages/about.md` and `_pages/cv.md`. Confirm your M.S. completion status and add your PhD institution, department, and start date.
2. Edit `_config.yml`: `author.bio`, location, employer (university), email, and social profiles. Your existing photo and contact details are preserved. Blank profile fields are hidden. Restart Jekyll after configuration changes.
3. Add your headshot to `images/` and set its filename in `_data/profile.yml`. The current photo is `profile_photo.png`. Jekyll reloads this data file automatically; no server restart is needed for photo changes.
4. Add homepage news in reverse chronological order in `_pages/about.md`.
5. Update `_pages/mentoring.md` when you have mentoring experience to share.
6. Replace `files/cv/resume.docx` with your latest resume, keeping that exact filename. The CV tab downloads it directly.

Teaching and course pages are unpublished (`published: false`) and are no longer linked from the menu or CV. Their source files are retained for your records.

Edit the final paragraph of `_pages/about.md` to update your hobbies and interests. The former Miscellaneous page is unpublished.

## Add publications

Edit `_data/publications.yml`. Each entry has `title`, `authors`, `venue`, `year`, and `status` (`accepted` or `under_review`). Add an optional `paperurl` when a public paper link is available. The Publications page groups these entries by status automatically. Update the status when a decision arrives.

The old `_publications/` demo collection remains excluded; do not enable those fictional entries.

## Navigation and unused examples

Edit `_data/navigation.yml` to change menu links. Clicking your name returns home. Starter blog posts, talks, portfolio items, and tutorial pages remain in the source but are excluded from the build. Replace their demo content before enabling them. Do not edit `_site/`; it is generated.

## Preview

With Ruby and the repository's Bundler version installed:

```sh
bundle install
bundle exec jekyll serve
```

Open http://localhost:4000. To check a production build, use `bundle exec jekyll build`. Review all placeholders before committing and pushing to the branch configured for GitHub Pages. These source edits do not publish the site themselves.

## Updating the downloadable resume

The current resume is stored at `files/cv/resume.docx`. To update it, copy your new Word resume into that location and name it `resume.docx`, replacing the previous file. No template or link changes are needed. Jekyll copies the updated file on rebuild; commit and push the replacement to update GitHub Pages.

The browser downloads it as `Benjamin-Scott-Resume.docx`. To switch to PDF later, add `files/cv/resume.pdf` and update the CV entry's `url` and `download` fields in `_data/navigation.yml` (use a `.pdf` download filename). Update the format label in `_pages/cv.md` too. Keep private drafts and old versions outside `files/`, since files there are publicly served when deployed.
