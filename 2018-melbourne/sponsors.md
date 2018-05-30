---
layout: 2018-melbourne/melbourne
title: "C&#9702;mp&#9702;se :: Melbourne - 2018 Sponsors"
---

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
        C&#9702;mp&#9702;se :: Melbourne sponsorship directly benefits the functional programming community as
        proceeds go towards operating costs that includes speaker travel expenses,
        diversity efforts, and providing refreshments at the event. As a sponsor, your
        company will be positioned for high-visibility in the Melbourne community.
      </p>
      <p>
        To find out how to be a sponsor, please take a look at
        <a href="/2018-melbourne/sponsorship-prospectus/">this page</a>
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
