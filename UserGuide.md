<h1 align="center">  CheatLogs User Guide </h1>

![Our Logo](https://i.ibb.co/VxzKbbz/a1.png)

**CheatLogs** is a free and open-source cheat sheet manager with blazing fast organization, editing and searching via both a command-line interface (CLI) and a graphical user interface (GUI).

This user guide serves as a reference for using the features of **CheatLogs**. We tailored the level of technicality within this document towards our target audience, novice programmers. If you are new, we recommend reading this from the very [start](#before-start).

The table of contents below lets you easily access the documentation for installation, specific features, and frequently asked questions. 

> <font size = “5” >:bulb: Here are some patterns you will come across and their meanings.
> ------
>|Pattern|Meaning  |
>|--|--|
>| :bulb: |Tip on current section  |
>|:exclamation:|Warning of potential error|
>|:memo:|Important details to note|
>|<font size="3"> [:arrow_up_small:](#table-of-contents)</font>| Returns to table of contents on left click|
>|**bold**|Key terms specific to **CheatLogs**|
>|*italics*|Files|
>|`Snippets`|Typed input or output going into or out of **CheatLogs**|

> :exclamation: Colour of images in this document may not be the same as what you see in your terminal due to syntax highlighting of the imaging software used.

<br>

# Table of contents

* [1. Before you start](#before-start)
* [2. Running CheatLogs](#start)
* [3. GUI text editor](#editor)
* [4. Commands](#commands)
   * [4.1. Storage commands (Aldo)](#storage-command-type)
   	  * [4.1.1. Adding a cheat sheet: `/add`](#add-command)
   	    * [4.1.1.1. Adding a cheat sheet using the easy mode](#add-command-easy)
   	    * [4.1.1.2. Adding a cheat sheet using the advanced mode](#add-command-advanced)
	  * [4.1.2. Deleting a cheat sheet: `/delete`](#delete-command)
	    * [4.1.2.1. Deleting a cheat sheet using the easy mode](#delete-command-easy)
        * [4.1.2.2. Deleting a cheat sheet using the advanced mode](#delete-command-advanced)
	  * [4.1.3. Clearing all entries: `/clear`](#clear-command)
  * [4.2.  Manipulation commands (Abner)](#manipulation-command-type)
	  * [4.2.1. Editing a cheat sheet: `/edit` ](#edit-command)
	  * [4.2.2. Favouriting a cheat sheet: `/fav` ](#favourite-command)
  * [4.3.  Viewing commands (Brandon)](#viewing-command-type)
	 * [4.3.1. Locating a cheat sheet by name: `/find`](#find-command)
	 * [4.3.2. Viewing the cheat sheet: `/view`](#view-command)
	 * [4.3.3. Listing all cheat sheets: `/list`](#list-command)
  * [4.4.  General commands (Adhy)](#general-command-type)
	 * [4.4.1. Viewing help: `/help`](#help-command)
	 * [4.4.2. Change program settings: `/set`](#settings-command)
	    * [4.4.2.1 Change color scheme](#settings-color)
	    * [4.4.2.2 Change behavior of help message](#settings-help-message)
	 * [4.4.3. Exiting the program: `/exit`](#exit-command)
* [5. Data storage (Theo)](#data-storage)
  * [5.1. Data file contents](#data-file-contents)
	  * [5.1.1. XML file configurations](#xml-file-configurations)  
	  * [5.1.2. Main](#main) 	
	  * [5.1.3. Favourite](#favourite) 
	  * [5.1.4. Subject](#subject) 
	  * [5.1.5. Contents](#contents) 	
  * [5.2. Data file organization](#data-file-organization)
  * [5.3. Preloaded data files](#preloaded-data-files)  	     	    	  	    
* [6. FAQ](#faq)
* [7. Command Cheat sheet](#command-cheatsheet)

<br>

<a id="before-start"></a>
#  1. Before you start<font size="5"> [:arrow_up_small:](#table-of-contents)</font>
**CheatLogs** requires Java 11 or above installed on your computer. You can follow the following instructions to install Java 11:
> &nbsp;:exclamation: If you are using earlier versions of Java, there may be compatibility issues. Thus, we recommend using the same one we developed on, Java 11. 
> 
 1. Download Java JDK 11 for your system from [here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).
 2. Run and follow the installation instruction in the wizard.
 3. Check your Java version.
	 * For computers on Windows, invoke`java -version` on the command prompt.
	 * For macOS or Linux distros, invoke `java -version` on your terminal of choice.
4. Verify that the version installed follows the “11.x.x” format. Refer to the image below for what you should expect to see.

![Java 11 installed message](https://i.ibb.co/tzV9GX3/image.png)

<br>

<a id="start"></a>
#  2. Running CheatLogs<font size="5"> [:arrow_up_small:](#table-of-contents)</font>
**CheatLogs** is easy to get running. You can follow the steps below to do so.
1.  You can download the latest version of **CheatLogs** from [here](https://github.com/AY2021S1-CS2113T-W11-3/tp/releases).
2. Scroll to the latest release.
3. Download only the *CheatLogs.jar* file highlighted in the orange box below.

	![](https://i.ibb.co/C24vhGg/image.png)
4. Create a new directory anywhere on your PC, This is the home folder where **CheatLogs** will create its own subdirectories to store cheat sheets. 

	> :bulb: Unfamiliar with navigating the terminal? Click [here](https://www.digitaltrends.com/computing/how-to-use-command-prompt/) for a basic introduction for Windows cmd and [here](https://www.pluralsight.com/guides/beginner-linux-navigation-manual) for macOS/Linux bash terminal.

5. Move *CheatLogs.jar* to the new directory.
6. On the terminal,  navigate to the directory.
	> :memo:  If you are running **CheatLogs** for the first time, proceed to step 7.1. Otherwise, proceed to step 7.2.

7. 
    1. Invoke `java -jar cheatlogs.jar first` to run the program. Through this command, **CheatLogs** will import [preloaded
cheat sheet files](#preloaded-data-files) for you to use.

    2. Invoke `java -jar cheatlogs.jar` to run the program. 

	> :exclamation: If a welcome message appears as shown below after running step 7.1 or 7.2, then great! **CheatLogs** is up and running.

![CheatLogs welcome screen]( https://i.ibb.co/L6LmYGZ/mainMenu.png)

8. Try typing some commands in the terminal and hit Enter to execute.
   Here are some example commands you can try, don’t worry if you don’t know them yet!
   
   * `/help`: Shows help info on how to use the application.
   * `/list`: Lists all cheat sheets.
   * `/exit`: Exits the app.

A bit confused? Here is a video guide on how to perform steps 4-9 using the terminal (not cmd). Note that CheatLogs.jar already has been placed in the Desktop folder.
> :bulb: The commands for Windows cmd and UNIX/macOS terminal are quite similar. You can achieve the same result with cmd using the same commands used in the following video.

> :exclamation: This demonstration follows step 8b instead of step 8a.

![ezgif-6-63beb94eab4e](https://i.ibb.co/Q9FShJt/ezgif-6-63beb94eab4e.gif)
 <br>
 
<a id="editor"></a>
#  3. GUI text editor<font size="5"> [:arrow_up_small:](#table-of-contents)</font>
**CheatLogs** provides a simple graphical user interface (GUI) text editor that automatically pops up on certain commands. These commands include `/add` and `/edit`. This allows you to have an easier time manipulating data, performing simple operations such as cut, copy and paste or even using your mouse, which are typically unavailable on the CLI. Below is what you can expect to see and be able to do when it pops up.
<p align="center">
   <img width="500" height="350" src="https://i.ibb.co/3kZ7Xjq/cheatlogs-editor.gif">
</p>

Our Graphical User Interface uses two main groups of functions:

Actions tab - Actions that relate to the cheat sheet files
 - Save: Saves the text inputted, then exits the text editor.
 - Clear All: Removes all text in the text editor, remains in the text editor.
 - Cancel: Removes all text and exit the text editor without saving.

Edit tab - Actions to manipulate the contents

  - Copy: Copies the text highlighted in the editor to the system clipboard.
 -  Cut: Cuts the text highlighted in the editor to the system clipboard.
 -  Paste: Pastes from the system clipboard to the position of the text cursor.
> :bulb: The editor has a built-in feature to prevent blank cheat sheets from being saved.
In the following sections, we will refer to this editor as **the Editor**. 
 
<a id="commands"></a>
# 4. Commands<font size="5"> [:arrow_up_small:](#table-of-contents)</font>
Commands are how you interact with **CheatLogs**. To understand the terminology being used in the subsequent sections, we would like you to understand the typical structure of a command, illustrated below.

<p align="center">
   <img width="540" height="390" src="https://i.ibb.co/r3JjNZs/Sprite-0005.png">
</p>

The anatomy of the command is broken down to colour-coded sections in the picture. These elements are used to execute the command and are elaborated below:
 * **Command identifier**: Every command needs one. It is used to determine exactly what type of command **CheatLogs** executes. In the command above, `/add` is the command identifier for adding cheat sheets.
 * **Flag**: Akin to options or parameters of the command, these are additional information passed to **CheatLogs** to use. Flags are sometimes optional, and you do not always need to type them. In the command above, `/n`  and `/s` are used to indicate the names and subject of the cheat sheet respectively, with `/s` being an optional flag.

	
	The command structure of **CheatLogs** uses several types of flags, that includes:
	 * Optional: Flag does not need to be included
	 * Necessary: Flag must be included
	 * At least one: At least one flag from the set must be included

* **Flag description**: Used when the flag itself does not provide enough information, **CheatLogs** takes in additional information for each flag through that flag’s description. Not all flags have flag descriptions, but each flag description needs to accompany a flag. In the command above, it is the name flag `n` is described by `help` and the subject flag `s` is described by `me`.

> :bulb: You need not worry if you forget the exact flags for each command. **CheatLogs** prompts you to enter the flag description for each missing necessary flags. <br>
> :exclamation: **CheatLogs** is case-sensitive, be sure to match the case for flags about names.

<br>

<a id="storage-command-type"></a>
## 4.1. Storage Commands:  <font size="5"> [:arrow_up_small:](#table-of-contents)</font> 

This is one of the most used command type in **CheatLogs**.
The storage commands allow you to manage the input and output of cheat sheets to and from the entire list of cheat sheets. 
**CheatLogs** only has one list of cheat sheets and the following storage commands all refer to this as **the List**.

___

<a id="add-command"></a> 

### 4.1.1. Adding a cheat sheet: `/add` <font size="5"> [:arrow_up_small:](#table-of-contents)</font> 

> :exclamation: The subject name would be automatically converted to pascal case, no matter whether your input is in lower or upper case.
> Example: 
>* `java` would be converted to `Java`
>* `PYTHON` would be converted to `Python`
>* `ruby on rails` would be converted to `RubyOnRails`

You can easily use the `/add` command to add your cheat sheets to  **the List** .
You can use the two available modes for adding the cheat sheet: **easy** and **advanced** mode.

<a id="add-command-easy"></a>

#### 4.1.1.1. Adding a cheat sheet using the easy mode<font size="5"> [:arrow_up_small:](#table-of-contents)</font>

> Format: `/add`

The first method that you can use to add chea tsheet is the easy mode. Just type `/add` without adding any flag or description. 
You will be prompted to fill in the `NAME` and the `SUBJECT` of your cheat sheet.

![image](https://i.ibb.co/n01kQ4Y/carbon.png)

Shortly after, a window will pop up to show the editing window.
Enter the details of your cheat sheet in the text area shown below:

![image](https://i.ibb.co/hYtY1GM/Screenshot-2020-11-09-at-6-30-12-PM.png)

Once you are done with entering the details, click the `Save` button to save the cheat sheet.

![image](https://i.ibb.co/n01kQ4Y/carbon.png)

> :bulb: **CheatLogs** has an autosave feature. When you close the window of the text editor, the cheat sheet will automatically be saved.

Congratulations! You have added your first cheat sheet into **CheatLogs**!

<a id="add-command-advanced"></a>

#### 4.1.1.2. Adding a cheat sheet using the advanced mode<font size="5"> [:arrow_up_small:](#table-of-contents)</font>

>Format: `/add /n <CHEATSHEET_NAME> /s <SUBJECT>` <br>

>Flag optionality: `/n` (required)`/s` (required)

For the more experienced users, you can also add cheat sheets using the advanced mode. 
A cheat sheet is first constructed with the name `CHEATSHEET_NAME` and subject `SUBJECT`. 
 **the Editor**  will then pop up for you to enter the description of the cheat sheet.

![image](https://i.ibb.co/440k5wv/Screenshot-2020-11-09-at-7-32-00-PM.png)

If you enter a valid description and click the `Save` button, **CheatLogs** will add the cheat sheet on to **the List** and stored it inside the */data* folder in the jar file directory. The expected outcome should be similar to below.

![image](https://i.ibb.co/hV499yH/image.png)

However, if you enter a blank description, then click the `Save` button, an error message below will show up and **CheatLogs** will not save the cheat sheet.

![image](https://i.ibb.co/j3STgFF/Screenshot-2020-11-09-at-6-30-28-PM.png)

If you try to enter a cheat sheet with an existing name on  **the List** , you will get a message to input another one as depicted below.

![image](https://i.ibb.co/mhgrwN0/image.png)

Examples:

* `/add /n classes /s Java`
* `/add /n Cppthings /s JavaisAwesome`

Shortly after, an editing window will pop up to show the editing window.
Enter the details of your cheat sheet there, then click the `Save` button.

If you want to clear the text editing area, click the `Clear All` button

If you decide to cancel adding the cheat sheet, click the `Cancel` button.

**CheatLogs** will discard the progress you made in the text editor, and **CheatLogs** will not create the cheat sheet.

<a id="delete-command"></a>

#### 4.1.2. Deleting a cheat sheet: `/delete`<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 

From the previous subsection, we learned how to add a cheat sheet into **CheatLogs**. 

In this section, you will learn how to use the `/delete` function.
You can use the delete command using two modes, **easy** and **advanced** mode.

<a id="delete-command-easy"></a>

#### 4.1.2.1. Deleting a cheat sheet using the easy mode<font size="5"> [:arrow_up_small:](#table-of-contents)</font>

The easy mode of the delete command lets you safely delete cheat sheets by prompting you to input the name and the index of the cheat sheet.

> Format: `/delete`

The prompts on the screen will request you to enter the name and the index of the cheat sheet; as shown in the picture below:

![image](https://i.ibb.co/12w4jCZ/delete-easy-mode.png)

<a id="delete-command-advanced"></a>

#### 4.1.2.2. Deleting a cheat sheet using the advanced mode<font size="5"> [:arrow_up_small:](#table-of-contents)</font>

The advanced mode of the delete command lets you delete a cheat sheet using its index or its name. 
The delete command will also delete the corresponding cheat sheet from the */data* folder.
To figure out the index of the cheat sheet, you can use the `/list` command.
The first cheat sheet has an `INDEX` of 1.

>Format: `/delete /n CHEATSHEET_NAME /i CHEATSHEET_INDEX` <br>
>
>Flag optionality: [`/n`, `/i`] (At least one) <br>
>
>Format: `/delete /n CHEATSHEET_NAME`<br>
>Format: `/delete /n CHEATSHEET_INDEX` <br>

This command deletes the matching cheat sheet from **the List** with a name matching `CHEATSHEET_NAME` or index matching `CHEATSHEET_INDEX` whichever you included. The expected result is similar to below if a matching cheat sheet is found.

This example bellow uses only the `CHEATSHEET_NAME` to delete a cheat sheet.

![image](https://i.ibb.co/vvwTBFb/namedelete.png)

This example bellow uses only the `CHEATSHEET_INDEX` to delete a cheat sheet.

![image](https://i.ibb.co/9bPBS09/delete-easy-1.png)

When either the name or index does not match, **CheatLogs** will specify the error as shown below.

![image](https://i.ibb.co/WyQMS2v/wrongnameindex.png)

> :bulb: Our program currently does not have any undo functionality.

> Once you delete a cheat sheet, it will be deleted forever and is not recoverable.

Examples:

* `/delete /n computer /i 15`
* `/delete /i 15` 
* `/delete /n computer`

___

<a id="clear-command"></a>

### 4.1.3. Clearing all entries: `/clear`<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 

>Format: `/clear`
>

If you want to reset everything to its original state, you can simply use the `/clear` command instead of using `/delete` multiple times.
This command will delete all cheat sheets from **the List** on your **CheatLogs**. No need to worry, `/clear` command will not remove the preloaded cheat sheets.
Here is the expected result if currently, you have two cheat sheets stored in the application.

![image](https://i.ibb.co/ysXp9DY/clearcommand.png)

Example:

* `/clear`

> :exclamation: The clear function only clears for the user made cheat sheets. <br>
> The preloaded cheat sheet will still appear inside  **the List** .
___

<a id="manipulation-command-type"></a>
## 4.2. Manipulation Commands:  <font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
After adding cheat sheets, you may want to edit them after some time. Manipulation commands allow you to modify the content of a specific cheat sheet in  **the List** .

___

<a id="edit-command"></a>
### 4.2.1. Editing a cheat sheet: /edit <font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
>Format: /edit /n CHEATSHEET_NAME /i CHEATSHEET_INDEX <br>
>Flag optionality: [/n, /i] (At least one)

This command allows you to edit the description of one of your existing cheat sheets. After `/edit`  is called, **CheatLogs** will match for a single cheat sheet in **the List** with a name matching `CHEATSHEET_NAME` or index matching `CHEATSHEET_INDEX` whichever you included (it will try to match only the name if you included both).
 
On a match, **the Editor** will pop up for you to edit the description of the matched cheat sheet. After you are done editing, saving or cancelling **the Editor** updates the cheat sheet details and the message below will be printed on the terminal, showing the updated version of the cheat sheet.

![image](https://i.ibb.co/c8xq2wY/image.png)

When either the name or index does not match, **the Editor** does not pop up and **CheatLogs** will specify an error as shown below.

![image](https://i.ibb.co/rZ6Rhgn/image.png)

**CheatLogs** does not allow you to save empty descriptions.  **The Editor** will print the error message at the bottom pane (illustrated below) if you try to do so.

![image](https://i.ibb.co/gdGnmZS/image.png)

Examples:
* `/edit /n switch /i 2`
* `/edit /i 3`
* `/edit /n commands`

____


<a id="favourite-command"></a>
### 4.2.2. Favouriting a cheat sheet: /fav <font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
>Format: /fav /n CHEATSHEET_NAME /i CHEATSHEET_INDEX /d  <br>
>Flag optionality: [/n, /i] (At least one), /d (optional)

If you have some cheat sheets which are used frequently, you can mark them as favourite so that those cheat sheets will always be displayed on the top of the table when using `/list` and `/find`. The command `/fav` marks the cheat sheet with a name matching `CHEATSHEET_NAME` or index matching `CHEATSHEET_INDEX `whichever you included.  The expected result is similar to below if a matching cheat sheet is found.
> :exclamation: Trying to match both name and index in the same command may result in conflicting matches. We recommend searching for a single one. 

![image](https://i.ibb.co/VW5JZNx/image.png)

When either the name or index does not match, **CheatLogs** will specify the error as shown below.

![image](https://i.ibb.co/vPgbnbW/image.png)

Favourited cheat sheets are shown at the top of the `/list` command table, with a [*] beside its name. This is shown below, to the right of loops.  This allows you to identify and access your favourite cheat sheets easily. 

![image](https://i.ibb.co/XWztfyX/image.png)

To unfavourite a cheat sheet, you can use the flag `/d` in the command e.g. `/fav /n string /d`. It will try to match for a cheat sheet the same way as a regular `/fav` (without `/d`) but unfavourites the matched cheat sheet instead. The matched cheat sheet is printed as shown below.

![image](https://i.ibb.co/F6MpX1m/image.png)

Trying to [un]favourite an already [un]favourited cheat sheet will show you an error and the matched cheat sheet. This is as shown below. 

![image](https://i.ibb.co/XWgygYK/image.png)

![image](https://i.ibb.co/cNHZmc6/image.png)

Examples:
* `/fav /n Integer /i 2`
* `/fav /i 1`
* `/fav /n string`
* `/fav /n string /d`

___

<a id="viewing-command-type"></a>
## 4.3. Viewing Commands: <font size="5"> [:arrow_up_small:](#table-of-contents)</font>

These are commands that allow you to lookup **the List** for the cheat sheets you want quickly. It is recommended to use one command after another,
e.g. using `/find` to list all matching cheat lists then `/view` with the corresponding name to view the cheat sheet.

Some of these commands present their results in a table form and allow you to sort the results through various filters provided. We will call this ****Sorting Mode****.

In **Sorting Mode**, cheat sheets are originally shown in the order they were found inside  **the List** . You can then sort them in [lexicographical order](https://en.wikipedia.org/wiki/Lexicographic_order#:~:text=In%20mathematics%2C%20the%20lexicographic%20or,of%20a%20totally%20ordered%20set.) 
according to any of the cheat sheet properties. For example, sorting by descending name means to enter`3`in this mode and an illustration of expected output is shown below. 

> :bulb: To exit **Sorting Mode**, enter any characters other than 1 - 4.

![image](https://i.ibb.co/jJZPNdM/image.png)

> :bulb:  Viewing/Deleting cheat sheets using index
> * Index of cheat sheets after sorting in `/list` command can be used to delete/view corresponding cheat sheets
> * However, index of cheat sheets in `/find` command cannot be used to delete/view cheat sheets. You would have to delete/view them using the name.

---

<a id="find-command"></a>
### 4.3.1. Locating cheat sheets with pattern : `/find`<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 


>Format: `/find /s <SUBJECT> /k <KEYWORD>` <br>
>Flag optionality: [`/s`, `/k`] (At least one)

`/find` command allows you to search for cheat sheets using `SUBJECT` and/or `KEYWORD`. The matching cheat sheets would be displayed in a table.

After getting prompted to enter a command, you can search for cheat sheets using:

1. `/find /s <SUBJECT>` to search for cheat sheets with matching subject. More details on the matching algorithm at the end of this section.
2. `/find /k <KEYWORD>` to search for cheat sheets with contents that contains `KEYWORD`.
3. `/find /s <SUBJECT> /k <KEYWORD>` to search for cheat sheets with matching subject and contains `KEYWORD`.

| `/find /s <SUBJECT>` |
| :-------------------------: |
| ![image](https://i.ibb.co/kSVw5r3/image.png) |

| ` /find /k <KEYWORD>` |
| :-------------------------: |
| ![image](https://i.ibb.co/TM4J8s1/image.png) |

| `/find /s <SUBJECT> /k <KEYWORD>` |
| :-------------------------: |
| ![image](https://i.ibb.co/fGdPMdC/image.png) |

cheat sheets that meet the criteria of the command you entered would be displayed in a table as shown in the images below.

| `/find /s <SUBJECT>` |
| :-------------------------: |
| ![image](https://i.ibb.co/HB7MNJx/image.png) |

| ` /find /k <KEYWORD>` |
| :-------------------------: |
| ![image](https://i.ibb.co/z7X4KF2/image.png) |

| `/find /s <SUBJECT> /k <KEYWORD>` |
| :-------------------------: |
| ![image](https://i.ibb.co/hym26SW/image.png) |

**CheatLogs** then enters **Sorting Mode**. In **Sorting Mode**, you can sort according to names or subjects by inputting the corresponding index (1-4).

| Name ascending |
| :-------------------------: | 
| ![image](https://i.ibb.co/yPRhvH3/image.png) |

| Subject ascending | 
| :-------------------------: |
| ![image](https://i.ibb.co/z2jHKSB/image.png) |

| Name descending | 
| :-------------------------: | 
| ![image](https://i.ibb.co/f8D0QXY/image.png) |

| Subject descending |
| :-------------------------: | 
| ![image](https://i.ibb.co/ThvTVnG/image.png) |

To exit **Sorting Mode** and simply enter another character (excluding 1-4).

![image](https://i.ibb.co/x8NVsPr/image.png)

However, if none of the cheat sheets meets the criteria of your `/find` command, **CheatLogs** will not enter **Sorting Mode** as shown in the image below.

![image](https://i.ibb.co/wcqcFxR/image.png)

> :bulb:  Notes on matching algorithm
> * The search is **case-sensitive** e.g. `help` matches `helpers` but not `Help`. 
> * A match contains the search term as a substring. e.g. `java` matches `java11` and  `Tricks for java`

Examples:
* `/find /s loop`
* `/find /s Integer /k 2`
* `/find /k hello`

 ---
 
<a id="view-command"></a>
### 4.3.2. Viewing a specific cheat sheet: `/view`<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
>Format: `/view /n CHEATSHEET_NAME /i CHEATSHEET_INDEX` <br>
>Flag optionality: [`/n`, `/i`] (At least one)

You can view the details of a specific cheat sheet using the `/view` command.
The `view` command requires you to enter either a name or index, and **CheatLogs** will display the content of the cheat sheet that matches what you entered.

After getting prompted to enter a command, you can view a specific cheat sheet using:

1. `/view /n <CHEATSHEET_NAME>` to view the cheat sheet with name `CHEATSHEET_NAME`
2. `/view /i <CHEATSHEET_INDEX>` to view the cheat sheet with index `CHEATSHEET_INDEX`
3. `/view /n <CHEATSHEET_NAME> /i <CHEATSHEET_INDEX>` to view the cheat sheet with name and index corresponding to `CHEATSHEET_NAME` and `CHEATSHEET_INDEX`. 
>:exclamation: If `CHEATSHEET_NAME` and `CHEATSHEET_INDEX` are pointing at two different cheat sheets, no cheat sheet content will be displayed.

| `/view /n <CHEATSHEET_NAME>`|
| :-------------------------: |
| ![image](https://i.ibb.co/ypPympz/image.png) |

| `/view /i <CHEATSHEET_INDEX>` |
| :-------------------------: |
|  ![image](https://i.ibb.co/k58qGf6/image.png) |

| `/view /n <CHEATSHEET_NAME> /i <CHEATSHEET_INDEX>` |
| :-------------------------: |
| ![image](https://i.ibb.co/h7qS4x8/image.png) |

Examples:
* `/view /n Read /i 2`
* `/view /i 1` 
* `/view /n documentation`

---

<a id="list-command"></a>
### 4.3.3. Listing all cheat sheets: `/list`<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 

>Format: `/list`

You can use the `/list` command with no additional flags to list all the cheat sheets in **the List** in a table.

After getting prompted to enter a command, you can view a specific cheat sheet using:

* `/list` to list all cheat sheets available.

![image](https://i.ibb.co/zF8F4PM/image.png)

**CheatLogs** then enters **Sorting Mode**. In **Sorting Mode**, you can sort according to names or subjects by inputting the corresponding index (1-4).

| Name ascending |
| :-------------------------: | 
| ![image](https://i.ibb.co/yPRhvH3/image.png) |

| Subject ascending | 
| :-------------------------: |
| ![image](https://i.ibb.co/z2jHKSB/image.png) |

| Name descending | 
| :-------------------------: | 
| ![image](https://i.ibb.co/f8D0QXY/image.png) |

| Subject descending |
| :-------------------------: | 
| ![image](https://i.ibb.co/ThvTVnG/image.png) |

To exit **Sorting Mode**, simply enter any other characters.

![image](https://i.ibb.co/x8NVsPr/image.png)

Example:
 *  `/list`

<a id="general-command-type"></a>
## 4.4. General Commands: <font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
These are useful general purpose commands that don’t fit into the other categories but are still very useful for you to know.

---

<a id="help-command"></a>
### 4.4.1. Viewing help: `/help`<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
>Format: `/help`
>
If you forgot the syntax of a certain command, you can simply type `/help`. It lists all the executable commands in the application together with its format and example. Below is what you should expect to see.

![image](https://i.ibb.co/n7gWdpQ/image.png)

Example:
* `/help`
---

<a id="settings-command"></a>
### 4.4.2. Change program settings: `/set`<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
**CheatLogs** is highly customizable. By using the `/set` command, you can enable/disable the help messages on each command and change the color scheme of the output text. 
**CheatLogs** saves the settings automatically and the next time you launch **CheatLogs**, it will be the same as the last time you opened it!

<a id="settings-color"></a>
#### 4.4.2.1. Change color scheme<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
>Format: `/set /c COLORSCHEME`<br> 
>Flag optionality: `/c` (required) 


**CheatLogs** provides 3 additional colour scheme options numbered from 1 to 3. Upon command invocation, **CheatLogs** will change the settings to the one matching `COLORSCHEME`. The image below shows the result of `/set /c` command.

![image](https://i.ibb.co/0JM5gBd/image.png)

If your flag description `COLORSCHEME` does not fall in the range mentioned above, it will change the colour scheme to the default setting (option 0).

> :bulb: The colours might vary depending on the terminal you use and differ from the one shown. We suggest picking the most readable one.
 
  Example:   
 * `/set /c 2`
 
<a id="settings-help-message"></a>
#### 4.4.2.2. Change behavior of help message<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
>Format: `/set /m [on/off]` <br>
>Flag optionality: `/m` (required) 

**CheatLogs** provides help messages for each command. Here is an example from `/add` command.

![image](https://i.ibb.co/6wPMRvF/image.png)

You can disable these help messages by using the `/set /m off` and later when you want to re-enable them again, you can type `/set /m on`.
> :bulb: We recommend you to turn on the help messages until you are reasonably comfortable with each command.

  Example:   
 * `/set /m on`
 * `/set /m off`
---

<a id="exit-command"></a>
### 4.4.3. Exiting the program: `/exit`<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
>Format: `/exit`

If you are done using **CheatLogs**, simple type `/exit` to close the application. **CheatLogs** hopes you will open it again.

![image](https://i.ibb.co/J2RWkRx/image.png)

 Example:   
 * `/exit`
<br>

<a id="data-storage"></a>
# 5. Data storage<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 

**CheatLogs** provides a robust storage system that works together with certain
commands to store your cheat sheets for future reference. This ensures that you
have a directory of organized cheat sheet files that **CheatLogs** can read anytime. 

Refer to the image below for an example of a cheat sheet file.

![image](https://i.ibb.co/RDjGFYZ/xml-File-Example.png)

<br>

<a id="data-file-contents"></a>
## 5.1. Data file contents<font size="5"> [:arrow_up_small:](#table-of-contents)</font>

Each cheat sheet file uses an [XML](https://www.w3schools.com/xml/xml_whatis.asp) file format. This file format organizes the contents
of the file into different sections based on certain attributes of the cheat sheet. The code
snippet below illustrates the structure of the entire cheat sheet file.

![image](https://i.ibb.co/mFJ1nDy/xml-Format.png)

By following this format, you can manually insert cheat sheet files recognized by **CheatLogs**. The following sections will guide you in
writing XML files that **CheatLogs** can convert to cheat sheets.

> :exclamation: Editing XML files can render **CheatLogs** incapable of reading your cheat sheets. You should only modify
>or add such files if you an advanced user of **CheatLogs**.

> :bulb:  If you are unsure where to place your new files, simply place it in the /data directory. **CheatLogs** will organize them when you execute a command to add, edit or delete any file.

---

<a id="xml-file-configurations"></a>
### 5.1.1. XML file configurations<font size="5"> [:arrow_up_small:](#table-of-contents)</font>

This section configures the settings of the XML file. By default, **CheatLogs** writes this line into both new and existing XML files.

>Format: `<?xml version="1.0" encoding="UTF-8" standalone="no"?>` 

> :bulb: If you are creating a new XML file, you can omit this line entirely. **CheatLogs** will still convert such XML files into cheat sheets.

> :exclamation: If you are including this section, use the exact settings defined by the format above. Any change to this format can cause **CheatLogs** not converting such files into cheat sheets.

---

<a id="main"></a>
### 5.1.2. Main<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 

This section acts as the root element of the document. **CheatLogs** analyses the relevant
sections you place inside `main` and creates a cheat sheet based on the input given by them.

>Format: `<main>CONTENTS</main>` 

> :bulb:  You can rearrange the order of sections within `CONTENTS`. **CheatLogs** does not take the ordering of such sections into account when parsing XML files.

> :exclamation: Any section that you do not insert into `CONTENTS` is not included in the cheat sheet.

---

<a id="favourite"></a>
### 5.1.3. Favourite<font size="5"> [:arrow_up_small:](#table-of-contents)</font>

This section indicates if **CheatLogs** should mark the cheat sheet as [favourite](#favourite-command). 
You can use this to mark cheat sheets which you want to view in your list of favourite cheat sheets.

>Format: `<favourite>STATUS</favourite>`

> :memo:  `STATUS` is not case-sensitive. For example, `YES` and `yes` are the same.

> :exclamation: If `STATUS` contains another word than `YES`, the cheat sheet will not be marked as a favourite. 

---

<a id="subject"></a>
### 5.1.4. Subject<font size="5"> [:arrow_up_small:](#table-of-contents)</font>

This section includes the subject of the cheat sheet. It allows **CheatLogs** to organize your cheat sheet 
files by assigning cheat sheets of the same subject to the same folder.

> Format: `<subject>SUBJECT</subject>`

> :exclamation: `SUBJECT` cannot take in special characters. You will
>  not be able to insert XML files with such names into **CheatLogs**.

---

<a id="contents"></a>

### 5.1.5. Contents<font size="5"> [:arrow_up_small:](#table-of-contents)</font>
This section includes the contents of the cheat sheet. You can type the notes you want to see in your cheat sheet
here.

>Format: `<contents>CONTENTS</contents>`

> :bulb:  You can append `CONTENTS` on a separate line.

<a id="data-file-organization"></a>
## 5.2. Data organization<font size="5"> [:arrow_up_small:](#table-of-contents)</font>
You can find all the data files in the */data* directory, which is in the same directory as
*CheatLogs.jar*. Within */data*, **CheatLogs** stores data files in folders whose name matches its subject name. 
This gives you a directory of cheat sheets organized by subject, which you can use to retrieve any external cheat sheet file. 

The figure below shows a sample organization of the cheat sheet files in a user’s directory.

![image](https://i.ibb.co/zbppwZZ/sample-User-Data.png)

In the example illustrated above, the user currently has created cheat sheets  of
3 different subjects. Having cheat sheets that are stored based on subject allows you
to conveniently retrieve notes for the programming language that you are seeking help in.

<a id="preloaded-data-files"></a>
## 5.3. Preloaded data files<font size="5"> [:arrow_up_small:](#table-of-contents)</font>
*CheatLogs.jar* contains some example cheat sheet files. They are transferred over to the */data* directory when you run the application for the first time. To differentiate these files from your 
personally created cheat sheets, they are placed under the */preloaded* subdirectory. By viewing and
editing these cheat sheets through **CheatLogs**, you will understand how to operate this program.

The figure below shows a sample organization of the cheat sheet files in a user’s directory with
two preloaded cheat sheets included.

![image](https://i.ibb.co/bzp4yJ2/preloaded-Illustration.png)

In the example above, you can see that **CheatLogs** keeps the organization of such preloaded cheat sheets separate
from the other cheat sheet files. This is to help you better identify preloaded files within the */data* directory.

> :exclamation: If you create a new file within any subdirectory of */preloaded*, **CheatLogs** will assume that these files are preloaded and will treat them as such.

<br>

<a id="faq"></a>
# 6. FAQ<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
**Q**: How do I transfer my data to another computer? <br>
**A**: You can simply drag and drop the `cheatlogs.jar`  and the `/data` directory in that same folder into the other computer.

**Q**: Why is **CheatLogs** so strict on formatting?<br>
**A**: **CheatLogs** is still under development but we plan to provide better ways for you to input ways in the future.

**Q**: Will future updates break my current cheat sheets?<br>
**A**: The current structure of cheat sheets may change in the future, but we plan to provide you with ways to convert so that you can enjoy the new features. 

<br>

<a id="command-cheatsheet"></a>
# 7. Command cheat sheet<font size="5"> [:arrow_up_small:](#table-of-contents)</font> 
The table below is for quick and easy reference to the **CheatLogs** commands with examples of use.

Action | Format | Examples
-------- | ---------- | ------------
Add | /add /n <CHEATSHEET_NAME> /s \<SUBJECT> | /add /n List /s Java
Delete | /delete /i <CHEATSHEET_INDEX> <br> /delete /n <CHEATSHEET_NAME> | /delete /n List <br> /delete /i 1
Clear | /clear | /clear
Edit | /edit /i <CHEATSHEET_INDEX> <br> /edit /n <CHEATSHEET_NAME> | /edit /i 1 <br> /edit /n List
Favourite | /fav /i <CHEATSHEET_INDEX> \[/d\] <br> /fav /n <CHEATSHEET_NAME> \[/d\]| /fav /i 2 <br> /fav /i 3 /d <br> /fav /n Cheat <br> /fav /n arrays /d 
Find | /find /s \<SUBJECT> /k \<KEYWORD> | /find /s Java <br> /find /s Java /k cheater
View | /view /i <CHEATSHEET_INDEX> <br>/view /n <CHEATSHEET_NAME> | /view /i 3 <br> /view /n List
List | /list | /list
Help | /help | /help
Settings | /set /c <OPTION_NUMBER> <br> /set /m \<OPTION> | /set /c 1 <br> /set /m on <br> /set /m off
Exit | /exit | /exit


