---
name: check-setting-consistency
description: Check logical completeness and consistency whenever creating, rewriting, extending, or revising original settings, worldbuilding, characters, organizations, histories, events, abilities, relationships, terminology, or related creative content. Detect contradictions inside newly written or modified content, compare it with unchanged source material, identify external conflicts, propose resolution options, and ask the user to decide before resolving conflicts that affect established content or authorial intent.
---

# Check Setting Consistency

Treat consistency checking as a required part of setting creation and revision.

## Establish the comparison scope

Before drafting, identify:

- The content requested for creation or modification.
- The existing material directly affected by the request.
- The unchanged material that acts as an established constraint.
- Any missing source material that prevents a reliable comparison.

Do not claim that the full setting is conflict-free when only part of it is available. State the actual inspection scope and mark conclusions that depend on missing information.

## Build a constraint map

Extract the relevant facts and constraints before finalizing content, including:

- Entity identity, attributes, roles, motivations, knowledge, and relationships.
- Timeline, age, duration, sequence, simultaneity, and historical dependencies.
- Location, distance, movement, jurisdiction, and spatial relationships.
- Cause and effect, prerequisites, consequences, and feedback loops.
- Capabilities, limitations, costs, resources, scale, and quantitative bounds.
- Social structures, institutions, customs, laws, terminology, and naming.
- Information availability, viewpoint differences, secrets, rumors, and unreliable claims.
- Explicit exceptions, unresolved mysteries, deliberate ambiguity, and retcons.

Distinguish hard facts from assumptions, interpretations, rumors, proposals, and intentionally uncertain material. Do not treat different viewpoints as contradictions unless the claims are intended to be objectively simultaneous and true.

## Check the new or modified content internally

Check the complete proposed content for:

- Directly incompatible statements.
- Timeline or sequence impossibilities.
- Broken causal chains or effects without sufficient causes.
- Missing prerequisites, transitions, motivations, or consequences.
- Circular explanations that provide no independent cause.
- Capabilities that bypass stated limitations, costs, or risks.
- Quantities, scale, geography, or resource demands that cannot coexist.
- Terminology that changes meaning without explanation.
- Entity, relationship, or viewpoint drift.
- Rules or principles that are applied inconsistently without a stated exception.

Repair clear drafting mistakes before presenting the proposal when the repair preserves the user's intent.

If multiple repairs are plausible, or a repair would change meaning, tone, stakes, characterization, established facts, or authorial intent, do not choose silently. Present the conflict and ask the user to decide.

## Compare against unchanged material

After the internal check, compare every new or changed claim with relevant unchanged material.

For each detected conflict, report:

1. **Conflict ID**: Use stable labels such as `C-01`.
2. **Changed claim**: Quote or precisely summarize the proposed claim.
3. **Existing constraint**: Quote or precisely summarize the conflicting unchanged claim.
4. **Locations**: Identify files, sections, headings, entries, or other available locations.
5. **Conflict type**: For example identity, timeline, causality, capability, relationship, terminology, geography, quantity, institution, or viewpoint.
6. **Why they conflict**: Explain the incompatible implications, not merely that the wording differs.
7. **Confidence**: Mark as confirmed, likely, or uncertain and explain any missing evidence.
8. **Resolution options**: Give concise alternatives with their consequences.
9. **Recommendation**: Recommend one option and explain the tradeoff.

Do not silently alter unchanged material to make the proposal fit.

Do not label harmless elaboration, compatible specificity, stylistic variation, deliberate ambiguity, or differing in-world viewpoints as confirmed conflicts.

## Handle completeness gaps

Identify omissions that prevent the proposal from functioning coherently even when no direct contradiction exists.

Classify each gap as:

- **Blocking**: The content cannot be applied coherently without a decision.
- **Material**: The content can be used, but the omission creates a significant logical weakness.
- **Optional**: Additional detail would improve clarity but is not required.

For blocking gaps, provide concrete completion options and ask the user to choose. Do not invent a consequential answer without authorization.

## Present the result

When no conflict is found, state:

- The scope checked.
- That no conflict was found within that scope.
- Any assumptions, uninspected sources, or optional completeness gaps.

When conflicts exist, present:

- The proposed new or modified content.
- An internal consistency result.
- A conflict list using stable IDs.
- Resolution options and a recommendation for each conflict.
- A consolidated decision request that lets the user answer by conflict ID.

Use a compact decision format such as:

`C-01：采用方案 A；C-02：保留旧设定并重写新内容。`

## Stop for user decisions

Ask the user how to resolve every blocking conflict and every conflict involving unchanged established material.

Do not apply a resolution, rewrite established content, or represent the proposal as final until the user decides.

After the user decides:

1. Apply only the selected resolutions.
2. Repeat the internal consistency check.
3. Repeat the comparison against affected unchanged material.
4. Report any newly exposed or remaining conflicts.
5. Proceed only when the revised result is internally coherent and all blocking conflicts are resolved.

If another active workflow requires approval before changing document files, keep the consistency review separate from that approval and satisfy both gates before writing.
