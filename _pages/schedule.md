---
layout: page
permalink: /schedule/
title: event schedule
description: Materials for courses you taught. Replace this text with your description.
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
      <th data-field="datetime" data-formatter="dateFormatter">Date and time</th>
      <th data-field="location">Location</th>
    </tr>
  </thead>
</table>

<script>
	function dateFormatter(value) {
		var dateArray = value.split('/');
		var startDate = dateArray[0];
		var endDate = dateArray[1];
		const fmt = new Intl.DateTimeFormat("en", {
			weekday: 'long',
			month: "short",
			day: "numeric",
			hour: "numeric",
		});
	return fmt.formatRange(startDate, endDate)
	}
</script>
