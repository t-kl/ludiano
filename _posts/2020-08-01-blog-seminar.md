---
layout: post
title:  "Seminar: Wie erstellst du einen Blog mit Jekyll auf GitHub"
date:   2020-08-01 15:12:20 +0200
categories: seminar blog jekyll github
---
# GitHub Account
Du brauchst ein Benutzerkonto bei [_GitHub_](https://github.com/).

## Sign Up
Falls du noch kein Benutzerkonto hast, wählst du einen _Username_, der noch frei ist.
Gib deine _Email_ Addresse ein und wähle ein _Password_.
Du bekommst dann eine Bestätigungsmail mit einem Link, um dein Benutzerkonto zu aktivieren.

## Sign In
Falls du bereits ein Benutzerkonto hast, meldest du dich dort an.

# Repository
Du erstellst ein neues Repository basierend auf einer Vorlage mit: [Import your project to GitHub](https://github.com/new/import)

Unter "Your old repository’s clone URL" gibst du `https://github.com/t-kl/jekyll-blog-template` ein.
Du kannst einen "Repository Name" dafür wählen.
Dieser Name wird dann in der _URL_ erscheinen.

## Privacy
Du musst dein _Repository_ auf "Public" belassen.
Andernfalls musst du dafür bezahlen.

# Struktur

Das neue Repository (sagen wir dem mal `blog`) sieht so aus:

```shell
blog
├── 404.html
├── Gemfile
├── Gemfile.lock
├── _config.yml
├── _posts
│   └── 2020-07-25-welcome-to-jekyll.markdown
├── about.md
└── index.md
```


