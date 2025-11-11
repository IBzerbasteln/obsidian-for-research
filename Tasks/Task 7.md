# Structuring your vault
> [!info] Introduction
> Once you start [[Task 2|transferring notes]] into Obsidian, taking [[Task 3|reading notes]] or [[Task 4|daily notes]], your vault will soon begin to fill up with content. Now, it becomes crucial to organise this information in a way that makes every information discoverable in the long-term. You might be able to mentally keep track of 10 notes, or maybe 100---but at some point, this won't be possible anymore and you'll want to be ready for when that day comes. Investing in the creation and maintenance of a sound structure allows you to save time when looking for a particular information or resource, and it might save you the nuisance of losing something altogether.
> 
> This task will explore different ways of structuring your vault and teach you how to use them.

## Learning outcomes
By the end of this task, you will be able to:
- distinguish different methods of vault organisation;
- understand their respective strengths and weaknesses; and
- reflect on what suits your personal needs best.

## Methods of organisation
> Obsidian allows introducing structure into your vault in three major ways: **folders**, **tags**, and **links**. 

### Folders
Folders are the most traditional way to organize files (if you've used a computer before, you will have seen and used folders), and Obsidian is no exception. Since every note in your vault is a [[Task 1|Markdown file]] on your computer, Obsidian also mirrors the folder structure within the vault. Put differently, every folder and sub-folder you see in the Obsidian menu also exists on your device and can be opened in the file explorer.^[You can try this by right-clicking on a folder and selecting `Show in system explorer`]

You can create new folders for your vault either in your file explorer, or within Obsidian. For the latter way, right-click in the menu pane and select `New folder` or click the 'new folder' icon at the top.

#### Strengths
- **Intuitive**: Pretty much every digital device we're using relies on folders, and even when we organise physical documents, we put them in different folders. This makes it easy to imagine what a folder is and what it works.
- **Hierarchical Organization**: Since you can have sub-folders (and sub-sub-folders, and sub-sub-sub-folders, and...), your file organisation can represent a clear hierarchy among different groups of items.

#### Weaknesses
- **Rigidity**: Notes can only exist in one folder at a time. This makes folders mutually exclusive, and might cause problems in cases where it is not entirely clear into which category a note belongs.
- **Opacity**: In the case of nested folders, i.e., folders that contain sub-folders and sub-sub-folders and so on, just looking at the top-level folder will often not tell you what exactly is inside: both in terms of the exact files and the files in the sub-folders.

> [!tip] Recommendations
> 1. **Use folders scarcely** and only for categories which you know for a fact are mutually exclusive. For example, you could have one folder for daily notes and another one for literature notes. 
> 2. **Don't overdo it with the nesting**; too many sub-folders will make it harder, not easier to find something. Implementing a system like [Johnny Decimal](https://johnnydecimal.com/) will help keeping your folder structure "flat," i.e., without too many levels of nested folders.

### Tags
In addition to placing notes into folders, Obsidian also allows you to assign tags to your notes. A tag in Obsidian looks like #this. You can click on tags, and the search tab on the left will automatically list all notes that have been accordingly tagged. If you open the menu on the right, you can also access a list of all tags in your vault. A note can contain any number of tags, and Obsidian also supports nested tags (or sub-tags, if you will). These can be created using a simple `/`: #nested/tag

Tags can be placed anywhere in the body of a note, or in its frontmatter. To place a tag there, open the command palette (`Ctrl+P`/`Cmd+P`) and select `Add file property`. Select the option `tags` and add the tags of your choice.

#### Strengths
- **Flexibility**: A note can have multiple tags so you won't have to choose between one tag or another.
- **Advanced filtering**: Using tags, you can dynamically group notes across different folders and immediately access a list of all relevant notes, irrespective of their location in your vault.^[Many plugins also rely on tags, for different purposes.] Moreover, you can combine several tags to create a custom query in the search tab on the right:

```query
tag:#this OR tag:#nested 
```

#### Weaknesses
- **Maintenance**: The more tags you have, the more difficult it becomes to manage them all and keep them consistent. Plugins like Tag Wrangler can help with that but if you use a tagging system that adds new tags as you go along, you will regularly need to check that your tags are consistent, remove dead ends (unused tags), consider merging tags etc.
- **Unclear threshold**: Some people struggle with knowing when to actually create a new tag, i.e., when a topic/feature is recurring enough to warrant a new tag that will then need to be manually added to all relevant notes.

### Links
Links are one of Obsidian's most powerful features; we've covered their creation in [[Task 2#Step 2 Linking your notes|Task 2]]. They allow you to create connections between notes, up to a point where your vault begins to resemble a networked structure that mimics a human brain---hence why many people refer to their personal knowledge management systems as their "second brain." The graph view displays this network of notes visually.

Using links as a method of organisation relies on so-called **maps of content (MOCs)**. MOCs are notes that don't contain original content but exclusively link to all other notes that are relevant to the topic at hand. This can be a structured list with section headings etc. or just a simple list of relevant notes.

In your **graph view**, MOCs serve as nodes that bring different notes together and tie them to a central MOC, a 'master index,' in the very middle of the graph. In addition, the right menu pane allows you to display the **backlinks** of the note that is currently open, i.e., a list of all other notes that link to the current one, and the **outgoing links**, so all links to which the current one refers.

#### Strengths
- **Flexibility**: You can link a note (and its sections, and blocks) in as many MOCs as you want, and an MOC can contain as many links as you want. You can attribute information (up to a very fine-grained level) to a large number of different contexts.
- **Networked thinking**: Linking encourages a non-linear, interconnected way of organising information that benefits relational thinking and the consistent search for new connections and ideas. It supports seeing individual thoughts, ideas, or pieces of information as raw material for (academic) creativity.
- **Organic emergence**: Linked MOCs are a structural methods that grows out of the actual content of your vault; you keep compiling notes and once you spot a recurring theme, you create an MOC for it. This prevents your thinking from being overly pre-determined by a structural principle. 

#### Weaknesses
- **Maintenance**: Links need to be manually added to the MOC, and it requires a certain amount of discipline to keep placing newly created notes in their right context.
- **Internal only**: Linking introduces a structure that is internal to Obsidian only and cannot be as easily modified using other software as folders and tags.

### Comparison at a glance

|                | Folders                                    | Tags                                  | Links                                                        |
| -------------- | ------------------------------------------ | ------------------------------------- | ------------------------------------------------------------ |
| **Strengths**  | - Intuitive<br>- Hierarchical Organization | - Flexibility<br>- Advanced filtering | - Flexibility<br>- Networked thinking<br>- Organic emergence |
| **Weaknesses** | - Rigidity<br>- Opacity                    | - Maintenance<br>- Unclear threshold  | - Maintenance<br>- Internal only                             |
## Instructions
### 1. Quiz
> The following ten multiple choice questions are designed to test your understanding of the different methods of organisation. More than one answer might be correct.

1. Which is the only organisation method that forces you between one option or another?
	- [ ] links
	- [ ] folders
	- [ ] tags
2. Obsidian supports nested tags.
	- [ ] true
	- [ ] false
3. Obsidian supports nested folders.
	- [ ] true
	- [ ] false
4. Which organisation method does not capture hierarchy?
	- [ ] links
	- [ ] folders
	- [ ] tags
5. Topic-based folders are suitable for interdisciplinary research.
	- [ ] true
	- [ ] false
6. Any note can only carry up to three tags.
	- [ ] true
	- [ ] false
7. How can you display all notes that link to the current note?
	- [ ] by opening the right menu and selecting `Backlinks for [Note X]`
	- [ ] by opening the command palette and selecting `Backlinks: Show backlinks`
	- [ ] by right-clicking on the `.md` file of a note in your system explorer and selecting `Properties`
8. MOC stands for...
	- [ ] Master of Ceremony
	- [ ] Map of Content
	- [ ] Maximum of Capacity
9. What is an advantage of folders over links?
	- [ ] A note can be part of two folders but only link to one MOC
	- [ ] Folders can visualise hierarchical relationships whereas links are bidirectional and symmetrical.
	- [ ] Folders support out-of-the-box thinking.
10. What do links and tags have in common?
	- [ ] They can grow organically out of content you add to your vault.
	- [ ] They're very flexible.
	- [ ] It may take some effort to properly maintain them.

> If you've finished answering the questions, please confirm [[Task 7_Solution|here]] whether your answers were correct.

### 2. Structuring your vault
This has been a lot to take in, and it has hopefully become evident that the structure of an Obsidian vault is not something to be 100% pre-determined from the start but rather something that develops over time. There is the 'second brain' metaphor but other like to refer to their vaults as '[digital gardens](https://anthonyamar.fr/Digital+garden/Digital+garden),' and there is certainly merit to a perspective that accounts for organic growth of structures and substance over time. 

What you can do now:
1. Decide whether you would like to use and/or combine these different organisational methods in your vault. Mixing them is very common; hardly anyone only relies on a single one of them alone.
2. Make up your mind as to the function that each of these methods should fulfil. You could, for instance, use tags for different substantive topics and folders for different types of notes.
3. Choose the specific categories you would like to use in the beginning. In concrete terms: What folders do you want? What topics do you think will require their own tags, or MOCs?

> [!warning] Avoid redundancies
> An important element of your vault organisation is that no two structural methods should serve the same goal. For example, you should not have a folder titled "Daily Notes" (where you place your daily notes) and a #daily-note (that you put in every daily note). There is no benefit in such a redundancy; it only multiplies your maintenance workload.   

4. Implement these categories in your vault.
5. As you proceed, make sure to evaluate your structure, tidy up loose ends, and make sure to consistently fit it to your needs.

This is an open ended process, and it's important not to forget along the way that the system is supposed to be working for you, not the other way round. Don't let any form of structural element limit your thinking or your work; these always come first.

---
overview: [[Getting started with Obsidian]]
previous task: [[Task 6]]
next task: [[Task 8]]