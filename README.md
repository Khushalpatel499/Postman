# Postman

1. It basically send request from client to server via network, it is used to test api's.
2. there are two way to use postman first one is dowloading from site, for temperory postman chrome extension.
3. API:(Application programming interface) is a set of protocols that enable different software components to communicate and transfer data.
4. reqres is a website to get test api's.
5. before there are only monolithic architecture (all ui,business logic,data access are in one layer)but now it is microservices architecture.
6. now the big functionality are divided into small parts and now they communicate with each other throgh api's .
7. API is a software interface that allows computers or programs to communicate with each other.
8. there are different api's and different protcols and generally used protocol is rest and soap.
9. cost of testing: manual tests> ui test> API(business and functional tests)> unit /component test.
10. API is basically a collection of functions and procedures which allows us to communicate two application or libraries.

# Types of API

1. we are going to learn REST API,we are only see about web API
2. Respresentational State Transfer(REST),Simple Object Access Protocol(SOAP),Remote Procedure Call(RPC)

# REST API

1. The rest architectural style describes six constraints(rules).
2. it is basically a design Pattern for Web API.
3. Rest Constraints: Uniform interface,stateless,cacheable,client-server,layered System,code on demand.
4. twitter,linkedin use rest api, facebook or meta shift to graphQl, microsoft service use soap ui.
5. type of testing: functional testing,Integration testing, Regression Testing,Load Testing,Penetration Testing,Fuzz testing
6. soap is a protocol (set of rules), Rest(archtectural style(design pattern)).
7. Soap use XML while rest use plain,html,xml,json data format .
8. Soap require more resources and bandwidth , rest requries fewer resources and is lightweight.
9. Soap cannot be cached while rest can be cached.
10. in simple soap is like an envelope while rest is like post card.

# Http Fundamental

(hyper text transfer protocol)

1. http send request to server and get response from server.
2. http status code : 200- everythink is good
   201- new created
   301- redirection
   400- client errors
   500- server errors
   102- Proccessing
   202- accepted
   504- gateway timeout
   400- not Found
3. http provide some method so that client and server can talk with each other.
4. http method Request has body response has body
   GET(take information) optional Yes
   Post(create a file on server) Yes Yes
   put(to update all content) Yes Yes
   patch(to update limited content) Yes Yes
   delete(to delete that file) No Yes
5. ALL this are CRUD operation.

# Postman Basic

1. Workspace: it is a shared space for organizing and collaborating on API projects.
2. Collection: a group of API requests that can be organized,shared, and reused.
3. Json: javascript object notation it is basically key value pair,it a syntax for storing and exchanging data.
4. https://reqres.in/api/users/2
   https: it is a method http and s means secured
   reqres.in is a base url and in api folder ,in users give 2
5. / means path para means find folder inside folder
   ? means query para means send some extra parameters to server ,it send by client to get that information

6. Authorization: postman support many authorization, means currently we are accessing public api using it's base url but facebook can't give access,it take authorization from us,if we are authorization then it will give data
7. in companies maximum time there is authorization in companies and that are basic auth mean it will send username and password in base 64,means the api response only when the client know the username and password.
8. when we send user name and password and see in header it will have authorization key with value basic= a string and this string is base 64 and we convert this base 64 string using decode it give the username and password
9. Header: header is nothing but meta data or client information
10. now we created request our self but we want to get from chrome in network copy as curl(bash) and in postman import raw text and paste
11. cookies: it is basically stord information like when we add anything in cart and come back it show which is because of cokkies, when we exist the website it store the cookie inside to know preference for next time.
12. now we use post request and create a user so we need to send a body then raw and then json
13. some time we have to put cookies, it is for the domain with key value pair.
14. monitor collection: to run at a sedule time and create a monitor and run every sedule time.
15. collection runner:it run the collection and generate html report.
16. Digest authorization- user ,Pass with encryption
17. Bearer Tokens- They are predominant type of access token used with OAuth 2.0 means if we are login in any website and it tell that we can singup with google means if you are valid user of google then you can sign here so google provide a auth for website ,google give a token to website and if it is valid then it will sign it.
18. to set variable as url select the url and the opiton come on the that set as variable and to see where this variable is set go to the collection and see the variable.
19. when we try to send book on the server it give 401 error means authorized error becuase we don't allowed everyone to send book on our server.
20. Think about why you might not want an API to have completely open endpoints that anyone can access publicly. It would allow unauthorized people to access data they shouldn't see, or allow bots to flood an API with thousands of calls per second and shut it down.
21. There are multiple methods for authorizing a request. Some examples are Basic Auth (username and password), OAuth (delegated authorization), and API Keys (secret strings registered to a developer from an API portal).
22. we are use api key basic in header to add with key value but it is difficult to add header for every request so postman give the auth help which add apikey in collection.
23. Postman has a helper object named pm that gives you access to data about your Postman environment, requests, responses, variables and testing utilities.
24. For example, you can access the JSON response body from an API with:
    pm.response.json()
    You can also programmatically get collection variables like the value of baseUrl with:
    pm.collectionVariables.get(“baseUrl”)
25. earlier to getBook we write id manually but we can write as varible by like script get id id and set the variable id it create a varible in collection and we can use it anywhere in collection.
26. now we see how to test it so we first share the collection by api key and generate url.then go to test collection and add varible.
