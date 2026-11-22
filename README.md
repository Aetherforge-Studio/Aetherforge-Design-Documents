# Aetherforge Game Development Documentation Template

An Obsidian-based documentation framework for game development, combining Game Design Documents (GDDs), Technical Design Documents (TDDs), Art Bibles, and Architecture Decision Records (ADRs) into an interconnected, customizable workspace.

This template was initially developed with JRPGs, cozy farming and life sims, and open-world survival/crafting games in mind. While its prepopulated systems and examples reflect those genres, the documentation structure is adaptable to a wide range of game projects.

## Features

- **Comprehensive documentation:** Templates for game design, technical design, art direction, and architectural decisions.
- **Modular structure:** Use, modify, or remove sections according to your project's needs.
- **Obsidian integration:** Uses Markdown, internal links, templates, Mermaid diagrams, and Dataview for organization and navigation.
- **Preconfigured workspace:** Includes Obsidian settings and plugin configuration to provide a functional documentation environment out of the box.
- **Expandable:** Supports high-level design documentation alongside detailed system and content documentation.
- **Genre-informed, not genre-locked:** Prepopulated gameplay systems provide a starting point for JRPGs, cozy sims, and survival/crafting games, but can be adapted to other genres.

## Documentation

The vault includes the following documentation frameworks:

### Game Design Document (GDD)

Documents the game's vision, gameplay, systems, world, narrative, characters, environments, items, interface, accessibility, and production considerations.

### Technical Design Document (TDD)

Provides a framework for documenting technical architecture, implementation details, and engineering considerations.

### Art Bible

Provides a framework for establishing visual direction, artistic conventions, asset specifications, and production guidelines.

### Architecture Decision Records (ADRs)

Provides a framework for recording significant architectural and technical decisions, including their context, rationale, and consequences.

## GDD Structure

The Game Design Document is organized into the following sections:

|Section|Purpose|
|---|---|
|Game Overview|Establishes the game's vision, design pillars, audience, scope, and identity.|
|Gameplay|Documents the core gameplay experience, loops, mechanics, controls, progression, and challenges.|
|Systems & Mechanics|Provides an overview and index of the game's gameplay systems.|
|World & Setting|Documents the world, setting, tone, and writing conventions.|
|Story & Narrative|Documents the narrative premise, structure, themes, choices, and story progression.|
|Characters|Establishes character design conventions and provides a directory of characters.|
|Levels & Environments|Establishes level design conventions and provides a directory of environments.|
|Items & Equipment|Establishes item design conventions and provides a directory of items.|
|Art & Audio Direction|Establishes the game's creative direction for visuals and audio.|
|Interface & Accessibility|Documents interface design, inputs, accessibility, and localization considerations.|
|Production Plans|Documents development strategy, team responsibilities, risks, and release considerations.|

Individual system and content documents provide additional detail where needed.

## Getting Started

1. Clone or download the repository.
2. Open the repository folder as a vault in Obsidian.
3. Open **Settings → Community plugins**.
4. Enable community plugins if they are disabled.
5. Enable the plugins included in the vault's configuration.
6. Begin adapting the documentation to your game.

The included `.obsidian` configuration directory provides workspace settings and plugin configuration. Plugin availability and functionality may depend on your Obsidian installation and version.

Review the templates and documentation structure before beginning. Remove or adapt sections that aren't relevant to your project.

## Requirements

- [Obsidian](https://obsidian.md/)
- Community plugins

### Required Plugins

The following community plugins are required for the vault's intended functionality.

| Plugin                                                                       | Purpose                                                                    |
| ---------------------------------------------------------------------------- | -------------------------------------------------------------------------- |
| [Dataview](https://github.com/blacksmithgu/obsidian-dataview)                | Generates dynamic tables, indexes, and table of contents.                  |
| [Templater](https://github.com/SilentVoid13/Templater)                       | Automatically applies templates when creating notes in designated folders. |
| [Kanban Bases View](https://community.obsidian.md/plugins/kanban-bases-view) | Provides the Kanban board used to track documentation status.              |

### Recommended Plugins

These plugins aren't required for the vault to function, but provide useful features.

| Plugin                                                               | Purpose                                                                                   |
| -------------------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| [Metadata Menu](https://community.obsidian.md/plugins/metadata-menu) | Provides dropdowns and other controls for managing metadata, including document statuses. |
| [Git](https://community.obsidian.md/plugins/obsidian-git)            | Provides Git integration within Obsidian for version control.                             |

### Optional Plugins

These plugins are included in the configuration but aren't required for the template's functionality.

| Plugin                                                                       | Purpose                                                                                        |
| ---------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------- |
| [Open Tab Settings](https://community.obsidian.md/plugins/open-tab-settings) | Customizes tab behavior to provide a workflow more similar to IDEs such as Visual Studio Code. |

Mermaid diagram support is provided natively by Obsidian and does not require an additional plugin.

## Philosophy

Game documentation should support the development process, not become an obstacle to it.

This vault is intended to provide structure, improve communication, and help developers organize their design and technical decisions. It is a starting point rather than a rigid specification.

Use the documentation that helps your project. Modify it as your game evolves.

## License

This repository is dedicated to the public domain under [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).

You are free to copy, modify, adapt, use, and distribute this template for any purpose without permission or attribution.