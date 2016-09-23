---
title: Textbook Plan
header-nav: true
week_numbers:
  01: "Preview and discuss book"
  02: Unit 1
  03: Unit 2
  04: Unit 3
  05: Unit 4
  06: Unit 5
  07: Unit 6
  08: Unit 7
  09: "Revision 1"
  10: Unit 8
  11: Unit 9
  12: Unit 10
  13: Unit 11
  14: "Revision 2"
  15: Unit 12
  16: Unit 13
  17: Unit 14
  18: Unit 15
  19: "Revision 3"
  20: "Revision"
  21: "Revision"
---

{% for week in page.week_numbers %}
Week {{ week[0] }} : {{ week[1] }}
{% endfor %}

