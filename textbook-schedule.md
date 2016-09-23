---
title: Textbook Plan
header-nav: true
week_numbers:
  01: "Preview and discuss book"
  02: "Unit 1, Greetings"
  03: "Unit 2, Subject Pronouns"
  04: "Unit 3, Present Simple of Be: Affirmative and Negative"
  05: "Unit 4, Present Simple of Be: Questions and Short Answers"
  06: "Unit 5, Articles: a/an and the"
  07: "Unit 6, Position of Adjectives, Nationality Adjectives"
  08: "Unit 7, Plural of Nouns"
  09: "Revision 1"
  10: "Unit 8, Possessive Adjectives"
  11: "Unit 9, Present Simple of Have Got"
  12: "Unit 10, Demonstratives and possessives ('s/s')"
  13: "Unit 11, Possessive Pronouns"
  14: "Revision 2"
  15: "Unit 12, Countable and Uncountable Nouns"
  16: "Unit 13, Present Simple with I, you, we and they"
  17: "Unit 14, Present Simple with he, she, it"
  18: "Unit 15, Present Simple in yes/no questions"
  19: "Revision 3"
  20: "Revision"
  21: "Revision"
---

{% for week in page.week_numbers %}
Week {{ week[0] }} : {{ week[1] }}
{% endfor %}

