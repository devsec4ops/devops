# **Files & Directories**

#### Basic Commands for Navigation

-   pwd: Show your current directory.
    `pwd`
-   cd [directory]: Change directory.
    `cd /var/www/html
    cd ..  # Move up one directory
    cd     # Go back to home directory`
-   ls [options] [directory]: List contents.
    `ls -l
    ls -a /etc
    ls -lh /home/user/`

#### Managing Files and Directories

- Create or update a file.
    `touch newfile.txt`
- Make a directory.
    `mkdir new_folder`
- Copy files or directories.
    `cp source.txt destination.txt
    cp -r source_directory new_directory`
- Move or rename.
    `mv oldname.txt newname.txt
    mv file.txt /home/user/`
- Remove files or directories.
    `rm unwanted_file.txt
    rm -r old_directory`

#### Working with Links
- Create a hard link.
    `ln original.txt hardlink.txt`
- Create a symbolic link.
    `ln -s /path/to/original.txt symlink.txt`

#### Advanced Navigation Techniques
- find [directory] [criteria]: Find files or directories.
    `find /home/user/ -name "*.txt"`
- grep [options] [pattern] [files]: Search inside files.
    `grep "search term" file.txt
    grep -ri "search term" /home/user/`

#### Quick Tips Example Commands
-   Navigating efficiently: Switch back to the last directory.
    `cd -`
-   Autocompletion: Start typing and press Tab to autocomplete.
-   Wildcards: List all `.txt` files
    `ls *.txt`