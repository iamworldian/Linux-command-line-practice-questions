
# Linux Command Line Practice Questions

# Index
* [Part - 1](#part---1)
    * [Warming Up](#warming-up)
    * [Navigation](#navigation)
    * [Manipulating Files And the Directories](#manipulating-files-and-the-directories)
    * [Working with commands](#working-with-commands)
    * [Redirecting and piping](#redirection-io-and-piping)
    * 

   
# Part - 1

## Warming Up

1. Show date in the terminal<details><summary>ANS</summary>
    `[me@linux ~] date`
</details>

2. Show calend in the terminal<details><summary>ANS</summary>
    `[me@linux ~] cal`
</details>

3. Show current amount of free space on your disk drives / disk drives info ?<details><summary>ANS</summary>
    `[me@linux ~] df`
</details>

4. Show disk drives infos(Size , Used , Available , Use% etc) ?<details><summary>ANS</summary>
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

1. Copy a file named 'Book.pdf' from the Downloads folder to Desktop ? <details><summary>ANS</summary>
    `[me@linux ~] cp /home/$USERNAME/Downloads/Book.pdf /home/$USERNAME/Desktop`
</details>

2. Copy a directory named 'Books' from the Downloads folder to Desktop ? <details><summary>ANS</summary>
    `[me@linux ~] cp -r /home/$USERNAME/Downloads/Book/ /home/$USERNAME/Desktop`
</details>

3. Copy all file starts with 'Book' and ends with '.pdf' from the Downloads folder to Desktop ? [hint : use wildcards] <details><summary>ANS</summary>
    `[me@linux ~] cp /home/$USERNAME/Downloads/Book*.pdf /home/$USERNAME/Desktop`
</details>

4. Create a directory names 'dir1' in the current directory <details><summary>ANS</summary>
    `[me@linux ~] mkdir dir1`
</details>

5. Create 3 directories names 'dir1' , 'dir2' , 'dir2' in the current directory <details><summary>ANS</summary>
    `[me@linux ~] mkdir dir1 dir2 dir3`
</details>

6. Move a file named 'Book.pdf' from the Downloads folder to Desktop ? <details><summary>ANS</summary>
    `[me@linux ~] mv /home/$USERNAME/Downloads/Book.pdf /home/$USERNAME/Desktop`
</details>

7. Move a directory named 'Books' from the Downloads folder to Desktop ? <details><summary>ANS</summary>
    `[me@linux ~] cp -r /home/$USERNAME/Downloads/Book/ /home/$USERNAME/Desktop`
</details>

8. Copy all file starts with 'Book' and ends with '.pdf' from the Downloads folder to Desktop ? [hint : use wildcards] <details><summary>ANS</summary>
    `[me@linux ~] mv /home/$USERNAME/Downloads/Book*.pdf /home/$USERNAME/Desktop`
</details>

9. Remove a file 'Book.pdf' from Downloads folder <details><summary>ANS</summary>
    `[me@linux ~] rm /home/$USERNAME/Downloads/Book.pdf`
</details>

10. Remove a directory 'Books' from Downloads folder <details><summary>ANS</summary>
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

## Permission

## Process

