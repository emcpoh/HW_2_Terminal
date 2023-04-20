# HW_2_Terminal
Here are the results of my second HW on Terminal

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
- first 1
- second 2
- third 3
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
    $ cat >> tf_2.txt
    the sec 3
## 12. Using `cat` to add the line 'the SeCoNd 2 ' in `tf_3.txt`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
    $ cat >> tf_3.txt
    the SeCoNd 2
## 13. Using `cat` to add the line 'the seConD 2 ' in `tf_2.txt`:

    kapli@mcpoh MINGW64 ~/Desktop/dir_1/inner_dir_1
    $ cat >> tf_2.txt
    the seConD 2
