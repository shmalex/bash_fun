
List of files in directory
`ls -ahl`

# Counts

Count of files in current directory
`find . -type f | wc -l`

Count of files size 7
`find . -type f -size 7 | wc -l`

Delete empty (size zero) files
`find . -size 0 -print0 | xargs -0 rm --`