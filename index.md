---
layout: home
title: Tested Configurations
---
iSpyConnect [maintains a large database](https://www.ispyconnect.com/sources.aspx) of camera manufacturers, supported methods (MJPEG, FFMPEG, RTSP), and the necessary URLs for accessing video, audio, and stills.

If you don’t know, or can’t find this information, start with this website.

Despite what some older posts and comments you come across may mention, it is strongly recommended that you do not use the `-re` setting in your source, as it is known to cause problems with live sources.
{% assign collection = site.configs | sort_natural:"title" %}
{% for config in collection %}
 - [{{ config.title }}]({{ site.baseurl }}{{ config.url }}){% if config.comment %}: {{ config.comment }}{% endif %}
{% endfor %}
