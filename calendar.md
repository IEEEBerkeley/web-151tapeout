---
title: Calendar
layout: page
nav_order: 1
hide_right_toc: true
---

<h1>Calendar</h1>

{% assign button_groups = site.data.calendar.categories | map: "name" | uniq %}

{%- if site.discussions_under_construction -%}
<p class="WARNING">
This schedule is tentative; additional times may be added later. The existing times shouldn’t change though (pending a couple of room bookings).
</p>
{%- endif -%}

If you would like to view this calendar ouside of the course website, please click "Open in Google Calendar" below. If you would like to add this calendar to your personal Google Calendar, please click "Add to your personal calendar" below.

[Open in Google Calendar]({{ "https://calendar.google.com/calendar/embed?src=c_5667391b618ea271c4025a8fc2700937cc1d32a195e1873f00f570f251ee5a4b%40group.calendar.google.com&ctz=America%2FLos_Angeles" }}){: .btn .btn-outline .fs-3 } [Add to your personal calendar]({{ "http://berkie.ee/tapeoutcalendar" }}){: .btn .btn-outline .fs-3 }

{% include calendar.html %}

<div id="calendarContainer">
  Alongside tab navigation, the following keyboard shortcuts are available for use on this page:
  <div id="calendarShortcuts" class="justify-content-between">
    <span class="shortcut"><kbd aria-label="Left Arrow" title="Left Arrow" style="margin-right: 0.2em;">￩</kbd> Jump to Previous Period</span>
    <span class="shortcut"><kbd aria-label="Right Arrow" title="Right Arrow" style="margin-right: 0.2em;">￫</kbd> Jump to Next Period</span>
    <span class="shortcut"><kbd style="margin-right: 0.2em;">t</kbd> Jump to Today</span>
    <span class="shortcut"><kbd style="margin-right: 0.2em;">d</kbd> Switch to Day View</span>
    <span class="shortcut"><kbd style="margin-right: 0.2em;">w</kbd> Switch to Week View</span>
  </div>
  <div id="calendarControls" class="btn-toolbar justify-content-between" role="toolbar" aria-label="Calendar control toolbar">
    Use the following toggles to customize your calendar view. If you'd like to hide a category of events, click on the respective button to do so. The calendar will immediately update to reflect your selection. To re-enable that category, click again.
    <span style="display: block; height: 1rem;"></span>
    <div class="input-group mb-3" role="group" aria-label="Calendar category toggles" style="text-align: center;">
      {% for group in button_groups %}
        <button class="btn btn-outline-primary" data-action="toggle-category-{{ group | downcase | replace: " ", "-" }}" aria-label="Toggle {{ group }}" >{{ group }}</button>
      {% endfor %}
    </div>
  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function() {
    initCalendar();
  });
</script>
