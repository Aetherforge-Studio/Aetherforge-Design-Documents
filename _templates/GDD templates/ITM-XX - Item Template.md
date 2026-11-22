<%*
let title = tp.file.title;
if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("ITM-XX - Item Name");
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
  - item
category: 
purpose: 
---
# Item Name

_Briefly describe the item, its purpose, and what makes it noteworthy. This should be a concise introduction rather than a complete specification._

## Overview

|Field|Details|
|---|---|
|Category|[Weapon, consumable, material, etc.]|
|Item type|[Specific subtype]|
|Rarity / Quality|[If applicable]|
|Value|[Base value, if applicable]|
|Stackable|[Yes / No / Limit]|
|Unique|[Yes / No]|

## Description & Presentation

_Describe the item's appearance and how it is presented to the player._

- **Description:** [Player-facing description]
- **Appearance:** [Visual description]
- **Icon:** [Icon or reference]
- **Flavor text:** [Optional descriptive text]
- **Visual references:** [Links or images]

## Purpose & Function

_Explain what the item does, why it exists, and how it contributes to the gameplay experience._

- **Primary purpose:** [Purpose]
- **Function:** [What it does]
- **Player benefit:** [What the player gains]
- **Limitations:** [Restrictions or drawbacks]

## Stats & Attributes

_Document the item's numerical properties and gameplay statistics. Refer to the relevant gameplay systems for attribute definitions, formulas, and calculation rules._

### Base Attributes

- [Attribute]:: [Value]

### Derived Attributes

- [Statistic]:: [Value]

### Attribute Notes

- **[Attribute]:** [Explanation or design rationale]

## Usage & Requirements

_Describe how and when the item can be used, including any requirements or restrictions. Detailed usage mechanics belong in the relevant gameplay system._

- **Usage:** [How it is used]
- **Requirements:** [Prerequisites]
- **Restrictions:** [Limitations]
- **Effects:** [Result of use]
- **Duration:** [If applicable]

## Acquisition

_Document how the player obtains this item and any relevant conditions or limitations._

- **Sources:** [Vendors, crafting, drops, quests, exploration, etc.]
- **Requirements:** [Conditions for obtaining it]
- **Availability:** [When or where it can be obtained]
- **Quantity:** [If relevant]

## Upgrades & Variants

_Document upgrades, modifications, alternate forms, or related versions of the item._

|Variant|Differences|Requirements|
|---|---|---|
|[Variant]|[Changes]|[Requirements]|

## Lore & Significance

_Describe the item's history, cultural significance, narrative relevance, or other background information where applicable._

[Relevant lore and narrative details.]

## References

_Collect visual, historical, literary, or other references that inform the item's design._

- [Reference]
## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-07 - Items & Equipment]] · [[GDD-01 - Gameplay]] · [[GDD-05 - Characters]]
