# Suno v6 music direction reference
Last verified: 2026-10-20. Official primary sources:
- https://suno.com/blog/introducing-v6
- https://help.suno.com/en/articles/13924801
- https://help.suno.com/en/articles/13924737

## Officially supported model distinctions
- **v6**: precise, polished, expressive; Pro/Premier.
- **v6-wild**: exploratory, unpredictable, diverse; Pro/Premier.
- **v6-mini**: quick ideation; available on all plans.
- All three support up to 8 minutes per generation (not a guarantee of song duration).
- Suno describes natural-language edits, section replacement, source mixing and multimodal starting materials, where available in the user's UI.
- Existing Suno tools include Extend, Cover, Replace Section and Custom Models. Verify their current availability before giving click-by-click directions.

## Prompt composition
Use a compact musical production brief in readable sentences, describing:
1. genre/subgenre plus emotional trajectory, without piling contradictory labels;
2. groove/tempo feel and primary instrumental roles;
3. vocal identity, delivery and intelligibility when needed;
4. section arc and dynamic contrast;
5. mix priorities, e.g. kick/bass separation and vocal intelligibility.

Example Style:
`Cinematic progressive metal with a dark orchestral core. Tight syncopated rhythm guitars and articulate kick/snare support a warm, audible bass guitar with distinct low-mid attack. Cellos and violas carry counter-melodies in verses; the full string section opens the chorus without masking the lead vocal. Restrained intimate verses build into a wide, forceful final chorus; natural drums, controlled distortion, clear central vocal, defined low end.`

Example Lyrics structure (not official grammar promises):
`[Intro]`
`[Verse 1]`
`[Pre-Chorus]`
`[Chorus]`
`[Verse 2]`
`[Bridge]`
`[Final Chorus]`
`[Outro]`

Exclude: keep brief and targeted, e.g. `boomy low end, harsh cymbals, buried vocals, excessive synth pads`. Exclude words are a preference, not an absolute prevention system.

## Editing prompt
`Replace only the second chorus. Make the strings rise in countermelody while bass guitar becomes more articulate beneath the kick. Preserve the lead melody, lead vocal timbre, lyric wording, tempo feel and all other sections.`
Do not claim that all unaffected audio will necessarily remain bit-identical.

## A/B tests and reporting
Test one variable at a time, e.g. model v6 vs v6-wild, or plain natural-language direction vs structure-cued version. Record actual audio observations, not invented measurements. For low-end problems distinguish composition/arrangement from mix/mastering: prompt changes cannot guarantee post-production EQ, compression or stem separation.

## Evidence boundary
Suno documents its model family and edit abilities; it does not guarantee precise instrument placement, section cue interpretations, vocal identity switching, or mix levels through prompt wording. Do not treat crowdsourced tags as an official command syntax.
