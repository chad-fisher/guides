---
tags: r r-studio
---

# Introduction to RStudio

## Learning Objectives
- Understand the layout and components of the RStudio interface.
- Learn how to interact with the Console, Source, Environment, and File (Output) panes.
- Gain insights into managing R projects, running scripts, and utilizing the built-in help and packages.

## Starting RStudio

On your computer, start RStudio by going to the application search (either the Windows search box next to the start menu icon or the MacOS Spotlight Search) and searching for "RStudio." Note that you do not need to start R in order to start RStudio, but you do need both R and RStudio installed. 

When you first open RStudio, you will see the **Menu**, the **Console Pane**, the **Environment Pane**, and the **Files (Output) Pane**. To open the **Source Pane**, click on the "+" icon in the top left corner. From the dropdown menu, select **R Script** to create a new script. You should now see the following window structure:

<img src="https://tufts.box.com/shared/static/gkkd0ljdm693g0oqj8ianz7p5ozrde7x.jpg" alt="console_commandline" width="90%"/>


## The Console Pane

The Console Pane is the interface to R. If you opened R directly instead of opening RStudio, you would see just this console. You can type commands directly in the console. The console displays the results of any command you run. For example, type:

```
2 + 4
```

in the command line and press **Enter**. You should see the command you typed, the result of the command, and a new command line.

<img src="https://tufts.box.com/shared/static/ylhcq5dqxbnpyys987zha9rnja3s6lap.jpg" alt="console_commandline" width="90%"/>

To clear the console, press **Ctrl+L**.

When you create a new RStudio session, the console will be cleared. In order to retain your code across sessions, you'll need to save the code in the Source Pane.

## The Source Pane

The Source Pane is a text editor where you can type your code before running it. You can save your code in a text file called a script. Scripts typically have filenames with the extension `.R`. To open a script, click on **File** in the Menu bar or press **Ctrl+O**. 

Any text shown in green is a comment in the script. You write a comment by adding a `#` at the beginning of a line. Anything to the right of a `#` is considered a comment and is ignored by R when running code. Any text in black or blue is the actual code. Place your cursor anywhere on the first few lines of code and click **Run**. You can also run code by pressing **Ctrl+Enter**.


<img src="https://tufts.box.com/shared/static/9wh3ntg37i6eyb4kv5ugan177ozordb6.png" alt="Memory-Storage" width="60%"/>

R will run the line where your cursor is placed. If it is a comment, R will ignore it and run the next line. R will skip all comments until it finds a line of code. 

### Code Sections

Code sections allow you to break a script into distinct regions. To create a new code section, include at least four dashes, equal signs, or pound signs (`-`, `=`, or `#`) at the end of a comment. You can easily hide and show code sections by clicking the arrow next to the code section line.

<img src="https://tufts.box.com/shared/static/huhaapsm1krz7tim2abmebvte87g1ybe.png" alt="code_section" width="60%"/>

## The Environment Pane

The Environment Pane includes an **Environment** tab and a **History** tab. If you are using RStudio version 1.1 or later, you will also see a **Connections** tab. The **Connections** tab makes it easy to connect to data sources on your system. You will not see this tab in earlier versions of RStudio.

### The Environment Tab

The **Environment** tab displays any objects that you have created during your R session. For example, in the Example code section, we created three variables: `x`, `y`, and `z`. 

<img src="https://tufts.box.com/shared/static/szt6wrzltatcut5ctx11z2ab7x0jeb15.png" alt="Memory-Storage" width="50%"/>

R stored these variables as objects, and you can see them in the Environment tab. To see a list of all objects in the current session, type:

```
ls()
```

in the command line. To remove an individual object from the environment, use the `rm()` command, e.g., `rm(x)`. To remove all objects from the environment, click the **broom** icon or type:

```
rm(list=ls())
```

in the command line.

### The History Tab

The **History** tab keeps a record of all the commands you have run. To copy a command from the history into the console, select the command and press **Enter** or click **To Console**. To copy the command into the script, select the command and press **Shift+Enter** or click **To Source**. You can clear your history by clicking the **broom** icon.

## The Files (Output) Pane

The **Files Pane** contains several tabs that provide useful information.

### The Files Tab

The **Files** tab displays the contents of your working directory. R reads and saves files in this directory, similar to how your web browser saves files to the "Downloads" folder. This is where R is looking for and saving files by default. To find out which directory R is currently using, type:

```
getwd()
```

in the command line. 

Remember to use forward slashes (`/`) when specifying the working directory.

If you do not see the contents of your working directory in the **Files** tab, click **Refresh**.

### The Plots Tab

The **Plots** tab displays all graphs that you create. If you have multiple plots, navigate through them using the **Previous** and **Next** buttons. As part of the Example code section, a plot should appear in this tab. Click **Zoom** to open the plot in a new window. Click **Export** to save the plot as an image or PDF. To remove a single plot, click **Remove**. To remove all plots, click **Clear All** or type:

```
dev.off()
```

in the command line.

### The Packages Tab

An R package typically includes code, data, documentation, and tests. R packages make it easy to share and use additional functionality. As of 2024, there were over 19,000 packages available in the official R repository ([CRAN](https://cloud.r-project.org/)). Packages allow you to perform tasks without extensive coding. 

The **Packages** tab lists installed R packages in your system. To check if the **moments** package is installed, search for it in the list. If it is not there, install it by typing:

```
install.packages("moments")
```

and load it with:

```
library(moments)
```

Once a package is installed, you do not need to reinstall the package again unless you install a new version of R. If you want to use a package, you have to load it every time you start a new RStudio session. 
The Packages tab should now show the moments package. Packages that are loaded in the current R session have a check mark next to their name. 

<img src="https://tufts.box.com/shared/static/32m7iyv5hpd53njjnnbl7byafi1ujjkm.png" alt="Memory-Storage" width="50%"/>

### The Help Tab

The **Help** tab contains built-in documentation for packages and functions. Help is available for any loaded packages. Access the help file for the `mean` function by typing:

```
help(mean)
```

or:

```
?mean
```
<img src="https://tufts.box.com/shared/static/gbwrdt8xzi3w8rdnwh63eksm46c86ps4.png" alt="Memory-Storage" width="50%"/>

An R documentation file includes:
- **Header**: Function name, package name, title, and description.
- **Usage**: Function syntax and required arguments.
- **Arguments**: Descriptions of function parameters.
- **Examples**: Sample code demonstrating the function's use.
<img src="https://tufts.box.com/shared/static/43qomrwbnfof0avj3x5vbtqz3o0qwtkw.png" alt="Memory-Storage" width="50%"/>

### The Viewer Tab

The **Viewer** tab displays HTML output generated by packages such as R Markdown and Shiny.

## The Menu

On MacOS, the menu bar is at the top of the screen on hover by default. On Windows, the menu bar is static and stays at the top of the screen by default.

The **Menu** in RStudio includes dropdown menus and buttons for file management, code execution, and tool configuration. Key menu options include:
- **File**: Create, save, or open files.
- **Edit**: Search, undo/redo, and clear console.
- **Code**: Insert sections and run code.
- **View**: Navigate between tabs.
- **Plots**: Save or navigate through plots.
- **Session**: Restart R, manage workspace.
- **Debug**: Add breakpoints to troubleshoot.
- **Profile**: Profile code to identify slow functions.
- **Tools**: Install packages and manage add-ins.
- **Help**: Access documentation and resources.

  >  **To Get Support:** - Please email tts-research@tufts.edu for questions and requests.
