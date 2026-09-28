# Venkata Sai Ram Dasari

Source for my academic website: **https://7gb-ram.github.io**

Graduate researcher in Computer Science at Montclair State University, working on uncertainty quantification and AI for healthcare.

- Email: dasariv1@montclair.edu
- Google Scholar: https://scholar.google.com/citations?user=qNi--CgAAAAJ
- LinkedIn: https://www.linkedin.com/in/venkata-sai-ram-dasari/

## Editing the site

| What                     | Where                                     |
| ------------------------ | ----------------------------------------- |
| About, bio, hobbies      | `_pages/about.md`                         |
| Publications             | `_bibliography/papers.bib`                |
| Experience and education | `_pages/experience.md`                    |
| Projects                 | `_projects/*.md`                          |
| Announcements            | `_news/*.md`                              |
| Social links             | `_data/socials.yml`                       |
| Name, site settings      | `_config.yml`                             |
| Images                   | `assets/img/` (profile: `prof_pic.jpg`)   |

Pushing to `main` builds and deploys the site to the `gh-pages` branch through `.github/workflows/deploy.yml`.

Local preview: `docker compose up -d`, then open http://localhost:8080/.

Built with [Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) theme (MIT License).
