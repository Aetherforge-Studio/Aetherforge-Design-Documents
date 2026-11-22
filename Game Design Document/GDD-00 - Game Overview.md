---
id: GDD-00
name: Game Overview
status: Open
last_reviewed: 2026-11-21
tags:
  - gdd
---
# Game Overview

_How to use this template: italic lines are guidance. Replace them with your own words, then delete them. Values in square brackets are yours to fill in. Keep the overview content concise: it is the page everyone reads first, and every other part of the design is one link away._

```dataviewjs
// Configuration
const includeCurrentFile = true; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "";
const title = "Table of Contents";
const maxLevel = -1;  // -1 means no max

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path);
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

let toc = { files: [], indent: []}

for (const page of pages) {
	// Get the path relative to the root folder
	let relPath = rootFolder
		? page.file.path.slice(rootFolder.length + 1)
		: page.file.path;
	
	const parts = relPath.split("/");
	const fileName = parts.pop(); // Remove the filename, leaving on subfolders
	
	let currentLevel = parts.length;
	if (maxLevel < 0 || currentLevel < maxLevel) {
		toc.files.push(page);
		toc.indent.push(currentLevel);
	}
}

// Render table of contents
let output = `## ${title}\n`;
for (let i = 0; i < toc.files.length; i++) {
	for (let j = 0; j < toc.indent[i]; j++) {
		output += `\t`;
	}
	output += `- ${toc.files[i].file.link}\n`;
}

dv.paragraph(output);
```
## At A Glance

| Field          | Your game                                      |
| -------------- | ---------------------------------------------- |
| Working Title  | [Title]                                        |
| Logline        | [One sentence a stranger could repeat]         |
| Genre          | [Genre and subgenre]                           |
| Players        | [Single player, co-op for 2 to 4, competitive] |
| Platforms      | [PC, consoles, mobile]                         |
| Session Length | [A typical session, in minutes]                |
| Engine         | [Engine and version]                           |
| Team           | [Solo developer, team size, roles, etc.]       |
| Business Model | [Price, free to play, subscription]            |
_Example Logline (Bramblewick, a sample game): A wandering herbalist settles in a forgotten woodland village, gathering resources, restoring abandoned homes, uncovering the forest's history, and rebuilding a community one season at a time._
## Pitch

_Two or three sentences describing who the player is, what they do, and what makes the game distinctive. This should communicate the core concept clearly to someone unfamiliar with the project._

_Example (Bramblewick, a sample game): Restore Bramblewick, a quiet village hidden deep in an overgrown forest. Gather, craft, explore ancient ruins, and forge friendships with the woodland's curious inhabitants as you uncover why the village was abandoned. Your choices shape the community and the forest around it._

[Your pitch]

## Design Pillars

_Three to five principles that define the game's design identity and guide decisions. A pillar that could describe any game, such as “fun combat”, is not specific enough. Features should reinforce these pillars, and features that conflict with them should be reconsidered._

1. **[Pillar one]**: [what it means, in one sentence]
2. **[Pillar two]**: [what it means, in one sentence]
3. **[Pillar three]**: [what it means, in one sentence]

_Example (Bramblewick, a sample game): Restoration is the reward. Every resource gathered, structure repaired, and relationship built contributes to bringing the village back to life. Rebuilding a home reveals pieces of its history, attracts new residents, and creates new opportunities for the community. Progress is measured not just by what the player acquires, but by what the world becomes._

## Audience

_Who the game is intended for, what those players enjoy, their existing gaming habits, and what might cause them to disengage. Focus on actual player preferences and behaviors rather than demographics alone._

- Primary players: [Who they are and how they play]
- What they play today: [Three or four relevant games]
- They stop playing when: [What frustrates them, causes disengagement, or conflicts with their preferences]
- Secondary players: [Other audiences the game may appeal to]

## Comparable Games

_Three or four games that provide useful points of comparison for your design. Identify what you admire, what you want to learn from, or what you intend to adapt from each, as well as what you deliberately want to avoid. Comparisons can be about mechanics, pacing, presentation, player experience, or design philosophy._

| Game | What we take | What we leave |
| --- | --- | --- |
| [Game] | [...] | [...] |
| [Game] | [...] | [...] |
| [Game] | [...] | [...] |

## Scope

_Define the intended scope of the initial release or milestone. Identify what is included, what is explicitly excluded, and what has not yet been decided. This helps prevent scope creep and distinguishes planned features from speculative ideas._

- In scope: [...]
- Out of scope: [...]
- Open questions: [...]

