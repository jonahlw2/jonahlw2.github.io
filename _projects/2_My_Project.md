---
name: Vega/Altair Plots
tools: [Python, Altair, vega-lite]
image: assets/pngs/homework.png
description: This is a "showcase" project that uses vega-lite for interactive viz!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# License Discipline Graph

We can use a csv file and python with altair to make this:

<vegachart schema-url="{{ site.baseurl }}/assets/json/altair_licenses.json" style="width: 100%"></vegachart>


<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jnaiman/online_cv_public/blob/main/python_notebooks/homework5.ipynb" text="The Analysis" %}

</div>

