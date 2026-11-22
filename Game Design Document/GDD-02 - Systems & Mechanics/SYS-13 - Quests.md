---
id: SYS-13
name: Quests
status: Open
last_reviewed: 2026-11-21
tags:
  - system
does:
reads_from:
feeds_into:
sub_systems: []
parent_system: 
---
## Overview

_Summarize the system's purpose, primary responsibilities, and scope. Explain what it governs and establish the boundaries between this system and related systems._

## Design Goals

_Describe what the system is intended to accomplish and the experience it should provide. Identify the design principles and goals that guide decisions about its behavior and features._

- [Goal or design principle]

## Mechanics & Rules

_Describe the mechanics that govern how the system works. Document its core functionality, rules, conditions, restrictions, and expected behavior during normal gameplay._

- [Mechanic or rule]

## Player Experience

_Describe how the player encounters, accesses, and interacts with the system. Document the information and feedback presented to the player, along with any interface or usability considerations that affect the experience._

- [Player-facing behavior or consideration]

## Progression & Customization

_Describe how the system changes throughout the game and what aspects can be customized or influenced by the player. Document relevant unlocks, upgrades, scaling, and configuration options._

- [Progression or configuration detail]

## System Integration

_Describe how this system interacts with other gameplay systems. Identify its dependencies, the information or resources it receives, what it provides to other systems, and how these interactions affect gameplay._

- [Related system and interaction]

## Content & Data

_Document the content and data associated with this system. Identify relevant content collections, properties, variables, configuration values, and supporting documents. Link to individual content documents or external data sources where appropriate._

- [Content or data reference]

```dataviewjs
// Configuration
const includeCurrentFile = false; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "SYS-13 - Quests";
const title = "Quests";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path)
	.where(p => p.file.name.startsWith("QST-"));
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name
	])
)
```

## Edge Cases & Exceptions

_Document unusual situations, exceptional conditions, and behaviors that fall outside the system's normal rules. Explain how the system should handle these situations and any interactions that could produce unexpected results._

- [Edge case or exception]

## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-02 - Systems & Mechanics]] · [Related Systems] · [Related Game Design Document Page]
