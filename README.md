# Synopsis

This Ansible Asset is intended for getting TSM internal Process running for specified process names under extra varaiable, fetch the process number and cancel before the backup window , to make the tapes drives available for PROD backups 


# Variables

Variable | Default| Comments
----------|-----------------|--------
execution_node (String) | - | **Mandatory**. Hostname of the endpoint as configured in Ansible Tower inventory. It should be having active connectivity with TSM Server.
process_name (List) | - | **Mandatory**. This variable will be having the process names which need to be terminated as per the account requirements

# Results from execution
After successful execution, TSM internal process will be terminated as per list porived under  "process_name" varibale 
Here is the list of return codes that this asset returns.

Return Code Group | Return Code | Comments
----------|--------------|---------


# Procedure

Cancel_Process Playbook is responsible to collect the TSM internal process as per defined extra variable (having connectivity with TSM Servers) to cancel the process before the backup window.

# Support

# Known problems and limitations
* No known problems and limitations as of know within the scope of this automation.

# Prerequisites
* python 3.6 (release 3.6.3) or above
* "execution_node" variable should be configured in Job Template details section with hostname that is configured in inventory. This host should have connectivity enabled with TSM Server.
* TSM admin should have the rights to terminate the process

# Examples

Instructions to use this role 

1- Use Extra Variables section in Job Template to pass values to __process_name__ , __execution_node__

# License

