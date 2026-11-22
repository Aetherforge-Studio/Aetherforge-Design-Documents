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
date: <% tp.file.creation_date("YYYY-MM-DD") %>
decided_by:
supersedes:
---

## Context

_The forces at play: what is true today, what hurts, what constrains the choice. Facts, not the decision._

[Context]

## Options considered

| Option | For | Against |
| --- | --- | --- |
| [Option A] | [...] | [...] |
| [Option B] | [...] | [...] |

## Decision

_What you will do, in full sentences, starting with “We will”._

We will [...].

## Consequences

- Easier: [...]
- Harder: [...]
- To watch: [...]
