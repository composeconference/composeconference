---
layout: 2017-melbourne/speaker
title: "Compose :: Melbourne Speaker - Jurriaan Hage"
---

{% for t in site.data.2017-melbourne.speakers.times %}
{% unless t.hide %}
{% if t.name contains "Jurriaan Hage" %}

  <div class="container cfpsection" id="{{t.id}}">

    <div class="row" id="h1">
      <div class="col-lg-12 col-md-12 col-sm-12 name">
        <br />
        <br />
        <br />

        <h1> Compose :: Melbourne Speaker - {{t.name}} </h1>

        <br />

        <p style="font-weight: bold;">
          Compose :: Melbourne will feature many excellent speakers.
          One of this year's lineup is {{t.name}}.
          If you want to see the whole lineup <a href="/2017-melbourne/day-one-program/">look here!</a>
        </p>

        <br />
        <br />
        <br />
      </div>
    </div>

    <div class="row">
      <div class="col-lg-4 col-md-4 col-sm-4 name">
        <h2> {{t.time}} {% unless t.break %} - {{ t.name }} {% endunless %} </h2>
        {% if t.img %} <img src="{{t.img}}" /> {% endif %}
      </div>
      <div class="col-lg-8 col-md-8 col-sm-8 name-desc">
        <div class="col-lg-10 col-md-10 col-sm-10">
          <h3 class="no-top-space"> {{t.title}} </h3>
          <div class="abstract">
            {{ t.details }}
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

{% endif %}
{% endunless %}
{% endfor %}

