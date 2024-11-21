## Package installation and module generation with container-mod
Yucheng Zhang, Bioinformatics Engineer, TTS Research Technology
Yucheng.Zhang@tufts.edu

### Introduction
High-Performance Computing (HPC) environments are designed to handle computationally intensive tasks by leveraging powerful hardware, distributed systems, and parallel processing. However, these same features can make package installation more challenging compared to standard desktop or cloud-based computing environments. Users typically lack administrative rights (root access) on HPC systems. This means they cannot use system-wide package managers like apt, yum, or brew to install dependencies.

Tools like Singularity and Apptainer allow users to package their software and dependencies in a container, ensuring portability across HPC systems. However, many users are intimidated by the container syntax. 

To simplify the usage of using containers on Tufts HPC, we developed [container-mod](https://github.com/TuftsRT/container-mod). `container-mod` can serve four purposes: 

- pull the singularity container image from a public container registry, such as [Docker Hub](https://hub.docker.com/).
- generate the modulefile in lmod format, allowing to use `module load xx` command to use the application.
- generate the wrapper executables for the programs provided by the application.
- [Optional] generate the jupyter kernel for containers (e.g., pytorch and tensorflow) that are able to run on Jupyter Lab/Notebook.  

### Syntax
```
container-mod pull|module|exec|pipe [options] URIs
```

### Subcommands
- pull <URI>: Pulls a container image from the provided URI.
- module <URI>: Generates a module file for the container.
- exec <URI>: Creates a wrapper bash script for the container’s programs.
- pipe <URI>: Executes a pipeline that pulls the image, generates a module file, and creates the executable in one step.

### Options

- -d|--dir DIR: Specify the output directory for images, module files, and executables. Defaults to the current directory.
- -f|--force: Force overwrite of existing module files, or executables. Default is to skip existing files.
- -m|--moduledir DIR: Specify the directory that stores module files that can be used as template. Defaults to modulefiles.
- -u|--update: If set, the repository app file will be updated with new version information.
- -p|--personal: Create personal module files in the privatemodules directory (default is no).
- -h|--help: Display this help message and exit.

### Usage
For users, the recommended subcommand is `pipe`, this will run all three subcommands (`pull`, `module`, and `exec`). For options, users need to use `-p` or `--personal`. This will generate the modulefile into users' `$HOME/privatemodules`. 
Another commonly used option is `-j` or `--jupyter`. Many users prefer to run python codes within Jupyter lab/notebook on [Tufts Open OnDemand platform](http://ondemand.pax.tufts.edu). However, to enable python codes to run Jupyter lab/notebook, users need to write a jupyter kernel first. These steps are too complex for beginner users. Adding `-j` or `--jupyter`, the jupyter kernel will be created for users. When users start Jupyter lab/notebook, the newly created kernel is ready to use. 

### Load the module
```
module load container-mod
container-mod -h
```

### Examples
#### vcftools
##### Create the app
```
container-mod pipe -p docker://quay.io/biocontainers/vcftools:0.1.16--h9a82719_5
```
#### Use vcftools
```
module load use.own
module load vcftools/0.1.16 
```

#### pytorch with jupyter support
```
container-mod pipe -p -j docker://tuftsttsrt/pytorch:2.5.1-cuda12.1-cudnn9-runtime-jupyter
```
#### Use pytorch in a jobscript
```
module load use.own
module load pytorch/2.5.1-cuda12.1-cudnn9-runtime-jupyter
```
#### Use pytorch in Jupyter notebook
