
# Web Scraping Lab

## Questions

Resident Advisor is an events listing website for electronic music.

Go to www.residentadvisor.net/events.  This is the url we'll be starting with for this lab.  For question 1, just use this url.  In the next two, you'll use country and region in the format: http://www.residentadvisor.net/country/region/ i.e. us/losangeles/.  Be sure to explore the web pages in both the browswer and the HTML file.  You'll need both to really understand what's going on.

1. Which venues are hosting events this week?
2. Make a function which returns the events this week given region and country (this will take two arguments)
    - return the event name, link, and list of artists
    - function returns list of ['event name', 'www.linkaddress.com', ['artist1','artist2','artist3']]
3. Create a function which returns the users attending 
4. Bonus


### Question 1 - Which venues are hosting events this week?


```python
import requests
from bs4 import BeautifulSoup

r = requests.get('https://www.residentadvisor.net/events')
c = r.content
soup = BeautifulSoup(c, 'html.parser')
```


```python

```

Your solution output should look like: '101bklyn', '291 Hooper St', '99 Scott Ave','Alphaville', 'Analog Bkny'...

### Question 2 - Write a function to which returns the events this week given region and country.


```python
def find_events(country, region):

    
    
    
    
    
    
    
    
    

```


```python
# you should be able to output something like this
find_events('us','sanfrancisco')[0]
```




    ['Housepitality:Della, Homero Espinosa, Jason Peters at F8 1192 Folsom',
     'http://residentadvisor.net/events/1173172',
     ['Della', 'Homero Espinosa', 'Jason Peters']]



### Question 3 - Create a function which returns the numbers of users attending each event this week, given country and region.  Then plot a histogram


```python
def users_attending(country, region):

    
    
    
    
    
```


```python
# you should be able to output something like this
users_attending('us','newyork')[:10]
```




    [8, 5, 4, 3, 49, 18, 10, 3, 2, 11]




```python
#now use the function to make a histogram
import plotly.offline as offline
import plotly.graph_objs as go

offline.init_notebook_mode()

offline.iplot([go.Histogram(x = users_attending('jp','tokyo'))])
```


<script type="text/javascript">window.PlotlyConfig = {MathJaxConfig: 'local'};</script><script type="text/javascript">if (window.MathJax) {MathJax.Hub.Config({SVG: {font: "STIX-Web"}});}</script><script type='text/javascript'>if(!window._Plotly){define('plotly', function(require, exports, module) {/**
* plotly.js v1.42.2
* Copyright 2012-2018, Plotly, Inc.
* All rights reserved.
* Licensed under the MIT license
*/



<div id="c5c40f1e-7ee3-493a-81fc-887fd4f8f86e" style="height: 525px; width: 100%;" class="plotly-graph-div"></div><script type="text/javascript">require(["plotly"], function(Plotly) { window.PLOTLYENV=window.PLOTLYENV || {};window.PLOTLYENV.BASE_URL="https://plot.ly";Plotly.newPlot("c5c40f1e-7ee3-493a-81fc-887fd4f8f86e", [{"x": [16, 21, 3, 2, 15, 11, 2, 2, 76, 41, 26, 19, 16, 13, 10, 3, 99, 28, 19, 3, 2, 51, 16, 7, 15, 7, 3, 2, 7, 11, 6, 3, 4, 2, 1, 1], "type": "histogram", "uid": "ab9e99ca-2a49-4e8e-99ea-12500940d9d9"}], {}, {"showLink": true, "linkText": "Export to plot.ly"})});</script><script type="text/javascript">window.addEventListener("resize", function(){Plotly.Plots.resize(document.getElementById("c5c40f1e-7ee3-493a-81fc-887fd4f8f86e"));});</script>


## Bonus: Build object relations between artists, venues, and events with sqlalchemy!
Think about what each table should include - URLs, dates, etc.


```python

```