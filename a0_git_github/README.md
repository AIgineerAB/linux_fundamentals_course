# Git and github

<a href="" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/.png?raw=true" alt="file management" width="600">
</a>

This is a short introduction to git and github 

## Setup

Install git on oracle linux 

```bash
sudo dnf install git-core
```

Follow the steps to signup for an account in [github](https://github.com/signup).

Now go into your terminal and generate an SSH keypair. You will learn more about SSH later on.

```bash
ssh-keygen -t ed25519 -C "you@example.com"
```

You will be prompted with `Enter file in which to save the key (/home/user/.ssh/id_ed25519):`

here you can just press enter

Then when prompted for passphrase just click enter to skip it for simplicity. 

Now add this key to ssh agent

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519.pub
```

Then finally print out the public key that we will paste into github
```bash
cat ~/.ssh/id_ed25519.pub
```

Now paste it and go into github in the browser and click settings -> ssh and gpg keys and add it to there. 

## Create a repo

Create a repo inside of github 

<printscreen here>


## Clone the repo 

Copy the repo ssh link 

Clone it to local 

```bash
git clone <ssh-url>
```


## Add, commit, push

```bash
git add .
git commit -m "your commit message"
git push
```


## Other videos 📹

## Read more 👓
- [vim cheatsheet](https://vim.rtorr.com/)

