---
name: Vega/Altair Plots
tools: [Python, Altair, vega-lite]
image: assets/pngs/homework.png
description: This is a visualization about disciplinary actions on different licenses!
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# License Discipline Graph

We can use a csv file and python with altair to make this:

<vegachart schema-url="{{ site.baseurl }}/assets/json/altair_licenses.json" style="width: 100%"></vegachart>


# Analysis of Visualizations

I created 2 visualizations that can be used to provide insight on the amount and reasons for disciniplary actions among many different licenses that are included in the dataset.

Viz 1:
The first visualization (Disciplinary Amounts) sorts the data by each type of license. This can include dental, detective board, cosmotology as well as many others. The bars represent the amount of disciplinary actions that have been taken against each of these license types. As you can see from the graph, the detective board has the most by a lot. In order to create this visualization I first had to create a subset of the dataset and group by license type. From there I reorganized the disciplined column to numbers in order for it to able to be counted and displayed all the results. 
The interactivty of this plot comes with the combination of the second visualization. The amount of disciplinary actions doesn't mean a whole lot without some context. That is why I decided to add another plot that was linked to the first one. In order to view the second plot you can click on any of the bars in the first plot to see the reasons why each license type got disciplinary actions which brings me into the description for the next plot.

Viz 2:
The second visualization (Reasons) is another bar graph that represents different categories of disciplinary actions. I split the categories into 6 major groups: Taxes, Criminal/Conviction, Qualifications, Billing, Unprofessional and other. The reason that I chose these categories was through a detailed look into the descriptions for the disciplinary actions. The dataset provided these reasons and after looking through them I found key words that fit into these 6 major categories. I then made a subset of the data with only these instances and grouped the data by these groups. After counting the amount in each group this visualization provides much more detail into the different types of actions taken against each license type.
The interactivity for this graph is directly correlated with the first graph, changing based on which license type the user selects.\

Choices:
I chose to make these graphs a bar chart because I feel like it is a simple visualization that is easy to understand with just a glance. The data isn't meant to be studied very deeply as the visualizations don't provide specific details just an overview of the trends about the disciplinary actions taken against different licensing types.

Below are the links to the data itself and the analysis I preformed on the data.

<!-- these are written in a combo of html and liquid --> 

<div class="left">
{% include elements/button.html link="https://github.com/UIUC-iSchool-DataViz/is445_data/raw/main/licenses_fall2022.csv" text="The Data" %}
</div>

<div class="right">
{% include elements/button.html link="https://github.com/jonahlw2/jonahlw2.github.io/blob/main/python_notebooks/Workbook.ipynb" text="The Analysis" %}

</div>

