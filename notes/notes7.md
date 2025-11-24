# Wildcards and Brace Expansion

## Wildcards

### `*` (matches zero or infinite characters)
Examples:
- `ls *.txt`
- `rm file*`

### `?` (matches only one character)
Examples:
- `ls img?.jpg`
- `cp doc?.pdf`

### `[]` (matches any one character in brackets)
Examples:
- `ls file[1-3].txt`
- `ls report[a-c].log`


## Brace Expansion

### Basic Examples
- `echo {A,B,C}`
- `touch file{1..5}.txt`

## Creating Directory Structures with Brace Expansion

### Example 1
mkdir -p project/{docs,src,bin}

### Example 2
mkdir -p data/{2023,2024}/{01..12}

### Example 3
mkdir -p site/{html,css,js}/{dev,prod}
