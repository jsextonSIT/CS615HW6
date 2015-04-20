Dan Hup, Julian Sexton, Neal Trischitta

April 20,2015A
CS615: System Admin

Required Flags
	EC2_BACKUP_FLAGS_AWS : Must contain --key_name
	EC2_BACKUP_FLAGS_SSH : Must be give full path to private ssh key.

Opinional Flags
	EC2_BACKUP_FLAGS_VERBOSE: true/false

Usage
	ec2-backup.sh [-h] [-v vol-id] [-m method] dir
		- Required
	    EC2_BACKUP_FLAGS_SSH="-i path_to_private_key"
		Note: The User must specified --key-name also the program expect the user to have the security groups presented of two ways
			1. Specified --security-groups [value] otherwise it will use the default group.
			2. Specified default security group to allow access to the current host

Error Codes
 
1: parameters or flags not set.

Running Examples
 ./ec2_backup -h : will display usage statement then exit
 ./ec2_backup -v : will allow verbose output

Notice: if a method isnt given method will default to dd. 
./ec2_backup dir

Notice: if a vol-id isnt given a vol-id will be generated.
 ./ec2_backup  -v [vol-id] dir

Sample Output:
