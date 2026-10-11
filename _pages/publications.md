---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

Published work:

(* These authors have equal contributions.)

{% for pub in site.data.publications %}
* {{ pub.citation }} [Link]({{ pub.link }}), [Paper]({{ pub.pdf }})
{% endfor %}

<!-- * Sorting System Based on RFID Positioning Technology. 2019SR1151524. *Software Copyright filed Nov. 2019.* 

* Grab-type flexible sorting method based on RFID spatial positioning technology. CN 201910875139.3. *Patent filed Sep. 2019.*  -->


<!-- {% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %} -->
