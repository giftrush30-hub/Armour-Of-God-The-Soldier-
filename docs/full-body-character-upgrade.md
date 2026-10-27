# Full-Body Character Upgrade — Implementation Plan

## Goal
Upgrade the existing single-file prototype into a readable, full-body biblical combat game while preserving the current combat loop and mobile performance.

## Character silhouettes
- **David / male fighter:** adult human proportions; blue and gold palette; visible head, neck, shoulders, chest, both arms, hands, hips, both legs, knees, shins, and boots. Practical layered armour, cloth mantle, readable sword grip.
- **Deborah / female fighter:** adult human proportions and distinct silhouette; red and bronze palette; same complete visible anatomy and practical armour. Keep her face, hair, shoulder width, torso, hips, and movement distinct rather than recolouring the male model.
- Both characters must remain recognisable at phone-screen size. Avoid oversized heads, disconnected limbs, hidden hands, or armour that obscures the attack pose.

## Build order
1. **Preserve combat:** keep movement, blocking, sword timing, kicks, health, and existing controls working.
2. **Establish a common rig:** define consistent anchors for head, neck, shoulders, elbows, wrists, chest, pelvis, knees, ankles, and feet. Mirror only shared rig logic, not the final art.
3. **Build readable full-body shapes:** torso and pelvis first, then upper/lower arms, hands, thighs, shins, and boots. Layer armour over the body so joints remain legible.
4. **Bind animation to joints:** idle breathing, cape sway, guard, strike wind-up, impact, recovery, kick extension, hit reaction, and defeat. Keep the weapon attached to the hand through every pose.
5. **Combat readability:** attacks should have anticipation, clear contact timing, brief hit reaction, and recovery. Add impact effects only after body motion reads clearly.
6. **Mobile performance:** prefer lightweight SVG/canvas/vector shapes for the current prototype; avoid heavy real-time 3D assets until a stable playable version exists.
7. **Test:** verify both fighters in idle, walk/approach, block, sword attack, kick, hit, and victory/defeat states on a narrow mobile viewport.

## Art direction
- Premium, dramatic biblical-fantasy atmosphere, but the characters remain human and anatomically readable.
- David: blue/gold materials, controlled highlights, cloth mantle.
- Deborah: red/bronze materials, distinct hair and armour silhouette.
- Strong light/dark separation between skin, armour, cloth, weapon, and background.
- No graphic gore. Combat communicates through motion, impact flashes, sound cues, and non-graphic reactions.

## Acceptance checklist
- [ ] Full head and face visible.
- [ ] Both hands visible in neutral and attack poses.
- [ ] Shoulders, chest, waist/pelvis, both legs, knees, shins, and boots present.
- [ ] Weapon remains connected to the gripping hand.
- [ ] Male and female fighters are visibly distinct in silhouette and movement.
- [ ] Existing controls and combat timing still work.
- [ ] No clipping or detached limbs on a phone-sized screen.
- [ ] No claim of AI Scripture speech until the feature is actually wired to a reliable, reviewed Scripture library.
