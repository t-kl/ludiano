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

Unter "Your old repository’s clone URL" gibst du `https://github.com/t-kl/jekyll-blog-template` ein.
Du kannst einen "Repository Name" dafür wählen.
Dieser Name wird dann in der _URL_ erscheinen.

## Privacy
Du musst dein _Repository_ auf "Public" belassen.
Andernfalls musst du dafür bezahlen.

# Struktur

Das neue _Repository_ (sagen wir dem mal `blog`) sieht so aus:

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

## Fehlermeldung

Die Seite `404.html` wird benutzt, um eine Fehlermeldung anzuzeigen, falls etwas nicht gefunden wird.
Normalerweise musst du daran nichts ändern.

## Jekyll Konfiguration

Die Files `Gemfile` und `Gemfile.lock` werden zur Konfiguration von _Jekyll_ benötigt.
Normalerweise musst du daran nichts ändern.

## Settings

Im File `_config.yml` können gewisse Attribute deines Blogs definiert werden.
Unter anderem können hier weitere _Plugins_ aufgelistet werden.

## Posts

Deine Blog-Posts werden im Verzeichnis `_posts` erfasst.
Die Namen der Files müssen folgendem Schema genügen: `YYYY-MM-DD-<titel-des-eintrags>.md`

## Pages

Du kannst neben Blog-Posts auch ganz konventionelle Seiten wie `about.md` erstellen.

## Home

Die Start-Seite befindet sich in `index.md`.

# Anpassungen

Im File `_config.yml` muss allenfalls die `baseurl` angepasst werden:

```yaml
baseurl: "/blog" # the subpath of your site, e.g. /blog
```

Dies muss mit dem "Repository Name" übereinstimmen.
Auch andere Einträge wie `title`, `email` oder `description` können hier angepasst werden.
Das kann aber auch später noch gemacht werden.

# GitHub Pages

Unter **Settings** kann nun bei **GitHub Pages** dein Blog aktiviert werden.
Wähle dazu den `master` Branch und das Verzeichnis `/ (root)` aus.
Nach kurzer Zeit sollte dein Blog unter `https://<username>.github.io/<repository>/` publiziert sein.

# Der Erste Pfosten

## Neues File

Navigiere zu `_posts` und erstelle eine neue Seite mit: [Add file ▼] [Create new file]
Der Name des Files muss folgendem Schema genügen: `YYYY-MM-DD-<titel-des-eintrags>.md`

## Präambel

Am Anfang von jeder Seite befindet sich jeweils eine kleine Sektion mit Meta-Information für _Jekyll_:

```yaml
---
layout: post
title:  "<Titel des Pfosten>"
date:   <Datum> <Zeit> +0200
categories: <Liste von Kategorien> 
---
```

## Inhalt

Den eigentlichen Inhalt kannst du mit [Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) strukturieren.

## Ansicht

Du kannst dir mit [Preview changes] eine Ansicht anzeigen lassen.
Gewisse Dinge wie Links auf Fotos funktionieren allerdings nicht.

## Ab die Post

Ganz unten kannst du dann mit [Commit changes] deinen neuen Pfosten publizieren.
Es dauert jedoch eine kurze Zeit, bis _GitHub_ deinen Text von _Markdown_ mit _Jekyll_ in statisches _HTML_ übersetzt hat.
Erst dann kann sie korrekt dargestellt werden.

# Bilder

## Upload

Es können mit [Add file ▼] [Upload files] auch Bilder hochgeladen werden.
Allerdings gibt es im Web-Interface von _GitHub_ gewisse Beschränkungen.
So kann kein Verzeichnis deklariert werden.
Ausserdem scheint es nicht möglich zu sein, die Namen der Bilder zu verändern.

## Links

Bei Links auf Bilder oder andere Seiten des eigenen _Repository_ muss die `baseurl` im Link benutzt werden:

```markdown
![Feuerwerk]({{ site.baseurl }}/fireworks.jpg)
```

Andernfalls werden die Links von _Jekyll_ nicht korrekt generiert.
