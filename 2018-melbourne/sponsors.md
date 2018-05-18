---
layout: 2018-melbourne/melbourne
title: "C&#9702;mp&#9702;se :: Melbourne - 2018 Sponsors"
---

<!--

TODO:

* Update sponsorship prospectus link to an internal page

-->

<style type="text/css">
		.panel-default .panel-body.unrestricted-height {
			max-height: none;
		}
</style>

<div class="sep talk melbourne" data-stellar-background-ratio="0.5" style="background-position: 50% -91.5px;"></div>
<br />

<div class="container">

  <h1 class="centered">Sponsors</h1>
  <br />

  <div class="row">
    <div class="col-sm-offset-2 col-sm-8">
      <p>
        C&#9702;mp&#9702;se :: Melbourne deeply appreciates our sponsors' contributions,
        which directly benefit the local functional programming community. The proceeds
        go towards operating costs that include speaker travel expenses,
        diversity efforts, and providing refreshments at the event.
      </p>
      <p>
        To find out how to be a sponsor, please take a look at our
        <a href="http://www.composeconference.org/2018-melbourne/sponsorship-prospectus/">sponsorship prospectus</a>
        for information. If you would like additional information on sponsorship,
        please contact us at: <a href="sponsors@mfpai">sponsors@mfpai</a>.
      </p>
      <!-- <h3> More details coming soon... </h3> -->
    </div>
  </div>
  <div class="row">

    <br />
    <hr style="color: #ddd; border-color: #ddd; border-style:dotted">
    <br />

	{% for t in site.data.2018-melbourne.sponsors.sponsors %}
			<div class="col-sm-6">
				<div class="panel panel-default">
					<div class="panel-heading">{{t.name}}</div>
					<div class="panel-body centered unrestricted-height">
						<a href="{{t.link}}">
						  <img src="{{t.img}}" class="img-responsive" alt="{{t.name}}"> <br><br>
						</a>
						<p> {{t.by_line}} </p>
					</div>
				</div>
			</div>
	{% endfor %}
  </div>
</div>
