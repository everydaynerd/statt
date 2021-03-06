---
title: Project Scaffold
published: 2016-10-25
parentDir: blog
collection: posts
layout: post.html
starter:
  templates:
    - page
    - post
    - blank
  partials:
    - head
    - nav
    - header
    - footer
    - scripts
    - errors
---

## To get your new site started, there are some basic layouts, partials, pages, and posts already set up for you.

Default settings can be edited in `site.json`

```json
{
  "siteName":        "{{siteName}}",
  "siteTitle":       "{{siteTitle}}",
  "siteDescription": "{{siteDescription}}",
  "assetsDir":       "{{assetsDir}}",
  "buildDir":        "{{buildDir}}",
  "contentDir":      "{{contentDir}}",
  "layoutsDir":      "{{layoutsDir}}",
  "partialsDir":     "{{partialsDir}}",
  "defaultLayout":   "{{defaultLayout}}",
  "templateEngine":  "{{templateEngine}}"
}
```

And referenced in your site or like `\{{siteName}}` or `\{{siteTitle}}`

**There are {{starter.templates.length}} templates:**
<ul>
  {{#each starter.templates}}
    <li>`{{this}}` — `layouts/{{this}}.html`</li>
  {{/each}}
</ul>

**And {{starter.partials.length}} partials:**
<ul>
  {{#each partials}}
    <li>`{{@key}}` — `layouts/partials/{{@key}}.html`</li>
  {{/each}}
</ul>

**Which are used to make these {{add pages.length 1}} pages:**
<ul>
  <li>`index` — `content/index.html`</li>
  {{#each pages}}
    <li>`{{path}}` — `content/{{path}}.html`</li>
  {{/each}}
</ul>

**And these {{posts.length}} example posts:**
<ul>
  {{#each posts}}
    <li>`{{title}}` — `content/posts/{{slugify title}}.md`</li>
  {{/each}}
</ul>
