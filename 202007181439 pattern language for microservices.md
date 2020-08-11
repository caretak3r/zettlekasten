# pattern language for microservices

- **tags**: #microservices #patterns #architecture
- **sources**: 
	- https://microservices.io/patterns/index.html
---

![](https://microservices.io/i/MicroservicePatternLanguage.jpg)

- problem
	- _how to decompose an application (monolithic in nature) into services?_

- concepts
	- [[Common Closure Principle]] (CCP) - classes that change for the same reason should be in the same package
	- [[Single Responsibility Principle]] (SRP) - a responsibility of a class as a reason to change, and states that a class should only have one reason to change
	- [[Domain-Driven Design]] (DDD) - referring to an application's problem space - the business - as the domain, consisting of subdomains (different parts of the business)


- forces at play
	- architecture must be stable
	- services should be cohesive, by implementing a small set of strongly related functions
	- services must conform to the [[Common Closure Principle]]
		- _things that change together, should be packed together_ and we apply this to microservice concepts!
		- limits the [[blast radius]] to the respective service/functions only
	- services must be [[loosely coupled]]
		- where an API encapsulates it's implementation, and be changed without affecting end users
	- services must be testable by autonomous teams, where they can develop and deploy services with minimal collaborations with other teams

- decompose by business capabilities
	- defines services in respect to business capabilities
		- _whatever a business does to generate value_
			- _Traffic Management_ is responsible for orders
			- _Customer Management_ is responsible for customers and support
			- _Infrastructure Management_ is responsible for infrastructure components that keep a business in service

- decompose by [[subdomain]]
	- defines services in respect to business application components
		- core - key differentiator for the business and the most valuable part of the application
		- supporting - related to what the business does but not a differentiator. These can be implemented in-house or outsourced.
		- generic - not specific to the business and are ideally implemented using off the shelf software

![](https://microservices.io/i/decompose-by-subdomain.png)