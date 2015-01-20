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







