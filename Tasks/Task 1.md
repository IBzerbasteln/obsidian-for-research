# Formatting your notes using Markdown
> [!info] Introduction
>  Obsidian is a note-taking app that uses the [Markdown](https://en.wikipedia.org/wiki/Markdown) format. **Markdown** is a simple way to format text using plain text symbols. It's like a shorthand for formatting that you can use to make your notes look nice without having to use complicated software or editing options.
>  
>  This task will teach you how to use it!

## Learning outcomes
By the end of this task, you will be able to:
- understand the basics of Markdown syntax;
- use Markdown to format your notes in Obsidian; and
- replicate an example PDF using Markdown in Obsidian.

## Markdown and its benefits
First of all, it is important to understand that **using Markdown does not require doing anything extra**. In whichever way we take digital notes, we use some kind of formatting: we put headings that stand out from the text and give it structure, with set key terms in bold, we italicise sections that are written in a different language etc. In most note-taking apps and text processors like Microsoft Word, users access these formatting options using buttons in the menu ribbon, or keyboard shortcuts (like `Ctrl+B`/`Cmd+B` to set something in bold). 

Markdown, on the other hand, allows users to **format their notes using special characters**. For example, to italicise an expression, you can put it between two asterisks: \*raison d'être\*. Markdown will display this as follows: *raison d'être*.[^1] In addition, it also allows you to use the same keyboard shortcuts that you would use in any text processor; you can also italicise text by selecting it and then pressing `Ctrl+I`/`Cmd+I`.

Typing in special characters for formatting might be counter-intuitive in the beginning but becomes natural quite quickly and has a number of **significant benefits**. 

- **Markdown reduces distractions**. There are no buttons (unless you [want them](https://github.com/Reocin/obsidian-markdown-formatting-assistant-plugin)) and there are only limited formatting options. Markdown prevents you from playing around with font sizes and styles, page margins, line spacing, list symbols, and so on. It offers what you need to bring structure into your notes---but nothing more.[^2]
- **Markdown reduces friction**. You can copy and paste text across notes without ever having to worry about inconsistent font sizes, styles, colours, and so on. That also applies to text which you paste from outside your vault. Just right-click, select `Paste as plain text` and the pasted text will seamlessly fit into your note. All major LLMs also give their output in Markdown which can therefore be smoothly integrated into your vault, too. ^24fbc1
- **Markdown saves storage.** Because all the formatting in Markdown files is done using characters, the files tend to be quite small in comparison to `.docx` files. For example, this files is only 6 KB large. If I export it to Microsoft Word, it will require 14 MB of storage, and even 243 KB as a PDF.
- **Markdown purifies information**. Noting down ideas in Markdown format is perhaps the closest we can get to pure information. By that, I mean information that is not determined by the physical properties of its storage but by its content itself. Markdown does not display your notes with pages or fixed line widths; it is just plain text, displayed on whichever device you choose. Notes in Markdown are light, portable, readable, and they are easy to split, merge, and recombine.

[^1]: The reason why the first *raison d'être* is not displayed in italics is that the asterisks are each preceded by a backslash `\` which serves as an escape character that prevents the Markdown from being rendered.
[^2]: For completeness' sake: it is possible to change the style in which Obsidian renders the Markdown files; for further information see [[Task 5]].

With all of this in mind, let's move on and see how you can use it!


## Instructions
1. Create a new note (`Ctrl+N`/`Cmd+N`) with the title `Task 1_Practice`. You can also create and access that note by clicking on [[Task 1_Practice|this link]].
2. Open the [[Task 1_Example.pdf|example PDF]] in a new tab and use drag-and-drop to arrange them side by side.

![[side-by-side.png]]

3. Follow the example PDF provided and replicate its content and formatting using Markdown. 
	- You can copy and paste the text but you will need to accurately format it yourself.
	- Use the references below to figure out how to create different formatting options in Markdown.
	- If you right-click on selected text or in the editor, this will display the different formatting options, too.
	- Remember: Obsidian also supports the usual shortcuts for formatting (e.g., `Ctrl+B`/`Cmd+B` to set text in bold).
4. Once you've finished formatting your note, check the [[Task 1_Solution]] to compare your result. What is the same, what is different? And does that matter in practice?

## References
> [!warning] These are ordered from most accessible to least accessible.

1. concise overview over Markdown formatting options: [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
 2. [Markdown Live Editor](https://markdowneditor.net/markdown-editor) that lets you try out different formatting options and renders them in real time
 3. comprehensive documentation on how to format your notes in Obsidian: [Obsidian Documentation: Markdown](https://help.obsidian.md/How+to/Format+your+notes)

---
overview: [[Getting started with Obsidian]]
next task: [[Task 2]]
