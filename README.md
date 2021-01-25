# Pre-requisites
Install Ansible on the system

Steps for MoP:-
1. run var_tester_playbook with below command
 
Output:-
   


2. Validate the output and throw error message when the myapp01 & myapp02 not present
- if we pass myapp03/myapp04 or any other value other than myapp01 & myapp02 this will fail and throw the message as below.
 
-	If the value is myapp01, myapp02 it will be passed.

 



	Logic for Printing datastores_transient
Use with_sub_elements module and passed the “playbook_dict” fetched the 
item0 to fetch the “name” from dict and item1 to show the datastores_transient related to both “myapp01” & “myapp02”.

	Logic for Printing and fetching the validation 
Use fail module with when condition and check for if “myapp01” & “myapp02” present , if present it will be passed , if failed then it will throw the message and show expected variables are “myapp01” and “myapp02”. This can be achieved by using prompt, passing extra_args and other ways as well.
Here we are using “validation” as a role.
