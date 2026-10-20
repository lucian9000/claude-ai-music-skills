---
name: suno-v6-engineer
description: Create, revise, and troubleshoot Suno v6, v6-wild and v6-mini music prompts for original songs and instrumentals. Use when a Suno v6 model is selected or requested, including lyric arrangements, experimental genre fusion, section replacement, stems-aware repairs, and orchestral metal. Complements the existing suno-engineer skill without replacing legacy workflows.
argument-hint: <track-file-path or musical brief>
model: opus
effort: max
allowed-tools:
  - Read
  - Edit
  - Write
  - Grep
  - Glob
  - Bash
  - bitwize-music-mcp
---

# Suno v6 Engineer

Input: $ARGUMENTS

## Integration contract
- Preserve the existing album concept, lyric-writer, lyric-reviewer, pronunciation, research, pre-generation-check, mix-engineer, mastering-engineer, import and release flows. Call them as normal.
- This is an **additive v6 prompt director**. Do not modify the track's other sections, schema, filenames or state fields. When given a track file, inspect album context and current Suno Inputs, generate the v6 inputs, then update only those fields if the user requested file changes.
- For v5 or v5.5, delegate to `suno-engineer`. If version unspecified, suggest v6 for precise premium generations and state the assumption.
- Read [v6 guide](../../reference/suno/v6-guide.md) before composing any final v6 package. For orchestral metal also read [orchestral metal](../../reference/suno/v6-orchestral-metal.md).
- Honor the existing `load_override("suno-preferences.md")` preferences when the tool is available and never overwrite user-authored lyrics without approval.

## Creation workflow
1. Identify create vs. edit vs. instrumental vs. existing-lyrics request; note locked lyrics, voice or arrangement constraints. Do not ask for details already supplied.
2. Select v6 for fidelity, v6-wild for divergent experiments, or v6-mini for rapid drafts. Confirm current model availability where necessary.
3. Define an audible plan: subgenre and groove; specific instrument roles; lead vocal language, register and delivery if present; section-by-section energy; production priorities; what to exclude. Avoid artist-name mimicry.
4. Produce three independent paste-ready fields when the UI offers them: **Style**, **Lyrics**, and **Exclude**; plus **Model**, **Instrumental toggle**, **Generation/Revision notes**. If Exclude or other settings are not shown in the user's interface, keep them as optional rather than claiming they exist.
5. Use conventional section markers for navigation where helpful, and concrete musical directions in natural language. Treat nonstandard tags, exact BPM/pitches/timestamps, voice switching, and control sliders as testable hypotheses, not guarantees. Check current UI limits before claiming numerical field constraints.
6. For an instrumental, omit sung words and vocal requests; use a sparse structure map only if useful.
7. For a section replacement, specify the **target section**, **desired audible change**, and **what must remain unchanged**. Explain that preservation is a creative intention, not a sample-exact guarantee.
8. Deliver one strong default prompt, plus at most one deliberately changed A/B variant when requested. Never imply real listening tests occurred without an accessible audio file.
9. After hearing/receiving feedback, diagnose observed defects, change only relevant instructions, retain approved lyrics and arrangements, and log model, prompts, settings, perceived result and next hypothesis.

## Quality gate
Before output: check lyrics were preserved, sections agree with structure, instrumentation is noncontradictory, voice is intentional, bass/drums have defined roles, transition and final payoff are present, edits identify locks, paste-ready fields contain no commentary, and claims about model support are grounded in official sources. Separate **verified Suno capabilities** from **experimental prompting tactics**.

## Compatibility
The existing `suno-engineer` remains available for legacy songs. Existing audio, lyric QC, mastering, and album state are unchanged. This skill generates text and instructions; it does not operate Suno or consume credits.
