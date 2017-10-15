# grafana_launch
First approach to plugin development for grafana

## Grafana panel plugins

The intention is to develop panel plugins for the metric analytics and 
visuzalization suite which is Grafana.

From the actual docs of Grafana:
*The Panel is the basic visualization building block in Grafana. Each Panel
provides a Query Editor (dependent on the Data Source selected in the panel)
that allows you to extract the perfect visualization to display on the Panel by
utilizing the Query Editor.*

To this extent, it is supposed to provide a visualization for data from one or 
more of the supported data sources.

This project that you are looking at is my playground for learning. I will use
it to register everything that I may find useful in order to develop the
plugin.

### Structure of this self made manual
1. Tecnologies
2. Procedures
3. Best practices for each of the tasks
4. Working examples of plugins, and notes for  them
5. Notes

## 1 Tecnologies

There are three aspects of the plugin that are needed to be takien into
account. Such are :

* Visual representation
* Plugin logic
* Data sources

### Visual representation

Grafana is a web based application and that implies that the visualization of
the actual plugin is taken care by web tecnologies which are 
   * HTML
   * CSS
   * Javascript 

At the moment of writing this -15 October, 2017- HTML5 and CSS3 are been used.
The version of Javascript that we'll be using is the latest available ES6, but 
the actual version that will be uploaded and served for the plugin is ES5.

That implies a transpile from one version to the other, been Babel a good
option for it.

### Plugin  logic

The plugin logic, both for the visualization and configuration of it, will be
writen in Javascript using AngularJS as the framework.
This means that the logic will be distributed among components and services.

### Data sources

## 2 Tasks

Lets say that the plugin rests in a directory called *myPluginDirectory*


## 3 Best practices for each of the tasks

## 4 Working examples of plugins, and notes for  them

## 5 Notes

