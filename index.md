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
Hi, I'm Harsha -- currently a MSc Visual Computing student at Saarland University. I study systems and theory for developing compute and data efficient deep learning models.

Topics I am currently interested in [in no specific order]:
* *Systems-aware* efficient *training* [or fine-tuning] and *inference* techniques for deep learning models, [I like working with ResNets and Transformers equally :D].
* *Model Compression* methods (Sparsity, Pruning, Quantization, Knowledge Distillation): exploring their *effectiveness* and trade-offs.
* Enhancing *communication efficiency* in distributed and federated learning settings.
* Large-scale models (Transformers): unraveling the secrets of their success and the mysteries of over-parameterization.
* The interplay between *interpretability*, *fairness*, *privacy*, and model compression/efficiency techniques.

Please feel free to go through my [projects]({{ site.baseurl }}/projects), [publications]({{ site.baseurl }}/publications) and if you're interested in some music/book/movie recommendations check out [media]({{ site.baseurl }}/media)!

<br>

## News

---

<div id="newstable" style="
/* height:150px;overflow:auto;  */
/* padding-left: 0.7em; padding-right: 0.7em; padding-top: 0.7em; padding-bottom: 0.7em; */
border: none;
">
<table style="width:100%; border: none;">

<col width="18%">
<col width="82%">

{%- for update in site.data.news -%}
<tr><td><em>{{ update.date }}</em></td>
<td>{{ update.content }}</td></tr>
{%- if forloop.last == false -%}
<tr><td colspan="2"><hr></td></tr>
{%- endif -%}
{%- endfor -%}
</table>
</div>