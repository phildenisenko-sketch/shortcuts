# 🧭 Visual Style Router

Image Shortcuts uses two different kinds of intent:

1. **WHAT** — what the user wants to make: portrait, fashion campaign, paparazzi photo, travel image, LinkedIn portrait, product shot, carousel, etc.
2. **HOW** — the visual point of view: Editorial Minimalism, Surreal Minimalism, 90s Cinema, Flash Tabloid, and so on.

The user normally only needs to describe **WHAT**. The router supplies **HOW** automatically.

## Priority order

1. Explicit user visual direction.
2. Explicit `/style` or `/surprise` command.
3. Strong semantic intent from the request.
4. Default Visual DNA selection from `VISUAL-DNA.md`.
5. Never fall back to a bland generic style merely because the user did not specify an aesthetic.

## Examples

| User says | WHAT | HOW candidates |
|---|---|---|
| «Сделай рекламу моей футболки» | fashion/product campaign | Editorial Minimalism, Surreal Minimalism, Experimental Optical |
| «Сделай меня для LinkedIn» | professional portrait | Magazine Portrait, Editorial Minimalism, Quiet Humanism |
| «Сделай меня как будто меня поймали папарацци» | paparazzi | Flash Tabloid, Raw Documentary, Urban 2000s Grit |
| «Сделай кинематографичное фото ночью» | cinematic night scene | 90s Cinema, New Hollywood Intimacy, Dreamscape |
| «Сделай рекламу нижнего белья» | fashion/product campaign | Dark Luxury, Surreal Minimalism, Dreamscape |
| «Сделай фото в путешествии» | travel | Cinematic Travel, Surreal Minimalism, Quiet Humanism |
| «Сделай динамичный кадр бегуна» | action/sports | Hyperreal Sports Campaign, Experimental Optical |
| «Сделай фото для сайта знакомств» | dating portrait | Magazine Portrait, New Hollywood Intimacy, Urban 2000s Grit |
| «Сделай крутой tech-портрет» | technology portrait | Neo-Futurist, Experimental Optical |
| «Сделай красивую фотографию еды» | food/product | Editorial Minimalism, Pop Graphic Studio, Dark Luxury |

These are starting points, not rigid mappings.

## `/surprise`

`/surprise` is the Image Shortcuts equivalent of a visual **I'm Feeling Lucky** button.

When invoked:

- select one Visual School from the 20-style library;
- preserve the user's subject, identity, product and explicit constraints;
- choose a style that is materially different from the previous `/surprise` result when possible;
- do not merely randomize camera settings;
- randomize the **creative direction**.

If the user says `again`, `ещё раз`, or repeats `/surprise`, use another Visual School rather than repeating the previous one.

## Explicit style

The user may select a style directly using its name or a future shortcut alias, for example:

```text
/visual:surreal-minimalism
```

or simply:

```text
Сделай это в Surreal Minimalism.
```

The explicit style takes priority over automatic selection.

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

The same Visual DNA should produce a recognizable family resemblance while adapting its concrete scene decisions to the task.

## Output profiles are separate

Do not confuse Visual DNA with output formatting.

For example:

```text
WHAT: Instagram carousel
HOW: Dark Luxury
OUTPUT: 4:5 coherent series
```

The Visual DNA controls the creative language. The output profile controls aspect ratio, series count, continuity, safe zones and other delivery requirements.

## User intent beats style defaults

If the user says:

> «Сделай обычное документальное фото без художественной обработки»

do not force a Visual School.

If the user says:

> «Сделай максимально странно и сюрреалистично»

prefer Surreal Minimalism or Experimental Optical even if another style would normally be mapped to the intent.

The goal is not to make every image weird. The goal is to make default images **intentional rather than generic**.
