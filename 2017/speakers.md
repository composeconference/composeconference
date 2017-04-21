---
layout: 2017/page
title: C◦mp◦se 2017 Speakers
permalink: /2017/speakers/
---

Register for C◦mp◦se :: Conference 2017 tickets at [composeconference.eventbrite.com](http://composeconference.eventbrite.com)

---

<div id="biowrap">
  <div class="container">
  <div class="row">
      <div class="col-lg-8 col-md-8 col-sm-8 col-xs-8">
    <h2>Dr. Emily Riehl</h2>
    <h3><small>[KEYNOTE]</small> A categorical view of computational effects</h3>
    <p>
    Monads have famously been used to model computational effects, although, curiously, the computer science literature presents them in a form that is scarcely recognizable to a category theorist — I’d say instead that a monad is just a monoid in the category of endofunctors, what’s the problem? ;) To a categorical eye, computational effects are modeled using the Kleisli category of a monad, a perspective which suggests another categorical tool that might be used to reason about computation. The Kleisli category is closely related to another device for categorical universal algebra called a Lawvere theory, which may be a more natural framework to model computation (an idea suggested by Gibbons, Hinze, Hyland, Plotkin, Power and certainly others). This talk will survey monads, Lawvere theories, and the relationships between them and illustrate the advantages and disadvantages of each framework through a variety of examples: lists, exceptions, side effects, input-output, probabilistic non-determinism, and continuations.
    </p>
      </div>
  </div><!-- --/row ---->
  </div><!-- --/container ---->
</div>


{% for speaker in site.data.2017.speakers.speakers %}

  <hr>

  <div id="biowrap">
  <div class="container">
  <div class="row">
      <div class="col-lg-8 col-md-8 col-sm-8 col-xs-8">
        <h2>{{ speaker.name }}</h2>
        <h3>{{ speaker.title }}</h3>
        <p>
          {{ speaker.abstract }}
        </p>
      </div>
      <div class="col-lg-4 col-md-4 col-sm-4 col-xs-4">
      <h2>&nbsp;</h2>
      <h3><small>{{ speaker.start_time | date: '%h %-d, %I:%M%P'}}</small></h3>
      <p class="text-centered">
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
</div>
{% endfor %}

---

Register for C◦mp◦se :: Conference 2016 tickets at [composeconference.eventbrite.com](http://composeconference.eventbrite.com)
