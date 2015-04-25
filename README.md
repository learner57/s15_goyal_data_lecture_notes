# s15_goyal_data_lecture_notes

##Lecture 1: Jan 13, 2015

Data engineering - in this class, it will be termed as big data software engineering.

It includes:

1. social networks

2. Data analysis – sampling – (data analysis using machine learning)

3. Storage – NoSQL – for evolving schema, fast delivery of the data, but not good in doing arbitrary queries. NoSQL has document, graph, key value, columnar stored based databases. 

Data modeling is hard, expensive, easy to get wrong for large level big data situation, even in migration. Difficult to do migration in big data with tereabytes of the big data information. 

Data collection and cleaning of the data – from where data is coming and if the data is in the acceptable format 
Data needs to be cleaned before storage or you can store the data and run batch jobs to clean data and restore it. 

Infobiz side effect – examples- D3 javascript , tablon, R etc. frameworks 

Data life cycle – Its a closed loop of the steps namely: 
	
1. question – curation – triage (prioritizing according to the situation) -  persistence
2. collection then generation
3. cleanup	
4. storage
5. processing or analysis
6. query and visualize or act

After step 6, it again goes back to the step 1 to get refined responses. Life cycle described above will be in all the data engineering process in every company. 

As a user, google search, filter, mobile app, web app are ways to interact to big data. 

An HTTP request uses the HTTP network protocol to further use get, put, post, delete requests which goes to HTTP server, which receives the HTTP request and responses back. This is known as request response cycle. 


#Lecture 2: Jan 15, 2015

##Presentation 

Markdown - a type of markup language which uses plain text formatting, can be converted to HTML and has two types - standard version and GitHub flavored. 

You can add lists, emojis, styles, images, links, codes using the Markdown language. 

Lists can be unordered or ordered. 

"#" sign gives headers. Bold, italics can be used by using "**word**" and "*word*". 

links can be created by using [] or () 

for using code block, use three ``` in the start and end of the code block. 

You can add tables and horizontal lines. 

End of the presentation

##Communcation between web browser and web server 

using http request on http port. 

Majorly we use GET and PUT. 

Web server is deployed in APACHE and responds to the requests.

requests uses image tags, script tags to embedd in HTML.

rails modularize the structure of the page to be loaded accprding to the user demands. 

##RESTFUL SERVICES

REST : Representation about resources conveyed through a representing pattern. 

Resources are URIs which are a superclass of URLs. 

S- state, T- transtion. 

CRUD: Create, Read, Update, Delete operations are used in Representation of the resources. 

##Using REST over services: Just like the anamoly with CREATE

GET: Read and get back to the current state of the resources, eg. /users/{id} will get you back the ids of the user 

POST: Create the {data} 

PUT: Update the existing resource

DELETE: as usual

##Create a simple service using the restful services. 

ruby sinatra to create web services

require Json

configure-end

get-end

#Lecture 3: Jan 20, 2015

##REST 

Asynchronous requests with javascript - when page stays but reloads some parts of it. 

basic authentication and oath 2 authentication is required to complete high level complicated delete operations. 

##Operations on 2 resources: 

FIRST APPROACH: COMBINE BOTH THE RESOURCES IN ONE URL: 

Lets have /users/0 and /possesions/1 are the separate URL resources then combined REST service on both resources will be GET /users/0/possessions/1  for lets say GET example. You can do for POST too the same way. 

SECOND APPROACH: WHILE PERFORMING ONE OPERATION, REFER TO ANOTHER RESOURCE USING REFERENCE ID. 

##ISSUES:

1. Security: authentication of users
2. Identity: assigning IDs
3. Failure: handling of failing situations: using HTTP status codes(404 error) or handle using JSON, or combination of both. 
4. Persistance: storage of resources: java implemetation is shown in lecture and ruby implementation stores resources in files. You can also use databases like Cassandra. 

##EXAMPLES: 
Using Sinatra, Rspec, Typhoeus, Node and Express. 

Use Rspec testing framework. 

#Lecture 4: Jan 22, 2015

##Presentation 1- Git Version Control System
5 possible stages for workflow: Untracked, unmodified, modified, staged, remote. 

Initialization: git init

clone: git clone remote_repository_address

branch: git branch new_branch_name

	to delete the branch, use git branch -d new_branch_name

checkout: git checkout branch_name 

add file: got add file 

commit: got commit -m "Commit Message"

merge: got merge branch_name 

##Presentation 2: Introduction of Github

its a close loop of master to branch then to pull request

new branch is new feature. do not add directly to the master branch. 

after creating branches commit messages. Then pull request. to add to the master branch for production. 

fork - carbon copy of repository, for running experiments. 

difference between forking and cloning? forking is done when you don't have collaborator access. else you do cloning. 

#Lecture 5: Jan 27, 2015

##NODE.JS
Service side tool for executing Javascript like Chrome. 

most of the code is in package of a module in node. example, core module 

CreateServer() function implements server and returns object with method listen()

console.log prints the statement in Javascript. 

Event Loop and queue allows to add work and libraries for later execution. 

Example of EVent Loop - process.nexttick() - prioritize the procces over any pernding I/O

next tick makes the function which calls the event in next loop. 

setimmediate() - leaves current interation and processes I/O 

check about setTimeout() and setInterval()

###CALLBACK HELL

for async programming

callback gets intended

##Node Execution Model 

Node is single threaded. code written are in sync. no worries about race conditions. IOS is parallely handled. 

callback gets registered if issue is async call for IO

IO gets executed in separate thread

easy to do server side services

#Lecture 5: Jan 29, 2015

##EXPRESS 

Web application framework written in javascript. 

features to serve static files and is influenced by Sinata. 

middleware framwork 

package.json

#Lecture 7: Feb 5, 2015

##reviewing a complicated example of angular node.js

#Lecture 8: Feb 10, 2015
usin clojure and javascript for Ken's first Gist. It changes as per the javascript code develops. automatically defined by runtime engine. 

1. IIFEs - useful while returning object. global keyword can not use variable defined inside the block of code. 

##Getting Data from Twitter
create an account via twitter apps and work on access token. dev.twitter.com

#Lecture 11: Feb 17, 2015

##working with the twitter framework

5 REST APIs, timeline concept, automatic handle of twitter rate limits

#Lecture 12: Feb 19, 2015

##NoSQL DATABASES

need to switch to new type of databases to efficiently use DB's in the services. 

Vertical scaling 
Sharding
problems with the above solutions make us to switch to nosql DBs. We need to bring complexity to the architecture to make the application simpler while in terms of using the database. Challenege with relational DB is:
1. Fault tolerance is very hard
2. COmplexity is pushed to the application layer
3. Lack of human fault tolerance
4. maintainence is huge amount of work

NoSQL are distributed in nature and are horizontally scalable. They manage replication and sharding automatically. 

##Types of NoSQL DB:
1. Key value
2. Graphs
3. Columnar
4. Document

Key Vlaue stores are like hash tables, presented with a key and associated value. It can store any format of the data. There is no query language. Examples being Voldemort, S3, Redis. 

Graph stores provides structured query language, optimized to store graph structure, traversing of the graph is efficient, you can also calculate shortest path and relation among different set of nodes and hop from one node to another. SHarding could be difficult. 

Columnar Stores can scale to enormous amount of data. This type of DB has column families having row and their unique row keys. There is a distributed hash table all the way. Examples being Cassandra and HBase. 

Document stores are bags of key value pairs also termed as documents stored in the collection. Example MongoDB, CouchDB

#Lecture 13: Feb 24, 2015

##CouchDB
Document based DB written in Erlang language used in telecommunications. 
It has RESTful API and is built for distribution and is highly consistent. 
It has self contained data based on storing documents. No use of foregin key or any other pointers. 
No schema available. 


While designing distributed systems, one must take into account CAP theorem - Consistency, Availability and Partition Tolerance. You can only work on two at once. CouchB=DB works with availability and Partiton Tolerance whcih guarantees EVENTUAL consistency. 

###Implementation of CouchDB
It uses B-tree storage engine. AUtomatic searching and uses MapReduce over the B-tree to compute views of parallel and incremental computation. No Locking used. Validation function can be written for classes of document in Javascript. Incremental replication allows to sync data between 2 servers. 

It supports CURD operations. 

#Lecture 14: Feb 26, 2015

##MongoDB Presentation - Vikas Mehta

No fixed schema. Stores the data in BSON format. Indexes are implemented as B-trees.
No multi document atomic transactions are allowed. MongoDB supports Consistency and Availability. 
Documents have hierarchical structure. Documents are ordered set of keys and keys are associated with values. 
Its type sensitive and case sensitive. Cannot contain duplicate keys. 

MongoDB has some reserved Databases like Admin, Local and Config. 

Windows Xp is not supported. 

Use of MongoLabs

#Lecture 16: Mar 5, 2015

##MongoDB Indexes

Import tweets
Clean data 
use MongoDB

MongoDB Indexes: 1 means ascending and -1 means descending. 

Compund Indexes: to sort and query on two attributes. 

#Lecture 17: Mar 10, 2015

##MongoDB Continued: More on Indexes and MapReduce

Indexes reduces the amount of documents needed and in memory sorting. Indexes get updated as soon as related document is updated. 

Index cardinality: possible values for the indexed field. High cardinality fields have greater possibility to reduce query much faster. 

Full text indexes and Geospatial indexes. 

MongoDB has full text search. 

Geospatial index supposrts GeoJSON format. Mongo supports, points, lines, polygons. 

#Lecture 18: Mar 17, 2015

##Solr Presentation

uses Apache lucene. used for search engine over the website. searches the index of the keywords found in the document. 
Problem with SOLR is to start the sunspot gem, killing the process manually, 

##REDIS Presentation 
(Re)mote (Di)ctionary (S)erver
key value sotore DB. 
keys are string 
final values are also string 
hashes, sets, strings, lists, bitmaps can be stored 
Features: Persistence, replication, clustering, lua scripting. 
Memory oriented
single threaded

##KAFKA & Distriubted Stream Processing 

distributed
fault tolerant
messaging system
high throughput 
publish subscribe 
ZooKeeper is required to run KAFKA
KAFKA written in Scala; keeps messages upto N days 

#Lecture 19: Mar 19, 2015

##Memcache Presentation

distribued memory object caching system
used to speed dynamic web 
low complexity, simple clustering, 
unbalanced clusters
Memcache vs Memcached

#Lecture 20: Mar 31, 2015

##ApacheHBase
open source distributed column oriented database 
built on hadoop file system
similar to google's big table 
data stored in tables 
multiple column families
no transactions
uses zookeeper
horizontally scalable 
java API client

#Lecture 21: Apr 02, 2015

##Cassanrda
scaled nosql
no single point of failure
elastic stability 
fast linear scale performance 
always in architecture 
flexible data storage 
operational simplicity
trancational support 
availability 
data partitioning done by - ordered or random
replication is done to tolerate fault 
used by netflix, ebay, twitter

#Lecture 22: Apr 07, 2015

##Javascript Closures and Design Pattern
scopes - where to look for things, uses functions
prototypes
closure
this - run time 
javascript is compiled, V8 is compiled
angular services, modular pattern, JS does not have private data 
class vs. prototype
JS uses prototype inheritance 
prototype uses delegation 

#Lecture 23: Apr 09, 2015

##Hadoop 
The Apache Hadoop software library is a framework that allows for the distributed processing of large data sets across clusters of computers using simple programming models. It is designed to scale up from single servers to thousands of machines, each offering local computation and storage. Rather than rely on hardware to deliver high-availability, the library itself is designed to detect and handle failures at the application layer, so delivering a highly-available service on top of a cluster of computers, each of which may be prone to failures. 

##Spark
Spark runs on Hadoop, Mesos, standalone, or in the cloud. It can access diverse data sources including HDFS, Cassandra, HBase, S3. Spark offers over 80 high-level operators that make it easy to build parallel apps. And you can use it interactively from the Scala and Python shells. Spark has an advanced DAG execution engine that supports cyclic data flow and in-memory computing. 

#Lecture 24: Apr 14, 2015

##React
open source
by facebook 
javascript library
subdivides UI into small chunks
maintains virtual DOM
mix and match components with HTML
one way state binding
JSX: JS with HTML

##Sinatra 
micro web environment 
rapid development 
no MVC
no default ORM
encapsulation
used in REST
route: matching pattern btw HTTP and URL- can include wildcard parameters, query parameters, 
use of static files 
filters, helpers, testing, error handling, custom matches, 

#Lecture 25: Apr 16, 2015

##Capristano 
Capistrano is written in Ruby, but it can easily be used to deploy any language.
If your language or framework has special deployment requirements, Capistrano can easily be extended to support them.
It supports the scripting and execution of arbitrary tasks, and includes a set of sane-default deployment workflows. Capistrano is also very scriptable, and can be integrated with any other Ruby software to form part of a larger tool.

##Docker
Docker is an open platform for developers and sysadmins to build, ship, and run distributed applications. Consisting of Docker Engine, a portable, lightweight runtime and packaging tool, and Docker Hub, a cloud service for sharing applications and automating workflows, Docker enables apps to be quickly assembled from components and eliminates the friction between development, QA, and production environments. As a result, IT can ship faster and run the same app, unchanged, on laptops, data center VMs, and any cloud. 


#Lecture 26: Apr 21, 2015

##Turf
GeoJson + turf = imformation
GeoJson + turf+ mapping = infographics 
geoJSON: points, line, collections, polygons, features, multipoint
geojson.oi is a graphing map site
use cases
tips and tricks 

##Flask
Flask is a microframework for Python based on Werkzeug, Jinja 2 and good intentions.
built in developmetn system
integrated unit testing support
restful dipatching
support for secure cookies
unicode based
properly documented

#Lecture 27: Apr 23, 2015

##D3
D3.js is a JavaScript library for manipulating documents based on data. D3 helps you bring data to life using HTML, SVG, and CSS. D3’s emphasis on web standards gives you the full capabilities of modern browsers without tying yourself to a proprietary framework, combining powerful visualization components and a data-driven approach to DOM manipulation. 

##Leaflet 
Leaflet is a modern open-source JavaScript library for mobile-friendly interactive maps. Leaflet is designed with simplicity, performance and usability in mind. It works efficiently across all major desktop and mobile platforms out of the box, taking advantage of HTML5 and CSS3 on modern browsers while still being accessible on older ones.




