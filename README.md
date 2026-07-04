# Summer Open And Reproducible Research (SOAR²)

Website source code for the Summer Open And Reproducible Research (SOAR²) Camp, taking place at UC Santa Barbara from September 21–23, 2026.
 
SOAR² is a three-day program for undergraduate students that aims to demystify the hidden curriculum of research and introduce open and reproducible practices as fundamental to conducting research. During these three days, students will participate in interactive modules, hands-on activities, field trips to campus research facilities, and your keynote talk. Students will learn about reproducible workflows, data management, research transparency, and open sharing. SOAR² is organized by the [UCSB Library](https://www.library.ucsb.edu/) in collaboration with [the Office of Undergraduate Research & Creative Activities (URCA)](https://urca.ucsb.edu/), with funding support from [the Open Research Community Accelerator](https://www.orcaopen.org/).

This repository contains the Jekyll site used to publish program information, session materials, instructor profiles, and other related content for SOAR².

<br/>

## Acknowledgement and Citation
This repo was originally cloned from [druckmann-lab/math-tools](https://github.com/druckmann-lab/math-tools), which was derived from [kazemnejad/jekyll-course-website-template](https://github.com/kazemnejad/jekyll-course-website-template), itself based on [svmiller/course-website](https://github.com/svmiller/course-website). Full citations to these repositories are included below

* Druckmann Lab. *Course website for Introduction to Mathematical Tools in Neuroscience (NEPR 209).* GitHub, 2026. https://github.com/druckmann-lab/math-tools
* Kazemnejad, A. *Jekyll Course Website Template.* GitHub, 2020. https://github.com/kazemnejad/jekyll-course-website-template
* Miller, S and Chhatre, V. *Steve's No-Good-Very-Bad Course Website Jekyll Template.* GitHub, 2019. https://github.com/svmiller/course-website

<br/>

## How to maintain this website (for RDS folks)?

This site is built with Jekyll. Most updates can be made by editing Markdown, YAML, images, and other static files without changing the underlying layouts.

### Repository structure

#### Pages and subpages

* `index.md`: homepage content
* `instructors.md`: instructor landing page
* `subpages_sessions/`: Sessions landing page and individual session pages
* [hidden from nav] `subpages_resources/`: Resources landing page and subpages for research programs, grants & awards, etc, currently hidden
* [hidden from nav] `about.md`: reserved About page, currently hidden
* [hidden from nav] `schedule.md`: schedule page, currently hidden
* [not in use] `assignments.md`: legacy assignments page, currently hidden


#### Content collections

* `_announcements/`: homepage announcements
* `_instructors/`: instructor profiles
* `_lectures/`: module metadata used to generate the session cards
* `_events/`: scheduled events such as research-facility visits and the keynote
* [not in use] `_assignments/`: assignment content

#### Site configuration and navigation

- `_config.yml`: site title, dates, URLs, collections, and other site-wide settings
- `_data/nav.yml`: navigation items and submenus
- `_data/entity.yml`: organizer and funder information
- `_layouts/`: page templates
- `_includes/`: reusable page components
- `_css/` and `_sass/`: site styling

#### Images, materials, and archives

- `_images/`: logos, instructor photos, module icons, and other site images
- `session_materials/`: slides, datasets, PDFs, and other downloadable session files
- `website_snapshots/`: archived PDF and PNG captures from earlier stages of the website


### Common update workflow

| Goal | Task |
|------|------|
| Change the program name, dates, publishing URL or other site-wide settings | Edit `_config.yml` |
| Show, hide, reorder, or rename nav items | Edit `_data/nav.yml` |
| Revise homepage content | Edit `index.md` |
| Publish a homepage annoucement to the Update box | Add or edit a file in `_announcements/` |
| Add or revise an instructor profile | Create or edit a file in `_instructors/` |
| Update the content for a session (e.g., slides, handouts) | Edit the corresponding files in `subpages_sessions/` |
| Add downloadable session files | Save the files in `session_materials/` and update the relevant page links |
| Update opportunities or resources for students | Edit files in `subpages_resources/` |


### Project-specific notes

* Some pages are intentionally omitted from `_data/nav.yml` until they are ready to be publicly promoted. Removing a page from navigation does not necessarily make its URL inaccessible.
* The reader-facing section is called **Sessions**, but it still uses the `lectures` collection and related layouts internally.
* Module summaries are stored in `_lectures/`, while the expanded module pages are stored in `subpages_sessions/`. Changes to a module description may therefore need to be made in both places.
* The `_assignments/` collection and assignments page are inherited from the original course template and are not currently used.
* Homepage organizer and funder information is driven by `_data/entity.yml` and `_layouts/home.html`.
* If the repo name or publishing location changes, update both `url` and `baseurl` in `_config.yml`. This applies when working with Forks and Pull Requests.

<br/>


## How to reuse this repo and deploy on GitHub Pages?
1. Fork or clone this repository.
2. Open `_config.yml`.
   1. Update `url` field according to your GitHub account (e.g., `https://<your-github-username>.github.io/`).
   2. Update `baseurl` field according to your repository's name (e.g., `/soar2`).
   3. Commit and push your changes.
3. Go to your repository's settings (`https://github.com/<your-github-username>/<your-repo-name>/settings`).
4. On GitHub Pages section, choose source to be your master branch, and enable Github Pages.
5. You are now ready to go! Start customizing your website.

For more information and tips about how to manage, update, and deploy this repository, see README of [kazemnejad/jekyll-course-website-template](https://github.com/kazemnejad/jekyll-course-website-template)


<br/>

## Gen AI usage

Generative AI (Codex, GPT-5.5, Medium Intelligence) was used to draft this README.md file and troubleshoot code. Content of this README.md file has been reviewed and edited to ensure accuracy.
