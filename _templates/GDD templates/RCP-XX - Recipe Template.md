<%*
let title = tp.file.title;
if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("RCP-XX - Recipe Name");
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
  - recipe
---
## Overview

_Summarize what the recipe produces, its purpose, and where it fits into the game's crafting or production systems._

- **Category:** 
- **Recipe Type:** 
- **Unlock Requirements:** 
- **Repeatable:** 

## Inputs & Requirements

_Document the materials, resources, tools, facilities, and other requirements needed to perform this recipe._

| Input | Quantity | Requirements or Conditions |
|---|---|---|
| [Material or resource] | [Amount] | [Condition] |

## Process

_Describe how the recipe is performed, including its steps, ordering, timing, and any choices or conditions that affect the process._

1. [Step]
2. [Step]
3. [Step]

## Outputs & Variations

_Document the products and byproducts created by the recipe, including quantities, quality variations, and conditional results where applicable._

| Output | Quantity | Conditions / Variations |
|---|---|---|
| [Product] | [Amount] | [Condition] |

## Acquisition & Unlocking

_Describe how the player discovers or obtains access to the recipe, including unlock conditions, sources, and any progression requirements._

## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[SYS-08 - Gathering & Resources]] · [[GDD-07 - Items & Equipment]]
