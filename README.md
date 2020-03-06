# VIM

wiki VIM

1. [How to insert a string at the beginning of a line](https://github.com/c4arl0s/VIM/blob/master/README.md#1-how-to-insert-a-string-at-the-beginning-of-a-line)
2. [How to cut and paste](https://github.com/c4arl0s/VIM/blob/master/README.md#2-how-to-cut-and-paste-ctrl-v-or-ctrl-v)
3. [How to find a string](https://github.com/c4arl0s/VIM/blob/master/README.md#3-how-to-find-a-string)
4. [how to replace with an / across the string to replace](https://github.com/c4arl0s/VIM/blob/master/README.md#4-how-to-replace-with-an--across-the-string-to-replace)
5. [Repeats the last action](https://github.com/c4arl0s/VIM/blob/master/README.md#5-repeats-the-last-action)
6. [Insert a # character at the beginning of the line](https://github.com/c4arl0s/VIM/blob/master/README.md#6-insert-a--character-at-the-beginning-of-the-line)
7. [Find an precise string an replace with something](https://github.com/c4arl0s/VIM/blob/master/README.md#7-find-an-precise-string-an-replace-with-something)
8. [Insert a character or string at the end of a selected line](https://github.com/c4arl0s/VIM/blob/master/README.md#8-insert-a-character-or-string-at-the-end-of-a-selected-line)

# 1. [How to insert a string at the beginning of a line](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

  * ctrl-v
  * drop down with "down arrow" up to the desired line
  * shift + i
  * type what ever you want to insert in the first line
  * type scape
  * then go down with the down arrow, it automatically will appear what you want
  
# 2. [How to cut and paste (ctrl-v or ctrl-V)](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

1. take place where your want to start to copy or cut
2. Type ctrl-v if you want to select a character or type cltr-V if you want to select a full line.
3. if you type ctrl-v move the cursor where you want to cut/copy. Or move down if you want to copy/cut several lines.
4. if you want to cut, type Esc then d (delete), if you want to copy, Press Esc then y (yank)
5. then you move where you want to paste, then press Esq then type p (paste)

# 3. [How to find a string](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

1. Press Esc
2. type: /
3. type what you want to find.
4. Once you find it, press n, to the next ocurrence.

# 4. [how to replace with an / across the string to replace](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

1. Press Esc
2. Type :%s/stringTolookFor/stringToReplace/

if the string contains an character like /, then type \/ to scape it.

example: 

- before: ()
- after: (https://github.com/c4arl0s/NavigationAndWorkflows#navigationandworkflows)

- type 
```console
:%s/()/(https:\/\/github.com\/c4arl0s\/NavigationAndWorkflows#navigationandworkflows)/
```
- Then type enter.

# 5. [Repeats the last action](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

1. Press ESC
2. press .

# 6. [Insert a # character at the beginning of the line](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

1. Press Esc
2. :1,40s/^/# /

# 7. [Find an precise string an replace with something](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

1. Press ESC
2. :
3. Type

```console
:%s/\<direccionMemoria\>/memoryDirection/
```

# 8. [Insert a character or string at the end of a selected line]()

1. Select the line or lines. Type ESC, then ctrl-V.
2. then type: s/$/anyString/

it will looks like this:

```console
:'<,'>s/$/anyString/
```
