---
# Featured tags need to have the `list` layout.
layout: about

# The title of the tag's page.
title: Works

# The name of the tag, used in a post's front matter (e.g. tags: [<slug>]).
slug: Works

# (Optional) Write a short (~150 characters) description of this featured tag.
description: >
  My music, in sheet music, audio, visual, code, or purely conceptual forms. 
---

{% for works in site.workss %}
  <h2>{{ works.name }}</h2>
  <h3>{{ works.instrumentation - works.length }}</h3>
  <p>{{ works.content | markdownify }}</p>
{% endfor %}