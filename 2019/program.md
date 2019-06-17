---
layout: 2019/page
title: C◦mp◦se 2019 Program
permalink: /2019/program/
---

Register for C◦mp◦se :: Conference 2019 tickets at [Eventbrite](https://www.eventbrite.com/e/new-york-compose-2019-tickets-56751182314)

---

<!-- Thursday's schedule -->
## Monday, June 24, 2019

<table class="table table-bordered" style="background: #fff">
    <tr class="active"><th width="200">Time</th><th>Talk</th></tr>
    <tr><td>8:30am - 9:00am</td><td>Registration & Breakfast</td></tr>

{% assign sorted = (site.data.2019.speakers.speakers | sort: 'start_time') %}

{% for speaker in sorted %}
  {% if speaker.start_time <= '2019-06-24 18:00:00 -0500' %}
    <tr id="{{speaker.name}}">
      <td>{{ speaker.start_time | date: '%I:%M%P' }} - {{ speaker.end_time | date: '%I:%M%P' }}</td>
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
  {% endif %}
{% endfor %}
</table>


## Tuesday, June 25, 2019

{% assign sorted = (site.data.2019.speakers.speakers | sort: 'start_time') %}

<table class="table table-bordered" style="background: #fff">
    <tr class="active"><th width="200">Time</th><th>Talk</th></tr>
    <tr><td>8:30am - 9:00am</td><td>Registration & Breakfast</td></tr>

{% for speaker in sorted %}
  {% if speaker.start_time >= '2019-06-24 18:00:00 -0500' %}
    <tr id="{{speaker.name}}">
      <td>{{ speaker.start_time | date: '%I:%M%P' }} - {{ speaker.end_time | date: '%I:%M%P' }}</td>
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
 {% endif %}
{% endfor %}
</table>



---

Register for C◦mp◦se :: Conference 2019 tickets at [Eventbrite](https://www.eventbrite.com/e/new-york-compose-2019-tickets-56751182314)
