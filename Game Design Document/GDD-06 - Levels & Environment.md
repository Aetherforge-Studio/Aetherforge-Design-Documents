---
id: GDD-06
name: Levels & Environment
status: Open
last_reviewed: 2026-11-21
tags:
  - gdd
---
# Levels & Environment

_An overview of the game's levels, areas, environments, and their design conventions. Use this page as a directory of individual level documents and a reference for shared level-design principles. Document the overall structure and intended player experience here; detailed layouts, encounters, and environmental content belong in individual level documents._

## Places and levels

_List the game's levels, areas, missions, or other distinct environments. Identify each location's purpose in the game and the mechanics or activities it emphasizes. Create an individual document when a location needs detailed design documentation. The structure and level of detail will vary depending on the game._

```dataviewjs
// Configuration
const includeCurrentFile = false; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "GDD-06 - Levels and Content";
const title = "Levels";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path)
	.where(p => p.file.name.startsWith("LVL-"));
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name", "Purpose In Game", "Main Mechanics"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name,
		p.purpose,
		p.main_mechanics
	])
)
```

## Level Design Principles

_Document the principles and conventions that guide level and environment design throughout the game. These rules help maintain a consistent player experience while allowing individual levels to serve different purposes. Document shared conventions here rather than repeating them in individual level documents._

Potential topics:
- **Navigation and guidance:** How players recognize paths, identify destinations, and understand where they can go.
- **Visual landmarks:** How landmarks are used for navigation, orientation, and memory.
- **Environmental readability:** How interactive elements, hazards, exits, and important objects are communicated.
- **Level pacing:** How exploration, action, tension, challenge, and respite are balanced.
- **Traversal:** Shared conventions for movement, obstacles, verticality, and navigation.
- **Checkpoints and recovery:** If applicable, how checkpoints, respawns, and recovery opportunities are distributed.
- **Secrets and optional content:** How hidden content is signaled and how discovery is rewarded.
- **Environmental storytelling:** How environments communicate history, narrative, and information.
- **Boundaries:** How the game communicates accessible areas, inaccessible areas, and intended routes.
## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-01 - Gameplay]] · [[GDD-03 - World & Setting]] · [[GDD-04 - Story & Narrative]] · [[GDD-05 - Characters]] · [[GDD-10 - Production Plans]]
