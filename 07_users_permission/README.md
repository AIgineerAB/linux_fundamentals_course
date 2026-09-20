# Permissions and ownership

<a href="https://youtu.be/r5q11F9Vr_s" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/permissions.png?raw=true" alt=" permissions" width="600">
</a>

## Create a user

We won't go into details on users in this lecture, but to illustrate a multiuser system we need to create a user

```bash
# adds a user and a home directory for that user
sudo useradd -m username

# creates a password for that user
sudo passwd username 
```


Check users in your system 
```bash
cat /etc/passwd | grep home
```

Delete a user and their home directory 
```bash
sudo userdel -r username
```


## View file permissions
```bash
# create a file called script 
nano script
```

Then add the following into that file 

```bash 
#!/usr/bin/env bash

name='Coolname'
echo "Hello $name"
```

Check file permission 

```bash 
ls -l 
```

## Change the owner 

Change the owner to David

```bash
sudo chown David script
```

Now check long listing and you will see the ownership has changed to David 
```bash
ls -l 
```

## Change permission 

```bash
# gives execute for users, group and owner
chmod +x script 
```
note not possible if David owns this script. You can chmod using sudo to give yourself root permissions



## Other videos 📹

## Read more 👓
- [How do you view Linux file permissions? - Red Hat blog](https://www.redhat.com/en/blog/linux-file-permissions-explained)