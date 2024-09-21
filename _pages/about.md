---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

## About

I am an Electrical Engineering PhD candidate at the University of Maryland in the [Deparment of Electrical and Computer Engineering](https://ece.umd.edu/), and I research control theory and evolutionary game theory. While at UMD, I was a teaching assistant for several courses, on controls, optimization, and FPGA development, and I took courses on controls, optimization, and stochastic processes. 


Before starting my PhD, I received my B.Eng. from [Universidade Estadual de Maringá](https://uem.br/), Brazil, and worked on embedded systems, electronic design, software development and project budgeting.


## Research Interests



My research interests are in the intersection of control theory, game theory, and machine learning.  I am particularly interested in analyzing the dynamics of large-scale systems influenced by the strategic interactions of large populations of learning agents, and in data-driven techniques to determine stabilizing payoff mechanisms for such coupled systems.



## Recent Publications

  {% assign few_pubs =  site.publications | sort:"date" | reverse  %}
  <ul>{% for post in few_pubs limit:3 %}
    {% include archive-single-publication.html %}
  {% endfor %}</ul>