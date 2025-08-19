---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
cv_pdf: "/files/cv.pdf" # Set your PDF path here. If missing, page will redirect to 404
---

{% include base_path %}

{%- assign cv_path = page.cv_pdf | default: '/files/cv.pdf' -%}
{%- assign cv_file = site.static_files | where: 'path', cv_path | first -%}
{%- if cv_file -%}

<div class="cv-embed">
  <object data="{{ cv_path | relative_url }}" type="application/pdf" width="100%" height="1000">
    <iframe src="{{ cv_path | relative_url }}" width="100%" height="1000"></iframe>
  </object>
  <p><a href="{{ cv_path | relative_url }}" download>Download CV (PDF)</a></p>
  <hr />
</div>
{%- else -%}
<meta http-equiv="refresh" content="0; url={{ '/404.html' | relative_url }}">
{%- endif -%}

{% comment %}
Education
======

- Ph.D in Version Control Theory, GitHub University, 2018 (expected)
- M.S. in Jekyll, GitHub University, 2014
- B.S. in GitHub, GitHub University, 2012

# Work experience

- Spring 2024: Academic Pages Collaborator

  - GitHub University
  - Duties includes: Updates and improvements to template
  - Supervisor: The Users

- Fall 2015: Research Assistant

  - GitHub University
  - Duties included: Merging pull requests
  - Supervisor: Professor Hub

- Summer 2015: Research Assistant
  - GitHub University
  - Duties included: Tagging issues
  - Supervisor: Professor Git

# Skills

- Skill 1
- Skill 2
  - Sub-skill 2.1
  - Sub-skill 2.2
  - Sub-skill 2.3
- Skill 3

# Publications

  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Currently signed in to 43 different slack teams
{% endcomment %}
