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

Now we'll use grep to search this article for various things and go through some useful options for grep



## pipe 


- pipe standard output to grep

## Other videos 📹

## Read more 👓
