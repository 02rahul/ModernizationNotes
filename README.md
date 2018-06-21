OKRs - could have, should have, potential problm area, potential starting point, Slice candidate
Event Storming - define events and categories
	Choreography - services listens for what it cares about
	Orchestration - send events to consumers
Boris - Spider diagram
	define services, ext services, queues, connect all


	SnapE - 
		Looks into one of the service/node in Boris dig
		Dig with list of API, UI, Datasource, Risks and stories for each of those
		Inform Architecture, Event Flow
		Contexts to microservice, API discovery
		Scenario Modeling, Orchestration to Choreography
		Validate Slice Candidate, Fill the Backlog


Slice Analisys

Snap Analysis - Checks characteristics of Existing system for mordernization. To help understand complexity. Risks.

Implementation Patterns
Pattern 1 Seams - api, rmi, rest, etc...
Pattern 2 ACL (Anti Corruption Layer so that new service node talks to old system so that 
	  its still functional) - Functionality
	  Teams which builds the new service is responsible for the ACL
Pattern 3 Event Shunting 
	New system without interacting to old system.
	EX: New system will listen to same queue as old system and responds in similar fashion as old system.
Pattern 4 Proxies/Facades/Adapters
	Proxies - put in middle of old system like gateway by which we gain control to route traffic to old and new system. Then eventually retire old system.
	Facade - Create a facade service 
	Ex: if old system is using RMI, create RMI facade that interacts with new system
	Adapter - When old system routes to an API like to downstream service, create a adapter to downstream service that calls new service.
Patter 5 Gateways
	Edge router, zuul, apigee
	Gateway assesses the requests from consumers, makes call to new system and old system in combination to solve the purpose of request.

	
	

