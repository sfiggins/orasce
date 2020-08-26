# 3. Use http router

Date: 2020-08-25

## Status

Accepted

## Context

Routing of REST calls to functions and handling of message bodies can be done with net/http in Go, but using a framework will provide common utility functions and make the structure of the application clearer, allowing me to focus more on logic, and less on the language.

There are several options. I want to use one that is simple, popular, and well documented both by its creators and commonly used by others in tutorials. The simplest and most popular routers are either gorilla/mux or go-chi. A looks at google hits shows that there are more references to gorilla mux than go-chi. Both are compatible with net/http. Both aim for simplicity. Looking at more recent posts and tutorials, go-chi seems to be gaining in popularity.

## Decision

Use go-chi as our http router

Influences on that decision included Bruno Scheufler's [Choosing the right go web framework](https://brunoscheufler.com/blog/2019-04-26-choosing-the-right-go-web-framework) and Emir Ribic's [Writing RESTful APIs in Go, 3 years later](https://www.ribice.ba/rest-api-go3/). If I have time, I might try using Ribic's go-chi middleware wrapping solution zerolog logging.

## Consequences

Simplified routing and handling of responses. Support for middleware that could be used to improve logging.
