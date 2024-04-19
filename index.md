---
title: Home
layout: default
permalink: /
profile:
  align: right
  image: profile.png
published: true
order: 1
---

## About Me

Hi, I’m Harsha :) a Graduate student at Universitat Des Saarlandes in Visual Computing. I study math and systems that aim to understand perception, learning and creativity.

My current research interests lie at the intersection of **data and compute efficient deep learning**.

Questions my research seeks to answer:

* Ways to make DNN training **efficient** - computationally, memory-wise and just improving wall-clock time.
* How best to scale model training to take advantage of **distributed** training, systems and research [Federated or otherwise]
* **How** do deep neural networks learn? What makes a Transformer (or a ResNet) go brr?
* Does training make full use of the data, and can we make sense of these representations? *What* do they learn :0
* What mysteries does **over-parameterization** hold? Prune, quantize, low-rank but things often work out – but **why**?

Take a look at my [projects]({{ site.baseurl }}/projects) to see how I've brought these ideas to life. 


## News

---

<div id="newstable" style="height:150px;overflow:auto; padding-left: 0.7em; padding-right: 0.7em; padding-top: 0.7em; padding-bottom: 0.7em;">
<table>

<col width="18%">
<col width="82%">

{%- for update in site.data.news -%}
<tr><td><b>{{ update.date }}</b></td>
<td>{{ update.content }}</td></tr>
{%- if forloop.last == false -%}
<tr><td colspan="2"><hr></td></tr>
{%- endif -%}
{%- endfor -%}
</table>
</div>