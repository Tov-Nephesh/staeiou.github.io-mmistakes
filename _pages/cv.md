---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
---

{% include base_path %}
{% capture written_label %}'None'{% endcapture %}

[Also available in PDF format.](http://www.stuartgeiger.com/geiger-cv-apr2013.pdf)

# **R. Stuart Geiger**

**Curriculum Vitae**

stuart at  stuartgeiger.com | [http://www.stuartgeiger.com](http://www.stuartgeiger.com/) | [@staeiou](http://www.twitter.com/staeiou) | [Google Scholar](http://is.gd/geiger_cites)

## Education:

* **Ph.D., Information Management and Systems with a designated emphasis in New Media, University of California at Berkeley**
    * **Date:** December 2015
    * **Doctoral Thesis:** robots.txt: An Ethnographic Investigation of Automated Software Agents in User-Generated Content Platforms
    * **Advisor:** Prof. Jenna Burrell

* **M.A., Communication, Culture, and Technology**, **Georgetown University**
    * **Date:** May 2009
    * **Master’s Thesis**: Working within Wikipedia: Infrastructures of Knowing and Knowledge Production
    * **Advisor:** Prof. David Ribes

* **B.A., Humanities Honors, University of Texas at Austin**
    * **Date: **May 2007
    * **Senior Thesis**: Democracy in Wikipedia
    * **Advisor:** Prof. Elizabeth Keating

## Research Interests and Skills:

* **Topical:** collaboration, socialization, literacy, and governance in distributed, decentralized communities, specifically new/social media platforms and scientific research networks
* **Disciplinary:** social informatics, computer-supported cooperative work, human-computer interaction, science and technology studies, new media and communication studies
* **Theoretical:** socio-technical systems, communities of practice, ethnomethodology, symbolic interactionism, distributed cognition, actor-network theory, phenomenology
* **Methodological:**
    * Ethnography, including interviews, focus groups, and participant-observation
    * Archival analysis, including individual and group-based qualitative coding
    * Quantitative collection and analysis of log and trace data with R, SQL, and python
    * User interface evaluation, including experimental design, A/B testing, and analysis
    * Inductive, mixed-methodological approaches to answer complex socio-technical questions and problems using all of the above methods, as appropriate and relevant

## Publications

{% for collection in site.collections %}
  {% unless collection.output == false or collection.label == "posts" %}
    {% capture label %}{{ collection.label }}{% endcapture %}
    {% if label != written_label %}
      <h3 id="{{ label | slugify }}" class="archive__subtitle">{{ label }}</h3>
      {% capture written_label %}{{ label }}{% endcapture %}
    {% endif %}
  {% endunless %}
  {% for post in collection.docs %}
    {% unless collection.output == false or collection.label == "posts" %}
      {% include archive-single.html %}
    {% endunless %}
  {% endfor %}
{% endfor %}
