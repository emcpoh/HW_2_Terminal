# HW_2_Terminal
Here are the results of my second HW on Terminal. This file has not been fully updated. The results of all items can be found in the file HW_2_Terminal.txt.

## 1. Create a folder `dir_1`:

    kapli@mcpoh MINGW64 ~/Desktop
    $ mkdir dir_1
## 2. Go into folder `dir_1`:

    kapli@mcpoh MINGW64 ~/Desktop
    $ cd dir_1
## 3. Create a folder `inner_dir_1`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1
    $ mkdir inner_dir_1
## 4. View current directory:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1
    $ pwd
    /c/Users/kapli/Desktop/dir_1
## 5. While in the dir_1 folder, create an empty text file `tf_1.txt`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1
    $ touch tf_1.txt
## 6. While in the dir_1 folder, use the `cat` command to create a text file `tf_2.txt` with the following lines:
####\- first 1
####\- second 2
####\- third 3
-------------------------------
    kapli@mcpoh MINGW64 ~/Desktop/dir_1
    $ cat > tf_2.txt
    - the first 1
    - the second 2
    - the third 3

after the last line you need to use `ctrl + c` to exit the input command. This rule also used in the next tasks, but i will not mention about it.
## 7. Go to the `inner_dir_1` folder:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1
    $ cd inner_dir_1
## 8. Using `cat` to make a text file `tf_3.txt` with any strings:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
    $ cat > tf_3.txt
    the 1-st one
    the 2-nd one
    the 3-rd one
    the 4-th one
## 9. Using `cat` to add the line 'the second 2' in `tf_3.txt`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
    $ cat >> tf_3.txt
    the second 2
## 10. Using `cat` to add the line 'the sec 2' in `tf_3.txt`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
    $ cat >> tf_3.txt
    the sec 2
## 11. Using `cat` to add the line 'the sec 3' in `tf_2.txt`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
    $ cat >> ../tf_2.txt
    the sec 3
## 12. Using `cat` to add the line 'the SeCoNd 2 ' in `tf_3.txt`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
    $ cat >> tf_3.txt
    the SeCoNd 2
## 13. Using `cat` to add the line 'the seConD 2 ' in `tf_2.txt`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
    $ cat >> ../tf_2.txt
    the seConD 2
## 14. Make a text file `tf_4.txt` in which there will be 15 lines:

        kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
        $ seq 15 | cat > tf_4.txt
## 15. Make a text file `tF_5.txt` in which there will be 13 lines:

        kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
        $ seq 13 | cat > tF_5.txt
## 16. List all files in the folder:

        kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
        $ ls -la
        total 3
        drwxr-xr-x 1 kapli 197609  0 Apr 20 23:37 ./
        drwxr-xr-x 1 kapli 197609  0 Apr 20 23:12 ../
        -rw-r--r-- 1 kapli 197609 30 Apr 20 23:37 tF_5.txt
        -rw-r--r-- 1 kapli 197609 88 Apr 20 23:26 tf_3.txt
        -rw-r--r-- 1 kapli 197609 36 Apr 20 23:36 tf_4.txt
## 17. Exit the `inner_dir_1` folder

        kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
        $ cd ..
## 18. Output the contents of the file `tf_3.txt` to the terminal:

        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ cat inner_dir_1/tf_3.txt
        the 1-st one
        the 2-nd one
        the 3-rd one
        the 4-th one
        the second 2
        the sec 2
        the SeCoNd 2
## 19. Find the path to the file `tf_4.txt`:

        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ find -name tf_4.txt
        ./inner_dir_1/tf_4.txt
## 20. Clear all the content in file `tf_4.txt` without deleting the file itself:

        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ find -name 'tf_4.txt' | xargs -I{} truncate -s 0 {}
## 21. Find the path to files that have “tf” in the name:
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ find -type f -name '*tf*'
        ./inner_dir_1/tf_3.txt
        ./inner_dir_1/tf_4.txt
        ./tf_1.txt
        ./tf_2.txt
## 22. Find the path to files that have “tf” in the name and letters in any case:
            kapli@mcpoh MINGW64 ~/Desktop/dir_1
            $ find . -type f -iname "*tf*"
            ./inner_dir_1/tf_3.txt
            ./inner_dir_1/tf_4.txt
            ./inner_dir_1/tF_5.txt
            ./tf_1.txt
            ./tf_2.txt
## 23. Find lines in files where there is a combination of letters “sec” in the current folder:
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep "sec" *.*
        tf_2.txt:- second 2
        tf_2.txt:the sec 3
## 24. Find lines in files where there is a combination of letters “sec” in any case in the current folder: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep -i "sec" *.*
        tf_2.txt:- second 2
        tf_2.txt:the sec 3
        tf_2.txt:the seConD 2
## 25. Find lines in files where there is only a combination of letters “sec” in the current folder: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep -w "sec" *.*
        tf_2.txt:the sec 3
## 26. Find lines in files where there is only a combination of letters “sec” in any case in the current folder: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep -iw "sec" *.*
        tf_2.txt:the sec 3
## 27. Find lines in files where there is a combination of letters “second” in the current folder: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep 'second' *.*
        tf_2.txt:- second 2
## 28. Find lines in files where there is a combination of letters “second” in any case in the current folder: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep -i 'second' *.*
        tf_2.txt:- second 2
        tf_2.txt:the seConD 2
## 29. Find lines in files where there is a combination of letters “second” in all folders below the level: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep -r 'second'
        inner_dir_1/tf_3.txt:the second 2
        tf_2.txt:- second 2
## 30. Find only the path and the name of the file in the lines of which there is a combination of the letters “second” in the current folder: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep -l 'second' ./*.*
        ./tf_2.txt
## 31. Find all lines in all files where there is no “second” combination: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep -v 'second' *.*
        tf_2.txt:- first 1
        tf_2.txt:- third 3
        tf_2.txt:the sec 3
        tf_2.txt:the seConD 2
## 32. Find only the name and path to files where there is no “second” combination: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ grep -lv 'second' *.*
        tf_2.txt
## 33. Output the last 4 lines of any text file to the terminal: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ seq 20 | cat > new_file.txt && tail -4 new_file.txt
        17
        18
        19
        20
## 34. Output the first 4 lines of any text file to the terminal: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ head -4 new_file.txt
        1
        2
        3
        4
## 35. One-line command. Create a folder and create a text file with the contents: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ mkdir inner_dir_2 && cat > inner_dir_2/new_file_2.txt
        First line
        Second line
        Third line
## 36. One-line command. Move text files that have the word “sec” in their contents to any one folder: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ find . -type f -name '*.txt' | xargs -I{} grep -l 'sec' {} | xargs -I{} mv {} inner_dir_2
## 37. One-line command. Copy text files that have the word “sec” in their contents to any one folder: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ find . -type f -name '*.txt' | xargs -I{} grep -l 'sec' {} | xargs -I{} cp {} inner_dir_1
## 38. One-line command. Find all lines with “sec” in all text files, copy and paste these lines into one newly created text file: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ find . -type f -name '*.txt' | xargs -I{} grep 'sec' {} | cat > new_file_2.txt
## 39. One-line command. Delete text files that have the word “sec” in their contents: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ find . -type f -name '*.txt' | xargs -I{} grep -l 'sec' {} | xargs -I{} rm {}
## 40. Output the line “Good job!!” to the terminal: 
        kapli@mcpoh MINGW64 ~/Desktop/dir_1
        $ echo 'Good job!!'
        Good job!!
## P.S.
This is my second homework assignment in the Vadim Ksendzov software testing course. If you have any questions or suggestions, you can contact me in the telegram [@raregodpi](https://t.me/raregodpi/ 'Telegram link')