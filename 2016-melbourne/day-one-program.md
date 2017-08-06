---
layout: 2016-melbourne/melbourne
title: "Frequently Asked Questions"
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
</style>

<div class="sep talk melbourne" data-stellar-background-ratio="0.5" style="background-position: 50% -91.5px;"></div>

<br />

<div class="container">
  <div class="row">
    <div class="col-lg-10 col-lg-offset-1">
        <h1 class="text-center">Melbourne 2016 Day One - Speakers and Presentations</h1>
        <br />

        <table class="agenda">
          {% for t in site.data.2016-melbourne.speakers.times %}
            {% unless t.hide %}
              <tr>
                <td>{{t.time}}</td>
                <td>{{t.name}} {% unless t.committee or t.break or (t.bio and t.img) %} * {% endunless %}</td>
                <td>
                  <a href="#{{t.id}}">{{t.title}}</a>
                  {% if t.video %}<a href="{{ t.video }}">(Video)</a>{% endif %}
                  {% if t.slides %}<a href="{{ t.slides }}">(Slides)</a>{% endif %}
                  </td>
              </tr>
            {% endunless %}
          {% endfor %}
        </table>

        <br />

    </div>
  </div>
</div>

{% for t in site.data.2016-melbourne.speakers.times %}
{% unless t.hide %}

  <div class="container cfpsection" id="{{t.id}}">
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

{% endunless %}
{% endfor %}
