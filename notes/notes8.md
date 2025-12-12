# Linux Text Processing Commands

## `cat`
**Definition:**  
`cat` displays the contents of a file or combines multiple files.

**Usage / Formula:**  
`cat [options] file(s)`

**Examples:**  
`cat notes.txt`  
**Output:**  
```
Line 1  
Line 2  
Line 3  
```
`cat file1.txt file2.txt`  
**Output:**  
```
Content of file1  
Content of file2  
```

## `tac`
**Definition:**  
`tac` displays file contents in reverse.

**Usage / Formula:**  
`tac [options] file`

**Examples:**  
`tac notes.txt`  
**Output:**
```  
Line 3  
Line 2  
Line 1  
```

`tac list.txt`  
**Output:**  
```
C  
B  
A  
```

## `head`
**Definition:**  
`head` displays the first lines of a file (10 for the example).

**Usage / Formula:**  
`head [options] file`

**Examples:**  
`head notes.txt`  
**Output:**  
```
Line 1  
Line 2  
Line 3  
```

`head -n 2 notes.txt`  
**Output:**  
```
Line 1  
Line 2  
```

## `tail`
**Definition:**  
`tail` displays the last lines of a file (10 for the example).

**Usage / Formula:**  
`tail [options] file`

**Examples:**  
`tail notes.txt`  
**Output:**  
```
Line 8  
Line 9  
Line 10  
```

`tail -n 2 notes.txt ` 
**Output:**  
```
Line 9  
Line 10  
```
## `cut`
**Definition:**  
`cut` extracts selected sections from each line.

**Usage / Formula:**  
`cut [options] file`

**Examples:**  
`cut -c 1-4 notes.txt`
**Output:**
```  
Line  
Line  
```

`cut -d "," -f 1 names.csv`  
**Output:**  
```
Alex  
Robert  
```
---
## `awk`
**Definition:**  
`awk` is a text-processing tool used to search, filter, and manipulate text based on patterns and fields.

**Usage / Formula:**  
`awk 'pattern { action }' file`

**Examples:**  
`awk '{print $1}' names.txt`  
**Output:**  
```
Alex  
robert  
Potato 
```
`awk -F "," '{print $1, $3}' data.csv`  
**Output:**  
```
Alex 24
robert 50  
potato 1  
```

---

## `sort`
**Definition:**  
`sort` orders lines alphabetically or numerically.

**Usage / Formula:**  
`sort [options] file`

**Examples:**  
`sort names.txt`  
**Output:**  
```
Alex  
robert  
platano 
```
`sort -n numbers.txt` 
**Output:**  
```
1  
5  
10  
```

## `wc`
**Definition:**  
`wc` counts lines, words, and characters.

**Usage / Formula:**  
`wc [options] file`

**Examples:**  
`wc notes.txt`  
**Output:**  
```
10  50  300 notes.txt  
```
`wc -l notes.txt`  
**Output:**  
`10 ` 
