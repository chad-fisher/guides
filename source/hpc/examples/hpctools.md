# HPC Helper Tool - hpctools

`hpctools` is availabe a set of helper scripts that helps users locate avaliable resources, checking home directory usage and research storage space quota, monitoring active and completed jobs, .etc

Users can run hpctools on any node (compute or login):

```
[username@login-prod-01 ~]$ module load hpctools
	 command: hpctools
[username@login-prod-01 ~]$ hpctools
 Please select from the following options:

  1. Checking Free Resources On Each Node in Given Partition(s)

  2. Checking Free GPU Resources On Each Node in Given Partition(s)

  3. Checking username Past Completed Jobs in Given Time Period

  4. Checking username Active Job informantion

  5. Checking Project Space Storage Quota Informantion

  6. Checking Any Directory Storage Usage Informantion

  Press q to quit

Your Selection:
|
```

**Then follow the on-screen instructions to select option `1` to `6`.**

`Option 1. Checking Free Resources On Each Node in Given Partition(s)` 

- Check available CPU core and memory in specified partition(s) user has access to.
- Memory is in MB.

` Option 2. Checking Free GPU Resources On Each Node in Given Partition(s)`

- Check avalilable CPU and GPU resources in specified partition(s) user has access to.

`Option 3. Checking username Past Completed Jobs in Given Time Period`

- Check all of user completed job since a specific date YYYY-MM-DD

`Option 4. Checking username Active Job informantion`

- List all of user's running jobs
- Check details on specified job

`Option 5. Checking Project Space Storage Quota Informantion`

- Check lab research storage usage and quota

`Option 6. Checking Any Directory Storage Usage Informantion`

- Check the detailed usage of user specified directory (provide full path)
- This may take a while if the directory is large