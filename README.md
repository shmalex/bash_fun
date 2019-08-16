
List of files in directory
`ls -ahl`

# Counts

Count of files in current directory
`find . -type f | wc -l`

Count of files size 7
`find . -type f -size 7 | wc -l`

Delete empty (size zero) files
`find . -size 0 -print0 | xargs -0 rm --`


# Environment Variables

List Environemtn variables
`export`

idea
`grep -rl FIND_TEXT * | xargs sed -i "" 's/FIND_TEXT/REPLACE_TEXT/g'`


List Environment variables of a running process
`cat /proc/100/environ`

List of environement 
`pgrep python3.6 | xargs -I % sh -c 'cat /proc/%/environ' | sed 's/=/\n/g' > temp0.txt`
`cat temp0.txt | sort | grep -a '/root/path'`


List of files and entries. List of preccess with specific values in environment variables
`grep -Paso '(?<==)[^\0]*\.csv(?=\0)' /proc/[0-9]*/environ | sort`

# Network

List of processes that use port 443
`lsof -i:443`

# Install SSH certificate

The first step is to create a key pair on the client machine (usually your computer):
`ssh-keygen`

Copy the Public Key to CentOS Server
`ssh-copy-id username@remote_host`

done