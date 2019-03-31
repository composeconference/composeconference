---
layout: 2019/page
title: Organizers
permalink: /2019/organizers/
---


<div id="organizers">
    <div class="container">
        <div class="row">
{% for person in site.data.2019.organizers.organizers %}
    <div class="col-lg-3 col-md-3 col-sm-3 col-xs-3">
        <img src="{{ person.photo }}" class="img-responsive img-rounded" />
        <h2>{{ person.name }}</h2>
        <div style="min-height:10px;">
        <p>
        {{ person.bio | markdownify }}
        </p>
        </div>
    </div>
{% endfor %}
</div><!--/row -->
</div><!--/container -->
</div>

<hr style="border:1px dotted #efefee "/>
