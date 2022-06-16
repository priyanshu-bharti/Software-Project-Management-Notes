# Software Project Manangement

## Module 3 : Activity Planning

- [ ] Scheduling projects
- [ ] Activity vs product based approach for scheduling
- [ ] Hybrid approach for scheduling projects
- [ ] Precedence Diagramming Method
- [ ] Network Planning Models : Forward and Backward Pass

## Scheduling projects

- Listing of milestones, activities and deliverables.
- Dependencies and allocated resources are defined for each task.
- Deadlines, resources, and completion dates are decided.
- Sometimes also describes the ordering of the tasks to be performed.
- Helps identify issues early.
- Identify what person has what role.
- Effective business management and risk mitigation.

### Activity

- Must have clear start and end dates.
- Requirements and duration must be forcasted earlier.
- It should depend on other activities to be completed first.

### Activity Networks

- Assumes that project consists of many activities.
- Help assess feasibility of project's completion date.
- Identify when a resource would need to be allocated.
- Calculate when cost will be incurred.
- Establish Coordination between team members.

## Work vs Product based approach for identification of tasks.

### Activity based approach

- Create a list of all the activities in the project.
- Usually done while brainstorming with the team and analyzing past projects.
- Creates a tree like structure for activities involved.
- It follows top-down approach.
- Root is labelled by the project name itself.
- Each node (activity) is recursively decomposed and divided into smaller sub-activities.
- At leaf node non-decomposable activites are kept.
- These are carried out by the dev team for couple of weeks.

**Levels of Activity Breakdown Structure**

1. Project : Main Objective to achieve.
2. Deliverables : Subproducts generated after each milestone.
3. Components : Key items for making deliverables.
4. Work-Packages : Collection of tasks to make a component.
5. Tasks : Assigned to single team or member.

### Product Based Approach

- Consists of Product Breakdown Structure (PBS) and a Product Flow Diagram.
- Similar to the Activity based approach.
- The PBS is constructed prior to the Activity based approach.
- Focuses on generating list of all sub products required to complete the project.
- This helps in the creation of the Activity based approach which identifies activites to create sub-products.

### Hybrid approach

- Alternative work breakdown structure is constructed based on:
  - A simple list of final deliverable.
  - For each deliverable, a set of activities required to produce that product.
- Hybrid approach gives us a modified version of the Activity approach.
- It includes some of the important properties of the PBS.

## Precedence Diagramming Method

- Visual representation techinque for scheduling activities.
- Used to make network diagram for activities and determining critical path.
- Depicts activity relationships.

## Network Planning Models : Forward and Backward Pass

- Model the activities and their relationships as a network
- Time flows from the left to the right.
- Two most common models are :
  1. CPM (Critical Path Method)
  2. PERT (Program Evaluation Review Technique).
- Previously they used to be represented using arrow diagrams
- Recently precedence networks using nodes have become popular.
- Precedence network should have only one start and end node.
- Nodes should have some duration while links connecting them don't.
- PDM shouldn't have any loops or dangling nodes.

### PERT

- We would be given the following things in the question
  - Activity
  - Predecessor
  - Optimistic Time `(to)`
  - Most Likely Time `(tm)`
  - Pessimistic Time `(tp)`
- Draw the network diagram
- After making the diagram, perform forward and backward pass with only 2 values (early start and late finish)
- Based on the above values and using the following formula, we need to calculate:
  - **Mean** `(te)` = `((tp + to + 4*tm) / 6)`
  - **Variance** = `((tp - to) / 6) ^ 2`
  - **Estimated Completion time of the project** `∑te` = Sum of all the `te` in the Critical Path
  - **Probability of completion in x weeks** = `P(X ≤ 22 = ((x - ∑te) / sd))`
    - Here `X` is the probability to be calculated
    - `x` is the number of weeks in the question
    - `∑te` is the sum of all `mean` of the CP nodes.
    - `sd` is the root of `variance`

### CPM

- We would be given the following things in the question
  - Activity
  - Predecessor
  - Duration
- Then make the network diagram
- After making the network diagram, perform forward and backward pass with 6 values (early start, early end, name, duration late start and late end).
- Determine the Critical Path
- **Calculate slack** = `Latest start time` - `Earliest start time`

### Difference between PERT and CPM

| PERT                              | CPM                                 |
| --------------------------------- | ----------------------------------- |
| PERT manages uncertain activities | CPM manages well-defined activities |
| Plan and controls time            | Control cost and time               |
| Event Based                       | Activity Based                      |
| Probabilistic Model               | Determistic Model                   |
| 3 Time estimates                  | 1 Time Estimate                     |