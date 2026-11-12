---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

You can also find my articles on <u><a href="https://scholar.google.com/citations?user=CJBGkTwAAAAJ&hl=en">my Google Scholar profile</a></u> (560+ citations, h-index 12).

{% include base_path %}

Published work:

(* These authors have equal contributions.)

{% for pub in site.data.publications %}
* {{ pub.citation }}{% if pub.link %} [Link]({{ pub.link }}){% endif %}{% if pub.pdf %}, [Paper]({{ pub.pdf }}){% endif %}
{% endfor %}

<!-- * Sorting System Based on RFID Positioning Technology. 2019SR1151524. *Software Copyright filed Nov. 2019.* 

* Grab-type flexible sorting method based on RFID spatial positioning technology. CN 201910875139.3. *Patent filed Sep. 2019.*  -->


<!-- {% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %} -->
