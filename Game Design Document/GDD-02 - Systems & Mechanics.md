---
id: GDD-02
name: Systems & Mechanics
status: Open
last_reviewed: <% tp.file.last_modified_date("YYYY-MM-DD") %>
tags:
  - gdd
---
# Systems & Mechanics

_Every system in the game, the rules it follows and the numbers behind it. Numbers change every week: keep them in tables or spreadsheets, and keep the reasoning here._

## Systems

_List the gameplay systems that make up the game and how they relate to one another. Identify what each system does, what information or resources it depends on, and what other systems it influences. Use these relationships to identify dependencies, integration points, and systems that deserve closer documentation._

```dataviewjs
// Configuration
const subFolder = "GDD-02 - Systems & Mechanics";
const title = "Systems & Mechanics";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => p.file.name.startsWith("SYS-"))
	.sort(p => p.id, 'asc');
	
dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name", "What It Does", "Reads From", "Feeds Into"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name,
		p.does,
		p.reads_from,
		p.feeds_into
	])
)
```


_Example (Bramblewick, a sample game): Restoration connects gathering, crafting, inventory, and the village population. Materials gathered in the forest become crafted supplies, which are used to repair abandoned homes. Restored homes attract new residents, expanding the village and creating new opportunities for the player._

## Tuning knobs

_Identify important balance and configuration values that affect multiple systems or influence the overall gameplay experience. Detailed values and tuning data belong in their respective system documents or supporting spreadsheets._

| Knob  | Current value | Range tested | Affects |
| ----- | ------------- | ------------ | ------- |
| [...] | [...]         | [...]        | [...]   |

## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-01 - Gameplay]] · [[GDD-06 - Levels & Environment]] · [[GDD-10 - Production Plans]]
