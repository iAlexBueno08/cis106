# Notes 9

## grep
**Definition:** `grep` filters through text and shows lines that match.

**Usage / Formula:** `grep [options] pattern file`

**Example 1:**
grep Honda cars.csv

**Example 2:**
grep -i "^honda" cars.csv
- `grep` → command used to search text  
- `-i` → ignores uppercase/lowercase differences  
- `"^honda"` → `^` means “start of the line”, so it matches lines that start with Honda  
- `cars.csv` → file being searched  

---

## awk
**Definition:** `awk` is used to work with columns in a file.(Better cut)

**Usage / Formula:** `awk ' Field { action }' file`

**Example 1:**
awk '{print $1}' cars.csv
- Prints the first column of each line

**Example 2:**
awk -F"," '{print $1, $3}' cars.csv
- `awk` → command  
- `-F","` → sets the field separator to a comma   
- `{print $1, $3}` → prints column 1 and column 3  
- `cars.csv` → file  

---

## sed
**Definition:** `sed` edits text.

**Usage / Formula:** `sed 's/pattern/replacement/' file`

**Example 1:**
sed 's/;/,/g' cars.csv
- Replaces semicolons with commas

**Example 2:**
sed 's/Honda/Toyota/g' cars.csv
- `sed` → command
- `s` → substitute command  
- `Honda` → text to change 
- `Toyota` → replacement text  
- `g` → replace all matches on each line  
- `cars.csv` → file being edited  

---

## Pipe |
**Definition:** `|` sends the output of one command into another command.

**Example 1:**
ls | grep txt
- Sends file list to `grep` to show only `.txt` files

**Example 2:**
grep Honda cars.csv | sed 's/;/,/g'
- `grep Honda cars.csv` → finds Honda lines  
- `|` → passes result to next command  
- `sed 's/;/,/g'` → replaces semicolons with commas  

## redirecting Output to a File >
**Definition:** `>` saves command output to a file and overwrites it( deletes what was in it and put the new output).

**Example 1:**
ls > files.txt

**Example 2:**
grep 'Honda' cars.csv > honda.csv
- `grep Honda cars.csv` → finds Honda 
- `>` → redirects output  
- `honda.csv` → file created or overwritten  

---

## Append Output to a File >>
**Definition:** `>>` adds output to the end of a file without deleting the data that was already in it.

**Example 1 (Simple):**
date >> log.txt

**Example 2 (More in-depth):**
grep 'Honda' cars.csv >> honda.csv
- `grep Honda cars.csv` → gets Honda lines  
- `>>` → adds output  
- `honda.csv` → file being added to  


