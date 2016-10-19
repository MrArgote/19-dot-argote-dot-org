---
title: Points
header-nav: true
nav-icon: /assets/four-dots.svg
---


<style>
  .student-tasks-grid .number {
    border-radius: 10em;
    padding: 0.7em;
    display: inline-block; }
  .student-tasks-grid .done .number {
    color: #404 ;
    background-color: #fbf; }
  .student-tasks-grid .yet-to-do .number {
    color: #0FC ;
    background-color: #F65; }
</style>



## Act I

<div class="student-tasks-grid" style="display:flex-wrap;">
  {% for student in site.data.textbookProgress.students %}
    {% assign compSize = student[1].completed | size %}
    <div class="
    {% if compSize > 1 %}
      done
      {% else %}
        yet-to-do
    {% endif %}
    ">
      <div class="number">
      {{ student[0] }}
      </div>
      <div>
      {% if student[1].completed["quiz"] != empty %}
        quiz:
        {{ student[1].completed["quiz"] }} points
      {% endif %}
      </div>
      <div>
      {% if student[1].completed["01"] != empty %}
        unit 1:
        {{ student[1].completed["01"] }} points x 2
      {% endif %}
      </div>
      <div>
      {% if student[1].completed["02"] != empty %}
        unit 2:
        {{ student[1].completed["02"] }} points x 2
      {% endif %}
      </div>
      <div>
      {% if student[1].completed["03"] != empty %}
        unit 3:
        {{ student[1].completed["03"] }} points x 2
      {% endif %}
      </div>
      <div>
      {% if student[1].completed["04"] != empty %}
        unit 4:
        {{ student[1].completed["04"] }} points x 2
      {% endif %}
      </div>
      <div>
      {% if student[1].completed["05"] != empty %}
        unit 5:
        {{ student[1].completed["05"] }} points x 2
      {% endif %}
      </div>
    </div>
  {% endfor %}
</div>






