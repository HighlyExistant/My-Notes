# Automated Planning
Goal oriented action planning is derives itself from this technique. Here we have two things we keep in mind:
## Facts / Predicates
These are small pieces of information which are true at a given time, which is stored in a ==**state**==.
### Example
1. Given an object *door*, a predicate could be the door is open or closed.
## Planning Action
When we plan an action we need to know a few details:
1. ==**Objects**==: The Items with which the action is involved with
2. ==**Preconditions**==: Facts that must be true for the action to work
3. ==**Effects**==: How the facts in the state change when the action is complete.
# Barebones GOAP
The way GOAP is supposed to work is that  you are given a goal, which is simply a set of conditions that you are looking to satisfy, and to satisfy those conditions, you will search for the ==**effects**== of actions. Every action has a precondition, so you will search for actions which satisfy those preconditions, until you finally reach a series of actions which will satisfy the ultimate goal. The hard part comes from when plans need to be reevaluated, etc.
## Planner
The planner is carried by each individual A.I, and contains the set of actions which can be performed by that particular A.I. Given a [[Blackboard|blackboard]] containing the worlds global state, and a goal saying the desired state, you will generate an array of actions to be performed sequentially to achieve the state. If at any given time, the plans preconditions are affected, then you should scrap the plan.
# References
1. [This video](https://www.youtube.com/watch?v=PaOLBOuyswI) by AI and Games