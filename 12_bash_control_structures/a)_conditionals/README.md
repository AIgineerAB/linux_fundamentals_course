# Conditionals 

## Test operators

| operator | meaning          |
| -------- | ---------------- |
| -eq      | equal            |
| -ne      | not equal        |
| -gt      | greater than     |
| -lt      | less than        |
| -ge      | greater or equal |
| -le      | less or equal    |
|          |                  |


## Exit status

Every command in bash returns a numeric exit status (return code) when it finishes running. 

- 0 success
- 1-255 failure/false

It's stored in a special variable `$?`

```bash
ls /tmp
echo "$?" # 0 success

ls /tmpu 
echo "$?" # 1 failure (of course given that you don't have a /tmpu file/directory)
```

## Logic and exit status

```bash
# && AND - run next command only if previous succeeded
mkdir cool_diru && cd cool_diru

# || OR - run next command only if previous failed
cd coolu || echo "failed to cd into coolu"

false; echo $? # 1
true; echo $? # 0 
```
