---
students:
  ranking:
    01: false
    02: 04
    03: false
    04: false
    05: 01
    06: false
    07: 02
    08: false
    09: 03
    10: false
    11: 05
    12: 06
    13: false
    14: false
    15: 08
    16: 11
    17: 10
    18: 09
    19: false
    20: false
    21: false
    22: 07
    23: false
    24: false

---


how quick are you to install LastPass extension and log-in?

<style>
  .student-tasks-grid span {
  display: inline-block;
  border-radius: 1em;
  padding: 0.3em;
  }
  .student-tasks-grid span.yet-to-do .number {
  background-color: #EEE;
}
  .student-tasks-grid span.done {
  background-color: #2F8;
  }
  .student-tasks-grid span.yet-to-do {
  background-color: #F4A;
  }
</style>

<div class="student-tasks-grid" style="display:flex-wrap;">
{% for student in page.students.ranking %}
  <span>
  {% if student[1] %}
    <span class="done">
      <span class="number">
      {{ student[0] }}
      </span>
      Done
    </span>
  {% else %}
    <span class="yet-to-do">
      <span class="number">
      {{ student[0] }}
      </span>
      Not ready?
    </span>
  {% endif %}
  </span>
{% endfor %}
</div>



