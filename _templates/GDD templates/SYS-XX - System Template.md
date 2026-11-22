<%*
let title = tp.file.title;
if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("SYS-XX - System Name");
	if (title) {
		await tp.file.rename(title);
	}
}

// Split at the first " - " into id and name
const separatorIndex = title.indexOf(" - ");
const id = separatorIndex !== -1 ? title.slice(0, separatorIndex).trim() : title;
const name = separatorIndex !== -1 ? title.slice(separatorIndex + 3).trim() : title;
%>---
id: <% id %>
name: <% name %>
status: Open
last_reviewed: <% tp.file.last_modified_date("YYYY-MM-DD") %>
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

## Edge Cases & Exceptions

_Document unusual situations, exceptional conditions, and behaviors that fall outside the system's normal rules. Explain how the system should handle these situations and any interactions that could produce unexpected results._

- [Edge case or exception]

## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-02 - Systems & Mechanics]] · [Related Systems] · [Related Game Design Document Page]