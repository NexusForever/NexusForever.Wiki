# Bug Submission

If you encounter a bug while testing the Nexus Forever project, please write up a bug report using the template below.\
You can post it [here](https://github.com/NexusForever/NexusForever/issues), please put **\[Bug]** in the title for clarity.

Before you submit a bug, familiarise yourself with our [Project Status page](../project-status.md), if the bug is for a different fork of the project please submit it in the relevant repository.\
Please do **NOT** submit bugs saying a certain feature isn't yet implemented, only report bugs you find in features that are currently available.

### Template

> **Title:** A brief summary of the issue. It helps to include identifying categories, such as UI, Faction, World, Housing, etc.
>
> **Date:** The date you encountered this bug.
>
> **Description:** A full description of the issue. Be sure to clearly describe all relevant information.
>
> **Occurrence:** Once, sometimes, or always
>
> **OS:** The operating system you're using.
>
> **Branch/Commit:** The version of NexusForever you're running (master or develop) and the latest commit (if you don't know this, just leave it blank)
>
> **STR:** Steps to reproduce. A detailed guide to help a developer reproduce the exact situation where you encountered the bug.
>
> **Observed:** Brief summary of the bugged behavior
>
> **Expected:** Brief summary of the proper, bug-free behavior
>
> You can also attach screenshots if applicable.

### Example

> **Title:** Character-Cassian/Human-Models missing eyes after creation
>
> **Date:** 03/11/2019
>
> **Description:** Cassian and Human Exile character models, both male and female, are missing their eyes in-game. The eyes are visible as expected in character creation, but vanish upon first login. The issue persists through relog. Note that eyes appear and function normally when the first skin tone option is chosen during character creation. All other skin tone options result in missing eyes upon login.
>
> **Occurrence:** Always
>
> **OS:** Windows 7
>
> **Branch/Commit:** develop/ca11cbf
>
> **STR:**
>
> 1. On the character creation screen, select Cassian or Exile (either gender).
> 2. Create a character with any skin tone option EXCEPT option 1.
> 3. Log into the game.
> 4. View the character's face.
> 5. Repeat as necessary to observe different gender/skin tone combinations.
>
> **Observed:** Creating a Cassian/Exile character with any but first skin tone option results in missing eyes upon login
>
> **Expected:** Cassian/Exile of all skin tone options should have visible eyes upon login
