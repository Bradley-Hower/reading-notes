# *Course 401 Python, Entry 14: Data Visualization

**What are the key differences between Matplotlib, Seaborn, and Bokeh libraries in terms of their features and use cases? Provide an example of a specific visualization that is more suitable for each library.**

Matplotlib - Basic visualizations. Charts and graphs. Versatile. Pandas uses matplotlib.

Seaborn - Heatmaps, improved data distributions visualization. Add-on to Matplotlib.

Bokeh - Interactive visualization. Zoom in, pan, or toggle the display.

(https://machinelearningmastery.com/data-visualization-in-python-with-matplotlib-seaborn-and-bokeh/)[https://machinelearningmastery.com/data-visualization-in-python-with-matplotlib-seaborn-and-bokeh/]

**In the Seaborn library, what are the main functions to create relational, categorical, and distribution plots? Briefly explain the purpose of each type of plot and provide an example use case.**

## Relational

Visualization Statistical Relationship 

seaborn.relplot - Figure-level interface for drawing relational plots. Provides access to other axes-level functions.

seaborn.scatterplot()

seaborn.lineplot()

Syntax : 

seaborn.relplot(x=None, y=None, data=None, **kwargs) 

## Categorical

### Barplot

By default is uses mean.

Syntax:  

barplot([x, y, hue, data, order, hue_order, …])

### Countplot

Basic bar graph, by count.

Syntax:  

countplot([x, y, hue, data, order, …])

### Boxplot

Also known as the "box and whisker" plot. Shows a distribution of data representing comparison between two variables. The whiskers represent data that lays outside the core confidence interval.

Syntax: 

boxplot([x, y, hue, data, order, hue_order, …])

### Violinplot

Similar to boxplot but more visual using kernel density. 

Syntax:  

violinplot([x, y, hue, data, order, …])

Syntax: 

boxplot([x, y, hue, data, order, hue_order, …])

## Distribution

### Displot

A histogram.

Syntax:

distplot(a[, bins, hist, kde, rug, fit, ...])

### Joinplot

Combines two graphs into one. For example, scatter and histogram.

### Pairplot

Another two in one. This time, overlaying the data.

### Rugplot

Shows ditribution of individual plots as ticks along the axis. A good visualization for clusters.

Syntax:

rugplot(data=None, *, x=None, y=None, hue=None, height=0.025, expand_margins=True, palette=None, hue_order=None, hue_norm=None, legend=True, ax=None, **kwargs)

**Discuss the role of the Seaborn Cheat Sheet in a Python developer’s workflow. What are some key sections or elements featured in the cheat sheet that can help a developer quickly reference Seaborn functionalities?**

The cheatsheet makes it much faster and easier to find the code to enter at any given stage. It is a excellent reference for any stage of the development in Seaborn. This turns changes into a menu, reducing the need to remember all the names and syntax.

## Things I want to know more about

What use cases are Seaborn and Bokeh better? Or is it all preference? 
