# Project Research Log

## Project

Smart Group Travel Optimizer

## Purpose

This document records the research conducted during the development
of the Smart Group Travel Optimizer. It includes observations from
existing travel-planning systems, articles, technical resources,
datasets, algorithms, and other sources that influence project decisions.

---

## Research Entries

### Research 001 — Existing Travel Planning Systems

**Date:** 21 August 2026

**Research Question:**

What existing travel-planning systems are available, and what
features do they provide for individual and group travel planning?

**Systems Investigated:**

- Wanderlog
- TripIt
- Google Maps
- Mindtrip
- Route/itinerary optimization systems

**Initial Findings:**

- Wanderlog provides collaborative itinerary planning, route
  optimization, budgeting, map-based planning and an AI assistant.
- TripIt focuses on organizing travel reservations and creating
  comprehensive itineraries.
- Further research is required for Google Maps, Mindtrip and
  optimization-focused systems.

**Relevance to Our Project:**

The research will help determine whether existing systems already
solve the specific problem of generating multiple optimized
itineraries for groups with conflicting preferences, budgets,
availability and travel constraints.

**Sources:**

- [Add sources in sources.md]

**Decision/Impact:**

To be determined after completing the comparison.

### Research 002 — Wanderlog AI Assistant Behavior

**Date:** 21 August 2026

**Research Question:**

Does Wanderlog's AI assistant take multiple travelers' individual
preferences and generate multiple optimized itinerary options, or
does it work differently?

**Findings:**

Wanderlog's AI assistant is prompt-based: a single user writes one
free-text prompt describing the group (e.g. number of travelers,
ages, interests, rough budget), and the AI returns one itinerary.
There is no structured input for multiple travelers to submit
individual preferences separately, and no mechanism to reconcile
conflicting interests automatically. The AI does not generate
multiple alternative plans (e.g. budget-friendly vs.
preference-optimized) — only one itinerary per prompt, which the
user can then ask to refine conversationally (limited to 5 free
messages per trip). Budget figures are computed as an estimate
after the itinerary already exists, rather than being used as a
constraint that shapes place selection.

**Relevance to Our Project:**

This is strong evidence for our research gap: Wanderlog's AI
solves single-prompt itinerary generation, not multi-traveler
preference reconciliation or constraint-based optimization across
budget/time/preference simultaneously. It also does not produce
comparable alternative plans, which is a core feature we intend
to build.

**Sources:**

See sources.md — "Wanderlog — Independent Review (AI Feature Test)"

**Decision/Impact:**

Confirms that group-level preference optimization and
multi-plan generation remain unaddressed by Wanderlog. This
strengthens the case for our project's core differentiator.

### Research 003 — TripIt Core Functionality

**Date:** 21 August 2026

**Research Question:**

Does TripIt do any itinerary generation or preference-based
optimization, or is it purely an organizational tool?

**Findings:**

TripIt is fundamentally a logistics organizer, not a planner. It
builds itineraries from confirmation emails (forwarded manually or
synced automatically) rather than generating or suggesting travel
plans. Its group feature only allows shared visibility or
collaborative merging of already-booked items — there is no
mechanism for collecting group members' interests, budgets, or
preferences, and no optimization of any kind takes place.

**Relevance to Our Project:**

TripIt confirms a different but related gap: it solves
"organizing what's already decided," not "deciding what to do."
This reinforces that no researched system so far handles
group-level preference reconciliation or itinerary generation
under shared constraints.

**Sources:**

See sources.md — "TripIt — Independent Review"

**Decision/Impact:**

TripIt is excluded from consideration as a comparable system for
itinerary generation — it operates one layer downstream (managing
confirmed bookings) from where our project operates (deciding what
to book/visit in the first place).