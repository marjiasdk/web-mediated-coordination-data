# Coding sheet: web-mediated coordination in LLM-based multi-agent incidents

Data for the paper "Web-Mediated Coordination as a Harm Pathway in LLM-Based Multi-Agent Systems" (anonymised for review).

## Files
- `incidents.csv`: the coding sheet. One row per screened candidate (35), UTF-8.
- `legend.csv`: definitions of every code, plus the summary counts.

## What the 35 rows are
- 15 coded incidents (Assessment = Keep, Tier A or B): 4 Tier A, 11 Tier B.
- 7 Tier C demonstrations (Keep, Tier C): peer-reviewed or preprint mechanism studies, not deployment incidents. They are not coded for role or observability.
- 13 excluded candidates (Assessment = Exclude), kept for traceability. The reason is in `Evidence gaps / tier rationale`.

## Screening rules (all four must hold; harm is not required)
- R1: at least two agents interacted, at least one LLM-based with tool or action access.
- R2: a documented outcome, either realised harm or a near-miss.
- R3: the source describes how the agents interacted.
- R4: a real deployment, or a realistic evaluation with effects beyond a sandbox.

## Codes
- **Tier A (reconstructable):** message content or record, sequence and agent identity or role are available. **Tier B (codable):** enough to code, without message-level evidence. **Tier C (demonstrated):** mechanism study.
- **Web channel class** (`Web channel class`): Repurposed Web resource (the paper's core pattern); Purpose-built agent channel; Internal / non-Web channel; Not stated in sources. A Web resource is one reachable over web protocols by parties outside the deploying organisation.
- **Coordination role** (`Coordination role`): Necessary (the harm as described would not have occurred without the interaction); Amplifying (the interaction widened or sped up harm one agent could already have caused; the default where necessity is not shown); Incidental.
- **External observability** (`External observability (public record only)`): could an outside monitor with only the public record have seen the coordination? Yes / Partly / No (operator or platform records; attacker-side artefacts; disclosure only).
- `>1 independent source`: whether a source independent of the discloser exists.

`legend.csv` has the full definitions.

## Limits
One coder coded all rows; no inter-rater agreement is reported. Where a primary source was gated or only partly read, the `Evidence gaps / tier rationale` column says so. Sources were read up to 15 November 2026.

## Licence

The data in this repository (`incidents.csv` and `legend.csv`) is released under the Creative Commons Attribution 4.0 International licence (CC-BY-4.0): https://creativecommons.org/licenses/by/4.0/

## AIAAIC keyword screen

The screen used the headline and technology fields only, with the terms "multi-agent", "agents", "agentic", "swarm", "orchestrat", "sub-agent", "AI agent" and "autonomous agent". It returned 32 entries; the four that involve interacting agents were already in the sample.
