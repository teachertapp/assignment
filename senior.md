# HTTP Microservice
#### Golang, Typescript, Rust, Modern C++

This project is to create an in-memory microservice to manage a single entity via a REST API. 

This service will manage a list of School objects. A School looks like this: `{ "id": 1, "name": "Ewell Castle School" }`

### API Specification

The REST API should support the following operations:

|method|url|description|
|------|---|-----------|
|POST   |    /schools     |  Create a new school from a JSON Body |
|PUT    |    /schools/:id |  Update a school with a given integer ID |
|DELETE |    /schools/:id |  Delete a school with a given integer ID |
|GET    |    /schools/:id |  Fetch a school with a given integer ID |
|GET    |    /schools     |  Return the full list of schools |

If a School cannot be found then the API should return a status code of `404`.

The server should return a status code of `500` if it encounters an error.

### Implementation

This service can be implemented using libraries.  

We recommend to layer up the implementation in phases:
- A Server to manage the incoming client sockets
- Request, Response and a Router
- Routes and Data Access

### Delivery

Send us a link to to the completed assignment on your Github. 

Supply a README on how to compile and run the project. 

### What we're looking for

For grading, we’ll be: 
- Testing if the service meets the given spec with [Postman](https://www.postman.com/)
- Measuring the performance with [wrk](https://github.com/wg/wrk)
- Looking at code readability and consistent use of syntax
- Looking for effective use of unit tests
- Reading the documentation

We'd expect the performance of GET /schools/1 to be in the order of 5k requests per second on a single core.

### Extra Notes & Tips

We welcome the use of GitHub Copilot and any other internet resources. 

Nouns: Server, Request, Response, Router, Route, Repo, School

Frameworks & Tools: [CMake](https://cmake.org/), [vcpkg](https://vcpkg.io), [GTest](https://github.com/google/googletest), [nlohmann-json](https://github.com/nlohmann/json), [fmt](https://fmt.dev/), [spdlog](https://github.com/gabime/spdlog), [wrk](https://github.com/wg/wrk)

Every senior member of our team has completed this project. We'll be eagerly awaiting your submission and look forward to discussing it further with you!