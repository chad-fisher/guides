---
tags: r r-studio
---

# Getting started with R for new users

**put into description of the block as an "overview"

Learn about R: guide on how to download and install, and present different environments and methods for running R, including the popular RStudio IDE and the Tufts HPC cluster.

## Learning Objectives

- Understand how to use R.
- How to set up their environment for using R.
- Explore different options for executing R code locally in RStudio or in a high-performance computing (HPC) environment. 

*Note: To navigate to a specific section in the below, please click the Table of Contents located in the right panel under the "On this Page".*

## What is R?

R is a free and open-source programming language that is particularly well-suited for statistical analysis and data visualization. It is widely used by data scientists, statisticians, and researchers for its powerful data manipulation capabilities and an extensive library of packages. These packages support a broad spectrum of applications, including machine learning, bioinformatics, geospatial analysis, and natural language processing.

### Key Features of R:
- **Statistical Analysis**: Perform complex statistical analyses with ease.
- **Data Visualization**: Create high-quality, customizable graphs and charts.
- **Community Support**: Leverage thousands of community-contributed packages to extend functionality.
- **Cross-Platform Compatibility**: Works on Windows, macOS, and Linux.

## What is RStudio?

RStudio is the most popular integrated development environment (IDE) for R. It is designed to enhance your productivity when coding in R and supports Python as well. RStudio provides a user-friendly interface that includes a console, syntax-highlighting editor, and tools for executing code. Additional features include:

- **Plotting Tools**: View and export visualizations directly.
- **Workspace Management**: Manage variables, data frames, and other workspace elements efficiently.
- **History and Debugging**: Track code history and debug programs.
- **Package Management**: Easily install, update, and manage R packages.


## Running R on a Local Computer

### Step-by-Step Guide to Install R

1. **Visit the CRAN Website**: Go to [CRAN R Project](https://cran.rstudio.com/).
2. **Choose Your OS**:
   - **Windows**: Click on "Download R for Windows" and follow the installation prompts.
   - **macOS**: Select "Download R for macOS" and install the downloaded file.
   - **Linux**: Follow the instructions for your specific distribution (e.g., Debian/Ubuntu).
3. **Run the Installer**: Follow the prompts to complete the installation.

### Step-by-Step Guide to Install RStudio

1. **Ensure R is Installed**: Make sure you have installed R as outlined above.
2. **Download RStudio**: Visit [RStudio Desktop Download](https://posit.co/download/rstudio-desktop/).
3. **Install RStudio**:
   - Run the installer and follow the on-screen instructions.
   - Open RStudio after installation and ensure it recognizes your R installation.

## Running R on Tufts Datalab computer
R and RStudio have been donwloaded and installed in all computers in the Tufts Data Lab, and you are welcome to use them. 
For more information on hours, services available, and the other software installed on those computers, please see the [Medford Data Lab](https://sites.tufts.edu/datalab/medford-data-lab/) and [Boston Data Lab](https://sites.tufts.edu/datalab/boston-data-lab/).

## Running R in Linux/MacOS (UNIX)

Although most users prefer RStudio for its intuitive interface, R can be run directly in any BASH terminal. Follow these steps to get started:

1. **Open Terminal**: Launch a terminal window on your Linux/MacOS system.
2. **Start R Interpreter**: Type the command:
   ```
   R
   ```
   This will open the R interpreter.
3. **Execute Commands**: You can now run R commands directly in the terminal.
4. **Exit R**: When you are finished, type:
   ```
   q()
   ```
   This will close the R session.

## Running R in the Tufts HPC Cluster

R can be used on the high-performance computing (HPC) cluster. For more information and detailed guidance, visit the [Tufts HPC R Guide](https://tuftsrt.github.io/guides/dev/hpc/Application/r.html). For more information on how to use the HPC, see the [Tufts HPC Guide](https://tuftsrt.github.io/guides/dev/hpc/Access/index.html).

>  **To Get Support:** - Please email tts-research@tufts.edu for all Tufts HPC cluster questions and requests.