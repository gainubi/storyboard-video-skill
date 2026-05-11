---
name: storyboard-video-previs
description: Generate cinematic storyboard plans and image generation prompts from a story, theme, script, music video idea, commercial concept, or visual brief. Use when Codex needs to turn narrative text into a panel by panel storyboard, shot list, animatic plan, video previs prompt, image model prompt, or bilingual Chinese and English storyboard prompt with camera language, motion notes, annotation systems, continuity cues, and visual style constraints.
---

# Storyboard Video Previs

## Overview

Use this skill to turn a story or theme into a video ready storyboard prompt. The goal is not to summarize the story, but to design the viewing experience: composition, panel rhythm, camera grammar, motion continuity, emotional escalation, annotation language, and final image prompt.

## References

Load `references/shot-language.md` when the task needs camera vocabulary, shot variation, annotation symbols, or motion design.

Load `references/storyboard-formats.md` when choosing panel count, grid structure, beat rhythm, or adapting the storyboard to action, dance, horror, dialogue, ad, music video, or experimental styles.

## Workflow

1. Infer or confirm the production target.
   Use the user supplied target if present. Otherwise default to a single 16:9 storyboard sheet, 12 panels for most stories, 16 panels for action or dance sequences, rough hand drawn cinematic previs style, and a consolidated image generation prompt.

2. Extract the story engine.
   Identify protagonist, desire, obstacle, emotional arc, setting, key prop or motif, motion vocabulary, visual contrast, and final beat. Keep this short and operational.

3. Decide the storyboard rhythm.
   Map the story into a beginning, escalation, rupture, climax, and release. Give every panel a new function. Avoid panels that merely repeat the same pose, distance, or camera angle.

4. Assign shot language.
   For each panel choose shot size, camera angle, camera movement, lens or framing, subject movement, environment change, and transition cue. Use standard terms when helpful, but prioritize clarity over jargon.

5. Preserve continuity.
   Track screen direction, character facing, prop visibility, spatial geography, light direction, and any motif that must remain readable across panels. If the user asks for a visual element such as a rope, microphone, vehicle, weapon, fabric, smoke, or energy trail, keep it visible and purposeful in every relevant panel.

6. Produce the output in four sections unless the user requested another format.
   Section 1: Storyboard creative brief.
   Section 2: Panel table with one row per panel.
   Section 3: Consolidated generation prompt.
   Section 4: Negative prompt and quality checklist.

7. Offer video extension only when useful.
   If the user is preparing for image to video, add a compact per panel motion plan with camera move, subject move, transition, and approximate duration. Do not add timestamps when the user asks for no timestamps.

## Output Contract

For a complete storyboard response, include:

1. Format line
   Aspect ratio, panel count, layout, medium, drawing style, color rules, and whether it is one sheet or separate frames.

2. Storyboard creative brief
   One paragraph covering subject, world, emotional trajectory, dominant motion, visual motif, camera personality, lighting, and ending image.

3. Panel table
   Columns: Panel, Story beat, Visual action, Shot language, Motion and camera notes, Annotation notes, Continuity cue.

4. Consolidated image prompt
   A single prompt suitable for GPT Image or another image model. It should mention the whole sheet, exact panel count, style constraints, character consistency, key motif, camera variety, annotation system, and final panel requirement.

5. Negative prompt
   Exclude static poses, missing key props, inconsistent character, unreadable panels, over detailed finished illustration when rough previs is requested, excessive text, wrong aspect ratio, and contradictions with user constraints.

## Prompt Rules

Use concrete visual verbs. Prefer actions like lunges, recoils, vaults, slides, folds, twists, punches through smoke, tilts into camera, or collapses into spotlight.

Name the camera behavior inside each panel. Combine shot size, angle, and movement, for example wide low angle tracking shot, overhead static geometric shot, handheld close up with whip pan blur, or compressed telephoto profile.

Make rhythm visible. Use speed lines, smear frames, repeated limb ghosts, floor marks, light pulses, debris arcs, cloth trails, reflection streaks, impact shapes, or annotation arrows when they support the requested style.

Keep prompts image model friendly. A panel should describe one readable moment, not a full scene that requires time to unfold.

Respect the drawing style. If the user asks for black and white storyboard art, keep the actual drawings monochrome. Colored annotation marks can be used only when the user requested a color annotation system.

If a reference image is supplied, use it for character continuity, costume, silhouette, hairstyle, and attitude. Do not let it override the storyboard style unless the user explicitly asks.

## Defaults

Panel count: 12 for balanced narrative, 16 for kinetic action, 8 for short proof of concept, 24 for detailed animatic planning.

Aspect ratio: 16:9 unless the user specifies vertical, square, or platform specific format.

Style: rough cinematic storyboard, readable silhouettes, simple anatomy, energetic linework, clear camera notes.

Language: match the user language. If the user provides Chinese and English examples or asks for image prompts, provide Chinese planning plus an English generation prompt when useful.

## Quality Checklist

Before finalizing, verify:

1. Every panel has a distinct beat and visible motion.
2. The camera language changes with intention, not randomness.
3. The story arc is readable without the original text.
4. Key props and motifs stay visible when required.
5. The final panel is visually decisive.
6. The consolidated prompt preserves all non negotiable user constraints.
7. The sheet can be judged quickly for composition, rhythm, and tone before video generation.
