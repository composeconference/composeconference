---
layout: 2017-melbourne/melbourne
title: "Compose :: Melbourne Unconference"
---

<!--

Unconference Content:

* What is it?
* What do you need to do?
* Why isn't it ready yet?

-->


<div class="sep talk melbourne" data-stellar-background-ratio="0.5" style="background-position: 50% -91.5px;"></div>

<br />


<div class="container">
  <div class="row">
    <div class="col-lg-4 col-md-4 col-sm-4 name">

      <div class="row">
        <div class="col-lg-12 col-md-3 col-sm-3 col-xs-3 logo">
          <span style="font-size: 1300%; font-family: cursive;">UC</span>
        </div>
      </div>

    </div>

    <div class="col-lg-8 col-md-8 col-sm-8 name-desc">
      <div class="col-lg-10 col-md-10 col-sm-10">

        <h1>Unconference and Workshops</h1>

        <br />

        <p>
          Day two of Compose :: Melbourne will be a smorgasbord of
          <a href="https://en.wikipedia.org/wiki/Unconference">unconference</a> and workshops.
          Attendees will be free to present on topics of their choosing throughout the day
          with audiences assembling organically based on interest.
        </p>

        <p>
          Workshops will be run in parallel, focusing on introducing new concepts from
          the typed-functional-programming sphere to the curious and engaged.
        </p>

        <p>
          The second day of the conference is going to be a free event to encourage
          interested people in Melbourne to become part of the functional-programming
          community.
        </p>
      </div>
    </div>
  </div>
</div>

<div class="container cfpsection">
  <div class="row">
    <div class="col-lg-4 col-md-4 col-sm-4 name">
      <h2>Venue </h2>
    </div>

    <div class="col-lg-8 col-md-8 col-sm-8 name-desc">
      <div class="col-lg-10 col-md-10 col-sm-10">
        <p> RMIT Building 80 </p>
        <p> Rooms: 80.03.06, 80.03.15 and 80.02.07.  </p>
      </div>
    </div>
  </div>
</div>

<div class="container cfpsection">
  <div class="row">
    <div class="col-lg-4 col-md-4 col-sm-4 name">
      <h2>Unconference</h2>
    </div>
    <div class="col-lg-8 col-md-8 col-sm-8 name-desc">
      <div class="col-lg-10 col-md-10 col-sm-10">
        <p>
          As is standard practice with unconferences, topics to be decided on the day.
          However, if you wish to <a href="mailto:composemel-admin@googlegroups.com">let the committee know</a>
          that you are planning to announce an unconference talk on the day
          then we would be happy to hear from you so that we can get a feel for
          what people are offering on the second day!
        </p>
      </div>
    </div>
  </div>
</div>

<div class="container cfpsection">
  <div class="row">
    <div class="col-lg-4 col-md-4 col-sm-4 name">
      <h2>Workshops</h2>
    </div>
    <div class="col-lg-8 col-md-8 col-sm-8 name-desc">
      <div class="col-lg-10 col-md-10 col-sm-10">
        <p>
          Although the second day is a largely-unstructured event, if you wish to run
          a workshop then please <a href="mailto:composemel-admin@googlegroups.com">get in touch with the committee</a>
          to let them know so that they can advertise that your work will be there for others.
          Also, if your workshop requires more than spontaneous organisation then
          getting in touch is a must!
        </p>
      </div>
    </div>
  </div>
</div>

<div class="container" id="activities">
  <div class="row">
    <div class="col-lg-10 col-lg-offset-1">
        <br> <br> <br>
        <h1 class="text-center">Un-Conference Activities (More on the Day!)</h1>
        <br>

        <table class="agenda">
          <tr> <td> <strong> Talks </strong> </td> </tr>

          {% for w in site.data.2017-melbourne.unconference.talks %}
            <tr>
              <td> {% if w.time %} {{w.time}} {% endif %} </td>
              <td> {% if w.room %} {{w.room}} {% endif %} </td>
              <td> {{w.name}} </td>
              <td> <a href="#{{w.id}}">{{w.title}}</a> </td>
            </tr>
          {% endfor %}

          <tr> <td> <br> </td> </tr>

          <tr> <td> <strong> Workshops </strong> </td> </tr>

          {% for w in site.data.2017-melbourne.unconference.workshops %}
            <tr>
              <td> {% if w.time %} {{w.time}} {% endif %} </td>
              <td> {% if w.room %} {{w.room}} {% endif %} </td>
              <td> {{w.name}} </td>
              <td> <a href="#{{w.id}}">{{w.title}}</a> </td>
            </tr>
          {% endfor %}
        </table>
        <br> <br> <br>
    </div>
  </div>
</div>

{% for w in site.data.2017-melbourne.unconference.talks %}

<div class="container cfpsection" id="{{ w.id }}">
  <div class="row">
    <div class="col-lg-4 col-md-4 col-sm-4 name">
      <h2> {{ w.name }} </h2>
      {% if w.img %}
        <p>
          <img style="max-width: 80%; max-height: 300px;" src="{{ w.img }}" />
        </p>
      {% endif %}
      <p> <em> (Talk) </em> </p>
    </div>
    <div class="col-lg-8 col-md-8 col-sm-8 name-desc">
      <div class="col-lg-10 col-md-10 col-sm-10">
        <p><strong> {{ w.title }} </strong></p>
        {{ w.details }}
        {% if w.prereqs %}
          <p><strong> Pre-Requisites </strong></p>
          <p> {{ w.prereqs }} </p>
        {% endif %}
      </div>
    </div>
  </div>
</div>

{% endfor %}

{% for w in site.data.2017-melbourne.unconference.workshops %}

<div class="container cfpsection" id="{{ w.id }}">
  <div class="row">
    <div class="col-lg-4 col-md-4 col-sm-4 name">
      <h2> {{ w.name }}</h2>
      {% if w.img %}
        <p>
          <img style="max-width: 80%; max-height: 300px;" src="{{ w.img }}" />
        </p>
      {% endif %}
      <p> <em> (Workshop) </em> </p>
    </div>
    <div class="col-lg-8 col-md-8 col-sm-8 name-desc">
      <div class="col-lg-10 col-md-10 col-sm-10">
        <p><strong> {{ w.title }} </strong></p>
        {{ w.details }}
        {% if w.prereqs %}
          <p><strong> Pre-Requisites </strong></p>
          <p> {{ w.prereqs }} </p>
        {% endif %}
      </div>
    </div>
  </div>
</div>

{% endfor %}
