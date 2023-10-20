---
layout: default
title: ASAC
---

## {{ page.title }}
### About ASAC
Program synthesis typically takes either natural language or formal specifications as input. While large language models generate substantial code from natural language descriptions, the inherent ambiguity in natural language makes it challenging to guarantee the correctness of generated programs. On the other hand, using formal specifications offers the potential for precise semantics and provable program correctness. However, traditional specification-based approaches often fall short as they tend to produce code snippets too small for practical use.

Some researchers focus on synthesizing algorithms from specification which is both meaningful and feasible.  To motivate research on synthesizing algorithms, we present the first benchmark for this problem: ASAC. ASAC consists of 136 tasks collected from a competitive programming contest and covers a wide range of algorithmic paradigms and various difficulty levels. Each task in ASAC includes a formal specification and an efficiency requirement, and the program synthesizer is expected to produce a program that satisfies the formal specification and meets the efficiency requirement. 
### Get the whole Benchmark
<a href="https://github.com/AuQWQuA/ASAC" target="_blank">GitHub Repository</a> 

<table>
  <thead>
    <tr>
      <th>Tasks</th>
      <th>Tags</th>
      <th>Difficulty</th>
    </tr>
  </thead>
  <tbody>
    {% for task in site.tasks %}
    <tr>
      <td><a href="{{site.baseurl}}{{ task.url }}">{{ task.title }}</a></td>
      <td>
        {% for tag in task.tags %}
        {{ tag }} 
        {% unless forloop.last %}, {% endunless %}
        {% endfor %}
      </td>
      <td>{{ task.difficulty }}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>
****