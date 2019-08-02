---
layout: 2019-melbourne/melbourne
title: Melbourne C◦mp◦se 2019 Speakers
permalink: /2019-melbourne/speakers/
---

<style type="text/css">
  .container img {
    max-height: 300px;
  }
  .no-top-space {
    margin-top: 0;
  }
  .agenda td {
    vertical-align: top;
  }
  .agenda td h2 {
    margin: 0 0;
  }
  .agenda .heading td {
    padding-top: 30px;
    padding-bottom: 20px;
  }
  .key td {
    vertical-align: top;
    padding-width: 5px;
  }
  tr .break {
    background-color: #eee;
    text-align: center;
  }
</style>

<div class="sep talk melbourne" data-stellar-background-ratio="0.5" style="background-position: 50% -91.5px;"></div>

<br />

<div class="container">
  <div class="row">
    <div class="col-lg-10 col-lg-offset-1">
        <h1 class="text-center">Programme</h1>
        {% if site.data.2019-melbourne.speakers.show-level %}
        <div class="keybox">
          <table class="key agenda">
            <tr><td>&#x1f535;&nbsp;</td> <td>Little assumed knowledge </td></tr>
            <tr><td>&#x1f535;&#x1f535;&nbsp;</td> <td>Moderate assumed knowledge</td> </tr>
            <tr><td>&#x1f535;&#x1f535;&#x1f535;&nbsp;</td> <td>Significant assumed knowledge </td></tr>
          </table>
        </div>
        {% endif %}
        <br/>
        <table class="agenda">
          {% for t in site.data.2019-melbourne.speakers.times %}
            {% unless t.hide or t.hide_toc %}
            {% if t.heading %}
              <tr class="heading">
                <td colspan="3">
                  <h2><a href="#{{t.id}}">{{ t.time }} - {{ t.heading }}</a></h2>
                  {{ t.blurb }}
                  <i class="fa fa-map-marker fa fa-fw"></i>{{ t.location }}
                </td>
              </tr>
            {% else %}
              <tr class="time">
                <td>{{t.time}}</td>
                <td>{{t.name}}{% if t.name2 %}, {{t.name2}} {% endif %}</td>
                <td>
                  <a href="#{{t.id}}">{{t.title}}</a>
                  {% if t.video %}<a href="{{ t.video }}">(Video)</a>{% endif %}
                  {% if t.slides %}<a href="{{ t.slides }}">(Slides)</a>{% endif %}
                </td>
                {% if site.data.2019-melbourne.speakers.show-level %}
                 <td>
                   <nobr>
                   {% if t.level >= 1 %} &#x1f535; {% endif %}
                   {% if t.level >= 2 %} &#x1f535; {% endif %}
                   {% if t.level >= 3 %} &#x1f535; {% endif %}
                   </nobr>
                 </td>
                {% endif %}
              </tr>
            {% endif %}
            {% endunless %}
          {% endfor %}
        </table>
      </div>
  </div>


{% for t in site.data.2019-melbourne.speakers.times %}
{% if t.heading %}
----
<div class="container cfpsection" id="{{t.id}}" class="no-top-heading" style="padding-top: 60px;">
  <div class="row">
    <div class="col-lg-10 col-lg-offset-1">
      <h1 class="text-center">{{ t.time }} - {{ t.heading }}</h1>
      <div class="text-center">{{ t.blurb }}</div>
    </div>
  </div>
</div>      
{% endif %}
{% unless t.hide or t.heading %}

  <div class="container cfpsection" id="{{t.id}}">
    <div class="row" style="margin-top: 60px;">

      <div class="col-lg-4 col-md-4 col-sm-4 name">
        <h2>{% unless t.break %}{{ t.name }}<br/>{{t.name2}}<br/>{% endunless %}{{t.time}}</h2>
        {% if t.img %} <img src="{{t.img}}" /> {% endif %}
<br/>
<br/>
        {% if t.img2 %} <img src="{{t.img2}}" /> {% endif %}
      </div>

      <div class="col-lg-8 col-md-8 col-sm-8 name-desc">
        <div class="col-lg-10 col-md-10 col-sm-10">
          <h3 class="no-top-space">
            {{t.title}}
            {% if t.permalink %}
              <a style="font-size:40%;" href="{{t.permalink}}#h1">(Permalink)</a>
            {% endif %}
          </h3>
          <div class="abstract">
            {{ t.abstract }}
          </div>
          {% if t.video %}
            <div class="links">
              <a href="{{ t.video }}">(Video)</a>
              {% if t.slides %}<a href="{{ t.slides }}">(Slides)</a>{% endif %}
            </div>
          {% endif %}

          {% if t.bio %}
            <div class="bio">
              <h3> About {{t.name}} </h3>
              {{ t.bio }}
            </div>
          {% endif %}

          {% if t.bio2 %}
            <div class="bio">
              <h3> About {{t.name2}} </h3>
              {{ t.bio2 }}
            </div>
          {% endif %}
        </div>
      </div>
    </div>
  </div>

{% endunless %}
{% endfor %}

---

<div class="container">
Register for Melbourne :: C◦mp◦se 2019 tickets at <a href="https://www.eventbrite.com.au/e/2019-mini-melbourne-compose-conference-tickets-61752774210">Eventbrite</a>
</div>
