---
layout: 2018-melbourne/melbourne
title: C◦mp◦se 2018 Speakers
permalink: /2018-melbourne/speakers/
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
            {% endif %}
            {% endunless %}
          {% endfor %}
        </table>
      </div>
  </div>

  <div class="row">
    <div class="col-lg-10 col-lg-offset-1">
        <table class="table table-bordered">
         <thead>
          <tr>
           <th>&nbsp;</th>
           <th>Room 1 - Hacking/sharing</th>
           <th>Room 2 - Workshop</th>
           <th>Room 3 - Workshops</th>
          </tr>
         </thead>
         <tr>
           <td scope="row">9am</td>
           <td colspan="3" class="break">Registration, catered morning tea, & signup for workshops & activities</td>
         </tr>
         <tr>
          <td>10am</td>
          <td>Mentoring matchups</td>
          <td rowspan="2"><a href="#david_laing">Front-end development with Reflex</a></td>
          <td rowspan="2"><a href="#lyndon_maydwell">CRASHKELL</a></td>
         </tr>
         <tr>
          <td>10:30am</td>
          <td>Flappy Bird in Haskell group learning</td>
         </tr>
         <tr>
          <td>12pm</td>
          <td class="break" colspan="3">Lunch</td>
         </tr>
         <tr>
          <td>1pm</td>
          <td>Lightning talks</td>
          <td rowspan="2">Front-end development with Reflex<br/>(continued)</td>
          <td rowspan="2"><a href="#rob_howard">Building a Small Compiler in JavaScript</a></td>
         </tr>
         <tr>
          <td>1:30pm</td>
          <td>My first paper: recursion schemes group learning. </td>
         </tr>
         <tr>
          <td>2:30pm</td>
          <td colspan="3" class="break">Catered afternoon tea</td>
         </tr>
         <tr>
          <td>3pm</td>
          <td>Unrecruiting</td>
          <td rowspan="2">Front-end development with Reflex<br/>(continued)	</td>
          <td rowspan="3"><a href="#luke_stephenson">Monix Adventures</a></td>
         </tr>
         <tr>
          <td>4pm</td>
         </tr>
         <tr>
          <td>5pm</td>
          <td colspan="3" class="break">The End</td>
         </tr>

        </table>
    </div>
  </div>
</div>



{% for t in site.data.2018-melbourne.speakers.times %}
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
