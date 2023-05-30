# IBM Data Visualization with Python

###Week 1 - Intro to DV Tools  
Matplotlib - John Hunter - EEG/EcoG Visualisation  
Architecture-  
Scripting Layer - pyplot  
Artist layer - artist  
![Artist Layer](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/38aa8ecd-a563-41f7-82fc-4ba96c67e9ca/Untitled.png)  
Backend Layer - FigureCanvas , renderer , eventAGG - anti grain geometry  
![Backend Layer](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/451edc23-20f4-4e3e-ae74-3270382d9f96/Untitled.png)  

%matplotlib inline - magic function - cannot modify a figure once its rendered  
%matplotlib notebook - can modify  

###Week 2 - Basic and Specialized DV Tools  
######Line plot  
series of data points called markers connected by straight lines  
years=list(map(str, range(1980,2014)))  
.columns, .index, .tolist()  

######Area plot  
represents cumulated totals using numbers or  percentages over time  
(kind=’area’)  

######Histogram  
represents frequency distribution of a variable  
(kind=’hist’)  
count, bin_edges=np.histogram(df[’2012’])  

######Bar chart  
is used to compare the values of a variable at a given point in time  
(kind=’bar’)  

######Pie chart  
circular statistic graphic  
(kind=’pie’)  

######Box plots  
(kind=’box’)  
minimum = Q1 - 1.5 IQR  
Q1 - 25%  
Median  
Q3 - 75%  
Maximum = Q3 + 1.5 IQR  
Outliers - individual dots  

######Scatter plot  
Displays two variables against each other  
dependent x independent to find correlation  

###Week 3 - Advanced Viz and Geospatial Data  
-Waffle chart - displays progres towards goals  
converts a dataframe into tiles  
Not builtin for matplotlib  

-Word Cloud - depiction of frequency of words in textual data  
Not builtin for matplotlib  
Andreas Mueller - word cloud generator  

Seaborn is based on matplotlib  
-Regression plots  
ax=sns.regplot(x='yar',y='total',data=df)  
color,marker  

Folium - leaflet maps(geospatial data)  
longitudes and latitudes  
world_map=folium.Map(location=[x,y],tiles='style',zoom_start=n)  

canada_map=folium.Map(location=[56.130,-106.35])  
ontario=folium.map.FeatureGroup()  
ontario.add_child(folium.features.CircleMarker([51.25,-85.32],radius=5,color='red',fill_color='red'))  
folium.Marker([51.25,-85.32],popup="Ontario").add_to(canada_map)  

Chloropleth Maps - thematic maps in which areas are shaded  
It requires a GeoJSON file  
Folium enables binding of data to map for chloropleth visualizations as well as passing visualizations as markers on the map  
It has built-in tilesets from OpenStreetMap, Mapbox, Stamen, Mapbox API Keys.  
  
###Week 4 - Creating Dashboards with Plotly and Dash  
Dashboard  
	- Real time visuals  
	- KPI  
	- Decisions and Analysis  

Web based dashboards - plotly dash, panel, voila, streamlit  
Bokeh, ipywidgets, matplotlib, Flask, bowtie  

Intro to Plotly  
- available in python, R and JS  

 submodules  
-plotly graph objects  
-plotly express  

Plotly dash  
dash_core_components - interactive and are generates with JS, HTML, CSS, React  
dash_html_components - has classes for every html tag  

[John Snow's data journalism: the cholera map that changed the world | Cholera | The Guardian](https://www.theguardian.com/news/datablog/2013/mar/15/john-snow-cholera-map)  
[Dashboarding tools — PyViz 0.0.1 documentation](https://pyviz.org/dashboarding/)  

To learn more about using Plotly to create dashboards, explore  
[Plotly python](https://plotly.com/python/getting-started/)  
[Plotly graph objects with example](https://plotly.com/python/graph-objects/)  
[Plotly express](https://plotly.com/python/plotly-express/)  
[API reference](https://plotly.com/python-api-reference/)  

Here are additional useful resources:  
[Plotly cheatsheet](https://images.plot.ly/plotly-documentation/images/plotly_js_cheat_sheet.pdf)  
[Plotly community](https://community.plotly.com/c/api/5)  
[Related blogs](https://plotlygraphs.medium.com/)  
[Open-source datasets](https://developer.ibm.com/exchanges/data/)  
[Complete dash user guide](https://dash.plotly.com/)  
[Dash core components](https://dash.plotly.com/dash-core-components)  
[Dash HTML components](https://dash.plotly.com/dash-html-components)  
[Dash community forum](https://community.plotly.com/c/dash/16)  
[Related blogs](https://medium.com/plotly/tagged/dash)  
[Python decorators reference 1](https://realpython.com/primer-on-python-decorators/)  
[Python decorators reference 2](https://www.python.org/dev/peps/pep-0318/#current-syntax)  
[Callbacks with example](https://dash.plotly.com/basic-callbacks)  
[Dash app gallery](https://dash-gallery.plotly.host/Portal/)  
[Dash community components](https://plotly.com/dash-community-components/)  

