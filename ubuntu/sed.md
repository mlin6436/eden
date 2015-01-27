# sed

### Replace a `newline` (\n)

```bash
$ sed ':a;N;$!ba;s/\n/ /g'
```

This will read the whole file in a loop, then replaces the newline(s) with a space.
- Create a label via :a
- Append the current and next line to the pattern space via N
- if we are before the last line, branch to the created label $!ba ($! means not to do it on the last line (as there should be one final newline)).
- finally the substitution replaces every newline with a space on the pattern space (which is the whole file).

### Double space content in file

```bash
$ sed 'G' file
```

- Sed reads a line and places it in the pattern buffer.
- G command appends the hold buffer to the pattern buffer separated by \n. so one newline will be appended with the pattern space content.
- Similarly, If you want to triple space a file, append hold buffer content to the pattern buffer twice. (G;G)

### Print file content in reverse order

```bash
$ sed -n '1!G;h;$p' thegeekstuff.txt
```

- First line will be placed into the hold space as it is.
- From the 2nd line onwards, just append the hold space content with the pattern space. (Remember 2nd line is in pattern space, and 1st line is in hold space).
- Now 1st and 2nd line got reversed and move this to the hold space.
- Repeat the above steps till last line.
- Once the last line is reached, just append the hold space content with the pattern space and print the pattern space.

### Print a paragraph, if it contains given pattern

```bash
$ sed -e '/./{H;$!d;}' -e 'x;/pattern/!d' file
```

- Till the empty line comes, keep appending the non empty lines into the hold space
- When empty line comes i.e paragraph ends, exchange the data between pattern and hold space. So that whole paragraph will be available in pattern space.

### Print the line immediately before a pattern match

```bash
$ sed -n '/pattern/{g;1!p;};h' file
```

- For each cycle, place the line into hold buffer, if it doesn’t match with the pattern “Mysql”.
- If the line matches with the pattern, get the data from the hold space(previous line) using g command and print it.
- In case, if the first line matches with the pattern “Mysql”,anyway hold space will be empty.(There is no previous line to the first line).So first line should not get printed(1!p)

### Delete the last line of each paragraph

```bash
$ sed -n -e '/^$/{x;d}' -e '/./x;p' file
```

- If the line is not empty,then exchange the line between pattern and hold space. So first line will be placed in the hold space.
- When next non empty line comes, exchange the pattern space and hold space, and print the pattern space. i.e first non empty line will be printed and 2nd line goes to hold. And in next cycle, 2nd non empty line is printed when 3rd line goes to hold and goes on like this.
- When empty line comes (previous line to the empty line will be available in hold buffer) just exchange pattern and hold space, and delete the line (last line of the paragraph) and start the next cycle.

### For each line, append the previous line to the end of it

```bash
$ sed 'H;x;s/^\(.*\)\n\(.*\)/\2\1/' file
```

- Place the first line in Hold buffer.
- When the second line comes, append to Hold space (first line)
- Then exchange pattern and hold buffer. So now pattern space will have first and second line separated by \n, Hold space will have only second line.
- So interchange the lines in the pattern space.
- The above steps happens till the end of the file
