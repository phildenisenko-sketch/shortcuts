# 🔬 Recipe Refinements v1

This file contains the refined recipes for shortcuts that have been reviewed against current prompt-library and photography-prompt references.

The goal is not to make recipes longer for their own sake. The goal is to increase **information density**: camera position, shot behavior, lens, exposure, light behavior, focus behavior, composition and photographic artifacts should all point toward one recognizable result.

Sources reviewed include PromptHero paparazzi examples, Techpresso's tested paparazzi prompt collection, PromptsEdge's photography library, Postcrest's photography/fashion prompt guidance, Adobe Firefly prompt guidance, and open photographic prompt-builder libraries. These sources repeatedly emphasize concrete camera/lens language, shot type, lighting setup, depth of field, movement, color/film cues and realistic imperfections over generic quality adjectives.

## `/paparazzi` — refined recipe

```text
Treat this as a real paparazzi photograph captured opportunistically from outside the subject's interaction, not as a fashion portrait pretending to be candid. The photographer is physically separated from the subject and reacts quickly to an unscripted moment: walking, crossing a street, entering or leaving a building, getting into a car, looking away, turning mid-step, talking or adjusting clothing. Use a full-frame camera with a 70–200mm telephoto lens around 135–200mm, typically f/2.8, from a believable distance. Use fast shutter speed around 1/500–1/1000s for a daylight walking frame, allowing only small natural motion blur when timing is imperfect. In daylight, use available light with realistic exposure; in low light or nightlife, use direct on-camera flash that creates hard frontal illumination, bright highlights, visible shadow falloff and slightly imperfect exposure. Keep the subject's face or decisive body area sharply focused while background pedestrians, cars and architecture show natural telephoto compression and optical blur. Build the frame with incidental foreground obstruction when appropriate: a passing person, car edge, pole, doorway or photographer partially entering the frame. Allow imperfect timing, uneven crop, off-center composition, slight camera tilt, visible street clutter, reflections and small exposure inconsistencies. Preserve pores, fine hair, fabric weave, wrinkles and natural body proportions. For a tabloid-era variant, allow high-ISO grain, stronger flash, blown highlights and slightly harsher color. The final image should look like evidence of a real photographer reacting in the street, not a model posing for an editorial shoot.
```

### Why this is stronger

The previous recipe already had lens, aperture, candid behavior and imperfections. The refined version adds the missing **capture mechanics** that repeatedly appear in tested prompt libraries:

- photographer distance and reaction rather than just "candid";
- explicit shot behavior and transitional moments;
- shutter-speed logic for walking/action;
- separate daylight vs direct-flash behavior;
- foreground obstruction and partial occlusion;
- optical focus behavior instead of generic blur;
- optional high-ISO/tabloid characteristics;
- crop, tilt and exposure imperfections as consequences of fast capture.

The key change is that `/paparazzi` now describes **why the frame looks accidental**, not merely that it is accidental.

## `/linkedin` — refined recipe

```text
Create a modern professional profile photograph that looks like it was actually taken by a portrait photographer for a real person's LinkedIn profile, not generated from a corporate headshot template. Use a full-frame camera with an 85mm lens around f/2.8–f/4, camera positioned at eye level and slightly farther back than a typical selfie. Frame from chest-up to mid-torso depending on the user's preference, leaving clean but natural headroom. Use soft window light or large open-shade daylight as the primary source, with gentle fill from the environment and realistic shadow definition across the face. Keep the eyes naturally sharp and preserve pores, fine hair, subtle skin variation and real fabric texture. Use a relaxed three-quarter or front-facing posture with shoulders slightly asymmetrical and a calm, confident micro-expression. Keep the background physically connected to the person: a real office, modern workspace, refined urban setting or softly blurred neutral environment, with enough recognizable context to avoid the feeling of a fake backdrop. Use moderate depth of field rather than extreme bokeh, neutral-to-warm professional color and restrained retouching. Clothing should remain faithful to the user's actual outfit or reference unless asked otherwise. Avoid plastic skin, fake office composites, excessive sharpening, perfect symmetry, exaggerated catchlights and stereotypical executive posing.
```

## Recipe construction standard

For future flagship refinements, prefer this order when relevant:

1. **Capture situation** — why and when the photograph was taken.
2. **Subject behavior** — what the person/object is physically doing.
3. **Camera position** — distance, height, angle and relationship to subject.
4. **Optics** — focal length, lens character and aperture.
5. **Exposure/motion** — shutter speed, ISO or motion behavior when they materially affect the look.
6. **Lighting** — source, direction, softness/hardness and interaction with materials.
7. **Focus/DOF** — what is sharp and how defocus transitions.
8. **Composition** — framing, layers, foreground/background and crop behavior.
9. **Material/anatomy realism** — skin, fabric, objects, proportions and physical interaction.
10. **Finish** — color, grain, contrast and restrained post-processing.
11. **Failure avoidance** — only the specific failure modes relevant to that recipe.

Do not mechanically fill every slot. Use only details that reinforce the intended visual result.
