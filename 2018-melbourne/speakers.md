---
layout: 2018-melbourne/melbourne
title: C◦mp◦se 2018 Speakers
permalink: /2018-melbourne/speakers/
---

<style type="text/css">
  .container img {
    max-height: 300px;
  }
  h3.no-top-space {
    margin-top: 0;
  }
  .agenda td {
    vertical-align: top;
  }
  .key td {
    vertical-align: top;
    padding-width: 5px;
  }
</style>

<div class="sep talk melbourne" data-stellar-background-ratio="0.5" style="background-position: 50% -91.5px;"></div>

<br />

<div class="container">
  <div class="row">
    <div class="col-lg-10 col-lg-offset-1">
        <h1 class="text-center">Programme</h1>
        <br />

        {% if site.data.2018-melbourne.speakers.show-level %}
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
          {% for t in site.data.2018-melbourne.speakers.times %}
            {% unless t.hide %}
              <tr>
                <td>{{t.time}}</td>
                <td>{{t.name}}</td>
                <td>
                  <a href="#{{t.id}}">{{t.title}}</a>
                  {% if t.video %}<a href="{{ t.video }}">(Video)</a>{% endif %}
                  {% if t.slides %}<a href="{{ t.slides }}">(Slides)</a>{% endif %}
                </td>
                {% if site.data.2018-melbourne.speakers.show-level %}
                 <td>
                   <nobr>
                   {% if t.level >= 1 %} &#x1f535; {% endif %} 
                   {% if t.level >= 2 %} &#x1f535; {% endif %} 
                   {% if t.level >= 3 %} &#x1f535; {% endif %} 
                   </nobr>
                 </td>
                {% endif %}
              </tr>
            {% endunless %}
          {% endfor %}
        </table>

        <br />

      </div>
  </div>
</div>

<h1 class="text-center">Day One - Speakers and Presentations</h1>

{% for t in site.data.2018-melbourne.speakers.times %}
{% unless t.hide %}

  <div class="container cfpsection" id="{{t.id}}">
    <div class="row" style="margin-top: 60px;">
      <div class="col-lg-4 col-md-4 col-sm-4 name">
        <h2>{% unless t.break %}{{ t.name }}<br/>{% endunless %}{{t.time}}</h2>
        {% if t.img %} <img src="{{t.img}}" /> {% endif %}
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
        </div>
      </div>
    </div>
  </div>

{% endunless %}
{% endfor %}

---

<div class="container">
Register for C◦mp◦se :: Conference 2018 tickets at <a href="https://www.eventbrite.com.au/e/compose-melbourne-2018-tickets-46002911948">Eventbrite</a>
</div>
