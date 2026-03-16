# project_config

A centralized collection of reusable configuration/content files for public personal projects.

This repository is intended to keep profile and portfolio-related data in one place so multiple apps/sites can consume a consistent source of truth.

## Purpose

Instead of duplicating profile/project metadata across repositories, this repo stores shared configuration that can be reused by:

- portfolio websites
- project showcase pages
- personal profile dashboards

## Current Contents

### `portfolio-content.sample.json`

Sample structured content for a personal portfolio application.

Main sections include:

- `typewriterStrings` – rotating hero/intro text
- `projects` – project cards (image, title, description, source/demo links)
- `skillset` – technical skills with icon identifiers
- `tools` – tooling/platform icons and labels
- `socialLinks` – social profiles and icon identifiers
- `contact` – public contact-related links (e.g., CV URL)

## How to Use

1. Copy `portfolio-content.sample.json` into your consuming project (e.g., as `portfolio-content.json`).
2. Replace sample values with your own public-safe content.
3. Load the JSON in your app and map fields to UI components.

You can consume this repository in different ways:

- copy files manually
- add as a git submodule/subtree
- fetch raw JSON from a hosted branch/tag

## Data Conventions

- Keep all URLs valid and publicly accessible.
- Keep icon names aligned with your UI icon library (e.g., React Icons naming).
- Use `isBlog` as a feature flag if the consuming app differentiates project/blog cards.
- Prefer backward-compatible changes when adding new fields.

## Privacy & Security

This repository is for **public** configuration only.

Do **not** include:

- API keys
- tokens/secrets
- private personal information

## Extending This Repo

When adding new config files:

1. Follow a clear, predictable JSON shape.
2. Include a `*.sample.json` version where possible.
3. Update this README with the new file and field descriptions.
