# Simple CLI Diary

This is a text based diary, inspired by [khal](https://github.com/pimutils/khal). Diary entries are stored in raw text. You may say C & ncurses are old, I say paper is older..

![Diary Demo](https://raw.githubusercontent.com/in0rdr/diary/master/demo.gif)

## Usage
1. Set the EDITOR environment variable to your favourite text editor:
    ```
    export EDITOR=vim
    ```

2. Compile (requires ncurses):
    ```
    make
    ```

3. Install the binary (optional):
    ```
    sudo make install
    ```

   This will copy the binary to /usr/local/bin. To use a different path,
   change the `INSTALL_DIR` variable in the makefile. You can undo this
   with `sudo make uninstall`.

4. Run the diary with the folder for the text files as first argument:
    ```
    diary ~/.diary
    ```

   Instead of this, you can also set the environment variable `DIARY_DIR`
   to the desired directory. If both an argument and the environment
   variable are given, the argument takes precedence.

   The text files in this folder will be named 'yyyy-mm-dd'.

5. Use the keypad or VIM-like shortcuts to move between dates:

    ```
    e, Enter  Edit the current entry
    t         Jump to today
    s         Go to specific date

    j, down   go forward by 1 week
    k, up     go backward by 1 week
    h, left   go left by 1 day
    l, right  go right by 1 day

    g         go to the first date
    G         go to the last date

    J         Go forward by 1 month
    K         Go backward by 1 month
    ```
