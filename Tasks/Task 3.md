# Taking reading notes in Obsidian

> [!info] Introduction
> Processing academic literature is an essential component of research---even more so in law where most research is not empirical and instead based exclusively on legal texts and secondary literature.  Obsidian provides a robust environment for managing and organising your literature notes efficiently. 
> 
> This task will guide you through different methods of taking literature notes in Obsidian. To accommodate for **different degrees of familiarity and comfort with technology**, it will offer three different levels of sophistication. Every level provides a functional solution for an efficient workflow.

## Learning outcomes
By the end of this task, you will be able to:
- use Obsidian to read and annotate PDFs;
- connect Obsidian to Zotero and EndNote using the Citations plugin; and
- to use the ZotMoov and BetterBibTex plugins to seamlessly integrate Obsidian and Zotero.

## Instructions

### Level 1: Handling PDFs in Obsidian
1. **Select a PDF**: Choose a PDF document that you want to take notes on.
2. **Import the PDF**: Drag and drop the PDF into your Obsidian vault and place it in the `Attachments` folder.
3. **Create a literature note**: Create a new note in Obsidian (`Ctrl+N`), ideally from a [[Task 6|Template]], enter some basic information about the text (author, year, title etc.) and a link to the PDF. 
4. **Read and annotate the PDF**: Open your literature note and the PDF side by side, read the text and take notes in your literature note. If you want to quote a passage, select the text in the PDF and right-click. Then, select the option `Copy as quote` and paste it into your literature note; this will copy the part of the test you're quoting together with a link to that precise location within the PDF. If you prefer having just a link to a specific section, choose `Copy link to selection` instead. ^578495

### Level 2: Obsidian with Citations Plugin
1. **Install the Citations plugin**: Go to `Settings` > `Community plugins`, click `Browse`, and select and install the Citations plugin by Jon Gauthier.^[There is another plugin you could use for this: Zotero Integration by mgmeyers. It has more options but is also harder to configure which is why we are not using it here.]
2. **Export your library**: 
	1. In **Zotero**, right-click on `My Library` and select `Export Library`. Choose BibLaTex format and save the resulting `.bib` on your device. 
	2. In **Endnote**, select `Tools` > `Output Styles` > `Open Style Manager...` and scroll down to tick the option `BibTeX Export`. Close the Style Manager. Go to `File` > `Export...`, assign a name to your library, select `Text File (*.txt)`, and select `BibTeX Export` as the output style. Save the file somewhere in your vault.
3. **Configure the plugin:** Back in the Obsidian settings, navigate to the `Community plugins` section and select the Citations plugin. Under `Citation database path`, add the path to the `.bib` or `.txt` file you just saved. If needed the plugin also allows you to specify in which folder new literature notes should be created. Also, you can configure a template; for starters, consider pasting the following into the `Literature note content template` field: ^16a6b6
```
# "{{title}}"

---
**title**: {{title}}
**authors**: {{authorString}}
**year**: {{year}}
**abstract**: {{abstract}}

---
## notes
```

4. **Create a literature note**: Use the command palette (`Ctrl+P`) to search for and select the `Citations: Open literature note` command. After a short moment of loading, this will show you a list of all titles in the exported Zotero bibliography. Select one, and the plugin will create a literature note for that title based on the template you specified.
5. **Read and annotate the PDF**: see [[Task 3#^578495|Level 1, Step 4]]

### Level 3: Obsidian and Zotero with Plugins
> [!tip] A smoother integration
> As you might have realised by know, the Obsidian-Zotero/EndNote integration from Level 2 has two crucial weaknesses: 
> - You always need to manually export your library whenever you changed something in it for Obsidian to have access to the latest version.
> - The PDFs live in Obsidian and not connected to your Zotero/EndNote library.
> 
> To my knowledge, these issues cannot be fixed in EndNote. In Zotero, we can do so using two plugins.

1. **Install Zotero plugins**: Install the [ZotMoov](https://github.com/wileyyugioh/zotmoov) and [BetterBibTex](https://retorque.re/zotero-better-bibtex/installation/index.html) plugins in Zotero according to the instructions on the respective websites.
2. **Configure Zotmoov**: In Zotero, go to `Edit` > `Settings` > `ZotMoov`. Copy the path of the `Attachments` folder in your Obsidian vault and paste it into `Directory to Move/Copy Files To`; alternatively, you can select the directory via the `Choose Directory` button.
3. **Move attachments from Zotero to Obsidian**: Select those titles in your Zotero library whose attachments you want to move into your vault, right-click and select `ZotMoov: Move Selected to Directory`.^[This will make the PDF available in your vault and at the same time keep it linked to your Zotero reference. It also saves you memory space on your Zotero account which is extremely limited (300 MB).]
4. **Export your Zotero library**: In Zotero, right-click on `My Library` and select `Export Library`. Choose BetterBibLaTex format, tick the box `Keep updated`, and save the resulting `.bib` in the `Attachments` folder in your vault.
5. **Configure BetterBibTeX**: In Zotero, go to `Edit` > `Settings` > `Better BibTeX`. Scroll down to the section `Automatic export`. Specify that your whole library (`My Library`) should be automatically exported `On Change` into the `Attachments` folder.
	- I also suggest using `zotero.clean` as the Citation key formula at the very top of the plugin settings. The Citations plugin in Obsidian will use the citation key to name the literature notes and `zotero.clean` produced neat, compact citation keys that are easy on the eyes. 
6. **Configure and use the Citations plugin**: In Obsidian, configure and use the Citations plugin as described under [[Task 3#^16a6b6|Level 2, Steps 3 to 5]].

---
Overview: [[Getting Started with Obsidian]]
Previous Task: [[Task 2]]
Next Task: [[Task 4]]