# Date Transfer with Globus

This step-by-step guide will show you how to log into Globus and use it to transfer files reliably and securely. You will become familiar with basic Globus concepts and interfaces, and begin to experience how Globus can help you spend more time on your research and less time on data management.

## What is Globus?

[Globus](https://www.globus.org/) is research cyberinfrastructure, developed and operated as a not-for-profit service by the University of Chicago.

Globus provides a secure, unified interface to your research data. Use Globus to 'fire and forget' high-performance data transfers between systems within and across organizations.

https://docs.globus.org/guides/tutorials/manage-files/transfer-files/

## Key Concept: *endpoint*

An endpoint is a server that hosts collections. If you want to be able to access, share, transfer, or manage data using Globus, the first step is to create an endpoint on the system where the data is (or will be) stored.

[Globus Connect](https://www.globus.org/globus-connect) is used to create endpoints. An endpoint can be a laptop, a personal desktop system, a laboratory server, a campus data storage service, a cloud service, or an HPC cluster. As explained below, it’s easy to set up your own Globus endpoint on a laptop or other personal system using Globus Connect Personal. Administrators of shared services (like campus storage servers) can set up multi-user endpoints using Globus Connect Server. You can use endpoints set up by others as long as you’re authorized by the endpoint administrator or by a collection manager.

## Gloubs Account Setup

Tufts has a subscription to Globus, and you can set up a Globus account with your Tufts credentials. 

You can also link other accounts, either personal or through other institutions.

### Link Tufts Account

Visit [www.globus.org](https://www.globus.org/) and click "Login" at the top of the page. On the Globus login page, choose "Tufts University"

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/Globus-auth-01.png" alt="globus-login-01" width=70%>

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/Globus-login.png" alt="globus-login-02" width=70%>

Click `Continue`. This will redirect you to the Tufts Shibboleth login page (SSO). 

Enter your Tufts credentials and log in.

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/Globus-sso.png" alt="globus-sso" width=70%>



Click `Continue` on the "Welcome – You've Successfully Logged In" page.

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/Globus-welcome.png" alt="globus-welcome" width=70%>

You may be prompted to provide additional information. Select "non-profit research or educational purposes" and agree to the "Terms of Service and Privacy Policy". Complete the form and click `Continue`.

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/Globus-auth-02.png" alt="globus-moreinfo" width=70%>

Finally, you need to give Globus permission to use your identity to access information and perform actions (like file transfers) on your behalf.

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/permission.png" alt="globus-permission" width=70%>



### Tufts Globus Collections

After you’ve signed up and logged in to Globus, you’ll begin at the File Manager. The first time you use the File Manager, all fields will be blank.

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/Globus-manager.png" alt="globus-filemanager" width=70%>

Click in the `Collection` field at the top of the File Manager page and type "Tufts". Globus will list collections with matching names. Select target collection.

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/globus-tufts-collections.png" alt="globus-collections" width=70%>



Tufts proivdes two site collections:

- Tufts HPC Cluster Storage - Access to Tufts HPC cluster storage `/cluster/tufts/` and `/cluster/home/`

- Tufts Microsoft Sharepoint

  

### Local Endpoint - Globus Connect Personal

[Globus Connect Personal](https://www.globus.org/globus-connect-personal) 

Select appropriate installer, download, and install. 

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/globus_versions.png" alt="globuspersonal-collections" width=70%>

Follow provided instruction link account and setup Globus Connect Personal.

Once successfully setup local endpoint with Globus Connect Personal, go to [www.globus.org](https://www.globus.org/) and click "Login" at the top of the page. (Follow instructions above)

Click in the `Collection` field at the top of the `File Manager` page and find your personal local endpoint (e.g. "mycollection"). Globus will list collections with matching names. 

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/globus_mycollection.png" alt="globuspersonal-mycollections" width=70%>

### Transfer Files between Two Endpoints

Once setup two desired endpoints in `File Manager`, navigate to the target folders (origion and destination), "drag and drop" files need to be transfered from origion to destination, or click **Transfer or Sync to** in the right-pane menu.

<img src="https://raw.githubusercontent.com/DelilahYM/ImageHost/master/TuftsGlobus/globus-transfer.png" alt="globus-transfer" width=30%>

Between the two `Start` buttons at the top of the page, the Transfer & Timer Options dropdown provides access to several options. By default, Globus verifies file integrity after transfer using checksums. Click the information icons for explanations of the other transfer settings. Globus gives you powerful control over the behavior of the transfer with a simple mouse click. You can modify the transfer settings as to fit your preference. You may also enter a label for the transfer, which is helpful to distinguish between multiple transfers that users submit, but this isn’t required; it tends to be done for "best practices".

Click the Start button to transfer the selected files to the collection in the right panel. Globus will display a green notification panel—confirming that the transfer request was submitted.

Click Activity in the sidebar menu on the left of the page to go to the Activity page. On the Activity page, click the arrow icon on the right to view details about the transfer. 
