# Getting your notes into Obsidian and linking them
> [!info] Introduction
> Probably, you have already been taking quite a few notes, both during your studies and your PhD journey---and Obsidian is the perfect place for keeping, organising and managing them all in one place. 
> 
> That's why this task will teach you how to import/incorporate your pre-existing notes into Obsidian, whether they are physical or digital.

## Learning outcomes
By the end of this task, you will be able to:
- import physical notes into Obsidian;
- import digital notes into Obsidian; and
- organise and link your notes.

## Instructions
### Step 1: Getting notes into Obsidian

#### Option A: Incorporating physical notes
1. **Select a physical note**: Choose a short physical note or a section from a longer note that you want to import into Obsidian.
2. **Transcribe the note**: Create a new note in Obsidian (`Ctrl+N`/`Cmd+N`), assign a name to it, and type the content of your physical note into this new note.
3. **Format the note**: Use Markdown to format the note as needed.
4. **Repeat this process**: Repeat steps 1-3 for to create least three different so you can practice linking afterwards.

#### Option B: Importing digital notes
1. **Select a digital note**: Choose a short digital note or a section from a longer note that you have taken in a Microsoft Word document, on OneNote, Evernote, Notion etc. to want to import into Obsidian.
2. **Copy the content**: Copy the content of your digital note.
3. **Create a new note**: Create a new note in Obsidian (`Ctrl+N`/`Cmd+N`), assign a name to it, and paste the content into this new note.
	- When you click right in Obsidian, it will offer you two options: `Paste` and `Paste as plain text`. 
		- If you select `Paste`, Obsidian will try and reproduce the formatting, links etc. in your original note using Markdown.
		- `Paste as plain text` removes all this information and just pastes the plain text into your note.
	- Play around with the different options, see what they do, and figure out what works best for a specific note.
4. **Format the note**: Use Markdown to format the note as needed.
5. **Repeat this process**: Repeat steps 1-3 for to create least three different notes so you can practice linking afterwards.  

### Step 2: Linking your notes
> [!tip] Tips for linking
> The linking functionality is one of Obsidian's most powerful features. It allows you to establish connections between notes that will then become visible in the graph. Using links, you can break down information in little chunks and recombine them and place them in different contexts as needed. This can be a great resource for creative thinking and academic research and writing alike.
>  

1. **Link to another note**: Create links to other relevant notes in your Obsidian vault. For example, if your note mentions a concept discussed in another note, link to that note using the double bracket syntax `[[Note Title]]`.^[Once you type `[[`, Obsidian will automatically suggest notes to link.]

![[link-basic.png|300]]

2. **Link to a section in another note**: Create a link to a relevant section in another note. To do this, create a normal link and add a `#` after the title. Obsidian will then display a list of the sections in that note to choose from. 
	- The link will then look like this: `[[Note Title#Section Title]]`.

![[link-section.png|500]]

3. **Link to a block in another note**: Create a link to a relevant paragraph or list item in another note. To do this, create a normal link and add `#^` after the title. Obsidian will then display a list of the blocks in that note to choose from. Once you hit enter, Obsidian will generate an identifier for that block and include it in your link.
	- The link will then look like this: `[[Note Title#^BlockID]]`.

![[link-block.png|500]]

4. **Changed displayed link:** You might want to change the text that is displayed for a given link. To do that, you enter a `|` at the end of the link and put the text you would like to be displayed instead. 
	- The link will then look like this: `[[Note Title#Section|Custom display text]]`

![[link-text.png|600]]

5. **Check the global graph**: Click on the second symbol in the task bar on the left to display the graph. This will show you a visualisation of all your notes and the connections between them. 

---
overview: [[Getting started with Obsidian]]
previous task: [[Task 1]]
next task: [[Task 3]]
