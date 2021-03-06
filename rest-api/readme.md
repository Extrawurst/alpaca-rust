## rest-api
Welcome. `#[api]` allows you to create a rest-api by simply annotating a trait.
Currently the rest calls are executed using the [request](https://crates.io/crates/reqwest) crate.
Don't expect much to work yet.

## goals
Support as many flavours and special cases out there in different Rest APIs with as little as possible effort.

## why all this magic?

* Modularity: Having an API simply implement a Trait allows to swap out the remote API against some internal one easily.
* Focus: Because working against an API should not distract from what you actually want to do *with* that API.
* Stability: Hand written API bindings are harder to maintain and easier to introduce bugs
* Testability: It also simplifies writing your application in a test driven approach. Simply use `#[mock]`([see mock crate](https://github.com/carlosdp/mock_derive)) and run against a mocked API

## why not just swagger?

* good point, also a good choice, but then you have to involve yet another tool in your pipeline
* rest-api allows you to stay in the rust eco-chamber
* rest-api is more lightweight and faster to prototype

## todo

- [x] proof of concept
- [x] support url parameters
- [ ] support query parameters
- [ ] future support, or more backends in general
- [ ] string results
- [ ] support post using json
- [ ] allow serializable types in api
- [ ] define base url in attribute