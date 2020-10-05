Below is command  for Mac to copy all the files with particular extension from one folder to another, while maintaining the directory structure.
 
Command >>
rsync -a -m --include '*/' --include '*.java' --exclude '*' <PATH-OF-SOURCE-DIRECTORY> <PATH-OF-DESTINATION-DIRECTORY>

Here,

rsync - remote (and local) file-copying tool.
-a - archive mode to preserve almost everything (including symlinks, modification dates, file permissions, owners etc.)
-m, --prune-empty-dirs - prune empty directories from source tree. If you want to include empty directories, just remove this option from the above command.
--include="*/" --include="*.java" --exclude="*" - To include only specific files, you first need to include those specific files, then exclude all other files. In our case, we have included *.java files and exclude everything else.
PATH-OF-SOURCE-DIRECTORY - Source directory.
PATH-OF-DESTNATION-DIRECTORY - Destination directory.
 
 
Example::
rsync -a -m --include '*/' --include '*.java' --exclude '*' ~/Source ~/Dstination
 
Note:: I have already tried this command and this worked for me as expected.
Reference:: https://ostechnix.com/copy-specific-file-types-while-keeping-directory-structure-in-linux/ 
