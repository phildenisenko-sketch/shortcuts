# 🎨 Image Shortcuts — Visual Style System

> **Image Shortcuts gives AI a visual point of view.**
>
> The user describes **what** they want. The Style System decides **how it should look**.

## 1. The product is a visual-direction layer

Image Shortcuts is not primarily a collection of camera presets or longer prompts.

Modern image models already understand common intents such as fashion, paparazzi, LinkedIn, travel, product photography and cinematic scenes. The value of Image Shortcuts is to add a deliberate **visual point of view** that the model does not have to invent on its own.

A Visual School is a reusable creative language made from:

- space and set design;
- subject behavior and posing;
- scale and visual hierarchy;
- lighting logic;
- color relationships;
- composition and negative space;
- styling and props;
- materials and surface treatment;
- photographic imperfections;
- atmosphere and narrative.

Camera settings are implementation details. They are never the identity of a Visual School by themselves.

## 2. Three independent layers

### WHAT — Intent

What the user is trying to create:

`portrait` · `fashion campaign` · `paparazzi` · `travel` · `LinkedIn` · `product` · `action` · `cinematic` · `dating` · `avatar` · `food` · `architecture` · etc.

### HOW — Visual School

The creative language applied to the intent:

`Editorial Minimalism` · `Surreal Minimalism` · `Raw Documentary` · `90s Cinema` · `Flash Tabloid` · `Dark Luxury` · `Maximalist Narrative` · `Cinematic Travel` · `Magazine Portrait` · `New Hollywood Intimacy` · `Urban 2000s Grit` · `Scandinavian Quiet` · `Analog Family Album` · `Hyperreal Sports Campaign` · `Neo-Futurist` · `Dreamscape` · `Pop Graphic Studio` · `Brutalist Editorial` · `Quiet Humanism` · `Experimental Optical`.

### OUTPUT — Delivery

How the result must be delivered:

`Instagram` · `Carousel` · `LinkedIn` · `Avatar` · `Portrait` · `Story` · `Website` · etc.

These layers are independent. A Visual School can travel across domains, while an Output Profile controls format and continuity.

## 3. Selection modes

Image Shortcuts has three modes.

### A. Automatic

If the user does not specify a visual direction, infer the intent and select a suitable Visual School.

The selection should be **intent-aware but not generic**. Use the candidate families in `STYLE-ROUTER.md`, then choose a school that creates a clear visual point of view while preserving the purpose of the image.

Do not always choose the same school for every task. Avoid repetitive defaults across consecutive requests when another suitable school is available.

### B. Explicit

If the user names a Visual School, that choice wins.

Examples:

```text
Сделай это в Surreal Minimalism.
```

```text
/visual:surreal-minimalism
```

The style name is a creative direction, not a requirement to reproduce a specific campaign, photograph, living artist or photographer.

### C. Surprise

`/surprise` is the visual equivalent of **I'm Feeling Lucky**.

It means:

> **Choose a strong visual direction for me.**

Rules:

1. Select one of the 20 Visual Schools.
2. Preserve the user's subject, identity, product, garment and explicit constraints.
3. Adapt the selected school to the user's intent.
4. Prefer a school materially different from the previous Surprise result.
5. Change the creative direction, not merely the lens, color grade or camera angle.
6. Do not announce the selected school unless the user asks.
7. If the user says `again`, `ещё раз`, or repeats `/surprise`, choose another suitable school.

Surprise is intentionally repeatable. The user can keep trying until one of the visual directions clicks.

## 4. What makes a school strong

A useful Visual School must create visible differences across several dimensions at once.

### Scene

Where is the image happening? What unusual environment, set or spatial relationship is created?

### Composition

How is the frame organized? What is deliberately centered, cropped, obscured, repeated, isolated or left empty?

### Subject direction

What is the person, product, vehicle or object doing? How does it behave rather than simply pose?

### Light

What is the source and motivation of the light? Is it hard, soft, practical, mixed, atmospheric, frontal or directional?

### Color

What is the palette and how are accents controlled? Avoid adding arbitrary color just to make an image look 'AI'.

### Materiality

How should skin, fabric, metal, glass, stone, paper, food or other surfaces behave under the chosen light?

### Imperfection

What small irregularities make the result photographic rather than synthetic? Use them intentionally and sparingly.

### Narrative

What story, tension, mood or human situation does the image imply?

A school that changes only one of these dimensions is usually too weak to be a Visual School.

## 5. Preserve, then transform

When a reference image is supplied:

1. Preserve what the user explicitly wants preserved.
2. Apply the Visual School around it.

Preserve by default:

- identity and recognizable facial features;
- important garment/product characteristics;
- requested body or subject continuity;
- explicit location or contextual constraints;
- safety and commercial-use constraints.

The Visual School may change lighting, framing, environment, pose, styling or photographic treatment when that is compatible with the request.

## 6. Output Profiles

Output Profiles solve delivery problems, not artistic direction.

For an Instagram carousel, for example, the system should infer a portrait-oriented social format, coherent series structure, identity/product continuity, useful variation between frames and composition that leaves room for interface or text when appropriate.

The user should not have to manually specify technical delivery requirements that are already implied by an obvious output request.

## 7. Legacy shortcuts

The original 300+ shortcut catalog remains available for compatibility.

Legacy commands such as `/35mm`, `/85mm`, `/hardlight` and `/flashphoto` can still be interpreted when explicitly requested.

They should not define the new product architecture. The new system is centered on **Visual Schools + Intent + Output**, with technical modifiers treated as optional implementation details.

## 8. Reference lineage

Visual Schools may document broad reference lineages such as fashion-editorial traditions, magazine photography, cinema eras, advertising languages or architectural photography.

Use references to explain the visual characteristics that informed a school. Do not treat the name of a brand, director or photographer as a magic prompt token.

The goal is to extract the underlying visual decisions and turn them into an original, reusable creative direction.

## 9. Product promise

The user should feel that Image Shortcuts changes the **point of view**, not just the prompt length.

> **Describe what you want. Choose a visual world — or let Surprise choose one for you.**
