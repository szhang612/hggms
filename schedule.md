---
title: "Schedule"
layout: page
permalink: /hggms/schedule/
---

Below is our current schedule. We update this page regularly; check back for new events and announcements.

{% assign sorted_events = site.data.events | sort: "date" %}

<table class="schedule-table">
  <thead>
    <tr>
      <th>Date</th>
      <th>Time</th>
      <th>Title</th>
      <th>Description</th>
      <th>Location</th>
    </tr>
  </thead>
  <tbody>
    {% for event in sorted_events %}
    <tr>
      <td>{{ event.date | date: "%b %-d, %Y" }}</td>
      <td>{{ event.time }}</td>
      <td><strong>{{ event.title }}</strong></td>
      <td>{{ event.abstract }}</td>
      <td>{{ event.location }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
