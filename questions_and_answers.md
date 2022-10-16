
# Linux Command Line Practice Questions

# Index
* [Part - 1](#part---1)
    * [Warming Up](#warming-up)
    * [Navigation](#navigation)
    * [Manipulating Files And the Directories](#manipulating-files-and-the-directories)
    * [Working with commands](#working-with-commands)
    * 
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

## Redirection and Piping

## Advanced Keyboard Tricks

## Permission

## Process

