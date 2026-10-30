---
name: rpg-character-design-sheet
description: "Create detailed, visually consistent RPG character design sheets for tabletop RPGs (TRPG), computer and video game RPGs (CRPG), MMORPGs, live-action role-play (LARP), solo RPGs and gamebooks, and animation or narrative projects. Includes mandatory intake questions, RPG character anatomy, classes, ancestries, attributes, equipment, abilities, factions, alignment, character bibles, turnarounds, expression and outfit sheets, tokens, portraits, sprites, costume guides, and workflows for each format. Tool-agnostic and compatible with any image-generation backend. Trigger when users request RPG character design, character reference sheets, RPG portraits, tokens, sprites, NPC concepts, LARP costumes, gamebook illustrations, character turnarounds, or consistent character artwork."
---

# RPG Character Design Sheet

Design, document, and maintain visually consistent RPG characters across the assets required by a project: tabletop tokens, character portraits, CRPG concept art, MMORPG equipment tiers, LARP costume kits, gamebook illustrations, and animation model sheets.

This skill is **tool-agnostic**. It describes the design process, reference material, and prompt structure without requiring a particular image-generation model, application, CLI, or service. Use the image-generation tools available in the current environment. Backend-specific features such as seeds, image-to-image, reference conditioning, LoRAs, or image stitching are optional and must only be used when the selected backend supports them.

The purpose is to create a reliable visual source of truth for a character. A character should remain recognizable across different poses, camera angles, outfits, scenes, illustrations, and production stages.

---

## STOP — Mandatory Intake Before Creating Anything

**Do not generate an image, write a production-ready image prompt, or create the character design sheet until the user has answered all three questions below.** This is a blocking requirement.

If the user has already supplied one or more answers in the conversation, do not ask for them again. Ask only for missing or genuinely ambiguous information. Do not infer the RPG format, subgenre, or reference preference from an image or from assumptions.

### Question 1 — What RPG format or medium is this for?

Ask which format is the primary target. The user may also identify secondary formats.

- **TRPG — Tabletop Role-Playing Game:** Dungeons & Dragons, Pathfinder, Call of Cthulhu, Blades in the Dark, and similar games.
- **CRPG / Video Game RPG:** Single-player or party-based computer and console RPGs.
- **MMORPG:** Massively multiplayer online RPGs.
- **LARP — Live-Action Role-Play:** A character represented by a real participant, costume, makeup, accessories, and safe props.
- **Solo RPG / Gamebook:** Solo role-playing games, branching gamebooks, and interactive fiction.
- **Animation / Narrative:** Animated series, motion comics, visual novels, comics, illustrated fiction, or stories intended for animation.
- **Other:** Ask the user to describe the intended medium.

### Question 2 — What is the RPG subgenre, setting, or aesthetic?

Offer examples without limiting the user's choice:

- Fantasy: medieval, high fantasy, low fantasy, dark fantasy, sword and sorcery.
- Action RPG (ARPG).
- JRPG / Japanese RPG.
- Tactical / strategy RPG (SRPG).
- Horror / survival horror.
- Science fiction: cyberpunk, space opera, military sci-fi, post-apocalyptic.
- Open-world / sandbox.
- Superhero, modern, or urban fantasy.
- Historical, mythological, or folklore-inspired.
- Cozy, comedic, or slice-of-life RPG.
- Other: the user's own setting or a combination of genres.

### Question 3 — Is there reference material, or should the character be created from scratch?

Offer these choices:

- **Image reference:** The user will provide an image, portrait, concept art, photograph of a costume, or other visual reference.
- **Text reference:** The user will provide a character description, existing character sheet, stat block, backstory, or notes.
- **Both:** The user has visual and written references.
- **From scratch:** Build the character collaboratively, starting with the character concept.

### Intake gate rules

1. Ask the three questions before starting the design work. They may be asked together in one short, clearly structured message.
2. If the user has already answered some questions, ask only the unanswered ones.
3. If the user selects multiple formats, ask which one is primary. Use the primary workflow and add deliverables from secondary formats where appropriate.
4. If the user gives a broad subgenre, accept it. Ask for clarification only when the answer materially changes the visual direction.
5. Do not generate an image or a production-ready image prompt while any required answer is missing.
6. Once all answers are clear, follow the matching reference-handling process and format-specific workflow.

---

## Workflow Selection

| Primary format | Main workflow | Typical deliverables |
|---|---|---|
| TRPG | Tabletop RPG | Character turnaround, portrait, VTT token, expressions, miniature reference |
| CRPG / Video Game | Game production | Concept turnaround, portraits, equipment callouts, poses, sprites or animation keyframes |
| MMORPG | Persistent online character | Base body and face, gear progression, cosmetic sets, guild insignia, mounts and pets |
| LARP | Physical realization | Concept art, costume breakdown, makeup chart, safe prop list, weather variants |
| Solo / Gamebook | Printed or digital narrative | Canonical portrait, scene illustrations, chapter icons, black-and-white or duotone artwork |
| Animation / Narrative | Reproducible character model | Model sheet, turnaround, expressions, poses, props, costume variants |
| Other | Custom workflow | Define deliverables from the intended use; combine relevant workflows above |

The subgenre influences visual language, materials, motifs, equipment, color palette, atmosphere, and pose direction. It does **not** automatically determine the character's rules, statistics, personality, or narrative. Preserve the user's setting and game-system choices.

---

## Handling Reference Material

### Image reference

1. Inspect the supplied image and describe only visible, relevant design features.
2. Extract a preliminary **Description Anchor** (see below), covering ancestry or species cues, apparent age, build, hair, eyes, skin colors, distinctive marks, clothing layers, armor, weapons, accessories, proportions, and art style.
3. Separate clearly visible details from uncertain interpretations. Do not invent unseen details or infer a character's backstory, personality, or game statistics from appearance alone.
4. Present the anchor to the user and ask for confirmation: **"Is this description accurate? What should I correct or add?"**
5. Do not proceed to final generation until the user confirms or corrects the anchor.
6. When supported by the selected backend, prefer image-to-image generation, reference-image conditioning, character reference, or a comparable feature to preserve identity. If unavailable, reuse the approved anchor consistently.
7. If the reference shows only a headshot but a full-body sheet is required, ask for missing outfit, body, footwear, and equipment details rather than fabricating them.

### Text reference

1. Parse the material and map its contents to the **RPG Character Sheet Anatomy** section.
2. Preserve names, terminology, game-system attributes, equipment, abilities, factions, and narrative facts as supplied.
3. Identify missing details that materially affect the visual result. Ask specific questions, preferably with two or three clear options when useful.
4. Do not change a weapon, armor type, ancestry, class, or signature ability merely to make the design more conventional.
5. Mechanical information should guide what is depicted, but should not be copied blindly into an image prompt. Translate relevant mechanics into visible design cues.

### Both image and text references

1. Compare the references and identify contradictions.
2. Treat explicit user instructions as authoritative. Ask which source should take precedence when a conflict cannot be resolved.
3. Create one consolidated anchor and one character bible after the user approves the interpretation.

### From scratch

Build the character collaboratively in manageable groups. Do not overwhelm the user with every field at once.

Recommended order:

1. **Identity and concept:** name (optional), ancestry/species, apparent age, class/archetype, role, and core concept.
2. **Appearance:** body type, proportions, skin, hair, eyes, distinctive marks, and art style.
3. **Equipment and abilities:** weapons, armor, clothing, accessories, tools, magic, and signature effects.
4. **Faction and narrative:** faction symbols, background, motivation, bonds, flaws, and other story details.

Offer two or three visual options when a field is undecided. Confirm each group before moving to the next. The user may skip fields that are not relevant to the project.

---

## RPG Character Sheet Anatomy

Use this as a flexible design framework, not as a mandatory form that must be filled in completely. Adapt terminology to the user's RPG system. If the system does not use attributes, alignment, levels, mana, or conventional classes, do not force those fields into the character.

Legend:

- **Visual:** Affects the character's appearance and should be represented in the Description Anchor when relevant.
- **Reference:** Mechanical, social, or narrative information that belongs in the character bible and guides design decisions.
- **Signature:** A highly recognizable visual or narrative feature that should remain consistent across relevant assets.

### Identity and role

| Field | Type | Notes |
|---|---|---|
| Name / true name / alias | Reference | The character's identifying name. |
| Age / apparent age | Visual | Prefer a concrete age or range over vague terms such as "young." |
| Gender / pronouns | Visual / Reference | Include only as specified by the user or relevant to the design. |
| Ancestry / race / species | Visual | Examples: human, elf, dwarf, orc, android, alien, spirit. Respect the setting's terminology. |
| Class / archetype / role | Visual / Reference | Examples: fighter, rogue, healer, technomancer, investigator. Show the role through clothing, tools, posture, and equipment. |
| Subclass / specialization / path | Visual / Reference | Add distinctive visual language when the specialization calls for it. |
| Level / rank / tier | Reference | May influence equipment quality, insignia, or visual progression. |
| Background / origin | Reference | Examples: noble, folk hero, exile, street urchin, soldier, scholar. |

### Attributes and game mechanics

| Field | Type | Notes |
|---|---|---|
| Primary attributes | Reference | Use the system's own terms, such as STR, DEX, CON, INT, WIS, CHA, or a different attribute set. |
| Secondary attributes | Reference | HP, MP, mana, defense, armor class, speed, initiative, stamina, and equivalents when applicable. |
| Derived values | Reference | Attack bonus, spell difficulty, resistance, skill ratings, and other system-specific values. |
| Alignment / morality | Reference | Include only if the system uses it. Keep it in the character bible; do not put abstract alignment labels directly into image prompts. |

### Combat, clothing, and equipment

| Field | Type | Notes |
|---|---|---|
| Primary weapon(s) | Visual | Be specific: "longsword with a leather-wrapped grip" rather than simply "sword." |
| Secondary / off-hand weapon | Visual | Dagger, shield, pistol, focus, or other item. |
| Ranged weapon | Visual | Bow, crossbow, rifle, throwing knives, and so on. |
| Armor | Visual | Type, material, condition, coverage, and quality tier. |
| Base clothing layer | Visual | Undergarment or foundational layer. |
| Mid clothing layer | Visual | Tunic, shirt, vest, gambeson, or equivalent. |
| Outer clothing layer | Visual | Cloak, coat, robe, mantle, tabard, or equivalent. |
| Footwear | Visual | Boots, shoes, sandals, greaves, or other footwear. |
| Accessories | Visual | Jewelry, belts, pouches, charms, insignia, and tools. |
| Signature item | Signature / Visual | The recognizable prop the character carries or wears. |
| Consumables / ammunition | Reference / Visual | Include visible containers, quivers, bandoliers, or pouches when relevant. |
| Alternate loadouts | Visual | Casual, formal, stealth, combat, ceremonial, damaged, or other requested variants. |

### Magic, abilities, and skills

| Field | Type | Notes |
|---|---|---|
| Known spells / abilities | Reference | Use the user's system and terminology. |
| At-will abilities / cantrips | Reference | Include when applicable. |
| Class resource | Reference | Rage, ki, mana, energy, focus, charges, or equivalents. |
| Signature move | Signature / Reference | Should inform dynamic poses or special-effect sheets. |
| Passive traits | Reference | Translate into visible details only when appropriate. |
| Visible magical or technological effects | Visual | Runes, aura, energy trails, glowing circuits, particles, or other effects. |
| Skills and proficiencies | Reference | Include notable skills that influence tools, props, or poses. |
| Languages | Reference | Include in the bible; show visually only when the design requires it. |
| Tools / kits | Visual | Lockpicks, medical kits, crafting tools, musical instruments, and similar props. |

### Social, faction, and affiliation

| Field | Type | Notes |
|---|---|---|
| Faction / guild / order | Visual / Reference | Use consistent colors, emblems, badges, uniforms, or heraldry. |
| Rank within faction | Visual / Reference | May influence insignia, trim, medals, or clothing details. |
| Patron / deity / belief | Visual / Reference | Include symbols or vestments when relevant to the character. |
| Allies / rivals / enemies | Reference | Narrative context; do not add other characters to a solo sheet unless requested. |
| Alignment | Reference | If supported by the system, record it here rather than relying on an image model to interpret it. |

### Appearance and visual identity

| Field | Type | Notes |
|---|---|---|
| Height / build / body type | Visual | Use concrete descriptions, not vague labels. |
| Skin tone | Visual | Record a descriptive shade and, where useful, a hex color. |
| Hair color / length / style | Visual | Define color, length, texture, parting, and silhouette. |
| Eye color | Visual | Record a precise color; use hex values when useful. |
| Distinctive marks | Signature / Visual | Scars, tattoos, birthmarks, prosthetics, horns, heterochromia, or other stable traits. |
| Voice / accent | Reference | Particularly useful for LARP, voice direction, and animation. |
| Proportions | Visual | Realistic, heroic, anime, stylized, chibi, or another defined style. |
| Art style | Visual | Examples: painterly concept art, cel-shaded, pixel art, ink illustration, low-poly, realistic costume reference. |

### Narrative identity

| Field | Type | Notes |
|---|---|---|
| Background / history | Reference | The character's relevant history. |
| Motivation / goal | Reference | What the character wants. |
| Flaw / secret | Reference | Optional narrative dimension. |
| Bond / relationship | Reference | A person, group, place, or ideal that matters to the character. |
| Quote / catchphrase | Reference | Useful for dialogue portraits, voice, or promotional material. |

### Visual hooks — the character's fingerprint

Choose **three to five** distinctive details that must remain visible in every asset where practical. If a generation has limited space or detail, preserve these before adding decorative elements.

Examples:

- Heterochromatic eyes: one green, one gray.
- A cracked left horn.
- A red sash tied at the right hip.
- A burn scar across the right jaw.
- A mechanical left hand.
- A crescent-shaped faction emblem on the shoulder.

Do not add a visual hook without user approval if it changes the character's established identity.

---

## The Description Anchor Technique

A **Description Anchor** is a concise, reusable description of the character's stable visual identity. It is one of the most useful consistency techniques across image-generation systems.

Write approximately **50–120 words**. Reuse the approved anchor consistently across prompts. Change the requested view, pose, expression, outfit variant, or scene—not the character's core identity.

### RPG anchor template

```text
[apparent age] [ancestry/species] [class/archetype] with [hair color, length, and style],
[eye color] eyes, [skin tone], and [distinctive marks].
They wear [base layer], [mid layer], and [outer layer], with [footwear and accessories].
They carry [primary weapon or signature item] and [secondary equipment].
[Include faction insignia or visible magical/technological details when relevant.]
[Body proportions] and [art style].
```

Use the user's preferred pronouns and language. For prompts, translate the anchor into the syntax and language that best suit the chosen image backend, while preserving its factual content.

### Example — fantasy TRPG fighter

```text
Human fighter in her mid-thirties with shoulder-length braided auburn hair,
sharp emerald-green eyes, weathered olive skin, and a long pale scar running
from her left temple to her jaw. She wears a chainmail hauberk beneath a
forest-green tabard with a silver stag sigil, worn leather bracers, and brown
riding boots. A silver signet ring sits on her right hand. She carries a
leather-wrapped longsword at her left hip and a round wooden shield with an
iron boss on her right arm. Realistic seven-and-a-half-head proportions,
detailed digital concept art.
```

### Rules for a strong anchor

1. **Be specific:** use exact materials, colors, shapes, and object names.
2. **Prioritize identity:** mention signature features early in the anchor.
3. **Record color values:** use hex codes for important recurring colors when precision matters.
4. **Describe visible evidence:** "confident upright stance" is actionable; "lawful good" is not a visual description.
5. **Keep the anchor stable:** do not rewrite it casually between generations.
6. **Separate stable identity from variations:** put alternate outfits, temporary injuries, weather, and scene-specific effects in separate prompt blocks.
7. **Check mechanics against visuals:** equipment and visible abilities must agree with the approved character information.

---

## Reference Sheet Types

Create only the sheets required by the user's format and production goals. All views of the same character should derive from the same approved anchor and visual references.

### 1. Turnaround sheet

Show front, three-quarter, side, and back views. Use a neutral standing pose, full body, consistent scale, and a clean background. Keep body proportions, garment construction, equipment placement, and silhouette consistent across views.

### 2. Expression sheet

Include at least six baseline expressions: neutral, happy, angry, sad, surprised, and thinking. Add genre-specific expressions when useful, such as battle cry, pain, smug, terrified, exhausted, or determined. Preserve face shape, hairstyle, and distinctive marks.

### 3. Outfit and equipment sheet

Show each requested outfit or loadout clearly. Separate individual props or armor pieces when callouts are useful. Include front and back views for garments with important rear details.

### 4. Color palette sheet

Record the persistent colors used in the design. Treat this as the visual source of truth when colors drift.

| Element | Example hex | Notes |
|---|---|---|
| Skin | `#C8A278` | Example only; use the approved character color. |
| Hair | `#C0392B` | Example only. |
| Eyes | `#27AE60` | Example only. |
| Primary outfit | `#2C3E50` | Example only. |
| Accent | `#E74C3C` | Example only. |
| Metal | `#7F8C8D` | Example only. |

### 5. Miniature / VTT token (TRPG)

Create a readable top-down or three-quarter top-down token, commonly with a transparent background and a circular crop. Prioritize a strong silhouette, contrast, and recognizable equipment at small scale. If the VTT or print format has a specific token size, follow that requirement rather than assuming a universal measurement.

### 6. Dialogue / UI portrait (CRPG)

Create a canonical bust or head-and-shoulders portrait with consistent framing. Produce the highest useful source size supported by the workflow, then resize or crop derivatives from that source where possible. Do not regenerate the same portrait independently at every UI size.

### 7. Sprite and animation frames (CRPG / MMORPG)

Common states include idle, walk, run, attack, cast, hurt, and defeat. Establish a canonical key pose and consistent sprite scale first. When supported, derive additional frames using image-to-image, pose control, or dedicated animation/sprite tools. Check frame alignment, silhouette, equipment, and facing direction.

### 8. Gear tier progression (MMORPG)

Show progression such as starter, leveling, dungeon, raid, and cosmetic/transmog sets. Keep the face, body, hair, and defining marks stable. Change only the approved outfit and equipment blocks unless the user explicitly requests a character progression that changes the body or identity.

### 9. LARP costume and kit guide

Include a concept reference, makeup/prosthetics chart, real-world garment breakdown, materials and colors, safe prop list, weather variants, and items that must remain part of the character's identity. Use practical construction language rather than purely imaginary material descriptions.

### 10. Gamebook illustration set (Solo / Gamebook)

Create one canonical portrait, followed by scene illustrations for major chapters, choices, or endings. Black-and-white ink, limited palettes, or duotone styles are common, but follow the project's chosen art direction. Keep silhouettes and facial identity readable at the intended printed or screen size.

### 11. Animation / narrative model sheet

Include a turnaround, head details, hands and feet, expression sheet, pose sheet, prop callouts, and costume variants. Make the design precise enough for another artist or production model to reproduce consistently.

---

## Proportion Guide

Use proportion language appropriate to the chosen art style. These values are approximate visual conventions, not rigid anatomical rules.

| Style | Approximate head-to-body ratio | Common uses |
|---|---:|---|
| Realistic | 7–8 heads | CRPG concept art, mature TRPG art, costume reference |
| Heroic | Around 8 heads | Superhero and action-oriented designs |
| Anime / manga | Around 5–7 heads | JRPGs, visual novels, stylized characters |
| Stylized | Around 4–5 heads | Western animation, approachable or cozy designs |
| Chibi / super-deformed | Around 2–3 heads | Cute tokens, mascots, expressive miniatures |

State the chosen proportion style explicitly in the anchor or prompt. Maintain the same ratio across all views unless the user requests a deliberate style change.

---

## Subgenre Adaptation

Adapt the visual language to the selected subgenre without replacing the user's worldbuilding.

| Subgenre | Visual considerations |
|---|---|
| Medieval / high fantasy | Layered fabrics, armor, heraldry, crafted weapons, symbolic accessories, magical motifs. |
| Low / dark fantasy | Worn materials, restrained palettes, practical equipment, weathering, ominous motifs. |
| Sword and sorcery | Strong silhouettes, expressive weapons, adventurous clothing, dramatic and functional props. |
| Action RPG | Clear combat role, readable weapon silhouette, dynamic poses, strong visual effects. |
| JRPG | Distinctive silhouettes, expressive costumes, stylized proportions, bold color design where appropriate. |
| Tactical / strategy RPG | Clear role and faction identity, readable class equipment, strong top-down or isometric silhouette. |
| Horror / survival | Practical clothing, signs of wear, restrained effects, believable tools, atmosphere without obscuring character identity. |
| Science fiction / space opera | Functional technology, environmental protection, materials, devices, insignia, and faction language. |
| Cyberpunk | Layered streetwear, cybernetic details, neon accents, wearable technology, and readable material contrast. |
| Post-apocalyptic | Reused materials, repairs, improvised protective gear, practical carrying capacity, environmental wear. |
| Open world / sandbox | Modular equipment, travel-ready clothing, recognizable silhouette across varied environments. |
| Superhero / modern fantasy | Strong shape language, signature costume elements, readable powers, and clear civilian/combat variants. |
| Historical / mythic | Research the specified culture and period when needed; avoid mixing unrelated historical elements without user approval. |
| Cozy / comedic | Friendly shapes, approachable proportions, softer materials, and readable expressions. |

These are starting points, not stereotypes. Ask the user to define any cultural, historical, or fictional references that are important to the project.

---

## Format-Specific Workflows

Run the workflow that matches the user's primary format. Each workflow assumes the intake gate is complete and the character anatomy and anchor have been approved.

### Workflow: TRPG — Tabletop RPG

**Primary goal:** Produce assets that work on a character sheet, printed handout, virtual tabletop, or battle map.

**Recommended deliverables:**

1. Full-body turnaround: front, three-quarter, side, and back.
2. Character portrait for the character sheet or VTT.
3. VTT / battle-map token with a readable silhouette.
4. Expression sheet for social encounters and role-play.
5. Optional miniature or paper-mini reference, including front and side views.
6. Optional isolated weapon, armor, faction emblem, or spell-effect callouts.

**Prompt pattern:**

```text
[approved anchor], [requested view], full body, neutral standing pose,
clean light background, clear silhouette, consistent equipment placement,
character concept sheet, [chosen proportions], [subgenre art direction].
```

**Token prompt pattern:**

```text
[approved anchor, simplified for readability], top-down or three-quarter
 top-down miniature token, strong high-contrast silhouette, [background
 requirement], centered composition, readable at the intended token size.
```

Prioritize the character's face, weapon silhouette, faction icon, and signature color. Small decorative details should not overwhelm readability at token scale.

### Workflow: CRPG / Video Game RPG

**Primary goal:** Connect high-resolution concept art to assets that can be modeled, animated, and shown in a game interface.

**Recommended deliverables:**

1. High-resolution turnaround: front, three-quarter, side, and back, plus head details.
2. Dialogue/UI portrait with a consistent crop.
3. Weapon and armor callouts, isolated and clearly labeled when useful.
4. Pose sheets: idle, combat-ready, movement, and signature ability.
5. Sprite or animation keyframes when the project uses 2D characters.
6. Optional simplified silhouette or level-of-detail reference for 3D production.

**Prompt pattern:**

```text
[approved anchor], [view or pose], full body, neutral studio lighting,
clean gray or white background, production-oriented character concept art,
clearly separated equipment shapes, [proportions], [game art direction].
```

For 3D production, make material, construction, silhouette, and equipment placement clear. For 2D production, maintain consistent canvas size, character scale, and facing direction across frames.

Generate or approve a canonical neutral pose before creating action variations. Use image-to-image or equivalent reference control when available; do not rely on unrelated text-only generations for every animation frame.

### Workflow: MMORPG

**Primary goal:** Preserve character identity across equipment progression, cosmetic variants, mounts, pets, and guild affiliation.

**Recommended deliverables:**

1. Base body and face reference sheet.
2. Starter / leveling equipment set.
3. Mid-tier / dungeon equipment set.
4. Endgame / raid equipment set.
5. Cosmetic or transmog set.
6. Mount and pet references, if requested.
7. Guild tabard or faction insignia, front and back.
8. Idle, emote, and signature pose sheet.
9. Optional race/class combination guide for a roster of characters.

**Prompt pattern:**

```text
[locked body and face anchor], wearing [complete approved gear-tier block],
[view or pose], full body, neutral background, [art style], [proportions].
```

Keep the face, body, hair, skin, and signature marks fixed unless the user specifies an intentional transformation. Change only the approved gear block between tiers. Record each set as a named variant in the character bible.

### Workflow: LARP — Live-Action Role-Play

**Primary goal:** Translate the fictional character into a practical, safe, wearable kit.

**Recommended deliverables:**

1. Character concept reference: front, three-quarter, and side.
2. Face chart for makeup, hair, and prosthetics.
3. Costume breakdown with real-world fabrics, construction, colors, and practical alternatives.
4. Prop list with event-compliant safety requirements.
5. Weather variants: warm weather, cold weather, and rain where relevant.
6. List of signature items that should remain with the character.
7. Accessibility and comfort notes: heat, mobility, visibility, hearing, weight, and duration of wear.

**Prompt pattern:**

```text
[approved anchor translated into wearable real-world materials], [view],
full-body costume reference, natural lighting, practical garment construction,
clear accessories and prop placement, [chosen art style].
```

**Safety requirements:**

- Follow the event organizer's rules and applicable local requirements.
- Never recommend a real weapon or unsafe prop as a substitute for an event-approved prop.
- Clearly distinguish fictional weapons from safe, approved prop construction.
- Do not assume a particular foam weapon core, material, or construction method is permitted; verify the event's rules.
- Include comfort and accessibility considerations, especially for heat, restricted movement, vision, and hearing.

The final output must be useful for making or assembling the kit, not merely an attractive concept illustration.

### Workflow: Solo RPG / Gamebook

**Primary goal:** Keep the character recognizable across pages, branches, endings, and small printed illustrations.

**Recommended deliverables:**

1. Canonical portrait or frontispiece.
2. Scene illustrations for important chapters, choices, or endings.
3. Chapter header or status icons when needed.
4. Optional progression variants: injured, equipped, corrupted, aged, or transformed.

**Black-and-white prompt pattern:**

```text
[approved anchor], [specific scene], black-and-white ink illustration,
clear linework, controlled hatching, strong readable silhouette,
high contrast, suitable for the intended printed page size.
```

**Duotone prompt pattern:**

```text
[approved anchor], [specific scene], duotone illustration using [approved
palette], limited values, consistent inking or rendering style,
clear silhouette, suitable for the intended page size.
```

Approve the canonical portrait first. Use it as the visual reference for subsequent scene illustrations whenever the backend supports reference images or image-to-image workflows.

### Workflow: Animation / Narrative

**Primary goal:** Make the design clear enough for repeated drawing, animation, storyboarding, comics, or visual-novel production.

**Recommended deliverables:**

1. Full model sheet with front, three-quarter, side, and back views.
2. Head details and close-ups of distinctive features.
3. Expression sheet with at least eight expressions.
4. Pose sheet: idle, action, signature gestures, and story-relevant poses.
5. Prop and weapon callouts.
6. Costume variants for each scene or narrative phase.
7. Optional style references showing the approved rendering approach.

**Prompt pattern:**

```text
[approved anchor], character model sheet, [requested views or poses],
consistent proportions and costume construction, clear labeled callouts
where supported, clean neutral background, [animation or narrative art style].
```

The model sheet should be reproducible by another artist. Avoid camera angles, lighting, or effects that hide the construction of the character. Keep turnaround views neutral and reserve dramatic poses for a separate pose sheet.

### Workflow: Other formats

If the user describes a format not listed above:

1. Identify how and where the character will be used.
2. Determine the required image dimensions, views, pose states, and production constraints.
3. Select the closest workflow above as a starting point.
4. Add or remove deliverables to match the actual use case.
5. Record the custom workflow in the character bible so future work remains consistent.

---

## Consistency Techniques

Use the simplest technique that satisfies the project's consistency needs. Do not require a particular backend feature.

| Technique | Typical usefulness | Effort | Best use |
|---|---|---|---|
| Approved Description Anchor | Medium to high | Low | All projects; the baseline method. |
| Reference-image conditioning | High when well supported | Low to medium | Maintaining face, clothing, and silhouette across views. |
| Image-to-image from an approved image | Medium to high | Medium | Pose, outfit, and scene variations. |
| Consistent seed and prompt structure | Variable by backend | Low | Related variations when the backend supports seed control. |
| Color palette sheet | High for color continuity | Low | All projects with recurring character assets. |
| Pose / structure controls | Backend-dependent | Medium | Turnarounds, sprites, and animation frames. |
| Character LoRA or equivalent trained identity model | Potentially high | High | Long-running projects with sufficient approved training images. |

A practical layered workflow is: **approved anchor + palette sheet + reference image + consistent prompt structure**, adding seed control or a trained character model only when available and useful.

### Seeds and backend-specific controls

- A seed may help reproduce or vary an image in some systems, but it does not guarantee identical character details across different prompts or backends.
- Reference-image controls may have backend-specific strength settings and limitations. Test them rather than assuming a universal value.
- Keep the original approved reference images and prompts so the project can be recreated or migrated to another tool.
- Never make a feature such as `--cref`, IP-Adapter, ControlNet, FLUX Redux, or a CLI command mandatory. Treat named technologies as examples only.

### Character model training (LoRA and equivalents)

Consider a trained character model only when the project requires many images of the same character and the chosen backend supports training. A collection of approximately 10–20 carefully curated images may be a useful starting point for some workflows, but the actual data requirements depend on the model and training service.

General practices:

1. Use only approved images that consistently represent the character.
2. Include varied views and poses while preserving identity and style.
3. Crop and caption images according to the training service's guidance.
4. Use a unique trigger token if the platform requires one.
5. Test the trained model against the approved turnaround and palette.
6. Keep versioned copies of training data and model settings.
7. Do not promise perfect consistency; inspect every result and correct drift.

Training is optional. For small projects, an anchor and approved reference images are usually a simpler starting point.

---

## Common Consistency Failures and Fixes

| Issue | Why it happens | Mitigation |
|---|---|---|
| Hair color drift | Color descriptions are too broad or underemphasized. | Record the exact shade and reuse it early in the anchor. |
| Eye color changes | Small facial details may be overlooked. | State eye color clearly and include a face reference. |
| Outfit inconsistency | Unspecified garment layers are filled in creatively. | Describe each layer, material, color, and silhouette. |
| Age shifts | Terms such as "young" are ambiguous. | Use a specific age or apparent-age range. |
| Face structure changes | Independent generations reinterpret the face. | Reuse an approved portrait and reference conditioning when available. |
| Proportion drift | Style and body proportions are not explicit. | State the proportion style and retain it across views. |
| Class / role drift | Class labels alone do not define appearance. | Translate the role into clothing, posture, equipment, and tools. |
| Mechanical mismatch | Art contradicts the character's game information. | Cross-check equipment and visible abilities against the character bible. |
| Faction emblem changes | Small symbols are easy to reinterpret. | Create a separate emblem reference and reuse it consistently. |
| Weapon scale changes | The generator exaggerates or shrinks props. | Specify relative size, grip, material, and carrying position. |
| MMO gear tier bleed | Each equipment tier is regenerated as a new character. | Lock the body and face anchor; change only the approved gear block. |
| LARP concept is impractical | Imaginary materials and unsafe props are not buildable. | Translate the design into real materials and check event safety rules. |
| Sprite frames drift | Each frame is generated independently. | Establish a canonical key pose and use compatible reference or animation controls. |
| Too much detail at small size | The asset is not designed for its actual display scale. | Simplify the silhouette and prioritize high-value visual hooks. |
| Overdesigned character | Decorative elements obscure the role or silhouette. | Remove details that do not support identity, function, or story. |

---

## RPG Character Bible Template

Maintain one character bible per character. It is the single source of truth for visual identity, game information, and approved variants. Update it when the user approves a change; do not silently overwrite established facts.

```markdown
# Character: [Name]

## Project and Format
- Primary format: [TRPG / CRPG / MMORPG / LARP / Solo / Animation / Other]
- Secondary formats: [Optional]
- Subgenre / setting: [Fantasy / sci-fi / horror / etc.]
- Game system: [Optional]
- Intended use: [VTT / game asset / LARP kit / gamebook / animation / etc.]

## Identity
- Name / alias:
- Age / apparent age:
- Gender / pronouns:
- Ancestry / race / species:
- Class / archetype / role:
- Subclass / specialization:
- Level / rank / tier:
- Background / origin:

## Attributes and Mechanics
- Primary attributes:
- Secondary attributes:
- Derived values:
- Alignment / morality (if applicable):
- Relevant skills / proficiencies:
- Languages:

## Visual Hooks (preserve across relevant assets)
1. [Hook 1]
2. [Hook 2]
3. [Hook 3]
4. [Hook 4 — optional]
5. [Hook 5 — optional]

## Approved Description Anchor
[Paste the approved 50–120 word visual anchor here.]

## Appearance
- Height / build / body type:
- Skin tone:
- Hair color / length / style:
- Eye color:
- Distinctive marks:
- Proportions:
- Art style:
- Voice / accent (if relevant):

## Color Palette
| Element | Hex | Notes |
|---|---|---|
| Skin | #______ | |
| Hair | #______ | |
| Eyes | #______ | |
| Primary outfit | #______ | |
| Accent | #______ | |
| Metal / material | #______ | |

## Current Equipment
- Primary weapon:
- Secondary / off-hand:
- Ranged weapon:
- Armor:
- Base clothing layer:
- Mid clothing layer:
- Outer clothing layer:
- Footwear:
- Accessories:
- Tools / kits:
- Signature item:
- Faction insignia:

## Alternate Outfits / Loadouts
- Casual:
- Formal:
- Combat:
- Stealth:
- Ceremonial:
- Other:
- (MMORPG) Starter / Dungeon / Raid / Cosmetic:

## Magic and Abilities
- Known spells / abilities:
- Signature move:
- Passive traits:
- Visible effects:
- Class resource:

## Faction and Relationships
- Faction / guild / order:
- Rank:
- Patron / deity:
- Allies:
- Rivals / enemies:

## Narrative
- Background:
- Motivation / goal:
- Flaw / secret:
- Bond:
- Quote / catchphrase:

## Approved Reference Assets
- Canonical portrait:
- Turnaround sheet:
- Expression sheet:
- Pose sheet:
- Palette sheet:
- Outfit / equipment sheets:
- Token / sprite / UI portrait:
- Faction emblem:
- Other:

## Generation / Model Notes (optional)
- Backend / service:
- Reference-image settings:
- Seed (if supported):
- Trained model / LoRA (if any):
- Trigger token (if any):
- Version:
- Notes:

## Change Log
- [Date or version] — [Approved change and reason]
```

---

## Final Quality Checklist

Before presenting a completed design sheet, verify the following:

- [ ] The user answered all three mandatory intake questions.
- [ ] The primary RPG format and subgenre are correctly identified.
- [ ] Reference material was analyzed and the anchor was confirmed when applicable.
- [ ] The design respects the user's setting, game system, and supplied facts.
- [ ] The character's class, ancestry, equipment, and abilities agree with the character bible.
- [ ] The Description Anchor is specific and consistent.
- [ ] Three to five visual hooks are preserved where practical.
- [ ] Important colors, proportions, clothing layers, and equipment are documented.
- [ ] The requested views and deliverables match the selected RPG format.
- [ ] Small-scale assets remain readable at their intended size.
- [ ] Variants change only the features the user approved.
- [ ] LARP props and costume recommendations respect event safety and accessibility requirements.
- [ ] The user is told what is complete and what remains optional or unavailable in the selected backend.

## Output and Handoff

When presenting the result:

1. State the selected format, subgenre, and intended use.
2. Present the approved character concept and Description Anchor.
3. Provide the relevant character-sheet fields and visual hooks.
4. Create or describe only the reference sheets required for that format.
5. Keep prompts and backend settings separate from canonical character facts.
6. Identify any assumptions or unresolved fields explicitly.
7. Provide the character bible so future generations can preserve continuity.

Do not claim that images, files, model training, or external operations were completed unless the available tools actually completed them. If a requested output is unsupported by the current backend, explain the limitation and provide the best tool-independent prompt or production specification instead.
