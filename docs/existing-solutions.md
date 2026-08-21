# Existing Solutions Research

## Analysis of Current Travel-Planning Systems for Group-Based Itinerary Optimization

---

## 1. Objective

This document analyzes existing travel-planning systems to understand their
capabilities, approaches, and limitations — particularly in handling
multiple travelers' preferences, budgets, and generating optimized group
itineraries. Each system below is evaluated based on its own official
information and independent reviews, with sources recorded in
`research/sources.md`.

---

## 2. Existing Solutions

### Wanderlog

**Focus:** AI-assisted trip planning combined with map, hotel search, and
budget tracking.

**Key Features:**
- AI assistant (chat-based itinerary generation)
- Interactive map with automatic place pins
- Explore — curated places catalog aggregating mentions from 50+ travel
  blogs
- Hotel aggregator (prices from Booking.com and Google)
- Budget tracker with category breakdown
- Collaboration — multiple travelers can view/edit a shared itinerary

**Strength:** Combines several useful tools (map, budget, hotels, AI) in
one place, and its AI can generate a full day-by-day itinerary with
specific places and addresses from a single natural-language prompt.

**Limitation for Our Problem:** Wanderlog's AI takes **one free-text
prompt written by a single person** to represent the entire group's
preferences (e.g. "2 adults + 1 child, want local food, moderate budget")
rather than collecting each traveler's preferences individually and
reconciling conflicts between them. It generates **one itinerary per
prompt**, refined only through follow-up chat messages (limited to 5 free
messages per trip) — there is no feature to automatically produce multiple
alternative itineraries (e.g. a budget-friendly version vs. a
preference-optimized version) from the same inputs. Budget figures are
also calculated as an estimate *after* the itinerary is generated, rather
than being used as a constraint that shapes which places are selected in
the first place.

**Sources:** See `research/sources.md` — "Wanderlog — Official Website /
Product Page" and "Wanderlog — Independent Review (AI Feature Test)"

---

### TripIt

**Focus:** Organizing already-booked travel into a single itinerary.

**Key Features:**
- Builds itinerary automatically from forwarded confirmation emails
  or inbox sync
- Manual entry for non-email items
- Offline access
- Real-time alerts (flight status, gate/terminal info) in Pro tier
- Sharing / collaborative itinerary for groups

**Strength:** Extremely reliable at consolidating logistics — flights,
hotels, reservations — into one clear, chronological view, including
offline.

**Limitation for Our Problem:** TripIt has no generative or
optimization capability at all — it organizes bookings a traveler has
already made, but never decides what to visit, matches destinations to
preferences, or considers budget. Its "group" feature only merges or
shares already-confirmed bookings; it does not reconcile differing
interests or generate a plan from group input.

**Sources:** See `research/sources.md` — "TripIt — Independent Review"

---

### Google Maps

**Focus:** *[To be researched]*

**Key Features:** *[To be researched]*

**Strength:** *[To be researched]*

**Limitation for Our Problem:** *[To be researched]*

**Sources:** *[Pending]*

---

### Mindtrip (AI Travel Planner)

**Focus:** *[To be researched]*

**Key Features:** *[To be researched]*

**Strength:** *[To be researched]*

**Limitation for Our Problem:** *[To be researched]*

**Sources:** *[Pending]*

---

### Route / Itinerary Optimization System

**Focus:** *[To be researched]*

**Key Features:** *[To be researched]*

**Strength:** *[To be researched]*

**Limitation for Our Problem:** *[To be researched]*

**Sources:** *[Pending]*

---

## 3. Comparative Analysis

*This table will be completed once all five systems above have been
researched and sourced. Filling it in early — before the evidence exists —
would make the comparison unreliable.*

| Solution | Individual Personalization | Multi-Traveler Collaboration | Group Preference Optimization | Multiple Alternative Plans |
|---|---|---|---|---|
| Wanderlog | Yes (via AI prompt) | Yes (shared itinerary) | No — single prompt represents whole group | No — one itinerary per prompt |
| TripIt | *Pending* | *Pending* | *Pending* | *Pending* |
| Google Maps | *Pending* | *Pending* | *Pending* | *Pending* |
| Mindtrip | *Pending* | *Pending* | *Pending* | *Pending* |
| Route Optimizer | *Pending* | *Pending* | *Pending* | *Pending* |

---

## 4. Research Gap

*This section will be written only after all five systems have been
researched. A research gap should be a conclusion drawn from complete
evidence, not stated in advance.*

**Preliminary observation (from Wanderlog alone):** Existing AI-assisted
planners can generate a plausible itinerary from a single natural-language
description of a group, but they do not appear to collect and reconcile
individual travelers' preferences separately, nor do they generate
multiple distinct itinerary options (e.g. budget-first vs.
preference-first vs. balanced) from the same set of constraints. Whether
this pattern holds across TripIt, Google Maps, Mindtrip, and dedicated
route optimizers remains to be confirmed.