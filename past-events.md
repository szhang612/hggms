---
title: "Past Events"
layout: page
permalink: /past-events/
---

Below is a list of some of our past events.  
We update this page periodically as new events happen.

{% assign sorted_past = site.data.past_events | sort: "date" | reverse %}

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
    {% for event in sorted_past %}
    <tr>
      <td>{{ event.date | date: "%b %-d, %Y" }}</td>
      <td>{{ event.time }}</td>
      <td>
  <strong>{{ event.title }}</strong>
  {% if event.photo %}
  <div class="event-photo-thumb">
    <img src="{{ event.photo | relative_url }}" alt="Photo from {{ event.title }}">
  </div>
  {% endif %}
</td>
      <td>{{ event.abstract }}</td>
      <td>{{ event.location }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
