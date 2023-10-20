# *Course 301, Entry 8: APIs*

## REST

>What does REST stand for?

Representational State Transfer.

>REST APIs are designed around a ____.

Resources.

>What is an identifier of a resource? Give an example.

An identifier, unique resource identifier (URI). For example: `adventure-works.com/orders/1`.

>What are the most common HTTP verbs?

GET - Retrieves representation of resource.

POST - Creates a new resource. Or data submit for processing.

PUT - Either creates or replaces resource. Idepotent.

PATCH - Partially updates a resource.

DELETE - Removes a resource.

>What should the URIs be based on?
Give an example of a good URI.

URIs should be based on nouns, not verbs. For example: `https://adventure-works.com/orders` or `https://adventure-works.com/customers`.

>What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

A chatty web API is a web API that results in unnecessary data transfers, which is bad. To avoid this, logically by grouping related resources. For example, if there were to be a pull for product images, pull a grouped set, rather than one at a time.

>What status code does a successful `GET` request return?

A successful get request will return a 200 (OK) code. When there is no content to the response and a 204 (No Content) code will be received instead.

>What status code does an unsuccessful `GET` request return?

An unsuccessful request returns a 404 (Not Found) code.

>What status code does a successful `POST` request return?

A successful POST results in 201 (Created) code.

>What status code does a successful `DELETE` request return?

A successful DELETE results in a 204 (No Content) status code. If the DELETE request is not successful, simply because it doesn't exist, a 404 (Not Found) code will result instead.

## Things I want to know more about

I would like to understand further about HATEOAS and if it is widely being adopted. What are the advantagesa nd disadvantages?
