**What is ELK Stack?**

![image](https://user-images.githubusercontent.com/85872541/201723938-0694aa21-f26d-4f93-af8e-71f1b52fb086.png)

*The ELK Stack is a collection of three open-source products called Elasticsearch, Logstash, and Kibana.*

*ELK stack provides centralized logging in order to identify problems with servers or applications. It allows you to search all the logs in a single place.* 

*ELK Stack is designed to allow users to take data from any source, in any format, and to search, analyze, and visualize that data in real time.*


**What is ElasticSearch?**

Elasticsearch is a robust and platform-independent search engine that can provide a rapid full-text search over millions of documents and store them a as JSON documents and give you back JSON data, when a document is stored, it is indexed and fully searchable in near real-time-within 1 second. Elasticsearch uses a data structure called an inverted index that supports very fast full-text searches. 

**What is Logstash?**

Logstash is the data collection pipeline tool. It collects data inputs in server-side and feeds into the Elasticsearch. It gathers all types of data from the different source and makes it available for further use.

**Logstash consists of three stages:**

**Input**: get data from different resources(beats, Redis, file).

**Filters**: It is a set of conditions to perform a particular action or event(grok, date).

**Output**: Decision maker for processed event or log(elasticsearch, file).


![image](https://user-images.githubusercontent.com/85872541/201727030-602bced7-6c3a-4cb8-9e72-01c09d53a42f.png)

**What is Kibana?**

Kibana is a data visualization which completes the ELK stack. This tool is used for visualizing the Elasticsearch documents and helps developers to have a quick insight into it. Kibana dashboard offers various interactive diagrams, geospatial data, and graphs to visualize complex quires. It can be used for search, view, and interact with data stored in Elasticsearch directories.

**Note:** there is another product called *beats* which is the forth product added to *ELK stack* and thats why since then we mention *ELK stach* as an **Elastic stack**

**Beats ecosystem**

Beats are data shippers that are installed on servers as agents used to send different types of operational data to Elasticsearch either directly or through Logstash, there are currently six official Beats from Elastic: Filebeat(read files from your system like log files), Metricbeat, Packetbeat, Heartbeat, Winlogbeat, and Auditbeat. Many applications will use both Logstash and Beats.

![image](https://user-images.githubusercontent.com/85872541/201728158-3d489a4f-4c95-46cd-8360-d725b4bd50fb.png)

**Why is ElasticSearch so popular?**

- It’s free and open source

*The basic features are free, if you need security and alerting features in Kibana, you can buy the commercial X-pack subscription for Kibana, or you can install some open source alternatives.*

- RESTful API

*ElasticSearch has a RESTful API. Query results are returned in JSON which means results are easy to work with. Querying and inserting data via the RESTful API means it’s easy to use any programming language to work with ElasticSearch.*

- Easy to Query

*ElasticSearch has a built-in full-text search engine that is based on Apache Lucene. Compared to other databases, Lucene is easy to query. Even non-technical people would be able to write common queries.*

- It’s fast - very fast

*Querying a large SQL database can easily take 10 or 20 seconds. It’s quite common for similar queries on a large ElasticSearch database to return results in under 10 milliseconds.*

**Note:** While dealing with very large amounts of data, you may need Kafka, RabbitMQ for buffering and resilience. For security, nginx can be used.

![image](https://user-images.githubusercontent.com/85872541/201729363-64847660-12d7-4eb0-90a7-2cd1a377496f.png)

**Case studies:** Netflix | LinkedIn | Medium | SoundCloud | GitHub

**What is Elastic APM?**

Elastic APM is an **application performance monitoring** system which is built on top of the ELK Stack (Elasticsearch, Logstash, Kibana, Beats) and It's a **real-time monitoring** tool for applications. It collects different metrics like incoming and outcoming requests, database queries, external requests and many more and allows you to manage overall performance of software applications to monitor availability, transaction times, and performance issues that could potentially impact the user experience.

The Elastic APM solution compromises 4 main building blocks, all open source—**Elasticsearch** for data storage and indexing, **Kibana** for analyzing and visualizing the data and two APM-specific components—**APM server and the APM agent:**
- **APM agents** are responsible for collecting the performance data and sending it to the APM server.
- **APM server** is responsible for receiving the data, creating documents from it and sending the data forth into Elasticsearch for storage.

![image](https://user-images.githubusercontent.com/85872541/201730493-552bb68a-5470-45c2-9240-fc3dfff7e2e6.png)



