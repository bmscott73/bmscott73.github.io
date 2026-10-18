---
layout: single
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% assign cv = site.data.navigation.main | where: "title", "CV" | first %}
<a href="{{ cv.url | relative_url }}" download="{{ cv.download | escape }}">Download my current resume (Word document)</a>.
