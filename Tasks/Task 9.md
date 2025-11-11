# Advanced reference notes and reference organisation
> [!info] Introduction
> You've learned how to create a reference note from your reference manager (Zotero or EndNote) in [[Task 3]], and [[Task 7]] has familiarised you with some general principles of vault organisation (tags, folders, links). This Task builds on what you've learned to create reference notes that are clear, well-structured, linkable, and findable when you need them.

## Learning outcomes
By the end of this task, you will be able to:
- use Properties to include important information in a readable format;
- use the Aliases property to create more convient links to reference notes; and
- create dynamic tables from your references using the [Bases core plugin](https://help.obsidian.md/bases/).

## Background: Properties
Obsidian supports frontmatter in [YAML](https://www.cloudbees.com/blog/yaml-tutorial-everything-you-need-get-started) format. In practical terms, this means that you can include **metadata about your note** in a specific format that different applications (within Obsidian and beyond) can read. Metadata is data about data. In the context of publications, metadata refers to information such as the title, author(s), publication date, location, language, number of pages, publisher, library classification, subject, and so on.

In Obsidian, such a metadata section is called **Properties**. You can easily **create a Properties section** by typing three dashes (`---`) in the very first line of any note. This will automatically generate the Properties heading and the first line:

![[properties-new.png|300]]

Obsidian by default offers you three options (aliases, cssclasses, tags) but you can define any amount of custom frontmatter properties. You can choose between a number of different **types of properties** that are suitable for different kinds of metadata:

![[properties-types.png|300]]

> [!question]- Why would I do this?
> Including metadata about your note in Properties will allow different applications, most notably the **Bases** core plugin, to display, filter, and sort your notes based on this information. The focus of the remaining task is dedicated to leveraging this for reference organisation but there is a broad range of use cases. 

## Instructions
### Using aliases
If you've followed the instructions in [[Task 3]], your vault will now contain a handful of reference notes whose title is the citation key that Better BibTeX has assigned to the reference in Zotero (e.g., @yates_artification_2024). This is efficient but not necessarily pleasant to look at, especially if you link this reference in another note ([[@yates_artification_2024]]). Fortunately, there is a frontmatter property which can solve this issue: aliases. 

The **aliases** property introduces an unlimited number of alternative names under which a note can be found and linked within your vault. This might be useful for reference notes named with a citation key, or for notes to which you refer in more than one language.^[In such a case, you can name the note using one language and then add the name in another language as an alias. That way, you will be able to find and link the file under either name.] 

1. If your reference note does not already have one, create a Properties section by typing three dashes (`---`) in the very first line of that note.
2. Create an aliases property. 
3. Add an alias that corresponds to what you would use as an in-text citation in a manuscript (e.g., `Yates & Peacock 2024`) and hit enter.
4. Open another note, type `[[` and the last name of the first author. Obsidian should now offer you to use the alias in addition to the actual file name of the note.

### Using reference metadata to create a table
One of Obsidian's core plugins, **Bases**, allows you to create databases from your notes and to display them in different ways. To do this, Bases can use the metadata fields that you have defined in the frontmatter (see above), or general properties of your notes such as the time when they were created, the file name, the links it contains, the time when it was last changed etc.

Let's use this to create a table with our references.

> [!todo]- Checklist
> To complete this sub-task, you will need to have 
> - [ ] a handful of reference notes, as well as
> - [ ] a separate folder that contains them, and only them, or 
> - [ ] a tag that you use to collect your references (something link \#reference).

1. **Create a new base.** In order to do that, you can either click the top bottom in the menu ribbon on the left, or you open the command palette (`Ctrl+P`/`Cmd+P`) and select the option `Bases: Create new base`. You should now be looking at an unfiltered table that lists the file names of all files in your vault (i.e., notes and attachments). The file name should be `Untitled`; rename it, if you like.

![[bases-new.png|600]]

2. **Filter your base.** For the moment, we only want your reference notes to appear on the list. Depending on how your vault is organised, we can achieve that in two ways. For each of them, you have to click the `Filter` button on the top right.[^1] By default, it will toggle `This view`; switch to `All views` instead.
	1. **Folder approach**: If your reference notes live in a dedicated folder, change `links to` to `in folder`. Then, select the folder with your reference notes from the list.
	2. **Tag approach**: If your references notes are tagged as such, change the first filter field, the property, from `File` to `file tags`. Then, change the operator field to `contains`. Finally, enter the tag that you use to identify your references.
3. **Display your metadata.** The table should not only show you the file names but also the metadata you've included in the properties of the reference notes. To display them, click on the `Properties` button and multi-select the properties that you would like to have displayed.
4. **Sort your references.** You might prefer sorting your references not by their title but instead by their authors or publication dates. This is possible using the `Sort` button. Here, you can select a property and sort by its values instead. The options you'll have will depend on the type of property (usually alphabetical or numeric).

This should give you a basic overview of all reference notes in your vault. This overview is **dynamic**. This means that Obsidian will automatically update the table if you make changes to the properties of any of these notes or if you add new reference note.

If you want to enhance the functionality of the reference base, you can **create additional views**. Let's assume that you use the tag \#to-read for references that you intend on reading soon. That will make it possible to create a dynamic reading list.

1. **Add a new view.** On the top left, click on the `Table` button. This will allow you to modify the mode in which Obsidian displays your notes in the current view. For our purposes, we're more interested in the option below: `+ Add view`. Click on it. This will open the `Configure view` dialogue.
![[bases-new-view.png|300]]
2. **Configure the new view.** Assign the name "reading list" to the newly created view and leave the remaining two options at their default values. This should create a new view within the same base that uses the same filtering criteria.
3. **Adjust the filter.** Compared to our "main view," this view should only include those reference notes with the tag \#to-read. To achieve that, click on the `Filter` button and add the tag \#to-read to the third filter field.

This view should now only display the references which you have tagged to be read. It, too, is dynamic: as soon as you remove the \#to-read tag from a note after you've read the reference, it will also disappear from your reading list. Alternatively, you could also achieve this by creating a checkbox property named `read`, and add a filter that requires the box to be unchecked.

> [!success] Going further
> Bases offers many, many options for customisation that can help you to refine not only your reference organisation but also the organisation of your notes in general. The possibilities are almost endless. For example, if you use [[Task 7#Links|Maps of Content (MOCs)]] to structure your vault, then you can create a Base with all notes that are relevant to a given project by creating a filter that uses the property `file`, the operator `links to`, and the file name of your project MOC as a value. 
> 
> Feel free to explore how it can help you in your reference and vault organisation!

[^1]: Filters for Bases have three components: the **property** of the note by which you filter, the **operator** which lets you choose how to compare the conditions, and the **value** to which you are comparing the property.

---
overview: [[Getting started with Obsidian]]
previous task: [[Task 8]]
next task: [[Task 10]]