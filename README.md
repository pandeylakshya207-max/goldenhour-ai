# GoldenHour AI

A concept and interactive demo for coordinating the first minutes after a road crash from a single chat message.

Submitted to the Road Safety Hackathon 2026 (BIMSTEC countries), organised by IIT Madras CoERS. Track: RoadSoS. Team: The Encoder.

> **Status: front-end prototype.** This repository contains one self-contained HTML file that simulates the whole flow in the browser. There is no backend, no language model, and no messaging, maps or hospital integration. Nothing here contacts emergency services. In a real emergency, call your local emergency number.

## The idea

The premise is that after a crash, help often arrives late because the steps happen one after another: someone calls, an ambulance is found, the hospital learns about the patient on arrival, and the family hears hours later.

GoldenHour AI proposes doing those steps in parallel. A bystander sends one message describing the crash. A triage step reads it, and separate agents then locate the scene, dispatch an ambulance, pre-alert the hospital, guide the bystander through first aid, notify the family and draft an incident report.

## Try the demo

Open `goldenhour_ai_full_app.html` in any browser. There is nothing to install.

- The left panel is a chat styled like a messaging app, with five preset messages and a free-text box.
- The right panel has four tabs: a dashboard with an incident card and a grid map, the agent timeline, a CPR guide in four languages, and the proposed architecture.

## What the demo really does

Everything runs in the page with fixed data and timers.

| What you see | What happens |
|---|---|
| Triage result (critical, moderate, minor) | English keyword matching in `classifyMessage()`, for example "not breathing" or "minor" |
| Location | Matching against nine place names in `extractLocation()`; anything else shows "Detected via GPS", and no GPS is used |
| Ambulance dispatched with an ETA | Fixed text; the ETA is 7, 12 or 18 minutes depending on severity |
| Hospital pre-alert, family notification, incident report | Messages shown on timers; nothing is sent or generated |
| Agent timeline | Six steps that complete on fixed delays |
| CPR guide | Seven text steps in English, Hindi, Bengali and Tamil on a 5-second timer, with a 30-compression counter; no audio |

The first-aid text in the demo was written for the prototype and has not been reviewed by a medical professional.

## Proposed design (not built)

The demo illustrates this design. None of it exists in this repository.

- **Input:** a chat message, SMS or voice call, so that no app install is needed.
- **Triage:** a language model turns a short, panicked message into a structured record (severity, location, number injured), with a rule-based fallback when the model is slow.
- **Agents, run in parallel:** location, ambulance dispatch, hospital pre-alert, first-aid guidance, family notification, incident report.
- **Services it would need:** a messaging provider, a maps and routing API, a task queue, and retrieval over published first-aid protocols.

## What stands between this and a real system

- **Institutions, not code.** Dispatching an ambulance or alerting an emergency room needs agreements with operators and hospitals.
- **Location accuracy.** A wrong location costs the minutes the system is meant to save.
- **Medical review.** Every instruction and every translation would need sign-off from qualified people.
- **Privacy and law.** Finding next of kin from a vehicle registration needs a legal basis.
- **Failure handling.** The system must behave safely when the model is wrong, slow or unavailable.

## License

MIT. See [LICENSE](LICENSE).
