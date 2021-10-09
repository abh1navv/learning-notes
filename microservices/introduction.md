# What are microservices?

## The classic architectures
If you have read about microservices before, you must have heard the term monolithic before. I'm not going to use the term extensively here. I will also leave out talking about multiple possible ways of creating a monolith. However, I will talk about 2 popular architectures which form the basis of all monolith definitions. 

### 3-Tier Architectures

Suitable for low usage and simple functionality applications. If the size and usage of the application can be predicted to a large extent, this is the easiest architecture to start with.

**Layers** 
1. Client - Any device/software from where the application can be accessed - For e.g. a web browser.
2. Application Server - Serves the application in the format requested by the client after running some programming logic. For e.g. the web browser makes a request for a webpage by providing a URL and a server which is responsible for handling requests on the URL will return the webpage. 
3. Database Server - helps the application in interating with the data. For e.g. if the application has several known users, the data specific to each user will be saved in the database and the database server will provide a way to access it.


### N-tier Architectures

An extension of the 3-tier architecture to remove the limitations of the 3-tier architecture in terms of application size.
