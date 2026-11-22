---
id: GDD-07
name: Items & Equipment
status: Open
last_reviewed: 2026-11-21
tags:
  - gdd
---
# Items & Equipment

_An overview of the game's items and equipment, including their design conventions, categories, and intended roles in the player experience. Use this page as a directory of individual item documents and a reference for shared item-design principles. The mechanics governing inventory, equipment, crafting, acquisition, and item usage belong in their respective gameplay systems._


```dataviewjs
// Configuration
const includeCurrentFile = false; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "GDD-07 - Items and Equipment";
const title = "Items";

const currentFile = dv.current().file;
const rootFolder = currentFile.folder + `/${subFolder}`; // Gather all markdown files in the current folder and subfolders

let pages = dv.pages(rootFolder ? `"${rootFolder}"` : "")
	.where(p => includeCurrentFile || p.file.path !== currentFile.path)
	.where(p => p.file.name.startsWith("ITM-"));
	
if (sortAlphabetically) {
	pages = pages.sort(p => p.file.path, 'asc');
}

dv.paragraph(`## ${title}\n`);
dv.table(
	["ID", "Name", "Category", "Purpose"],
	pages.map(p => [
		dv.fileLink(p.file.path, false, p.id),
		p.name,
		p.category,
		p.purpose
	])
);
```

## Item Design Principles

_Describe the principles that guide item design throughout the game. Consider what makes items interesting, how they contribute to the player experience, and how they reinforce the game's identity and design pillars._

Potential topics:
- Items as tools, rewards, expressions of character, or narrative objects.
- Meaningful choices versus incremental upgrades.
- Utility and versatility.
- How items encourage exploration or experimentation.
- How item design supports the game's overall progression.

## Item Categories

_Define the broad categories used to organize items and explain what distinguishes each category. These categories should help establish consistent expectations for how items function and are presented._

Potential categories:
- Weapons
- Armor and clothing
- Accessories
- Tools
- Consumables
- Crafting materials
- Quest and key items
- Collectibles
- Miscellaneous items

## Item Properties & Attributes

_Document the shared properties and characteristics used to describe items. Establish which properties are common to most items and which are specific to particular categories._

Potential properties:
- Name and description
- Category and item type
- Rarity or quality
- Value or sell price
- Weight or size
- Stackability
- Durability
- Usability and restrictions
- Item-specific statistics

## Equipment Design Principles

_Describe the principles governing equipment and how it contributes to character capabilities and customization. Consider equipment categories, restrictions, trade-offs, and how equipment choices affect the player._

Potential topics:
- Equipment slots
- Equipment restrictions and requirements
- Equipment statistics
- Set bonuses or combinations
- Upgrade and modification conventions
- Visual representation and character customization

## Item Presentation & Description

_Document how items are presented to the player, including their names, descriptions, visual identity, and other identifying information. Consider how presentation communicates an item's purpose, history, quality, or significance._

Potential topics:
- Naming conventions
- Description style and length
- Icons and visual representations
- Rarity indicators
- Flavor text and lore
- Distinguishing functional information from descriptive text

## Unique & Special Items

_Describe how unique, named, legendary, or otherwise exceptional items are treated. Explain what distinguishes them from ordinary items and how their uniqueness is communicated to the player._

_Example (Bramblewick, a sample game): The Warden's Lantern is an old lantern once carried by the village's forest warden. Its light reveals faint traces of forgotten paths and markings left by those who once maintained the woodland. The player discovers it in an abandoned watchpost while exploring the forest. It cannot be purchased or crafted, and its significance comes from its connection to Bramblewick's history and its ability to reveal otherwise hidden details of the world._

## Item Balance & Progression

_Describe the principles used to maintain item balance and how items relate to the game's overall progression. Consider power curves, meaningful trade-offs, availability, and how new items remain relevant as the player advances._

## Development Notes

_Record unresolved questions, additional design considerations, and ideas for future development. Remove questions once they have been answered or document the resulting decisions in the relevant section._

- [ ] [Question, consideration, or idea]

Related: [[GDD-02 - Systems & Mechanics]] · [[GDD-01 - Gameplay]] · [[GDD-05 - Characters]]
