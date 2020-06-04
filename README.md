# VIM


wiki VIM


0. [Basics of VIM]()
1. [How to insert a string at the beginning of a line](https://github.com/c4arl0s/VIM/blob/master/README.md#1-how-to-insert-a-string-at-the-beginning-of-a-line)
2. [How to cut and paste](https://github.com/c4arl0s/VIM/blob/master/README.md#2-how-to-cut-and-paste-ctrl-v-or-ctrl-v)
3. [How to find a string](https://github.com/c4arl0s/VIM/blob/master/README.md#3-how-to-find-a-string)
4. [how to replace with an / across the string to replace](https://github.com/c4arl0s/VIM/blob/master/README.md#4-how-to-replace-with-an--across-the-string-to-replace)
5. [Repeats the last action](https://github.com/c4arl0s/VIM/blob/master/README.md#5-repeats-the-last-action)
6. [Insert a # character at the beginning of the line](https://github.com/c4arl0s/VIM/blob/master/README.md#6-insert-a--character-at-the-beginning-of-the-line)
7. [Find an precise string an replace with something](https://github.com/c4arl0s/VIM/blob/master/README.md#7-find-an-precise-string-an-replace-with-something)
8. [Insert a character or string at the end of a selected line](https://github.com/c4arl0s/VIM/blob/master/README.md#8-insert-a-character-or-string-at-the-end-of-a-selected-line)
9. [Insert a consecutive number at the beginning of a selected line]()
10. [Delete all lines that contains a specific patter](https://github.com/c4arl0s/VIM#10-delete-all-lines-that-contains-a-specific-pattern)
11. [Make lowercase](https://github.com/c4arl0s/VIM#11-make-lowercase)
12. [Make upercase](https://github.com/c4arl0s/VIM#12-make-upercase)
13. [Find any String inside parenthesis Ex. (http://...)](https://github.com/c4arl0s/VIM#13-find-any-string-inside-parenthesis-ex-http-with-empty-content-)
14. [Find quickly a word in a line using f ](https://github.com/c4arl0s/VIM#14-find--a-particular-character-in-a-line-using-f-)
15. [Delete only a character](https://github.com/c4arl0s/VIM#15-delete-only-a-character)
16. [Change inside brackets](https://github.com/c4arl0s/VIM#16-change-inside-brackets)
17. [Quickly change a word or line](https://github.com/c4arl0s/VIM#17-quickly-change-a-word-or-line)
18. [Jump to the place of last Edit]()
19. [Yank the current line, including the newline character at the end of the new line, yy or Y]()
20. [Jump to the place before of the last Edit]()
21. [Yank the current word (no spaces)]()
22. [Yank the current word (with sorounding spaces)]()
23. [Yank all contained inside parenthesis ()]()
24. [Yank all contained inside brackets []]()
25. [Replace the character under the cursor]()
26. [Enter insert mode, replacing characters rather than inserting]()
27. [redo]()

# 0. [Basics of VIM]()

- normal mode [Esc]
- insert mode [i]
- replace mode

selection mode - visual 
							 - visual line
							 - visual block
- command line model

notations for control + V
´´´console
^V
Ctrl-V
<C-V>
´´´

> the interface itself is a programming language

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

# 8. [Insert a character or string at the end of a selected line](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

1. Select the line or lines. Type ESC, then ctrl-V.
2. then type: s/$/anyString/

it will looks like this:

```console
:'<,'>s/$/anyString/
```

# 9. [Insert a consecutive number at the beginning of a selected line](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

```console
let i=1 | '<,'>g/^/ s//\=printf("%d ",i) / | let i+=1
```
# 10. [Delete all lines that contains a specific pattern]()

1. Press Esc
2. type: 
```consoile
:g/.com/d
```
g - find it globally
.com - pattern .com
d - delete

- another example: Delete all lines that start with // and it is the end of the line

1. press Esc
2. type:

```console
:%g/^\/\/$/d
````

```vim
// hola
// 
// como estas
//
```

output:

```vim
// hola
// como estas
```

# 11. [Make lowercase](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

- Select word, line or several words, then:

```console
:gu
````

# 12. [Make upercase](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

- Select word, line or several words, then:

```console
:gU
```

# 13. [Find any String inside parenthesis Ex. (http://...) with empty content ()](https://github.com/c4arl0s/VIM/blob/master/README.md#vim)

```console
:%s/(.*)/()/
```

# 14. [Find  a particular character in a line using f ]()

In normal mode

type:

fa - finds the first a ahead of the cursor
Fa - fins the first a before of the cursor.

# 15. [Delete only a character](https://github.com/c4arl0s/VIM#vim)

type in normal mode:

x

# 16. [Change inside brackets](https://github.com/c4arl0s/VIM#vim)

in normal mode:

```console
ci[
```

# 17. [Quickly change a word or line](https://github.com/c4arl0s/VIM#vim)

cw		change word
caw		
ciw	
cc 		change an entire line
cis		change inside sentence


# 18. [Jump to the place of last Edit]()

```vim
g;
```

# 19. [Yank the current line, including the newline character at the end of the new line, yy or Y]()


```console
yy
Y
```

# 20. [Jump to the place before of the last Edit]()

Type again g; so many times required to find the last Edit

```
g;
```

# 21. [Yank the current word (no spaces)]()

```console
yiw
```
this command exclude white spaces around the word.

# 22. [Yank the current word (with sorounding spaces)]()

```console
yaw
```
This command include whithe spaces sorounding

#i23. [Yank all contained inside parenthesis ()]()

```console
yi)
```

24. [Yank all contained inside brackets []]()

```console
yi]
```

# 25. [Replace the character under the cursor]()

```console
r{character}
```
# 26. [Enter insert mode, replacing characters rather than inserting]()

```console
R
```

then start typing

# 27. [redo]()

Type Esc, then
```console
u
````
tyoe Esc, then

ctrl-r 

To redo the last undo command

Type . to copy the last redo command


