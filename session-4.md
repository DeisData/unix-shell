# Session 4: Loops
Linking together programs is why Unix has been so successful.
Now, we improve productivity through automation -- with loops!
All those commands we have learned will be put to use.

### Nested Loops Challenge!
What does this do?

```
$ for species in cubane ethane methane
> do
>     for temperature in 25 30 37 40
>     do
>         mkdir $species-$temperature
>     done
> done
```

## Questions of the day:
- How can I perform the same actions on many different files?

## Commands of the Day
**Loop Structure**
```{Loop Structure}
for thing in list_of_things
do
   operation_using $thing
done
```

## Loop Examples

### Output part of files in a directory
```
cd Desktop/data-shell/creatures
for filename in basilisk.dat minotaur.dat unicorn.dat
do 
   head -n 2 $filename
done
```

### Output part of files in a directory
```
cd Desktop/data-shell/creatures
for filename in basilisk.dat minotaur.dat unicorn.dat
do 
   head -n 2 $filename
done
```




### Commands We Already Know
- Navigating File System
  - `ls`: listing contents of working directory with many options: `-F` classify, `-a` list all, `-s` size, `-S` sort by size
  - `pwd` print working directory
  - `clear` the terminal
  - `man` will give you the manual for a command
  - `cd` will change working directory
  - `cd ..` change up to parent directory
  - `cd ~` change to home directory
- Creating Directories or Files:
  - `mkdir path` creates a new directory
  - `nano new` runs a text editor 
  - `touch new` creates an empty (0 byte) file
- Moving or Renaming directories or files safely:
  - `mv -i old new` 
- Copying directories and/or files:  
  - `cp old new` 
  - `cp -r` to copy a directory and all contents
- Removing / Deleting Safely: **Deleting is forever**
  - `rm -i path` delete file with confirmation
  - `rm -i -r path` delete directory and contents    
- Wildcards
  - `?` matches to one character
  - `*` matches to zero to many characters
- Filters 
  - `wc` is the word count 
  - `echo` prints text or the value of a variable
  - `sort` sorts the contents of a file.  `sort -n ` sorts numerically.
- Write to a file from Prompt
  - `>` **redirects** a command's output to a file 
  - `>>` **redirects* a command's output to append to end of a file 
- View particular file contents
  - `cat`concatentate prints the contents of files
  - `less` displays a screenful of the file and then stops
  - `head` shows the first few lines of a file
  - `tail` shows the last few lines of a file
  - `cut` removes or cuts out certain sections of each line in a file
     - `-d` option specifies a delimeter 
     - `-f` option specifies the column for extraction
  - `uniq` filters out adjecent matching lines in a file.
- Piping Commands Together
  - `|` command **pipe** tells the shell to use the output of a command on the left as the input of the command on the right
  
