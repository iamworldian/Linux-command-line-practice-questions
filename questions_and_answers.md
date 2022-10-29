
# Linux Command Line Practice Questions

# Index
* [Part - 1](#part---1)
    * [Warming Up](#warming-up)
    * [Navigation](#navigation)
    * [Manipulating Files And the Directories](#manipulating-files-and-the-directories)
    * [Working with commands](#working-with-commands)
    * [Redirecting and piping](#redirection-io-and-piping)
    * [Permission](#permission)
    * [process](#process)
* [Part - 2](#part---2)
    * [Environment](#environment)

   
# Part - 1

## Warming Up

1. Show date in the terminal<details><summary>ANS</summary>
    `[me@linux ~] date`
</details>

2. Show calendar in the terminal<details><summary>ANS</summary>
    `[me@linux ~] cal`
</details>

3. Show current amount of free space on your disk drives / disk drives info ?<details><summary>ANS</summary>
    `[me@linux ~] df`
</details>

4. Show disk drives infos(Size , Used , Available , Use% etc) in human readable format ?<details><summary>ANS</summary>
    `[me@linux ~] df -h`
</details>

5. Display how much free and used physical and swap memory in the system?<details><summary>ANS</summary>
    `[me@linux ~] free`
</details>

6. Display how much free and used physical and swap memory in the system in gigabytes?<details><summary>ANS</summary>
    `[me@linux ~] free --giga`
</details>

7. Exit from the terminal<details><summary>ANS</summary>
    `[me@linux ~] exit`
</details>

## Navigation
1. Print the name of the current directory?<details><summary>ANS</summary>
    `[me@linux ~] pwd`
</details>

2. Show the contents of a directory<details><summary>ANS</summary>
    `[me@linux ~] ls`
</details>

3. Show allocated size of each file in block of current directory<details><summary>ANS</summary>
    `[me@linux ~] ls -s`
</details>

4. Show allocated size of each file in human readable format of current directory<details><summary>ANS</summary>
    `[me@linux ~] ls -sh`
</details>

5. Show all files in long listing format<details><summary>ANS</summary>
    `[me@linux ~] ls -l`
</details>

6. Change your current directory to /usr/bin ?<details><summary>ANS</summary>
    `[me@linux ~] cd /usr/bin`
</details>

7. Go one step backward from your current directory <details><summary>ANS</summary>
    `[me@linux ~] cd ..`
</details>

8. Open a text file with less<details><summary>ANS</summary>
    `[me@linux ~] less [filename or path]`
</details>

## Manipulating Files And the Directories

1. Copy a file named `Book.pdf` from the Downloads folder to Desktop ? <details><summary>ANS</summary>
    `[me@linux ~] cp /home/$USERNAME/Downloads/Book.pdf /home/$USERNAME/Desktop`
</details>

2. Copy a directory named `Books` from the Downloads folder to Desktop ? <details><summary>ANS</summary>
    `[me@linux ~] cp -r /home/$USERNAME/Downloads/Book/ /home/$USERNAME/Desktop`
</details>

3. Copy all file starts with `Book` and ends with `.pdf` from the Downloads folder to Desktop ? [hint : use wildcards] <details><summary>ANS</summary>
    `[me@linux ~] cp /home/$USERNAME/Downloads/Book*.pdf /home/$USERNAME/Desktop`
</details>

4. Create a directory names `dir1` in the current directory <details><summary>ANS</summary>
    `[me@linux ~] mkdir dir1`
</details>

5. Create 3 directories names `dir1` , `dir2` , `dir2` in the current directory <details><summary>ANS</summary>
    `[me@linux ~] mkdir dir1 dir2 dir3`
</details>

6. Move a file named `Book.pdf` from the Downloads folder to Desktop ? <details><summary>ANS</summary>
    `[me@linux ~] mv /home/$USERNAME/Downloads/Book.pdf /home/$USERNAME/Desktop`
</details>

7. Move a directory named `Books` from the Downloads folder to Desktop ? <details><summary>ANS</summary>
    `[me@linux ~] cp -r /home/$USERNAME/Downloads/Book/ /home/$USERNAME/Desktop`
</details>

8. Copy all file starts with `Book` and ends with `.pdf` from the Downloads folder to Desktop ? [hint : use wildcards] <details><summary>ANS</summary>
    `[me@linux ~] mv /home/$USERNAME/Downloads/Book*.pdf /home/$USERNAME/Desktop`
</details>

9. Remove a file `Book.pdf` from Downloads folder <details><summary>ANS</summary>
    `[me@linux ~] rm /home/$USERNAME/Downloads/Book.pdf`
</details>

10. Remove a directory `Books` from Downloads folder <details><summary>ANS</summary>
    `[me@linux ~] rm -r /home/$USERNAME/Downloads/Books`
</details>

## Working With Commands

1. Locate the command `man` <details><summary>ANS</summary>
    `[me@linux ~] which man`
</details>

2. Open the manual page for `ls`<details><summary>ANS</summary>
    `[me@linux ~] man ls`
</details>

3. Display a brief description of the command `find`<details><summary>ANS</summary>
    `[me@linux ~] whatis find`
</details>

## Redirection I/O and Piping

1. Get the long listing of the directory `/usr/bin` and output the list in `output.txt` file not in `stdout` [hint: use `>` operator]<details><summary>ANS</summary>
    `[me@linux ~] ls -l /usr/bin > output.txt`
</details>

2. Show the output of `output.txt`<details><summary>ANS</summary>
    `[me@linux ~] less output.txt`
</details>

3. Get the long listing of the directory `/usr/share` and ***append*** output in `output.txt` file not in `stdout`  [hint: use `>>` operator]<details><summary>ANS</summary>
    `[me@linux ~] ls -l /usr/share >> output.txt`
</details>

4. How to redirect the output of  `ls -l /usr/share` & `stdout & stderr` together in a same file<details><summary>ANS</summary>
    `[me@linux ~] ls -l /usr/share &> output.txt`
</details>

5. Save the string - `The quick brown fox jumped over the lazy dog.` in a file name `dog.txt`<details><summary>ANS</summary>
    `[me@linux ~] cat > dog.txt`
</details>

6. Open the `dog.txt` file<details><summary>ANS</summary>
    `[me@linux ~] cat  dog.txt`

    OR
    `[me@linux ~] less  dog.txt`
</details>

7. Get the long listing of the directory `/usr/share` and print it through `stdout` via `less` in one single command [hint: use pipe `|` operator]<details><summary>ANS</summary>
    `[me@linux ~] ls -l /usr/share | less`
</details>

8. Get the normal listing of the directory `/home` and `/home/{$username}/Desktop` , sort the output and print it through `stdout` via `less` in one single command<details><summary>ANS</summary>
    `[me@linux ~] ls /home /home/{$username}/Desktop | sort | less`
</details>

9. Get the list of files in the directory `/usr/include` where the files have `.h` extension and show them via `stdout`<details><summary>ANS</summary>
    `[me@linux ~] ls /usr/include | grep .h`

    or `[me@linux ~] ls /usr/include *.h`
</details>

9. Get the list of files in the directory `/usr/include` where the files have `.h` extension and show them via `stdout`<details><summary>ANS</summary>
    `[me@linux ~] ls /usr/include | grep .h`

    or `[me@linux ~] ls /usr/include *.h`
</details>

10. Get the number of files in the directory `/usr/include` where the files have `.h` extension and show the number via `stdout`<details><summary>ANS</summary>
    `[me@linux ~] ls /usr/include | grep .h | wc -l`
</details>

11. Get the files in the directory `/usr/include` where the files have `.h` extension and redirect them to `headers.txt`<details><summary>ANS</summary>
    `[me@linux ~] ls /usr/include | grep .h > headers.txt`
</details>

12. Get the files in the directory `/usr/include` where the files have `.h` extension , sort them and redirect them to `headers.txt`<details><summary>ANS</summary>
    `[me@linux ~] ls /usr/include | grep .h | sort > headers.txt`
</details>

13. Get the number of unique files are in these directories `/bin` and `/usr/bin`<details><summary>ANS</summary>
    `[me@linux ~] ls /bin /usr/bin | uniq | wc -l`
</details>

13. Get the number of duplicate files are in these directories `/bin` and `/usr/bin`<details><summary>ANS</summary>
    `[me@linux ~] ls /bin /usr/bin | sort |uniq -d | wc -l`
</details>

13. Get the name of the files are in these directories `/bin` and `/usr/bin`<details><summary>ANS</summary> where they had the word `zip` in the name
    `[me@linux ~] ls /bin /usr/bin | sort | uniq -d | grep zip`
</details>

14. Get first 5 name of the files are in these directories `/bin` and `/usr/bin` where they had the word `zip` in the name<details><summary>ANS</summary> 
    `[me@linux ~] ls /bin /usr/bin | sort | uniq -d | grep zip | head -n 5`
</details>

15. Get last 5 name of the files are in these directories `/bin` and `/usr/bin` where they had the word `zip` in the name<details><summary>ANS</summary> 
    `[me@linux ~] ls /bin /usr/bin | sort | uniq -d | grep zip | tail -n 5`
</details>

15. Use `tail` command to see a live changes of a text file name `dog.txt`<details><summary>ANS</summary> 
    `[me@linux ~] tail -f dog.txt`
</details>

16. Get name of the unique files are in these directories `/bin` and `/usr/bin` where they had the word `zip` in the name and output it into a text file call `zipped.txt` and in `stdout` by one single command [hint: use `tee`]<details><summary>ANS</summary> 
    `[me@linux ~] ls /bin /usr/bin | sort | uniq -d | grep zip | tee zipped.txt`
</details>

## Advanced Keyboard Tricks

1. Display the contents of the history list<details><summary>ANS</summary> 
    `[me@linux ~] history`
</details>

2. Clear the screen<details><summary>ANS</summary> 
    `[me@linux ~] clear`
</details>

3. Move cursos to the begining of the line<details><summary>ANS</summary> 
    `Ctrl - a`
</details>

4. Move cursos to the end of the line<details><summary>ANS</summary> 
    `Ctrl - e`
</details>

## Permission

1. Display your identity?<details><summary>ANS</summary> 
    `[me@linux ~] id`
</details>

    
2. Obeseve the file permission details<br/>`-rw-rw-r-- 1 worldian worldian 16 Oct 21 16:53 test.sh`<br/>
write commands to add excution permission to all<details><summary>ANS</summary> 
    `[me@linux ~] sudo chmod +x test.sh`
</details>


3. Obeseve the file permission details<br/>`-rwxrwxrwx 1 worldian worldian 16 Oct 21 16:53 test.sh`<br/>
write commands to give `read` and `write` permission to only the user and `excution` to all all<details><summary>ANS</summary> 
    `[me@linux ~] sudo chmod u=rw,g=x,o=x test.sh` <br/>or<br/>
    `[me@linux ~] sudo chmod a=x,u=rw test.sh`
</details>


4. Obeseve the file permission details<br/>`-rwxrwxrwx 1 worldian worldian 16 Oct 21 16:53 test.sh`<br/>
write commands to give `read` and `write` permission to only the user and `read` permission toall<details><summary>ANS</summary> 
    `[me@linux ~] sudo chmod a=r,u=rw test.sh`
</details>

## Process

1. Show running process of the current shell ?<details><summary>ANS</summary> 
    `[me@linux ~] ps`
</details>

2. Show all current running processes ?<details><summary>ANS</summary> 
    `[me@linux ~] ps -ax`
</details>

3. Display all processes in BSD format ?<details><summary>ANS</summary> 
    `[me@linux ~] ps aux`
</details>

4. Filter processes according to the user<details><summary>ANS</summary> 
    `[me@linux ~] ps -u "username"`
</details>

5. Listing processes by PID<details><summary>ANS</summary> 
    `[me@linux ~] ps -fp PID"`
</details>

6. Perform full format listing<details><summary>ANS</summary> 
    `[me@linux ~] ps -ef"`
</details>

7. Find all process associated with `systemd`<details><summary>ANS</summary> 
    `[me@linux ~] ps -ef | grep systemd`
</details>

8. Display a tree view of current processes<details><summary>ANS</summary> 
    `[me@linux ~] pstree"`
</details>

9. Process tree with command line argument<details><summary>ANS</summary> 
    `[me@linux ~] pstree -a"`
</details>

10. Process tree with PID<details><summary>ANS</summary> 
    `[me@linux ~] pstree -p"`
</details>

11. Process tree with the user / owner of the process<details><summary>ANS</summary> 
    `[me@linux ~] ps -u"`
</details>

12. Viewing process Dynimically<details><summary>ANS</summary> 
    `[me@linux ~] top"`
</details>

13. Stop a process with PID<details><summary>ANS</summary> 
    `[me@linux ~] kill PID"`
</details>


# Part - 2

## Environment

1. Print the environment variables<details><summary>ANS</summary> 
    `[me@linux ~] printenv | less"`
</details>

2. Print the environment variable $SHELL<details><summary>ANS</summary> 
    `[me@linux ~] printenv SHELL"`
    <br>OR<br>
    `[me@linux ~] echo $SHELL"`
</details>

3. Print the Shell variables<details><summary>ANS</summary> 
    `[me@linux ~] set | less"`
</details>

4. Show the $HOME variable using `echo`<details><summary>ANS</summary> 
   `[me@linux ~] echo $HOME"`
</details>

5. Show the list of available aliases<details><summary>ANS</summary> 
    `[me@linux ~] alias"`
</details>

6. Show all exported environment variables<details><summary>ANS</summary> 
    `[me@linux ~] export"`
</details>

7. Show all exported environment variables to the current shell<details><summary>ANS</summary> 
    `[me@linux ~] export -p"`
</details>

8. Export a new variable called `$NAME` with the value `LINUX` to the current shell.<details><summary>ANS</summary> 
    `[me@linux ~] NAME=LINUX"`
</details>

9. Access the newly created variable `NAME` through `echo`<details><summary>ANS</summary> 
    `[me@linux ~] echo $NAME"`
</details>

## Vim - The Terminal Editor 

