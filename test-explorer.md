# Scaffolding/Testing Idea #

*IDEA*: Use ALPS to drive a scaffolding/testing harness. 

Utility woukld consume an ALPS document and then generate (random?) responses with sample data (from where?) based on the
semantic descriptors in the ALPS document.  The responses would also include (random?) affordances from the ALPS
document including arguments for templates. 

## Testing Clients ##
Client apps could run against the scaffold to make sure they can handle the responses (including templates). Since
ALPS allows definition documents that don't constrain the arguments for an affordance, clients would only go "green"
if they handled this case properly. Client would also need to be prepared for unknown fields in responses (including
templates) and not break. Client apps would need to return unknown form arguments untouched, too.

This get very close to the way a hypermedia client SHOULD behave. 

## Testing Servers ##
Reverse this for testing servers, the utility will generate (random?) requests to the server including varying the 
arguments for forms, etc. This gets harder since servers are _allowed_ to reject, ignore things. In fact, now we
are testing that the server _does_ ignore the right things

## Challenges ##
 * Can we write a test harness that can generate random requests/responses?
 * Does this kind of testing really help (for hypermedia, i think yes, but...)?
 * ALPS contains no data quality/type info, is that a big problem? 
 * ALPS contains no input validation/constraints, problem (e.g. what are we testing here?)?
 * ALPS has no workflow info, either. what about status/state issues for testing? (e.g. server is in X state, Y is not a valid transition, etc.)?
 * ALPS doesn't specify media types. how do we handle that in the tool?
 
There may need to be some collection of config/mapping of the missing info (data quality/validation, workflow, media-type)
that is used to _add_ to the ALPS document in order to create useful tests.

## Explorer ##
TK

