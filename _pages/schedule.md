---
layout: page
permalink: /schedule/
title: event schedule
description: Meeting information for upcoming Women in Math events; more information located on social media.
nav: true
nav_order: 2
---

<table
  id="table"
  data-toggle="table"
  data-url="{{ '/assets/json/fall2023.json' | relative_url }}">
  <thead>
    <tr>
      <th data-field="title">Title</th>
      <th data-field="host">Hosts</th>
      <th data-field="datetime" data-formatter="dateFmt">Date and time</th>
      <th data-field="location">Location</th>
    </tr>
  </thead>
</table>

<script>
	function dateFmt(value) {
		var dateArray = value.split('/');
		var startDate = new Date(dateArray[0]);
		var endDate = new Date(dateArray[1]);
		var fmt = new Intl.DateTimeFormat("en", {
			weekday: 'long',
			month: "long",
			day: "numeric",
			hour: "numeric",
		});
	return fmt.formatRange(startDate, endDate)
	}
</script>
