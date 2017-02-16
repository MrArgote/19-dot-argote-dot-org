---
title: Points
header-nav: false
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

<div class="student">
  <div class="pyramid">
    <div class="pyramid-top"></div>
    <div class="trapezoid-level-3"></div>
    <div class="trapezoid-level-2"></div>
    <div class="trapezoid-level-1"></div>
  </div>
  <div class="pyramid">
    <div class="trapezoid-level-2"></div>
    <div class="trapezoid-level-1"></div>
  </div>
  <div class="pyramid">
    <div class="pyramid-top"></div>
    <div class="trapezoid-level-3"></div>
    <div class="trapezoid-level-2"></div>
    <div class="trapezoid-level-1"></div>
  </div>
</div>
<div class="student">
  <div class="pyramid">
    <div class="trapezoid-level-1"></div>
  </div>
  <div class="pyramid">
    <div class="pyramid-top"></div>
    <div class="trapezoid-level-3"></div>
    <div class="trapezoid-level-2"></div>
    <div class="trapezoid-level-1"></div>
  </div>
  <div class="pyramid">
    <div class="trapezoid-level-3"></div>
    <div class="trapezoid-level-2"></div>
    <div class="trapezoid-level-1"></div>
  </div>
</div>

## Act II --- Talk on Slack about...

<div class="student-tasks-grid" style="display:flex-wrap;">
  {% for student in site.data.textbookProgress.students %}
    <div class="yet-to-do">
      <div class="number"> {{ student[0] }} </div>
      <div class="student">
      {% for assignment in student[1].completed.slack-act-ii %}
        <div class="topic"> {{ assignment[0] }} </div>
        {% assign pts = assignment[1] %}
        <div class="pyramid">
          {% if assignment[1] > 0 %}
            {% if assignment[1] > 1 %}
              {% if assignment[1] > 2 %}
                {% if assignment[1] > 3 %}
                  <div class="pyramid-top"></div>
                {% endif %}
                <div class="trapezoid-level-3"></div>
              {% endif %}
              <div class="trapezoid-level-2"></div>
            {% endif %}
            <div class="trapezoid-level-1"></div>
          {% endif %}
        </div>
        <div class="num-of-points"> {{ pts }} </div>
      {% endfor %}
      </div>
    </div>
  {% endfor %}
</div>

## Act I

Textbook points are x2.

<div class="student-tasks-grid" style="display:flex-wrap;">
  {% for student in site.data.textbookProgress.students %}
    {% assign compSize = student[1].completed.textbook | size %}
    <div class="
    {% if compSize > 1 %} done {% else %} yet-to-do {% endif %}
    ">
      <div class="number"> {{ student[0] }} </div>
      <div>
        {% if student[1].completed["quiz"] != empty %}
          quiz: {{ student[1].completed["quiz"] }} pts.
        {% endif %}
      </div>
      <div>
        {% if student[1].completed.textbook["01"] != empty %}
          unit 1: {{ student[1].completed.textbook["01"] }} pts.
        {% endif %}
      </div>
      <div>
        {% if student[1].completed.textbook["02"] != empty %}
          unit 2: {{ student[1].completed.textbook["02"] }} pts.
        {% endif %}
      </div>
      <div>
        {% if student[1].completed.textbook["03"] != empty %}
          unit 3: {{ student[1].completed.textbook["03"] }} pts.
        {% endif %}
      </div>
      <div>
        {% if student[1].completed.textbook["04"] != empty %}
          unit 4: {{ student[1].completed.textbook["04"] }} pts.
        {% endif %}
      </div>
      <div>
        {% if student[1].completed.textbook["05"] != empty %}
          unit 5: {{ student[1].completed.textbook["05"] }} pts.
        {% endif %}
      </div>
    </div>
  {% endfor %}
</div>






