# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. 
  - /home/cabox/workspace

* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?
  - LICENSE    
  - challenge_files        
  - nix_scavenger_hunt_stretch.md
  - README.md  nix_scavenger_hunt.md  super_scavengers.md

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?* 
  - total 40K
  - drwxrwxr-x  4 cabox cabox 4.0K Oct  3 17:13 .
  - drwxr-xr-x 11 cabox cabox 4.0K Oct  3 17:13 ..
  - drwxrwxr-x  8 cabox cabox 4.0K Oct  3 17:13 .git
  - -rw-rw-r--  1 cabox cabox 1.1K Oct  3 17:13 LICENSE
  - -rw-rw-r--  1 cabox cabox 2.7K Oct  3 17:13 README.md
  - drwxrwxr-x  7 cabox cabox 4.0K Oct  3 17:13 challenge_files
  - -rw-rw-r--  1 cabox cabox 5.5K Oct  3 17:21 nix_scavenger_hunt.md
  - -rw-rw-r--  1 cabox cabox  317 Oct  3 17:13 nix_scavenger_hunt_stretch.md
  - -rw-rw-r--  1 cabox cabox  191 Oct  3 17:13 super_scavengers.md

* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://linux.die.net/man/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?*
  - **a** Includes directory entries whose names begin with a dot (.).
  - **l** List in long format. If the output is to a terminal, a total sum for all the file sizes is output on a line before the long listing.
  - **h** When used with the -l option, use unit suffixes: Byte, Kilobyte, Megabyte, Gigabyte, Terabyte and Petabyte in order to reduce the number of digits to three or less using base 2 for sizes.

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
`bin   dev  fastboot  lib    media  opt   root  sbin  sys  usr
boot  etc  home      lib64  mnt    proc  run   srv   tmp  var`

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:
  - /

* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*
  - /home/cabox

* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?*
  - 3

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*
  - /home/cabox/workspace

* Press the up arrow on your keyboard.* 
  - It showed my previous command - pwd

* Press the up arrow a few more times.* 
  - It showed me all of my previous commands

* Run the `history` command. *What do you see?*
  - 1  pwd
  - 2  ls
  - 3  ls -alh
  - 4  cd
  - 5  pwd
  - 6  cd /
  - 7  cd ~
  - 8  cd
  - 9  ~
  - 10  pwd
  - 11  cd
  - 12  ~
  - 13  pwd
  - 14  cd
  - 15  pwd
  - 16  ls -alh
  - 17  ls /
  - 18  cd
  - 19  pwd
  - 20  cd ~
  - 21  pwd
  - 22  cd challeng_files
  - 23  cd challenge_files
  - 24  challenge_files
  - 25  cd -challenge_files
  - 26  cd ls
  - 27  ls
  - 28  cd /
  - 29  cd challenge_files
  - 30  cd .challenge_fiels
  - 31  cd .challenge_files
  - 32  cd c
  - 33  cd -c
  - 34  pwd
  - 35  cd nix_scavenger_hunt.md
  - 36  ls /
  - 37  cd challenge_files
  - 38  pwd
  - 39  ls -alh
  - 40  pwd
  - 41  cd
  - 42  pwd
  - 43  cd challenge_files
  - 44  cd
  - 45  pwd
  - 46  cd challenge_files
  - 47  cd /
  - 48  pwd
  - 49  cd
  - 50  pwd
  - 51  cd.
  - 52  cd .
  - 53  pwd
  - 54  cd workspae
  - 55  cd workspace
  - 56  pwd
  - 57  cd challenge_files
  - 58  pwd
  - 59  ls
  - 60  ls demo
  - 61  pwd
  - 62  cd .
  - 63  pwd
  - 64  cd ..
  - 65  pwd
  - 66  history
  
### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*
  - cabox

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*
  `cabox    pts/0        Oct  4 20:50 (52.161.27.120)`

* How long has your system been running? Use `uptime` to see, and *paste the result here:*
  `21:18:21 up 28 min,  1 user,  load average: 0.00, 0.00, 0.00`

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*
  - This command lets me see the processes that are currently running on my computer

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?*
  - This command is showing me my processor activity is real-time.

### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?*
  - 2 credit_cards.txt credit_cards2.txt 

* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*
  - Last updated 01-15-2015

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?*
  `./tmp/modi_laboriosam.txt`

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?*
  - 2
  - Britt-Erdman.user:O'Harachester, WA 37261
  - Lissi-Strosin.user:Jewessfurt, WA 00816-7241

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*
  `serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.`

### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*
  - LICENSE
  - README.md
  - challenge_files
  - files.txt
  - nix_scavenger_hunt_stretch.md
  - super_scavengers.md

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
  - Using the 'more' command outputs the information so that it is scrollable. This can make long lists of informtion easier to read. 

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:*
`cabox     1185  0.0  0.1   8816   772 pts/0    S+   00:33   0:00 grep --color=auto csdarcher`