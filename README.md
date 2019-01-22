# REST API Terminology 

Fork and clone this repository. Then, push to github with all bad answers deleted and only the correct answers showing.

**1. What does it mean REST?**
transferencia de representación de estado
Representational State Transfer

**2. Who coined the REST term?**
Es una tesis doctoral sobre la web escrita por Roy Fielding,


**3. In which protocol REST is based?**
Protocolo HTTP


**4. What are the main building blocks of a REST Architecture?**
Resources (URI, which goes after the slash in the endpoint of an API),
Representations
Messages
Hipermedia

Un servicio web (en inglés, web service o web services) es una tecnología que utiliza un conjunto de protocolos y estándares que sirven para intercambiar datos entre aplicaciones.

REST Web Services
REST (Representational State Transfer), es un estilo de arquitectura de software dirigido a sistemas hipermedias distribuidos como lo es la web. Este término se refiere específicamente a una colección de principios para el diseño de arquitecturas en red.

SOAP Web Services
Ahora que conocemos mejor qué es REST, llega el momento de presentar los SOAP (Simple Object Access Protocol) services. Se trata de un protocolo para el intercambio de mensajes sobre redes de computadoras, generalmente usando HTTP. Este protocolo está basado en XML, facilitando la lectura, aunque los mensajes resultan más largos y por lo tanto considerablemente más lentos de transferir.


**5. Identifying a resource is easy; you know how to access it and you even know how to request for a specific format. Since REST is using HTTP protocol as a standing point, there are some actions related to resources: CRUD operations.**

Complete the below table:+


|HTTP Verb|Proposed Action|
|---------|----------------------------------------------------------------------|
|GET      |**read** (or retrieve) a representation of a resource.                |
|POST     |**create** new resources.                                             |
|PUT      |**update** resources                                                  |
|DELETE   |**delete** a resource identified by a URI.                            |


6. Status Code

**6. Status Code**

Another interesting standard that REST can benefit from when based on HTTP is the usage of HTTP status codes.

+ What’s is a status code?
son códigos de respuesta estándar dados por los servidores de sitios web en Internet.
Are standard response codes given by web site servers on the internet.


+ Explain with your own words, the meaning of next codes:

|Status Code|Description                                                          |
|-----------|---------------------------------------------------------------------|
|404        | Es un error que nos indica que la página no se existe en el servidor|
|200        | Nos indica que la petición asido exitosa                            |
|500        | Error del lado del servidor Internal Server Error                   |


**7. Status Code are grouped in five sets.**

Write what are their meaning.

|Group|Description                                                                     |
|-----|--------------------------------------------------------------------------------|
|1XX  |(Informational): The request was received, continuing process                   |
|2XX  |(Successful): The request was successfully received, understood, and accepted   |
|3XX  |(Redirection): Further action needs to be taken in order to complete the request|
|4XX  |(Client Error): The request contains bad syntax or cannot be fulfilled          |
|5XX  |(Server Error): The server failed to fulfill an apparently valid request        |

8. HTTP Status Codes and Their Related Interpretation

**8. HTTP Status Codes and Their Related Interpretation**

There are the most common status codes in HTTP responses. Please, fill with the required description.

|Status Code| Meaning              |
|-----------|----------------------|
|200        | Ok                   | 
|201        | Created              |
|204        | No Content           |  			
|301        | Moved Permanently    |
|400        | Bad Request          |
|401        | Unauthorized         |
|403        | Forbidden            |
|404        | Not Found            |
|405        | Method Not Allowed   |
|500        | Internal Server Error| 



To see the full list of HTTP status codes and their meaning, please refer to the RFC of HTTP 1.1


 
###### [To see the full list of HTTP status codes and their meaning, please refer to the RFC of HTTP 1.1](http://tools.ietf.org/html/rfc7231#section-6)

**9. How are called the points of contact between all client apps and the API?**
endpoints


**10. The following is a good example or bad example of a named access point? And why?**

_meant to list the books in a bookstore_

+ `GET /books/action1`

Esta Mal, porque no sabemos que es la action1 hay que ser descriptivo 

**11. Uniform Interface**

To solve this problem, you can apply the REST style to the endpoints, and thanks to HTTP, you also have verbs to indicate actions.

Mencionar el recurso en una cnonvención
: paragram

|Old Style                 |       REST Style           |
|--------------------------|----------------------------|
|`/getAllBooks`            | GET /Books                 |
|`/submitNewBook`          | POST /Books                |
|`/updateAuthor`           | PUT /Authors:id            |
|`/getBooksAuthors`        | GET /Books/:id/Authors     |
|`/getNumberOfBooksOnStock`| GET /Books                 |
|`/addNewImageToBook`      | POST /Books/:id/Cover      |
|`/getBooksImages`         | GET /Books/:id/Cover       |
|`/addCoverImage`          | POST /Books/:id/Cover      |
|`/listBookCovers`         | GET /Books/:id             |

Old Style	REST Style



**12. What JSON does it mean?**
JSON (Javascript Object Notation)

**13. Anatomy of a `REQUEST`**

Make a `curl` request to _GitHub API_
Es una solicitud para obtener informacion de una API 

aceder una URL  

```sh
$ curl  GET -X https://api.github.com 
```

According to the responded request, answer what does it mean the next parts from the handler:

+ _`Content-Type`_. Tipo de Media
+ _`Status`_. Status Code
+ _`Date`_. Contiene la fecha y hora en la que genera un mensaje
+ _`Content-Length`_. Indica el tamaño de bytes.


If response is not showing those parts, ask to google how to print them in console.
curl -i GET https://api.github.com


###### If response is not showing those parts, ask to google how to print them in console.

```sh
# curl  GET https://www.google.com.mx/ --head
```
