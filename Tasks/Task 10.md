# Academic writing in Obsidian
> [!info] Introduction
> The principal functionality of Obsidian is taking notes and linking them. However, note-taking is often not an end in itself. Many researchers take notes to later use or build on them in the preparation of an article or another written output (e.g., books, blog posts, working papers etc.).  If you're taking notes to produce an output, it only makes sense to **produce the output in the same ecosystem**; put differently, if you're taking notes in Obsidian to write a paper, why not write the paper with Obsidian as well? That will be the focus of this task. Once you've understood how to [[Task 2|get notes into Obsidian]], [[Task 3|take reading notes]], and [[Task 9|organise your references]], you're ready to explore how you can use Obsidian for academic writing.

## Learning outcomes
By the end of this task, you will be able to:
- set up an academic writing environment in Obsidian;
- prepare an academic manuscript in Markdown format; and 
- use Pandoc to convert your manuscript into different formats like `.docx` or `.pdf`.

## Background: The ingredients of your writing setup
A key formal characteristic which distinguishes academic writing from other genres is the **use of (academic) references** that follows a specific style. Academics have traditionally done this by hand but the emergence of digital technology has given rise to a large variety of tools which take over much of the nuisance that comes with formal referencing. **Citation processors** are now widely available; they come with all major reference managers like Zotero, EndNote, Citavi, or Mendeley and represent, arguably, their most sought-after functionality.

If we break down the automatic generation of references, we can distinguish three essential components^[Parts of this section are taken from a [blog post](https://paul-stewens.com/blog/2025/csl-live-preview/) I've published on my website.]: 

1. **The bibliography file**. This is a file with the extension `.bib` which stores all the bibliographical information of the titles in your reference manager (see also [[Task 3]]). When you create a new title and fill in all the fields, the reference manager stores this information in a certain format, the `.bib` format. It can be written and read by all reference managers and citation processors. In the `.bib` file, every title in the bibliography gets its unique identifier, the so-called citation key.
2. **The citation style**. This is a file which contains the rules according to which the bibliographical information is transformed into actual citations. For example, if the bibliography file contains the first and last name of the author, the citation style determines whether the first name is abbreviated, whether the name is put in small caps, italicised, and so on. Some reference managers use closed, proprietary formats for their citations styles. But: there is also an open file format, the `.csl` format ([Citation Style Language](https://docs.citationstyles.org/)) which can be used and edited by anyone.
3. **The citation processor**: This is the programme which generates the citations. To do so, it relies on the first two components. It reads the bibliographical information from the `.bib` file and transforms it using the rules from the `.csl` file. The output can vary. Most often, this will be text in a Microsoft Word document (created by the add-in of a reference manager) but programmes like [Pandoc](https://pandoc.org/) can also generate these citation in a `.pdf` or `.html` file.

In this task, we're exploring how we can create such a setup around our Obsidian vault to use it for referenced, academic writing.

## Instructions
### Setup
#### Creating a writing environment
1. **Setting up a writing directory.**
	1. Create a [[Task 7#Folders|new folder]] in your vault and name it `writing`. 
	2. Within the folder, create sub-folders named `citation-styles`, `templates`, and `manuscripts`.
2. **Add a bibliography.**
	1. Follow the instructions in [[Task 3#Level 3 Obsidian and Zotero with Plugins|Task 3]] to create a permanent export of your bibliography and set the new folder `writing` as the target directory. This ensures that every time you make a change in your reference manager, your updated bibliography will get exported to the `writing` folder.
	2. Go to the community plugin settings for the Citations plugin and indicate the new path to your `.bib` file so that the plugin can continue to access it in its new location.
3. **Add a citation style.** 
	1. Go to the [Zotero Style Repository](https://www.zotero.org/styles) and search for a style of your choice.
	2. To download a style, click on its title. 
		- If you have the Zotero Connector browser plugin installed, this will open a dialogue where the plugin asks you whether you want to add the style to Zotero. Click `Cancel`. That should trigger the download of the `.csl` file.
		-  If you don't have the Zotero Connector installed, just save the `.csl file`.
	3. Transfer the `.csl` file to the folder `Your Vault/writing/citation-styles`

> [!warning]- Note
> We're saving the question of how to create and use templates for [[Task 10#Creating and using templates|later]].

#### Installing Pandoc
> [!info] About Pandoc
> Pandoc is a software that allows for **converting text documents**. It is mainly used by academics and supports a broad range of formats that covers practically all file extensions that might be relevant to researchers. In particular, it is able to generate a `.docx` document from a `.md` file. Also, it comes with a built-in citation processor. Note that Pandoc **does not have a graphical user interface** (or GUI), i.e., it's not an app that you can "see" on your device. 
> 
> Rather, you access Pandoc using the command-line interface (or CLI), which is, to put it in non-technical terms, the scary console with the black background and the white text. It may look something like this:
> 
> ![[CLI.png|400]]
> 
> This will probably look intimidating in the beginning but we will be using this interface to communicate with Pandoc through a small set of very simple commands. However, first things first, let's start with the installation!

1. Open [GitHub](https://github.com/jgm/pandoc/releases/latest) to find the latest list of installers.
2. Select the right installer:
	- For Windows: Select the installer that has `windows` in the file name and the file extension `.msi`.
	- For MacOS: Select the installer that has `macOS` in the file name and the file extension `.pkg`.
3. Download the installer.
4. Run it.

### Creating a manuscript in Markdown
> [!info] The source file
> Now that we've set up all that we need to convert a Markdown manuscript using Pandoc, it's time to create a manuscript. Currently, it might seem that academic writing in Obsidian requires all kinds of excessive extra steps and tools that would be redundant if one simply wrote the manuscript in Microsoft Word. That is somewhat true, but only to a certain extent. Yes, academic writing in Obsidian requires some extra steps---but it also creates unique benefits.
> 
 > [[Task 1]] already went into detail about [[Task 1#Markdown and its benefits|Markdown and its benefits]], and all these points also apply to the writing of manuscripts. In particular, writing in Markdown removes the distractions of a word processor with many formatting options and lots of colourful buttons, and it removes friction: between manuscripts, and between notes and manuscripts. This means that pieces of text can easily and smoothly be removed, pasted, and reinserted between different Markdown files. 
 > 
 > Moreover, the limited the degree of formatting that is possible in Markdown allows for one and the same manuscript to be exported to, say, `.docx` format in all kinds of different styles without having to change the manuscript. This applies to both the formatting and the citation style. The Markdown manuscript thus becomes a **[single source of truth](https://en.wikipedia.org/wiki/Single_source_of_truth)** for your writing. This allows you to truly focus on the content of your writing, and to flexibly decide on and change the format of the output as you go.
 
1. Create a new note in the `writing` folder. 
2. Create a `Properties` block (following the instructions from [[Task 9#Background Properties|Task 9]]) with the following text properties:
	- `title`
	- `subtitle`
	- `author`
	- `bibliography`
	- `csl`
	- `lang`
3. Fill in the fields with the metadata of your manuscript.
	- For `csl`, write `./citation-styles/yourstyle.csl`. 
	- For `lang`, use the [language code](https://www.loc.gov/standards/iso639-2/php/code_list.php) that corresponds to the language in which you are writing.[^1]
4. Write a few paragraphs. Whenever you want to include a citation, open the command palette (`Ctrl+NP`/`Cmd+P`) and select the option `Citations: Insert Markdown citation`. This will cause the Citations plugin to open a window that lets you select a reference from your bibliography. Once you've found the right one, select it. The plugin will then paste a citation in the following format: `[@citationkey]`. Place it in the end of the sentence for which you are using it as a reference, but before the period.^[This is because Pandoc will automatically move the reference behind the period during conversion if the citation style uses footnotes. If you place the citation after the period and use a style that requires in-text citations, there is no option that automatically moves the reference before the period.]
5. To use multiple reference for one sentence, apply the following format: `[@citationkey1; @citationkey2; @citationkey3]`.
6. Add locators. In many cases, authors are expected to pinpoint the exact page within a reference where an information can be found. Such a locator can be added like this: `[@citationkey, 27]`.
7. Add prefixes. You might want to introduce a reference, for instance by saying "For an in-depth exploration of this aspect see XYZ." Such a prefix can be included in the citation, too: `[For an in-depth exploration of this aspect see @citationkey]`.

[^1]: If some sections of your manuscript are in a language other than the main language, you can use the following expression: `[Lorem ipsum dolor sit amen.]{lang=la}`. 

### Converting a manuscript using Pandoc
> [!info] Conversion with Pandoc
> As mentioned above, the only way of accessing Pandoc is through the command-line interface (CLI).
> 
> A Pandoc conversion command will typically have the following components:
> - an input file
> - an output file
> - the citation processor
> - a reference document
>  
> The full command would look something like this:
> ```pandoc
> pandoc --citeproc --reference-doc="./templates/your_template.docx" "manuscript.md" -s -o "manuscript.docx"
> ```
> 
> This command
> 1. activates the citation processor (`--citeproc`);
> 2. specifies the path to a reference document (`--reference-doc=`);
> 3. specifies the source file; and 
> 4. specifies the output file (`-s -o`); the output format depends on the file extension.

1. Open the CLI.
	- On Windows, open `Start` and type `cmd` into the search bar. You should now be offered the `Command prompt` option; select it.
	-  On MacOS, open the the `Terminal` app.
2. Navigate to the `writing` directory. To to this, use the command `cd` and add the path to the `writing` folder that you created earlier.
```
cd C:/path/to/your/folder/writing
```
3. In the `writing` directory, paste the following Pandoc conversion command:
```
pandoc --citeproc "manuscript.md" -s -o "manuscript.docx"
```
4. Adjust the file names in the command as needed. Make sure to use the name of the Markdown file which contains your manuscript with the extension `.md` as your input file.
5. Execute the command by hitting `Enter`. This should create a new `.docx` file in your `writing` directory in which all citations have been rendered according to the citation style you've specified in the manuscript file.

> [!tip]- Saving time on conversions
> When using the terminal, you can **press the upward pointing arrow key** on your keyboard. This will allow you to access the commands that you have previously executed and bring them back to the command line for your to modify and re-execute them. That way, you to save time since you don't have to type or paste the full Pandoc conversion command every time; you can just fetch it using the arrow key and insert new information to convert another file, or re-convert the same file, or convert it to a different format.

### Creating and using templates
> [!info] Saving time and energy with templates
> There are various circumstances that might require the reformatting of a manuscript: rejection and resubmission to a different journal, the discovery of a previously overlooked section in a journal style guide, or the wish to have multiple chapters formatted consistently. Here, reference documents can help save a lot of time and energy that would otherwise have to be invested into manual reformatting.

1. **Create a template.** For the best results, use the Pandoc standard reference document and modify it according to your needs. Start by executing this command in the terminal to create a `custom-reference.docx` in your `writing` folder:
```
pandoc -o custom-reference.docx --print-default-data-file reference.docx
```

2. **Modify the template.** Open `custom-reference.docx` in Microsoft Word and modify the different styles. Make sure to select them afterwards, go to the `Style` section in the menu ribbon, right-click on the applicable style and `Update ... to Match Selection`. Alternatively, you can also right-click on a style and choose the option `Modify`.
3. **Rename and move the template.** Assign a new name to the file and move it to the folder `writing/templates`.
4. **Use the template for conversion.** Use the following command to convert your Markdown manuscript to `.docx`:
```
pandoc --citeproc --reference-doc="./templates/your_template.docx" "manuscript.md" -s -o "manuscript.docx"
```

> [!tip]- Custom styles
> By default, Pandoc only provides for a limited number of styles that are defined in the standard reference document. Nevertheless, you can create and use custom styles, for example to format long direct quotations. That work as follows:
> 
> 1. Open your template in Microsoft Office. 
> 2. Go to the `Styles` menu, expand it using the arrow on the right, and select the option `Create a style`. In the dialogue that opens, select `Modify`, and enter your formatting specifications. For long quotes, that could be a font size of 11 and an indentation of 1 cm from each side. Use a clearly identifiable name, e.g., `long-quote`. 
> 3. Save the reference document and close it.
> 4. Open your manuscript. To apply your custom style to a paragraph, enclose it as follows:
> ```markdown
> :::{custom-style="long-quote"}
> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris. Nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor
> :::
> ```
> 5. Export your manuscript. The new custom style should now have been applied to the relevant section.


# Common mistakes and errors
There are a few things to look out for when using Pandoc to covert Markdown files.

1. **Wrong file paths.** You might receive the error `(No such file or directory)`. This is Pandoc telling you that it could not find the file that you specified. 
	- If that happens, first check whether you're in the right directory. You'll want to always stay in `writing`. If you see on your terminal display that you're in a different folder, use the `cd` command to change back to the right directory.
	- Also, there might be an issue with the relative paths. These are the paths that start with a `./` and thus simply refer to a sub-folder of the one that's currently open in the terminal. So, if you place your `template.docx` in the `writing` folder instead of in the `writing/templates` sub-folder, then the conversion command from above will not be able to find the document and use it to convert your manuscript.
2. **Citation not found.** It might also happen that Pandoc displays the following message: `[WARNING] Citeproc: citation XYZ not found`. This means that Pandoc detected a citation in your Markdown manuscript which it then failed to find in the bibliography file that you specified. 
	- If that happens, check whether your `.bib` file is up to date; it might be the case that you've made a change in your reference manager but the bibliography has not been exported correctly (yet).
	- If you're using multiple `.bib` files on your device, you might also have specified the wrong one in the `Properties` section of your manuscript. If that is the case, check the file paths in the manuscript and also the settings of the Citations plugin.
	- Note that this is a warning that doesn't prevent your manuscript from being converted, but it does mean that the respective citation will not be rendered.
3. **Citations are displayed wrongly.** This points to an issue with the citation style, not with your manuscript. Try selecting a different `.csl` file or modifying the `.csl` file to match with your requirements.

# Moving on
With the information in this task, you should be able to get started with academic writing using Obsidian and Pandoc. Still, it only covers a tiny fraction of the functionality which Pandoc offers, and it is recommended to consult the [documentation](https://pandoc.org/MANUAL.html) in the case of question about this task or out of curiosity about what else is possible. There is, admittedly, a bit of a learning curve to this style of academic writing. However, once using a standardised terminal command to convert a Markdown manuscript to a fully referenced, spotlessly formatted Microsoft Word document becomes a routine (which happens sooner than you think), the benefits clearly outweigh the investment into learning how to use this new setup.

---
overview: [[Getting started with Obsidian]]
previous task: [[Task 9]]
next task: [[Task 11]]