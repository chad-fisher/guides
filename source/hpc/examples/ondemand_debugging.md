# OnDemand - Debugging

> Please try the following easy steps before contacting support team at tts-research@tufts.edu
>
> Make sure to include the following information:
>
>  - Network Info (which network you are on, Tufts Secure or Tufts VPN)
>  - Error Info (what error did you receive, screenshots will help. Please include all info)
>  - Application Issue Only: application launch form info (which application, and what are your selections in the launch form)


### OnDemand Site Connection Issue

1. Make sure you are either on Tufts Secure or Tufts VPN (when off-campus).
2. Make sure you have an active HPC cluster account.
3. Manually type `https://ondemand.pax.tufts.edu/` in your browser. Make sure **NOT** allowing autocompletion.
4. Open OnDemand in Incognito (Chrome) or Private (FireFox) window.
5. Clear your bowser cache.

If you went through all above steps and still can't access `https://ondemand.pax.tufts.edu/` , please contact us at tts-research@tufts.edu


### OnDemand Application Connection Issue

#### Quota Issue:

1. If you are receiving errors regarding your home directory storage `/cluster/home/your_username` out of storage space (quota exceeded), when starting an application. 
2. You can login to the cluster using "HPC Shell Access" or from a terminal app. Use [hpctools](hpctools.md) to check details of your home directory storage usage.
3. Clean up your home directory `/cluster/home/your_username`  and make sure it's under the 30GB home directory storage limit. (DO NOT delete EVERYTHING in your home directory, especially the hidden files)
4. Once your home directory is cleaned up, try launching the OnDemand Application again.

#### RStudio Issue:

Please follow instructions on [RStuido via OnDemand](../Application/rstudio.md) page.

#### Jupyter Notebook:

1. Currently, Jupyter Notebook on OnDemand can not rename files or folders. You can rename your notebooks by using the `Save as` option.
2. In the resource launching form, make sure to select `non-GPU` partition if you are not using GPUs.
3. Make sure you are running the intended version of Jupyter.
4. Make sure you don't have a conda initialization in your `.bashrc` which may have conflict with OnDemand Apps.
5. Once you are able to launch Jupyter Notebook, make sure you run your notebooks with appropriate kernel. 
6. Referece [Conda Environments](../Application/0010_condaenv.md) page on how to setup your conda environment and Jupyter kernel for your workflow.


If you have other issues with OnDemand applications, please contact us at tts-research@tufts.edu
