---
layout: 2017-melbourne/melbourne
title: "C◦mp◦se :: Melbourne - 2017 Sponsors"
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
        C◦mp◦se :: Melbourne sponsorship directly benefits the functional programming community as
        proceeds go towards operating costs that includes speaker travel expenses,
        diversity efforts, and provisioning sustenance at the event. As a sponsor, your
        company will be positioned for high-visibility in the Melbourne community.
      </p>
      <p>
        To find out how to be a sponsor, please take a look at
        <a href="https://github.com/composeconference/Compose-Melbourne/wiki/Sponsorship-Tiers">this page</a>
        for information. If you would like additional information on sponsorship,
        please contact us at: <a href="mailto:composemel-admin@googlegroups.com">composemel-admin@googlegroups.com</a>.
      </p>
    </div>
  </div>
  <div class="row">

    <br />
    <hr style="color: #ddd; border-color: #ddd; border-style:dotted">
    <br />

	{% for t in site.data.2017-melbourne.sponsors.sponsors %}
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
