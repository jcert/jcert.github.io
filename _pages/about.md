---
permalink: /
title: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

## About

I am an assistant professor at the [Instituto Tecnológico de Aeronáutica](https://www.ita.br/) (ITA) in Brazil. My work focuses on control theory, system-theoretic passivity, and evolutionary game theory. 

Prior to joining ITA, I was a Postdoctoral Researcher at the University of California, Santa Barbara (UCSB). I completed my Ph.D. in Electrical Engineering at the University of Maryland, College Park, within the [Department of Electrical and Computer Engineering](https://ece.umd.edu/). While at UMD, alongside taking courses in controls, optimization, and stochastic processes, I served as a Graduate Teaching Assistant for courses in control systems, optimization, and FPGA hardware development.

I hold a Bachelor's degree in Electrical Engineering from the [Universidade Estadual de Maringá](https://uem.br/) (UEM) in Brazil, having previously worked with embedded systems, electronic design, and software development.

## Research Interests

My research sits at the intersection of control theory, game theory, and machine learning. I am particularly interested in modeling and analyzing the network dynamics of large-scale systems driven by the strategic, decision-making behavior of large populations of learning agents. My current projects involve developing data-driven, stabilizing payoff mechanisms and dynamic incentive structures for such socio-technical systems.

## Recent Publications

  {% assign few_pubs = site.publications | sort:"date" | reverse %}
  <ul>{% for post in few_pubs limit:3 %}
    {% include archive-single-publication.html %}
  {% endfor %}</ul>
