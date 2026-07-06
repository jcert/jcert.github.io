---
title: 'IFAC "key words"'
date: 2024-07-09
permalink: /posts/2024/07/ifac_keywords/
sitemap: false
tags:
  - IFAC
  - Automatica
---

The IFAC list of "key words"
======

I always forget which keywords are available for journals... 

For *Automatica*, they instruct that the "keywords" (which on Papercept are called "key words") should be:

> chosen from the IFAC keyword list or with the help of the Automatica keyword wizard.

The template adds that we should select:

> Five to ten keywords.

Except that once you try to submit the paper, the instructions change. In summary:
- At least 2 keywords are required;
- Up to 3 can be made up by the authors, while the others must be IFAC keywords;
- There is a strict limit of 6 keywords.

The IFAC list of keywords is available [on IFAC's website](https://www.ifac-control.org/) under the description of the `Scope of Technical Committees`. But once you get to the paper submission page, you will notice that some of the keywords do not match the submission options (is that the so-called Automatica keyword wizard?). 

As an example:

| IFAC Scope of Technical Committees | Papercept |
| ------------- | ------------- |
| 1.4 Stochastic Systems, Stochastic control and game theory | 1.4 Stochastic Systems, Stochastic Control |
| 2.3 Non-linear Control Systems, Lyapunov methods | 2.3 Non-linear Control Systems, (???) |
| 2.3 Non-linear Control Systems, Passivity-based control | 2.3 Non-linear Control Systems, (???) |
| 2.4 Optimal Control, Differential or dynamic games | 2.4 Optimal Control, (???) |

The ones actually available on Papercept, as of today, are:

<button name="button" onclick="document.getElementById('IFACtable').style.visibility = 'visible'">See the whole table</button>

<table id="IFACtable" style="visibility:collapse; height: 100px;" >
  {% for row in site.data.IFAC_keyword %}
    {% if forloop.first %}
    <tr>
      {% for pair in row %}
        <th>{{ pair[0] }}</th>
      {% endfor %}
    </tr>
    {% endif %}

    {% tablerow pair in row %}
      {{ pair[1] }}
    {% endtablerow %}
  {% endfor %}
</table>
