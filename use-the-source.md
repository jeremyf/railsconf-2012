# Use the Source, Luke: High Fidelity History with Event-Sourced Data
by Keith Gaddis

## Presentation

Event Sourcing captures all changes to application state as a sequence of events.

Events are serialized and stored, allowing playback of events later to recreate application state.

Events as history of data…version control of your data…recreate application state at any point.

### Benefits
* ES is never (rarely?) having to say "I'm Sorry"
* Bugs: fix a bug, replay events, database is fixed
* Heavy/complex analytics on data
	- Some reports can not easily be generated off of normalized data
* Future requirements or changes in modeling
* ES pushes non-domain logic out of the domain models (YOU SHOULD DO THIS ANYWAY)
* System decoupling

### Drawbacks
* Forces you to really analyze/know your problem
* Early in product development domain may be unclear
* Agility tradeoff
* Performance large event logs (thousands, millions of events in some domains)
	- *Response: Store snapshot of domain models*
	- ActiveModel serialization is great for this

### Common Use Cases
* Source control
* Financial/accounting – you cannot screw up
* Complex domains
* Distributed systems, service oriented architecture

Database can't generate IDs for you.  You have to generate them.

Events were listed as objects; There is a command that applies event.

def apply_event(event)
	REDIS.rpush "order-#{self.order_id}-events", YAML.dump(event)
	
	#run event
	#don't change history; applying the event should be simple
end

### gem install replay
Facilitates event-sourcing
Handles the event storage and application
Allows other models to listen to events on the domain
Useful alone or as part of a CQRS architecture

Listeners are for non-domain processors

### DCI - Data Context Interaction

Separates domain models (data) from use-cases (context) and role (interaction)

Roles are modules that define actions/commands

Separate domain behavior from domain data

Mix in or compose roles into objects (models) in the associated context

### CQRS

CQS: Command Query Separation
Methods should be commands (mutate state) or queries

Command Query Responsibility Segregation – carries CQS to a system architecture

Domain models for Application state

"Read models" for system queries, such as reporting

Commands (typically objects) used to change system

Commands generate events, which mutate state and can be syndicated to distributed systems

Don't worry how events were applied, just make sure that the events are "raised"; tests don't get coupled to behavior

### More Info

* http://martinfowler.com/eaaDev/EventSourcing.html
* http://dddcqrs.com
* Domain Driven Design by Eric Evans
* http://karmajunkie.com

## Takeaway
This is a must read set of slides as well as a concept to pursue.