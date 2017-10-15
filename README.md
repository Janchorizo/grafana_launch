# grafana_launch
First approach to plugin development for Grafana

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

### 1 Tecnologies

There are three aspects of the plugin that are needed to be takien into
account. Such are :

* Visual representation
* Plugin logic
* Data sources

#### Visual representation

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

#### Plugin  logic

The plugin logic, both for the visualization and configuration of it, will be
writen in Javascript using AngularJS as the framework.
This means that the logic will be distributed among components and services.

#### Data sources

The current data sources supported by Grafana are the following :

* Graphite
* Prometheus
* Elasticsearch
* InfluxDB
* OpenTSDB
* MySQL
* PostgreSQL
* AWS Cloudwatch

##### Graphite [web](https://graphiteapp.org/)
!(https://graphiteapp.org/img/architecture_diagram.png)
Graphite can be used to store numeric time-series data, although not collecting
it.
Three componentes make up Graphite : carbon, a daemon that listens for new
time-series data; whisper, a simple database library for storing time-series
data; the Graphite webapp for rendering graphs, which is what we are doing in
Grafana.

##### Prometheus [web](https://prometheus.io/)
!(https://prometheus.io/assets/architecture.svg)
Prometheus implements a multi-dimensional data model -time-series data
identified by metric name and key/value pairs-, a flexible query language.

##### Elasticsearch [web](https://www.elastic.co/products/elasticsearch)
Elasticsearch is a distributed, RESTful search and analytics engine.
Elasticsearch lets you perform and combine many types of searches — structured, unstructured, geo, metric — any way you want. 

Elasticsearch uses standard RESTful APIs and JSON. 

##### InfluxDB [web](https://docs.influxdata.com/influxdb/v1.3/)
!(https://www.influxdata.com/wp-content/uploads/architecture-2.png)
InfluxDB is a time series database built from the ground up to handle high write and query loads. It is the second piece of the TICK stack. InfluxDB is meant to be used as a backing store for any use case involving large amounts of timestamped data, including DevOps monitoring, application metrics, IoT sensor data, and real-time analytics.

Uses an SQL-like query language.

##### OpenTSDB [web](http://opentsdb.net/)
!(http://opentsdb.net/img/tsdb-architecture.png)

OpenTSDB consists of a Time Series Daemon (TSD) as well as set of command line utilities. Interaction with OpenTSDB is primarily achieved by running one or more of the TSDs.
You can communicate with the TSD via a simple telnet-style protocol, an HTTP
API or a simple built-in GUI. All communications happen on the same port.

 In OpenTSDB, a time series data point consists of:

   * A metric name.
   * A UNIX timestamp (seconds or millisecinds since Epoch).
   * A value (64 bit integer or single-precision floating point value), a JSON formatted event or a histogram/digest.
   * A set of tags (key-value pairs) that describe the time series the point belongs to.


##### MySQL [web](https://www.mysql.com/)
##### PostgreSQL [web](https://www.postgresql.org/)
##### AWS Cloudwatch [web](https://aws.amazon.com/es/cloudwatch/)

### 2 Tasks

Lets say that the plugin rests in a directory called *myPluginDirectory*


### 3 Best practices for each of the tasks

### 4 Working examples of plugins, and notes for  them

### 5 Notes

