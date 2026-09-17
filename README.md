# ✨ Image Shortcuts

> **Give AI a visual point of view.**
>
> Опиши, что ты хочешь получить. Image Shortcuts поможет решить, **как это должно выглядеть** — через библиотеку из 20 характерных Visual Schools.

![Version](https://img.shields.io/badge/version-2.1-4F46E5)
![Visual DNA](https://img.shields.io/badge/Visual%20DNA-20%20schools-FFBF00)
![License](https://img.shields.io/badge/License-MIT-green)

## 🎨 Идея

Современные AI-модели уже умеют делать хорошие фотографии. Поэтому Image Shortcuts не пытается конкурировать с ними списком длинных prompt recipes.

Новая идея проще:

> **Пользователь говорит WHAT. Image Shortcuts добавляет HOW.**

Ты можешь попросить:

```text
Сделай рекламу моей футболки на модели.
```

И получить не очередную нейтральную AI-fashion фотографию, а изображение с осознанной визуальной режиссурой.

Image Shortcuts добавляет к любой задаче одну из 20 **Visual Schools** — переносимых визуальных языков, которые меняют пространство, постановку, свет, цвет, композицию, материалы, атмосферу и характер кадра.

## 🚀 Начните здесь

### 1. 🧠 Подключите Image Shortcuts

👉 **[PROMPT.md](PROMPT.md)** — готовый текст, который можно один раз вставить в ChatGPT, Gemini, Claude или другую AI-систему.

### 2. 🎨 Изучите Visual DNA

👉 **[VISUAL-DNA.md](VISUAL-DNA.md)** — библиотека из 20 визуальных школ.

В ней есть:

- Editorial Minimalism
- Surreal Minimalism
- Raw Documentary
- 90s Cinema
- Flash Tabloid
- Dark Luxury
- Maximalist Narrative
- Cinematic Travel
- Magazine Portrait
- New Hollywood Intimacy
- Urban 2000s Grit
- Scandinavian Quiet
- Analog Family Album
- Hyperreal Sports Campaign
- Neo-Futurist
- Dreamscape
- Pop Graphic Studio
- Brutalist Editorial
- Quiet Humanism
- Experimental Optical

Каждая школа задаёт не просто цвет или объектив, а **характер визуального мира**.

👉 **[STYLE-SYSTEM.md](STYLE-SYSTEM.md)** — архитектура системы, правила выбора и принцип работы Visual Schools.

### 3. 🎲 Попробуйте `/surprise`

`/surprise` — это **I'm Feeling Lucky для изображений**.

```text
/surprise

Сделай из этой фотографии необычный портрет.
```

Image Shortcuts выберет одну из 20 Visual Schools и адаптирует её под задачу. Если попросить ещё раз, система постарается выбрать другой визуальный язык.

Не понравилось? Просто:

```text
/surprise
```

Никаких промтов придумывать не нужно.

### 4. 🧭 Посмотрите, как работает роутер

👉 **[STYLE-ROUTER.md](STYLE-ROUTER.md)** — правила автоматического выбора Visual School.

Пользователь может вообще не знать названий стилей.

Например:

```text
Сделай меня для LinkedIn.
```

система сама определит задачу как professional portrait и выберет подходящую визуальную школу.

Или:

```text
Сделай рекламу нижнего белья.
```

Visual DNA адаптируется под commercial fashion.

## 📸 Где это работает

Visual DNA специально сделан **переносимым между задачами**.

Одну и ту же визуальную школу можно применять к:

- твоим фотографиям;
- fashion и clothing campaigns;
- product photography;
- travel photos;
- paparazzi;
- LinkedIn;
- professional portraits;
- dating profiles;
- avatars;
- websites;
- social media;
- cinematic scenes;
- cars;
- sports;
- food;
- architecture;
- family и lifestyle photography.

То есть Visual DNA — это не категория фотографии. Это **визуальный характер**.

## 🧩 Старые shortcuts остаются

Старый каталог из 300+ команд остаётся совместимым.

👉 **[CATALOG.md](CATALOG.md)** — legacy vocabulary.

Например:

```text
/paparazzi
/35mm
/flashphoto
```

по-прежнему можно использовать явно.

Но новая архитектура не заставляет пользователя запоминать команды. Технические shortcuts теперь являются совместимым legacy-слоем, а не центром продукта.

## 🧠 Архитектура

```text
USER
  ↓
WHAT — intent
  ↓
HOW — Visual School
  ↓
OUTPUT — delivery profile
  ↓
IMAGE
```

### WHAT

Что нужно сделать:

`portrait` · `fashion` · `paparazzi` · `travel` · `LinkedIn` · `product` · `cinematic` · `action` · `dating` · `avatar` · etc.

### HOW

Как это должно выглядеть:

`Surreal Minimalism` · `90s Cinema` · `Dark Luxury` · `Raw Documentary` · etc.

### OUTPUT

Как доставить результат:

`Instagram` · `Carousel` · `LinkedIn` · `Avatar` · `Portrait` · `Story` · etc.

## 🎯 Главный принцип

Image Shortcuts не пытается сделать prompt длиннее.

Он добавляет **намерение и визуальную точку зрения**.

> **Describe what you want. Choose a visual world — or let Surprise choose one for you.**

## License

MIT.
