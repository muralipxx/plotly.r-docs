---
description: How to create carpet plots in R with Plotly.
display_as: scientific
language: r
layout: base
name: Carpet Plot
order: 8
output:
  html_document:
    keep_md: true
permalink: r/carpet-plot/
thumbnail: thumbnail/carpet.jpg
---


### Set the Coordinates 

To set the `x` and `y` coordinates use `x` and `y` attributes. If `x` coorindate values are ommitted a cheater plot will be created.


```r
library(plotly)

p <- plot_ly(
    type = 'carpet',
    y = c(2, 3.5, 4, 3, 4.5, 5, 5.5, 6.5, 7.5, 8, 8.5, 10))
```

### Add Parameter Values

To save parameter values use `a` and `b` attributes.


```r
library(plotly)

p <- plot_ly(
    type = 'carpet',
    a = c(4, 4, 4, 4.5, 4.5, 4.5, 5, 5, 5, 6, 6, 6),
    b = c(1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3),
    y = c(2, 3.5, 4, 3, 4.5, 5, 5.5, 6.5, 7.5, 8, 8.5, 10))

p
```

<div id="htmlwidget-81a18ca2fc5697b44ad7" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-81a18ca2fc5697b44ad7">{"x":{"visdat":{"35c4ad5638a":["function () ","plotlyVisDat"]},"cur_data":"35c4ad5638a","attrs":{"35c4ad5638a":{"a":[4,4,4,4.5,4.5,4.5,5,5,5,6,6,6],"b":[1,2,3,1,2,3,1,2,3,1,2,3],"y":[2,3.5,4,3,4.5,5,5.5,6.5,7.5,8,8.5,10],"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"carpet"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"yaxis":{"domain":[0,1],"automargin":true,"title":[]},"aaxis":{"domain":[0,1],"automargin":true},"baxis":{"domain":[0,1],"automargin":true},"xaxis":{"domain":[0,1],"automargin":true},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"a":[4,4,4,4.5,4.5,4.5,5,5,5,6,6,6],"b":[1,2,3,1,2,3,1,2,3,1,2,3],"y":[2,3.5,4,3,4.5,5,5.5,6.5,7.5,8,8.5,10],"type":"carpet","xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Add Carpet Axes

Use `aaxis` or `baxis` lists to make changes to the axes. For a more detailed list of attributes refer to [R reference](https://plot.ly/r/reference/#carpet-aaxis).


```r
library(plotly)

p <- plot_ly(
    type = 'carpet',
    a = c(4, 4, 4, 4.5, 4.5, 4.5, 5, 5, 5, 6, 6, 6),
    b = c(1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3),
    y = c(2, 3.5, 4, 3, 4.5, 5, 5.5, 6.5, 7.5, 8, 8.5, 10),
    aaxis = list(
      tickprefix = 'a = ',
      ticksuffix = 'm',
      smoothing = 1,
      minorgridcount = 9
      ),
    baxis = list(
      tickprefix = 'b = ',
      ticksuffix = 'Pa',
      smoothing = 1,
      minorgridcount = 9
      )
    )

p
```

<div id="htmlwidget-dd7b587e5be08189f9b4" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-dd7b587e5be08189f9b4">{"x":{"visdat":{"35c42968b1fa":["function () ","plotlyVisDat"]},"cur_data":"35c42968b1fa","attrs":{"35c42968b1fa":{"a":[4,4,4,4.5,4.5,4.5,5,5,5,6,6,6],"b":[1,2,3,1,2,3,1,2,3,1,2,3],"y":[2,3.5,4,3,4.5,5,5.5,6.5,7.5,8,8.5,10],"aaxis":{"tickprefix":"a = ","ticksuffix":"m","smoothing":1,"minorgridcount":9},"baxis":{"tickprefix":"b = ","ticksuffix":"Pa","smoothing":1,"minorgridcount":9},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"carpet"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"yaxis":{"domain":[0,1],"automargin":true,"title":[]},"aaxis":{"domain":[0,1],"automargin":true},"baxis":{"domain":[0,1],"automargin":true},"xaxis":{"domain":[0,1],"automargin":true},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"a":[4,4,4,4.5,4.5,4.5,5,5,5,6,6,6],"b":[1,2,3,1,2,3,1,2,3,1,2,3],"y":[2,3.5,4,3,4.5,5,5.5,6.5,7.5,8,8.5,10],"aaxis":{"tickprefix":"a = ","ticksuffix":"m","smoothing":1,"minorgridcount":9},"baxis":{"tickprefix":"b = ","ticksuffix":"Pa","smoothing":1,"minorgridcount":9},"type":"carpet","xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Style Carpet Axes


```r
library(plotly)

p <- plot_ly(
  type = 'carpet',
  a = c(4, 4, 4, 4.5, 4.5, 4.5, 5, 5, 5, 6, 6, 6),
  b = c(1, 2, 3, 1, 2, 3, 1, 2, 3, 1, 2, 3),
  y = c(2, 3.5, 4, 3, 4.5, 5, 5.5, 6.5, 7.5, 8, 8.5, 10),
  aaxis = list(
    tickprefix = 'a = ',
    ticksuffix = 'm',
    smoothing = 1,
    minorgridcount = 9,
    minorgridwidth = 0.6,
    minorgridcolor = 'white',
    gridcolor = 'white',
    color = 'white'
  ),
  baxis = list(
    tickprefix = 'b = ',
    ticksuffix = 'Pa',
    smoothing = 1,
    minorgridcount = 9,
    minorgridwidth = 0.6,
    gridcolor = 'white',
    minorgridcolor = 'white',
    color = 'white'
  )
) %>%
  layout(
    plot_bgcolor = 'black', paper_bgcolor = 'black',
    xaxis = list(showgrid = F, showticklabels = F),
    yaxis = list(showgrid = F, showticklabels = F)
  )

p
```

<div id="htmlwidget-699cbd79c2d4d838de66" style="width:672px;height:480px;" class="plotly html-widget"></div>
<script type="application/json" data-for="htmlwidget-699cbd79c2d4d838de66">{"x":{"visdat":{"35c4482324b5":["function () ","plotlyVisDat"]},"cur_data":"35c4482324b5","attrs":{"35c4482324b5":{"a":[4,4,4,4.5,4.5,4.5,5,5,5,6,6,6],"b":[1,2,3,1,2,3,1,2,3,1,2,3],"y":[2,3.5,4,3,4.5,5,5.5,6.5,7.5,8,8.5,10],"aaxis":{"tickprefix":"a = ","ticksuffix":"m","smoothing":1,"minorgridcount":9,"minorgridwidth":0.6,"minorgridcolor":"white","gridcolor":"white","color":"white"},"baxis":{"tickprefix":"b = ","ticksuffix":"Pa","smoothing":1,"minorgridcount":9,"minorgridwidth":0.6,"gridcolor":"white","minorgridcolor":"white","color":"white"},"alpha_stroke":1,"sizes":[10,100],"spans":[1,20],"type":"carpet"}},"layout":{"margin":{"b":40,"l":60,"t":25,"r":10},"plot_bgcolor":"black","paper_bgcolor":"black","xaxis":{"domain":[0,1],"automargin":true,"showgrid":false,"showticklabels":false},"yaxis":{"domain":[0,1],"automargin":true,"showgrid":false,"showticklabels":false,"title":[]},"aaxis":{"domain":[0,1],"automargin":true},"baxis":{"domain":[0,1],"automargin":true},"hovermode":"closest","showlegend":false},"source":"A","config":{"showSendToCloud":false},"data":[{"a":[4,4,4,4.5,4.5,4.5,5,5,5,6,6,6],"b":[1,2,3,1,2,3,1,2,3,1,2,3],"y":[2,3.5,4,3,4.5,5,5.5,6.5,7.5,8,8.5,10],"aaxis":{"tickprefix":"a = ","ticksuffix":"m","smoothing":1,"minorgridcount":9,"minorgridwidth":0.6,"minorgridcolor":"white","gridcolor":"white","color":"white"},"baxis":{"tickprefix":"b = ","ticksuffix":"Pa","smoothing":1,"minorgridcount":9,"minorgridwidth":0.6,"gridcolor":"white","minorgridcolor":"white","color":"white"},"type":"carpet","xaxis":"x","yaxis":"y","frame":null}],"highlight":{"on":"plotly_click","persistent":false,"dynamic":false,"selectize":false,"opacityDim":0.2,"selected":{"opacity":1},"debounce":0},"shinyEvents":["plotly_hover","plotly_click","plotly_selected","plotly_relayout","plotly_brushed","plotly_brushing","plotly_clickannotation","plotly_doubleclick","plotly_deselect","plotly_afterplot","plotly_sunburstclick"],"base_url":"https://plot.ly"},"evals":[],"jsHooks":[]}</script>

### Add Points and Contours

To add points and lines to see [Carpet Scatter Plots](https://plot.ly/r/carpet-scatter) or to add contours see [Carpet Contour Plots](https://plot.ly/r/carpet-contour)

### Reference

See [https://plot.ly/r/reference/#carpet](https://plot.ly/r/reference/#carpet) for more information and options!
