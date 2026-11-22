```dataviewjs
// Configuration
const includeCurrentFile = true; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "Game Design Document";
const title = "Game Design Document";
const maxLevel = 2;

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
	if (currentLevel < maxLevel) {
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

```dataviewjs
// Configuration
const includeCurrentFile = true; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "Technical Design Document";
const title = "Technical Design Document";
const maxLevel = 2;

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
	if (currentLevel < maxLevel) {
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

```dataviewjs
// Configuration
const includeCurrentFile = true; // Set to true to include the MOC/index note itself
const sortAlphabetically = true; // Set to false to keep default file system order
const subFolder = "Art Bible";
const title = "Art Bible";
const maxLevel = 2;

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
	if (currentLevel < maxLevel) {
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
