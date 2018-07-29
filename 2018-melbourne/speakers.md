---
layout: 2018-melbourne/melbourne
title: C◦mp◦se 2018 Speakers
permalink: /2018-melbourne/speakers/
---

Register for C◦mp◦se :: Conference 2018 tickets at [composeconference.eventbrite.com](http://composeconference.eventbrite.com)

---

{% for speaker in site.data.2018.speakers.speakers %}

  <hr>

  <div id="biowrap">
  <div class="container">
  <a id="{{ speaker.id }}"></a>
  <div class="row" style="padding-top:60px;">
      <div class="col-lg-8 col-md-8 col-sm-8 col-xs-8">
        <h2>{{ speaker.name }}</h2>
        <h3>{{ speaker.title }}</h3>
        <p>
          <img src="{{ speaker.img }}" align="right" style="padding: 0px 25px 25px 0px; max-height: 300px;"> 
          {{ speaker.abstract }}
          <h2>Bio</h2>
          {{ speaker.bio }}
        </p>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-4 col-xs-4">
      <h2>&nbsp;</h2>
      <!-- <h3><small>{{ speaker.start_time | date: '%h %-d, %I:%M%P'}}</small></h3> -->
      <p class="text-centered">
        {% if speaker.home %}
        <a href="{{speaker.home}}">
        <i class="fa fa-home"> {{ speaker.home }}</i>
        </a>
        {% endif %}
        {% if speaker.twitter %}
        <a href="http://twitter.com/{{ speaker.twitter }}">
        <i class="fa fa-twitter"> {{ speaker.twitter }}</i>
        </a>
        {% endif %}
        {% if speaker.github %}
        <a href="http://github.com/{{ speaker.github }}">
        <i class="fa fa-github"> {{ speaker.github }}</i>
        </a>
        {% endif %}
        {% if speaker.irc_handle %}
        IRC: {{ speaker.irc_handle }}</i>
        {% endif %}
      </p>
    </div>
  </div><!-- --/row ---->
  </div><!-- --/container ---->
  </div><!-- biowrap -->
{% endfor %}

---

<div class="container">
Register for C◦mp◦se :: Conference 2016 tickets at <a href="https://www.eventbrite.com.au/e/compose-melbourne-2018-tickets-46002911948">Eventbrite</a>
</div>
