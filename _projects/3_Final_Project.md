---
name: Power Plant Visualization Plots 
tools: [Python, Altair, vega-lite]
image: assets/pngs/per-capita-energy-use.png
description: This is a visualization about power plants around the world, their fuel, capacity and location.
custom_js:
  - vega.min
  - vega-lite.min
  - vega-embed.min
  - justcharts
---


# Power Plants - A Fuel type & Location Analysis!
#### Created by Jonah Witte

<vegachart schema-url="{{ site.baseurl }}/assets/json/power_plants.json" style="width: 100%"></vegachart>


### Analysis of Main Visualization

This chart is broken down into 3 main components, the bar chart (pictured left), the map chart (pictured right) and the dropdown menu (pictured below). 

Starting with the bar chart, this graph is a representation of all the different power plants within a single country. It seperates the plants by primary fuel type (hyrdo, gas, coal etc) and then calculates the capacity in megawatts for each fuel type. Essentially what capacity means is the max amount of power that the plants can produce/provide at once. "Running at max capacity" means the power plant/plants would produce the pictured amount of megawhatts. 

The second chart is of a map. This chart shows the location of each power plant organzied by country. This gives an idea of how many plants are within a country and where they are located. Hovering over a marker of a plant on the map will show the country name, primary_fuel and capacity for that plant. This chart works in combination with the bar chart as when a specific fuel type is selected then the map will highlight which plants on the map use that primary fuel type. 

_**The selected fuel type and the map locations will turn red!**_

The last part of the chart is the country dropdown menu. This is a basic dropdown that allows a country to be selected and will update both the bar chart and the map to accurately reflect the selected country's power plant locations and seperations by fuel.



### Contextual Visulizations

#### KW/H Graph

![Countires Kw/h](/assets/pngs/per-capita-energy-use.png)

<span style="font-size: 10px;">“Data Page: Primary energy consumption per capita”, part of the following publication: Hannah Ritchie, Pablo Rosado, and Max Roser (2023) - “Energy”. Data adapted from U.S. Energy Information Administration, Energy Institute, Various sources. Retrieved from [OurWorldInData](https://archive.ourworldindata.org/20250925-233948/grapher/per-capita-energy-use.html) [online resource] (archived on September 25, 2025).</span>

The map pictured above is one from Our World In Data and shows a map of the world highlighted on a color scale based on the number of kilowatts per hour that the average person uses in the country. This is extremely relevant to the main visualization as it shows how much energy is used vs how much it is possible to produce. 

_**Keep in mind that a Megawatt is 1000x a kilowatt!**_


#### Carbon Emissions Graph

![Carbon Emmisions](/assets/pngs/annual-co2-emissions-per-country.png)

<span style="font-size: 10px;">“Data Page: Primary energy consumption per capita”, part of the following publication: Hannah Ritchie, Pablo Rosado, and Max Roser (2023) - “Energy”. Data adapted from U.S. Energy Information Administration, Energy Institute, Various sources. Retrieved from [OurWorldInData](https://archive.ourworldindata.org/20250925-233948/grapher/per-capita-energy-use.html) [online resource] (archived on September 25, 2025).</span>

This next chart shows a time series relating to how much carbon emission is in the atmosphere for the entire world. This chart is also from Our World In Data and is relevant in this instance because of the different types of plants around the world. As seen from my orginal graph, power plants that use primary carbon based fuel like coal and gas have a much higher max capacity than other more eco friendly options like solar or hydro. While this is beneficial as it increases the amount of energy that can be used, the above graph shows how much carbon emissions are being produced which ultimately destry our atmosphere and needs to be remedied as soon as possible.

### Artistic Choices:
I chose to make a bar and map chart combination since it is very user friendly and information can be extracted without too much direction. I chose to make the selected color red because it stands out very nicely on a gray background and can easily be seen. I chose dark green for the non selected color because I wanted a color that looks dull and not draw very much attention while also being able to show up on a gray neutral background.

Below are the links to the data itself and the analysis I preformed on the data.

<!-- these are written in a combo of html and liquid --> 
<div class="right">
{% include elements/button.html link="https://github.com/jonahlw2/jonahlw2.github.io/blob/main/python_notebooks/final_project.ipynb" text="The Analysis" %}

</div>

<div>
{% include elements/button.html link="https://datasets.wri.org/datasets/global-power-plant-database?map=eyJhY3RpdmVMYXllckdyb3VwcyI6W3siZGF0YXNldElkIjoiNTM2MjNkZmQtM2RmNi00ZjE1LWEwOTEtNjc0NTdjZGI1NzFmIiwibGF5ZXJzIjpbIjJhNjk0Mjg5LWZlYzktNGJmZS1hNmQyLTU2YzM4NjRlYzM0OSJdfV0sImJhc2VtYXAiOiJsaWdodCIsImJvdW5kYXJpZXMiOmZhbHNlLCJib3VuZHMiOnsiYmJveCI6bnVsbCwib3B0aW9ucyI6e319LCJsYWJlbHMiOiJkYXJrIiwibGF5ZXJzUGFyc2VkIjpbWyIyYTY5NDI4OS1mZWM5LTRiZmUtYTZkMi01NmMzODY0ZWMzNDkiLHsiYWN0aXZlIjp0cnVlLCJsYXllclNvdXJjZSI6bnVsbCwib3BhY2l0eSI6MSwidmlzaWJpbGl0eSI6dHJ1ZSwiekluZGV4IjoxMX1dXSwidmlld1N0YXRlIjp7ImxhdGl0dWRlIjo0NC40MTk2NzM0MTY1MjU5MSwibG9uZ2l0dWRlIjoxMi44MTQ0MDgxMTY3NjEzNDIsInpvb20iOjIuNjQzODY1OTY0NTE4OTI5NX19" text="Power Plant Location Data" %}
</div>



<div>
{% include elements/button.html link="https://ourworldindata.org/grapher/per-capita-energy-use" text="KW/h Usage Data" %}
</div>

<div>
{% include elements/button.html link="https://ourworldindata.org/co2-emissions" text="Carbon Emissions Data" %}
</div>



