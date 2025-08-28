---
layout: page
title: Staff
nav_order: 4
description: A listing of all the course staff members.
hide_right_toc: true
---

{% assign extra_instructors = nil %}
{% assign instructors = nil %}

{% assign extra_head_teaching_assistants = nil %}
{% assign head_teaching_assistants = nil %}

{% assign extra_teaching_assistants = nil %}
{% assign teaching_assistants = nil %}

{% assign extra_tutors = nil %}
{% assign tutors = nil %}

{% assign extra_readers = nil %}
{% assign readers = nil %}

{% assign extra_teaching_interns = nil %}
{% assign teaching_interns = nil %}

{% for staffer in site.staffers %}
  {% if staffer.extra and staffer.extra != empty %}
    {% case staffer.role %}
      {% when "Instructor" %}
        {% assign extra_instructors = extra_instructors | append: staffer %}
      {% when "Head TA" %}
        {% assign extra_head_teaching_assistants = extra_head_teaching_assistants | append: staffer %}
      {% when "TA" %}
        {% assign extra_teaching_assistants = extra_teaching_assistants | append: staffer %}
      {% when "Tutor" %}
        {% assign extra_tutors = extra_tutors | append: staffer %}
      {% when "Reader" %}
        {% assign extra_readers = extra_readers | append: staffer %}
      {% when "TI" %}
        {% assign extra_teaching_interns = extra_teaching_interns | append: staffer %}
    {% endcase %}
  {% else %}
    {% case staffer.role %}
      {% when "Instructor" %}
        {% assign instructors = instructors | append: staffer %}
      {% when "Head TA" %}
        {% assign head_teaching_assistants = head_teaching_assistants | append: staffer %}
      {% when "TA" %}
        {% assign teaching_assistants = teaching_assistants | append: staffer %}
      {% when "Tutor" %}
        {% assign tutors = tutors | append: staffer %}
      {% when "Reader" %}
        {% assign readers = readers | append: staffer %}
      {% when "TI" %}
        {% assign teaching_interns = teaching_interns | append: staffer %}
    {% endcase %}
  {% endif %}
{% endfor %}

# Staff
{% if site.staff_email and site.staff_email != '' and site.staff_email != 'None' %}
For logistics and administrative questions, please email <a href="mailto:{{site.staff_email}}">{{site.staff_email}}</a>.
Access to these emails is denoted by the `Staff Email Access` tag. Future instructors and
head TAs may also be able to read emails here, but we can delete emails upon request.

If you have a non-course related question, you can view staff emails by pressing the button below:

<div id="staffButtonContainer">
  <button id="email-trigger" class="btn btn-outline-primary">Show Emails</button>
</div>
{% endif %}

{% if extra_instructors or instructors %}
<!-- ## Instructors -->

<div class="role">
  {% for staffer in extra_instructors %}
    {{ staffer }}
  {% endfor %}

  {% for staffer in instructors %}
    {{ staffer }}
  {% endfor %}
</div>
{% endif %}


{% if extra_head_teaching_assistants or head_teaching_assistants %}
<!-- ## Head TAs -->

<div class="role">
  {% for staffer in extra_head_teaching_assistants %}
    {{ staffer }}
  {% endfor %}

  {% for staffer in head_teaching_assistants %}
    {{ staffer }}
  {% endfor %}
</div>
{% endif %}

{% if extra_teaching_assistants or teaching_assistants %}
<!-- ## TAs -->

<div class="role">
  {% for staffer in extra_teaching_assistants %}
    {{ staffer }}
  {% endfor %}

  {% for staffer in teaching_assistants %}
    {{ staffer }}
  {% endfor %}
</div>
{% endif %}

{% if extra_tutors or tutors %}
<!-- ## Tutors -->

<div class="role">
  {% for staffer in extra_tutors %}
    {{ staffer }}
  {% endfor %}

  {% for staffer in tutors %}
    {{ staffer }}
  {% endfor %}
</div>
{% endif %}

{% if extra_readers or readers %}
<!-- ## Readers -->

<div class="role">
  {% for staffer in extra_readers %}
    {{ staffer }}
  {% endfor %}

  {% for staffer in readers %}
    {{ staffer }}
  {% endfor %}
</div>
{% endif %}


{% if extra_teaching_interns or teaching_interns %}
## Teaching Interns (TIs)

<div class="role">
  {% for staffer in extra_teaching_interns %}
    {{ staffer }}
  {% endfor %}

  {% for staffer in teaching_interns %}
    {{ staffer }}
  {% endfor %}
</div>
{% endif %}

{% if site.staff_email and site.staff_email != '' and site.staff_email != 'None' %}
<script>
  var visible = false;
  document.addEventListener("DOMContentLoaded", function() {
    var button = document.getElementById("email-trigger");
    var emails = document.getElementsByClassName("staff-email");
    button.addEventListener("click", () => {
      if (visible) {
        button.innerHTML = "Show Emails"
      } else {
        button.innerHTML = "Hide Emails"
      }

      var i = 0;
      for (i; i < emails.length; i++) {
        if (visible) {
          emails[i].style.display = "";
        } else {
          emails[i].style.display = "inline";
        }
      }

      visible = !visible;
    })
  });
</script>
{% endif %}
