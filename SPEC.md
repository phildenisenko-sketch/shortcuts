# ISS Specification

Image Shortcuts Standard (ISS) is a semantic shorthand dictionary for AI image generation and editing.

## Priority

1. Explicit user instruction.
2. User override of a shortcut.
3. More specific shortcut.
4. Default shortcut definition.
5. Model defaults.

Users are allowed to clarify, extend, temporarily redefine, or replace a shortcut's default behavior.

## Unknown shortcuts

If a shortcut is not in the active dictionary, look it up in the configured external dictionary if available. Otherwise ask the user instead of inventing a precise definition.

## Parameters

Use `/name:value`, for example `/series:6`, `/aspect:9x16`, or `/camera:35mm`.

## GitHub dictionary mode

A compatible AI system may use this repository as the source of truth when explicitly configured to do so.

Recommended system instruction:

> Treat the Image Shortcuts repository as the shortcut dictionary. Whenever the user writes a token beginning with "/", use the repository definition when needed. Apply the user's explicit instructions and overrides before the default shortcut. If a shortcut is missing, ask the user to define it.

A GitHub URL mentioned in a normal conversation does not automatically guarantee repository lookup.

## Safety

ISS does not override the safety, privacy, copyright, or platform rules of the model being used.
