<%*
let title = tp.file.title;
if (title.startsWith("Untitled")) {
	title = await tp.system.prompt("CHR-XX - Character Name");
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
  - character
role: 
motivation: 
voice: 
---
# Character Name

_Briefly introduce the character, their place in the game, and why they matter. This should be a concise summary rather than a complete biography._

## Overview

|Field|Details|
|---|---|
|Full name|[Full name, if applicable]|
|Aliases / titles|[Other names, titles, nicknames]|
|Character type|[Playable character, NPC, enemy, boss, etc.]|
|Role|[Narrative and/or gameplay role]|
|Affiliation|[Organization, faction, community, etc.]|
|First appearance|[Where or when the player encounters them]|
## Appearance

_Describe the character's physical appearance and visual identity. Include distinctive features, clothing, equipment, and other details that help establish their appearance._

- **Physical description:** [Description]
- **Distinctive features:** [Features]
- **Clothing and equipment:** [Description]
- **Visual references:** [Links or references]

## Personality

_Describe the character's personality, temperament, behavior, and mannerisms. Explain what makes them distinctive and how those traits are expressed._

- **Personality traits:** [Traits]
- **Strengths:** [Strengths]
- **Flaws:** [Flaws]
- **Mannerisms:** [Habits, gestures, behaviors]
- **Values and beliefs:** [What they consider important]

## Motivations

_Describe what the character wants, what they need, and what drives their actions. Consider the difference between their conscious goals and underlying motivations._

- **Wants:** [Immediate desires or goals]
- **Needs:** [Deeper needs or personal growth]
- **Fears:** [Fears or insecurities]
- **Conflicts:** [Internal or external conflicts]
- **Motivations:** [What drives them]

## Background

_Document the character's history and experiences that are relevant to understanding who they are. Focus on information that informs their personality, motivations, relationships, or role in the game._

[Character history and relevant background.]

## Narrative Role

_Describe the character's contribution to the story. Explain their purpose, important story events, and how they relate to the larger narrative._

- **Story role:** [Role in the narrative]
- **Key events:** [Important appearances or contributions]
- **Character arc:** [How the character changes, if applicable]
- **Secrets and revelations:** [Information revealed over time, if applicable]

## Gameplay Role

_Describe how the character functions within the gameplay experience. Include abilities, services, interactions, or other gameplay contributions as appropriate._

- **Gameplay function:** [What the character does in gameplay]
- **Abilities or behaviors:** [Relevant capabilities]
- **Interactions:** [How the player interacts with them]
- **Related systems:** [Links to relevant system documentation]

## Relationships

_Document important relationships with other characters. Explain the nature of each relationship and how it influences the characters involved._

|Character|Relationship|Description|
|---|---|---|
|[[Character Name]]|[Relationship]|[Description]|

## Voice and Dialogue

_Describe how the character communicates, including speech patterns, vocabulary, tone, and distinctive expressions. Include sample dialogue where useful._

- **Speaking style:** [Description]
- **Vocabulary and phrasing:** [Description]
- **Tone:** [Description]
- **Sample dialogue:** [Examples]

## Stats & Attributes

_Document the character's gameplay statistics, attributes, and other numerical characteristics. Explain unusual values or distributions where they reflect the character's identity, abilities, background, or gameplay role. Refer to the relevant gameplay systems for definitions and calculation rules._

### Base Attributes

- [Attribute]:: [Value]

### Derived Attributes

- [Statistic]:: [Value]

### Attribute Notes

- **[Attribute]:** [Explanation or design rationale]

## ## References

_Collect visual, literary, historical, audio, or other references that inform the character's design._

- [Reference]

## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-04 - Story & Narrative]] · [[GDD-03 - World & Setting]] · [[GDD-05 - Characters]]
