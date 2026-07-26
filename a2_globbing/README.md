# Globbing

<a href="" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/.png?raw=true" alt="file management" width="600">
</a>

Globbing is shell expansion of wildcard patterns for files, meaning it will replace the pattern with filename that it matches.

| pattern | meaning                       |
| ------- | ----------------------------- |
| \*      | ≥ 0 sequence of characters    |
| ?       | exactly one character         |
| [abcd]  | one character a,b,c,d         |
| [a-z]   | one character in the range    |
| [^abcd] | one character not a,b,c,d     |
| {a,b,c} | brace expansion - each string |
| {1..5}  | each value in the range       |


## Brace expansion {..}

Brace expansions are pure text expansion -> it generates the strings 

Example 

```bash

# exapands to touch file1.txt file2.txt file3.txt file4.txt
touch file{1..4}.txt

# create directories dir_a, dir_b, dir_c
mkdir dir_{a,b,c}

# create files cool1.md, cool2.md, ... ,cool20.md
touch cool{1..20}.md
```

## Wildcard characters

```bash
# list all files ending with .txt
ls *.txt

# list all that matches cool0.md, cool1.md, ..., cool9.md
ls cool?.md

# list all that matches cool10.md, cool11.md, ..., cool20.md
ls cool??.md

# clean up all file.txt
rm file*.txt
```

## Bracket glob [..]

Bracket globbing is filename matching, so the files need to exists to be matched

```bash

# lists all files that matches this pattern
ls file[1-9].txt

# moves these files into a directory
mv file*.txt files_dir
```



## Other videos 📹

## Read more 👓
