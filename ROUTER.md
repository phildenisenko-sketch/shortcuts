# 🧭 Semantic Shortcut Router

Image Shortcuts should work by **meaning**, not by memorization.

The user does **not** need to know the exact slash command. AI should infer the user's visual intent and map ordinary language to the closest shortcut or combination of shortcuts.

## Core rule

If the user says:

> Сделай меня на улице Нью-Йорка, как будто меня снимает папарацци.

AI should internally select `/paparazzi` and apply its recipe. The user does not need to write `/paparazzi`.

If the user says:

> Сделай профессиональное фото для LinkedIn, но не как скучный корпоративный портрет.

AI should select `/linkedin` and preserve the user's explicit preference for a natural, non-stiff result.

If the user says:

> Сделай рекламную съёмку для моего бренда нижнего белья. Я загружу фото модели и изделия.

AI should select `/underwearcampaign` and treat the reference product and adult model as primary sources.

If the user says:

> Сделай карусель для Instagram.

AI should select `/carousel`, using the flagship 1080×1350 / 4:5 recipe.

## Routing algorithm

1. Read the user's entire request before choosing a shortcut.
2. Identify the **visual intent**: photography genre, commercial use, camera perspective, lighting, action, output format, mood, or editing constraint.
3. Match the intent to one or more shortcuts in `CATALOG.md`, `FLAGSHIP-30.md`, and `FLAGSHIP-EXTRA-5.md`.
4. Prefer a Flagship recipe when one exists.
5. Combine shortcuts when they affect different visual layers. Example: paparazzi + flash + full body.
6. Preserve explicit user instructions even when they differ from the shortcut default.
7. Do not force a shortcut merely because one word happens to match. Match by meaning and desired visual outcome.
8. If several shortcuts are plausible, choose the smallest useful combination rather than stacking unrelated styles.
9. If the intent is genuinely ambiguous and the difference would materially change the image, ask one concise clarification. Otherwise make the most natural match.
10. The user does not need to see the routing process or the full recipe unless they ask.

## Semantic examples

| User intent in ordinary language | Shortcut |
|---|---|
| «как папарацци», «будто меня подловили фотографы», «случайный снимок знаменитости» | `/paparazzi` |
| «естественный случайный кадр», «не позируй», «как будто фотограф поймал момент» | `/candid` |
| «уличная документальная фотография» | `/streetphoto` |
| «street style», «модная съёмка прямо на улице» | `/streetstyle` |
| «журнальная fashion-съёмка» | `/fashioneditorial` |
| «реклама коллекции», «fashion campaign» | `/fashioncampaign` |
| «как кадр из фильма» | `/cinematic` |
| «стоп-кадр из фильма» | `/filmstill` |
| «документальная фотография», «как настоящий репортаж» | `/documentary` |
| «профессиональный портрет» | `/portraitphoto` |
| «фото для LinkedIn», «профессиональное фото для профиля» | `/linkedin` |
| «снято с дрона», «вид сверху с воздуха» | `/droneview` |
| «снизу вверх», «камера у земли» | `/lowangle` |
| «широкоугольная естественная street перспектива» | `/35mm` |
| «естественная классическая перспектива» | `/50mm` |
| «классический портретный объектив» | `/85mm` |
| «снять издалека», «сжатая перспектива» | `/telephoto` |
| «размытый фон настоящей оптикой» | `/shallowdof` |
| «золотой час» | `/goldenhour` |
| «жёсткий прямой свет» | `/hardlight` |
| «мягкий студийный/оконный свет» | `/softlight` |
| «прямой вспышкой в лицо», «жёсткая on-camera flash» | `/flashphoto` |
| «плёночная фотография» | `/filmphoto` |
| «фото как в 90-х» | `/90sphoto` |
| «аниме» | `/anime` |
| «динамичный кадр движения», «спорт или действие в моменте» | `/action` |
| «фото с путешествия», «travel editorial» | `/travelphoto` |
| «профессиональная съёмка интерьера» | `/interior` |
| «фото товара для бренда» | `/productphoto` |
| «съёмка автомобиля» | `/carphoto` |
| «рекламная съёмка нижнего белья» | `/underwearcampaign` |
| «рекламная съёмка женского белья» | `/lingeriecampaign` |
| «визуал для Instagram» | `/instagram` |
| «карусель Instagram 1080×1350» | `/carousel` |

## Natural-language combinations

AI should also infer combinations when the request contains several independent intents.

Examples:

- «Папарацци на улице Нью-Йорка ночью, прямо со вспышкой» → `/paparazzi /flashphoto`
- «Профессиональный LinkedIn-портрет в современном офисе, но естественный» → `/linkedin /natural`
- «Динамичная фотография бегуна на улице с размытым фоном» → `/action /shallowdof`
- «Рекламная съёмка белья для бренда, вертикально для Instagram» → `/underwearcampaign /vertical`
- «Карусель Instagram для бренда одежды» → `/carousel /fashioncampaign`
- «Папарацци-снимок в стиле 90-х» → `/paparazzi /90sphoto`

The router should prefer semantic intent over exact wording. Russian, English and mixed-language requests should all work.

## Source of truth

- Full catalog: `CATALOG.md`
- Deep photographic recipes: `FLAGSHIP-30.md`
- Additional flagship recipes: `FLAGSHIP-EXTRA-5.md`
- Setup instructions: `PROMPT.md`

When a shortcut exists in the repository, its repository definition is authoritative. The slash syntax is an optional user-facing shorthand, not a requirement for the AI to recognize the intent.
