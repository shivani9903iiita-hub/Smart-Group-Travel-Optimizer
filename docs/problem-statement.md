# Problem Statement

## Problem

Planning a trip for a group can be difficult because different travelers may
have different interests, budgets, time constraints, transportation
preferences, and places they want to visit or avoid. Existing travel
planners often provide recommendations or collaborative planning features,
but creating an itinerary that balances the conflicting preferences and
constraints of all group members remains a challenging optimization problem.

## Motivation

The idea for this project comes from a recurring experience within our own
friend group at college. We have often tried to plan trips together, but the
plans rarely materialized — not due to lack of interest, but because each
person had different priorities, budgets, and available time, and
reconciling these manually became too difficult to coordinate. This is a
common situation among college students, who typically travel in groups but
have limited time, tighter budgets, and diverse interests compared to solo
or professional travelers.

This experience highlighted a real gap: existing travel-planning tools
assume either a single user's preferences or leave the group-coordination
problem to manual discussion. A system that can take everyone's constraints
as input and automatically produce a workable, balanced itinerary would
directly solve a problem we — and students like us — face in practice.

## Proposed Solution

The Smart Group Travel Optimizer aims to develop a system that generates an
optimized travel itinerary for a group by considering individual traveler
preferences, budget, available time, desired and avoided destinations,
destination characteristics, and travel distances. The system will evaluate
possible itineraries and select a plan that provides a good overall balance
between group satisfaction, cost, time, and travel efficiency.

## Main Objectives

1. Allow users to create a group trip.
2. Collect individual preferences and constraints.
3. Maintain structured information about destinations.
4. Generate feasible travel itineraries.
5. Optimize the itinerary according to group preferences.
6. Consider budget and time constraints.
7. Minimize unnecessary travel.
8. Allow the destination dataset to be expanded in the future.

## Expected Outcome

For Version 1, given a destination and the group's combined inputs
(individual preferences, budget, availability, must-visit/avoid lists), the
system should output **three distinct itinerary plans** for the same trip,
each optimized around a different priority:

1. **Budget-Friendly Plan** — minimizes cost and travel time, even if it
   includes places with lower overall group interest.
2. **Preference-Optimized Plan** — maximizes group satisfaction based on
   stated interests, even at a higher cost or longer duration.
3. **Balanced Plan** — a middle-ground itinerary that trades off cost, time,
   and preference to give a reasonable option across all factors.

**Example:** For a trip to Hyderabad, Golkonda Fort might be inexpensive and
quick to visit, but only a small fraction of the group is interested in
going.

- The **Budget-Friendly Plan** would include Golkonda Fort, since it keeps
  cost and time low.
- The **Preference-Optimized Plan** would likely exclude it, since few
  travelers want to go and better-rated alternatives exist for the same
  slot.
- The **Balanced Plan** would decide based on the overall trade-off between
  the two.

This gives the group real, comparable options instead of a single rigid
itinerary — letting them choose the plan that fits how they want to travel,
rather than forcing one "optimal" answer that may not suit everyone.
