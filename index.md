---
layout: default
---
<section>
<h1><a href="http://games.espn.com/ffl/leagueoffice?leagueId=24903">Super Cool Dynasty League</a></h1>
</section>

<section class="title open">
<h2>Team Pages</h2>
{% for team in site.data.rosters %}
		{% unless team.id == page.team %}
			<nav>
				<ul>
					<li><h1><a href="{{ site.baseurl }}/{{ team.id }}">{{ team.name }}</a></h1></li>
				</ul>
			</nav>
		{% endunless %}
	{% endfor %}
</section>
<section class="title open">
<h2>
	<a href="{{ site.baseurl }}/depth-chart">Depth Charts</a>
</h2>
<h2>
	<a href="{{ site.baseurl }}/rules">Rules</a>
</h2>
</section>