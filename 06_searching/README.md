# Searching

<a href="" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/.png?raw=true" alt="file management" width="600">
</a>

## setup

For this lecture we'll use curl in combination with an external program called html2text. You can install html2text by doing

```bash
sudo dnf install html2text
```

Then we'll curl this [Linus Torvalds wikipedia article](https://en.wikipedia.org/wiki/Linus_Torvalds) and then pipe the results to html2text and redirecting the content to linus.txt.

```bash
curl -s https://en.wikipedia.org/wiki/Linus_Torvalds | html2text > linus.txt
```

## grep

Now we'll use grep to search this article for various things and go through some useful options for grep.

```bash
# search all occurences of helsinki in linus.txt, one line by default
grep helsinki linus.txt

# search helsinki in linus.txt with two extra lines in top and bottom
grep -2 helsinki linus.txt

# search case insensitive - note how many more matches you get
grep -i helsinki linus.txt

# get the line numbers
grep -n helsinki linus.txt

# lines that starts with helsinki, case insensitive
grep -in ^helsinki linus.txt

# count matching lines for helsinki, case insensitive
grep -ci helsinki linus.txt
```


## pipe 

Piping | sends the standard output `stdout` from a command directly into standard input `stdin` to another command.
You already saw piping in the setup where we sent the output of curl into html2text. Here we'll give some more examples 

We'll use `journalctl` command, which prints log entries from the systemd journal. The systemd is the init system handling startup and management of services, networks etc.

```bash
# try it first without grep 
journalctl 

# now lets find errors
journalctl | grep -i error

# count the errors
journalctl | grep -ic error

# if grep didn't have -c option for count, we could pipe it further to wc (word count program)
# check that you get same result
journalctl | grep -i error | wc -l

# number of lines with kernel 
journalctl | grep -i kernel | wc -l

# words, lines, characters in journalctl
journalctl | wc

# number of errors not related to networks
journalctl | grep -i error | grep -vi network | wc -l
```

## Other videos 📹

## Read more 👓
- [Linux grep Command with Practical Examples - labex](https://labex.io/tutorials/linux-linux-grep-command-with-practical-examples-422703)