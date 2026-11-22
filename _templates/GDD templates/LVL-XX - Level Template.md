<%*
let title = tp.file.title;
if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("LVL-XX - Level Name");
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
  - level
purpose: 
main_mechanics: 
---
# Level Name

_Describe the level, its purpose, and the experience it is intended to provide. Keep this concise; detailed design belongs in the sections below._

## Overview

| Field            | Details                                       |
| ---------------- | --------------------------------------------- |
| Type             | [Level, region, dungeon, hub, mission, etc.]  |
| Location         | [Where it exists in the game world]           |
| Gameplay focus   | [Primary experience or activities]            |
| Estimated length | [Expected time or other relevant measurement] |
| Entry            | [How the player enters]                       |
| Exit             | [How the player leaves or progresses]         |

## Player Goals

_Describe what the player is expected or encouraged to accomplish in this environment. Include primary objectives and optional activities where relevant._

- **Primary objectives:** [Goals]
- **Optional objectives:** [Goals]
- **Exploration goals:** [Discoveries or activities]
- **Completion conditions:** [Conditions, if applicable]

## Layout & Structure

_Describe the physical or logical layout of the level and how its spaces connect. Include maps, diagrams, sketches, or other visual references where useful._

[Layout, map, diagram, or description.]

## Player Flow

_Describe how the player moves through the level and how the experience unfolds. Identify important transitions, routes, decision points, and areas of interest._

|Area or Segment|Player Experience|Transitions or Connections|
|---|---|---|
|[Area]|[Experience]|[Connection]|

## Encounters & Challenges

_Document the encounters, obstacles, challenges, and activities within the level. Include combat, puzzles, traversal challenges, environmental hazards, or other relevant content._

|Encounter or Challenge|Description|Purpose|
|---|---|---|
|[Encounter]|[Description]|[Purpose]|

## Mechanics & Interactions

_Document the mechanics, systems, and environmental interactions used within the level. Explain how they are introduced, used, combined, or tested._

- [Mechanic or interaction]

## Environmental Storytelling

_Describe how the environment communicates narrative, history, atmosphere, or other information to the player. Include visual details, objects, landmarks, and environmental events._

- [Detail]

## Resources & Rewards

_Document resources, rewards, discoveries, and other incentives found within the level. Include their placement and intended significance where relevant._

|Resource or Reward|Location|Purpose|
|---|---|---|
|[Reward]|[Location]|[Purpose]|

## Secrets & Optional Content

_Document hidden areas, optional activities, discoveries, and other content that rewards exploration. Describe how the player might discover them and what they offer._

- [Secret or optional content]

## Atmosphere & Presentation

_Describe the intended atmosphere and presentation of the level. Include environmental art, lighting, sound, music, ambient effects, and other elements that contribute to the experience._

- **Visual direction:** [Description]
- **Lighting:** [Description]
- **Sound and music:** [Description]
- **Atmosphere:** [Description]

## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-06 - Levels & Environment]] · [[GDD-01 - Gameplay]] · [[GDD-03 - World & Setting]] · [[GDD-04 - Story & Narrative]] · [[GDD-05 - Characters]]
