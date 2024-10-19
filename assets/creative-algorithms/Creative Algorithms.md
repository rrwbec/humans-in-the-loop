This document describes the essential characteristics of a flexible and creative reasoning system. It is limited to the bare minimum to convey the concepts, and many details have been omitted.

It may be that this architecture is of a class that requires care and governance. This being the case it should be noted that inherent in the design is a high level of transparency that is unusual in software and this will hopefully facilitate the creation of procedures and policy should this be necessary.
# Preamble
## Simple Reasoning Scenario

In the interests of brevity, this document covers a reasoning scenario that does not include interaction with / learning about the environment, though these processes could easily be described in similar terms. This scenario is analogous to an adult human closing their eyes and trying to work out the answer to a problem in their head.

## The System
#### Model of Reality

The system has a learned model of some reality that is made of states and state changes. This reality could be our own or something else (e.g. some part of mathematics, Minecraft, ARC puzzles etc).

These states of reality may transition to another state via certain valid transitions, e.g.

A -> X -> R

The system also has its own mental states that change as it reasons about other states. It can reason about the external reality states or its own internal states (which may recursively include other states including reality states - this part will hopefully become clearer in the example)

The system has (pre-loaded) experience of reality state transitions so has built up a model of which transitions are valid and which are not. As with a human's understanding of the world, this model will be vague, incomplete and sometimes wrong. 

It will also have experience of its mental state transitions. These will not be *valid* or *invalid*, but rather *good* (do this again) or *bad* (don't think down that path again). There needs to be some distinction (to the system itself) between reality states, speculative reality states, and mental states in this regard.

#### Preferences

The system will have a set of preferences (reactions, feelings, emotions, valences etc). Precisely what these are will require further work, however for the purposes of this illustration these might include (but not be limited to)...

* Curiosity
* Doubt
* Some states are to be avoided
* Some states are to be sought
* Coherence desire (a desire to fill in the gaps between states with valid state transitions)
* Dislike of wasted effort

There is much to say on this topic, but this is out of scope of this description.

# Interpolation

Given a pair of start and end speculative reality states, the system will be motivated by coherence desire to try and fill in the gaps. It will have past experience of this process and will use these experiences as building blocks.   Some of its basic capabilities include...

**Prediction**: guessing what comes next 
**Interpolation**: filling in the gaps
**Attention/Focus**: highlight a subset of the state to allow both problem sub-division and also targeted credit assignment.
**Coherence detection**: deciding whether a transition is valid.
**Resolution zoom**: zoom in to view a state transition in more detail (what are the sub-steps), or zoom out to view the higher level steps.
##### Operations
At a lower level these work using a subject data type and several (non-trivial) operations
**Subject Data Type**
* Subject of attention/focus - i.e. a state or state sequence.
* Context - the surrounding states.
* Feeling - the current feeling based on recent preference judgements.
**Operations**
* A pattern-matching / associative lookup - the input will be the subject of attention, the wider context and the current feeling.
* A generative instantiation of the returned pattern in the the current state instance.
* Assessment - getting the opinion of the system about the current subject.
#### Example

The purpose of this diagram is to illustrate the essential capabilities only. 

![[fig-creative-algorithms.png]]


![[fig-creative-algorithms-example-1-1.png]]


![[fig-creative-algorithms-example-1-2.png]]
## Creation

A different reasoning pattern is when there is no end point specified. Instead there is a more general instruction create some output based on some conditions and the system's preferences.
#### Example

This example uses the same mechanism as interpolation, but has been illustrated at a higher level of detail. It is assumed that there is some way to pass in a request for what is to be built.

In this example the system already has an ability to build structures in some reality state by adding squares adjacent to other squares. It is given a strong preference for symmetry and instructed to build structures in speculative reality.

![[fig-creative-algorithms-building-example-1.png]]
![[fig-creative-algorithms-building-example-2.png]]
## Comments
### Capabilities

**Compositionality**
* This system will be able to create valid routes between states that it has not seen before by constructing the new route from existing knowledge.
* Routes are composed from similar smaller parts. This has the following benefits...
	* Smaller chunks have greater re-use which...
		* Makes lookup much easier.
		* Saves storage space.
		* Is more flexible.
	* It is still possible to store larger chunks if they have value.
	* Focus is useful for
		* breaking up the task into small pieces.
		* credit assignment.
		* sifting out irrelevant details, especially in the reality state.

**Creativity and Orderliness**
* If some relevant sense of interestingness can be established, then the routes should have a genuine creative dimension that is beyond derivative combination.
* The dislike of wasted effort will shift the reasoning knowledge to more efficient / low entropy algorithms. One lens on this might be that this opinion acts like Maxwell's Demon in the selection of reasoning knowledge

**Safety Benefits**
* Thinking process is highly transparent and lends itself to auditing and tracing.
* Vary large overlap between ability to process knowledge of both reality and reasoning.
* Easily distributed between machines (see note on human language).
* Potential for agency to be limited to the system's internal reality - see SID below.
* 

**Safety Problems**
* Human mismanagement (not sure where writing this document fits into that story)
	* May prove too easy to implement
	* Relatively understandable, so many people may try
* Other - see internet

**Miscellaneous**
* Thoughts include concrete values...
	* This allows intermediate results to be stored
	* Experience may keep or discard these values
#### Participation

The transparency of this system should facilitate greater participation in its design and use compared to current LLMs and related systems. For systems that might interact with the human world in some way
#### Technical Challenges

Challenges include, but are by no means limited to...
* Associative lookup 
* Generative merge into a state
* Decay of unused experience and emergence of abstractions

General Points of Interest
* Episodic history can be moved to more optimum knowledge stores via some variant of sleep
* 

### The Generally Intelligent Daydreamer (GID)

An example deployment might be a distributed set of reasoning machines that have been given a reality model and are motivated to continuously build novel and coherent state paths in reality whilst improving their own reasoning knowledge. The concept of interestingness would be very useful here if it could be developed - this might emerge from the correct set of reality values.

Reality stories that have high uncertainty can be queried externally and used to gather new data for the SID. The machine has no *direct* motivation to independently gather such data and care would be needed to ensure that no indirect motivation arises or is embedded in imported real-world data.
### Note on Human Language

One can imagine that the resolution of human metacognition reached some threshold at which this type of plan construction and also language construction became possible. Furthermore, with language it becomes possible to distribute this process within a human group and so increase rate of improvement of plan building skills by some orders of magnitude.


ToDo

Possible todos include
* Examples that include
	* More nesting / metacognition
	* Choices
	* Values in reality
* Further illustrate the contents of experience
* More on governance
* 

