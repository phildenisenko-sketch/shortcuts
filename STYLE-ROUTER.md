# 🧭 Visual Style Router

Image Shortcuts separates three questions:

1. **WHAT** — what the user wants to make: portrait, fashion campaign, paparazzi photo, travel image, LinkedIn portrait, product shot, carousel, etc.
2. **HOW** — the visual point of view: one of the 20 Visual Schools in `VISUAL-DNA.md`.
3. **OUTPUT** — how the result should be delivered: Instagram, carousel, avatar, LinkedIn, story, website, etc.

The user normally only needs to describe **WHAT**. The router supplies **HOW** and **OUTPUT** when they are obvious.

## Priority order

1. Explicit user constraints and explicit visual direction.
2. `/surprise` or an explicit Visual School selection.
3. Strong semantic intent from the request.
4. Intent-aware Visual School selection from `VISUAL-DNA.md`.
5. Relevant Output Profile.
6. Never fall back to a bland generic AI look merely because the user did not specify an aesthetic.

## Automatic style selection

Automatic selection is **not random by default**. It should choose a Visual School that fits the task while creating a strong point of view.

Use the following as candidate families, not rigid mappings:

| User says | WHAT | HOW candidates |
|---|---|---|
| «Сделай рекламу моей футболки» | fashion/product campaign | Editorial Minimalism, Surreal Minimalism, Experimental Optical |
| «Сделай меня для LinkedIn» | professional portrait | Magazine Portrait, Editorial Minimalism, Quiet Humanism |
| «Сделай меня как будто меня поймали папарацци» | paparazzi | Flash Tabloid, Raw Documentary, Urban 2000s Grit |
| «Сделай кинематографичное фото ночью» | cinematic night scene | 90s Cinema, New Hollywood Intimacy, Dreamscape |
| «Сделай рекламу нижнего белья» | commercial fashion/product | Dark Luxury, Surreal Minimalism, Dreamscape, Editorial Minimalism |
| «Сделай фото в путешествии» | travel | Cinematic Travel, Surreal Minimalism, Quiet Humanism |
| «Сделай динамичный кадр бегуна» | action/sports | Hyperreal Sports Campaign, Experimental Optical |
| «Сделай фото для сайта знакомств» | dating portrait | Magazine Portrait, New Hollywood Intimacy, Urban 2000s Grit |
| «Сделай крутой tech-портрет» | technology portrait | Neo-Futurist, Experimental Optical |
| «Сделай красивую фотографию еды» | food/product | Editorial Minimalism, Pop Graphic Studio, Dark Luxury |

These are starting points. Do not force a style when the user's explicit direction clearly calls for another one.

## `/surprise`

`/surprise` is the Image Shortcuts equivalent of a visual **I'm Feeling Lucky** button.

When invoked:

- select one Visual School from the 20-style library;
- preserve the user's subject, identity, product, garment and explicit constraints;
- choose a school that is materially different from the previous Surprise result when possible;
- adapt the school to the user's intent rather than pasting the same recipe into every domain;
- change the creative direction, not merely camera settings;
- do not reveal the selected style unless the user asks.

If the user says `again`, `ещё раз`, or repeats `/surprise`, choose another suitable Visual School.

The user can keep trying until a visual direction feels right. Surprise is not a quality score or ranking. Every selected school is intended to be a deliberate creative option.

## Explicit style

The user may select a Visual School by name or alias:

```text
/visual:surreal-minimalism
```

or:

```text
Сделай это в Surreal Minimalism.
```

An explicit style takes priority over automatic style selection.

## Style + intent are independent

A Visual School must be portable across domains.

For example:

```text
WHAT: T-shirt campaign
HOW: Surreal Minimalism
```

```text
WHAT: LinkedIn portrait
HOW: Surreal Minimalism
```

```text
WHAT: Travel photo
HOW: Surreal Minimalism
```

The same Visual DNA should create a recognizable family resemblance while adapting concrete scene decisions to the task.

## Output is independent from style

Do not confuse Visual DNA with output formatting.

For example:

```text
WHAT: Instagram carousel
HOW: Dark Luxury
OUTPUT: portrait social carousel
```

The Visual DNA controls creative language. The Output Profile controls format, series structure, continuity, safe zones and other delivery requirements.

## User intent beats style defaults

If the user says:

> «Сделай обычное документальное фото без художественной обработки»

do not force a Visual School on top of that request.

If the user says:

> «Сделай максимально странно и сюрреалистично»

prefer Surreal Minimalism or Experimental Optical even if another style would normally be mapped to the intent.

The goal is not to make every image weird. The goal is to make default images **intentional rather than generic**.
