---
layout: 2019/page
title: Organizers
permalink: /2019/organizers/
---


<div id="organizers">
	<div class="container">
		<div class="row">
{% for person in site.data.2019.organizers.organizers %}
			<div class="col-lg-4 col-md-4 col-sm-4 col-xs-4">
			<img src="{{ person.photo }}" class="img-responsive img-rounded" />
			<h2>{{ person.name }}</h2>
			<h3></h3>
			<p style="min-height:60px;">
			{{ person.bio }}
			</p>
			</div>
{% endfor %}
</div><!--/row -->
</div><!--/container -->
</div>

<hr style="border:1px dotted #efefee "/>
