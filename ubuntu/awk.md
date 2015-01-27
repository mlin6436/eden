# awk

AWK is built to process column-oriented text data, such as tables. In which a file is considered to consist of N records (rows) by M fields (columns)

### Basic

```bash
$ awk < file '{print $2}'
$ awk '{print $2}' file
```

This prints $2 => 2nd field of the line, awk has whitespace as the default delimiter.

### Delimiter

```bash
$ awk -F: '{print $2}' file
```

This uses `:` as delimiter

```bash
$ awk -F '[:;]' '{print $2}' file
```

This uses multiple delimiter, parsing EITHER `:` OR `;`.

```bash
$ awk -F ':;' '{print $2}' file
```

This uses multiple delimiter, parsing using `:;` as THE delimiter.

```bash
$ awk -F ':' + '{print $2}' file
```

This uses multiple delimiter, to match any number of `:`.

### Arithmetic

```bash
$ echo 5 4 | awk '{print $1 + $2}'
```

Output is `9`, the result of `+` (works as addition).

```bash
$ echo 5 4 | awk '{print $1 $2}'
```

Output is `54`, the result of string concatenation.

```bash
$ echo 5 4 | awk '{print $1, $2}'
```

Output is `5 4`, result forms of the value of 1st and 2nd field.

### Variables

```bash
$ awk -F '<FS>' '{print $2}' file # e.g. awk -F ':' '{print $3}' /etc/passwd
```

`FS`, aka field separator variable, can consist of any single character or regular expression.

```bash
$ awk -F '<FS>' 'BEGIN{OFS="<OFS>"} {print $3, $4}' file # e.g. awk -F ':' 'BEGIN{OFS="|||"} {print $3, $4}' /etc/passwd
```

`OFS`, aka output field separator variable, is the value inserted input separated output.

```bash
$ awk 'BEGIN {RS='<RS>'} {print $1}' file
```

`RS`, aka row separator variable, it works the same as FS, but vertically.

```bash
$ awk 'BEGIN{ORS="<OFS>"} {print $3, $4}' file
```

`ORS`, aka output row separator variable, it works the similar way as OFS.

```bash
$ awk '{print NR}' file
```

`NR`, aka number of records, is equivalent to line number. It is quite helpful when calculating average

```bash
$ awk '{print NF}' file
```

`NF`, aka number of fields, uses whitespace as delimiter and returns the field number the value will change when delimiter is redefined with ``-F`

***Note**

`awk '{print $NF}' file` will print out the last field of the line instead of number of fields, the similar usage is $0, which prints out the line.

```bash
$ awk '{print FILENAME}' file
```

It prints out the file name.

```bash
$ awk '{print FILENAME, FNR}' file1 file2
```

`FNR`, aka number of records for each input file, will give number of records depends on file specified.
