---
layout: 2017/page
title: C◦mp◦se 2017 Program
permalink: /2017/program/
---

Register for C◦mp◦se :: Conference 2017 tickets at [composeconference.eventbrite.com](http://composeconference.eventbrite.com)

---

## Accepted Talks

<table class="table table-bordered" style="background: #fff">
    <tr class="active"><th>Talk</th></tr>
    <tr><td>
        <p class="lead">
          <b>KEYNOTE: Title TBA</b> <br/>
            <small>
             Dr. Emily Riehl
            </small>
        </p>
</td></tr>

{% assign sorted = (site.data.2017.speakers.speakers | sort: 'name') %}

{% for speaker in sorted %}

    <tr id="{{speaker.name}}">
      <td>
        <p class="lead">
          <b>{{ speaker.title }}</b> <br/>
            <small>
                {{ speaker.name }}
            </small>
        </p>
        <blockquote class="abstract">
            {{ speaker.abstract | markdownify }}
        </blockquote>
      </td>
    </tr>
{% endfor %}
</table>



---

Register for C◦mp◦se :: Conference 2017 tickets at [composeconference.eventbrite.com](http://composeconference.eventbrite.com)
