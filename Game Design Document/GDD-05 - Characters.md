---
id: GDD-05
name: Characters
status: Open
last_reviewed: 2026-11-21
tags:
  - gdd
---
# Characters

_An overview of the characters who inhabit the game world and contribute to its story or gameplay. Use this page as a directory, with individual character profiles for detailed information about their identities, motivations, personalities, relationships, and development. Focus on who the characters are; their narrative roles belong in [[GDD-04 - Story & Narrative]], and dialogue mechanics belong in the [[SYS-14 - Dialogue]] system._

## Character Design Principles

_Describe the principles that guide character creation across the game. Consider what makes characters distinctive, how they fit into the setting and tone, and what qualities make them memorable or believable. These principles should provide a consistent foundation without making every character feel the same._

Potential topics:
- Character identity and distinctiveness
- Believability versus stylization
- Characterization through appearance and behavior
- How characters reinforce the game's design pillars
- Intended emotional connection with the player

## Character Roles & Functions

_Describe the kinds of roles characters fulfill and how they contribute to the player's experience. Consider narrative roles, gameplay functions, and the balance between major characters and supporting cast members._

Potential topics:
- Protagonists and supporting cast
- Companions and party members
- Mentors, rivals, antagonists
- Merchants, quest-givers, and service providers
- Enemies and major adversaries
- Background characters and ambient inhabitants

## Character Appearance & Presentation

_Document shared conventions for how characters look and are presented. Consider proportions, silhouettes, visual readability, animation style, and how appearance communicates identity, personality, or gameplay function._

Potential topics:
- Character proportions and visual style
- Silhouette readability
- Color and shape language
- Clothing, equipment, and visual distinctions
- Animation and expressive movement
- Visual differentiation between character categories

## Personality & Characterization

_Describe how characters are characterized and made distinct from one another. Consider how personality is communicated through behavior, dialogue, decisions, relationships, and interactions with the world._

Potential topics:
- Personality and behavioral conventions
- Character flaws and contradictions
- Motivations and conflicting desires
- Character growth and change
- How much characterization is predetermined versus player-defined

## Character Relationships

_Describe how relationships between characters are designed and represented. Consider how relationships develop, how characters influence one another, and whether relationships affect gameplay, narrative, or available interactions._

Potential topics:
- Relationship types and dynamics
- Friendship, rivalry, family, romance, allegiance
- Relationship progression
- Group dynamics
- Relationship-driven gameplay or narrative consequences

## Character Naming & Identity Conventions

_Document conventions for character names, identities, and identifying details. Consider naming patterns, titles, cultural influences, and any rules that help maintain consistency across the cast._

Potential topics:
- Naming conventions by culture, region, or species
- Titles and forms of address
- Pronouns and gender conventions
- Naming unique creatures or non-human characters
- Consistency in character identifiers
## Characters

_List the characters who have a meaningful role in the game. Keep entries concise, using the table to identify each character and provide a quick reference to their defining traits. Create an individual profile when a character needs more detailed documentation, and link it from the directory. Not every character needs a separate profile._

```dataviewjs
// Configuration
const includeCurrentFile = false; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "GDD-05 - Characters/PCs";
const title = "Playable Characters";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path)
	.where(p => p.file.name.startsWith("CHR-"));
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name", "Role", "Motivation", "Voice"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name,
		p.role,
		p.motivation,
		p.voice
	])
)
```

```dataviewjs
// Configuration
const includeCurrentFile = false; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "GDD-05 - Characters/NPCs";
const title = "Non-Playable Characters";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path)
	.where(p => p.file.name.startsWith("CHR-"));
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name", "Role", "Motivation", "Voice"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name,
		p.role,
		p.motivation,
		p.voice
	])
)
```

```dataviewjs
// Configuration
const includeCurrentFile = false; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "GDD-05 - Characters/Enemies";
const title = "Enemies";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path)
	.where(p => p.file.name.startsWith("CHR-"));
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name", "Role", "Motivation", "Voice"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name,
		p.role,
		p.motivation,
		p.voice
	])
)
```

```dataviewjs
// Configuration
const includeCurrentFile = false; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "GDD-05 - Characters/Bosses";
const title = "Bosses";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path)
	.where(p => p.file.name.startsWith("CHR-"));
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name", "Role", "Motivation", "Voice"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name,
		p.role,
		p.motivation,
		p.voice
	])
)
```



```dataviewjs
// Configuration
const includeCurrentFile = false; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "GDD-05 - Characters";
const title = "Character Abilities";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path)
	.where(p => p.file.name.startsWith("CHR-"));
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name", "Attack", "Defense", "Magic", "Magic Defense", "HP", "MP"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name,
		p.attack,
		p.defense,
		p.magic,
		p.magic_defense,
		p.hp,
		p.mp
	])
);
```

## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-00 - Game Overview]] · [[GDD-04 - Story & Narrative]] · [[GDD-03 - World & Setting]] · [[GDD-08 - Art & Audio Direction]]
