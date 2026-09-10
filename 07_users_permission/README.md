# Permissions and ownership

<a href="" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/.png?raw=true" alt=" permissions" width="600">
</a>


## View file permissions
```bash
# long listing
ls -l   

ls -l /etc/ssh/sshd_config
# -rw-------. 1 root root 3672 Sep  8 18:44 /etc/ssh/sshd_config
```

### Output

First character (- in this case) is the file type.  Then follows the permissions `rw-------` and then follows dot ., which is extended attributes. Extended attributes means there is extra metadata such as security labels attached to this file.

**permission labels**

- owner: rw-
- group: ---
- others: --- 

Here owner has read and write, group and others have no permissions to this file.




- chmod
- chown
- permission numbers
- permission symbols

## Other videos 📹

## Read more 👓
- [How do you view Linux file permissions? - Red Hat blog](https://www.redhat.com/en/blog/linux-file-permissions-explained)