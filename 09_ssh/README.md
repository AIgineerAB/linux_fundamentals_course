# Secure shell - SSH

**part 1 - ssh**

<a href="https://youtu.be/28kq-XYsGno" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/ssh.png?raw=true" alt="ssh" width="600">
</a>

<br>
<br>

**part 2 - scp and sftp**

<a href="https://youtu.be/NB2Dx_6LstM" target="_blank">
  <img src="https://github.com/kokchun/assets/blob/main/linux/scp_sftp.png?raw=true" alt="sftp and scp" width="600">
</a>

Connect to remote Linux servers in a secure way and transfer files between client and server.

## Setup on VirtualBox

In VirtualBox you need to go into machine and then settings and change from NAT (Network Adress Translation) to `Bridged Adapter` as this gives the VM its own IP address on your real network. If we don't do this it hides behind a virtual router, causing SSH from host to VM not possible, unless we do port forwarding, which I won't go through here.

<img src="https://github.com/kokchun/assets/blob/main/linux/bridged_adapter.png?raw=true" alt="bridged adapter settings" width="500">

## ssh into your VM

Start with logging into your VM and check for ip address inet

```bash
ip a | grep inet
```

Fun fact: inet is a historical name standing for internet address that stucked around in ip command output.

Now you have your ip address and use your host system to connect with ssh. The host is the client and the VM is the server in this case. Linux, mac and windows have openssh installed, so just open a terminal in mac or in windows open git bash/cmd/ powershell and type

```bash
ssh <username>@<ip_address>
```

This will by default try to open port 22 which the server is listening to. Then it prompts for remote servers password and then you are logged in.

## Change name on remote server

On your host system or client open

```bash
nano ~/.ssh/config
```

and paste in this text

```md
Host <cool_server_name>
HostName <host_ip>
User <yourusername>
Port 22
```

Afterwards you can ssh using <cool_server_name> instead of ip address

## Public and private key

Generate a cryptographic key pair:

- private key - sign
- public key - verify

```bash
ssh-keygen -t ed_id25519 -C your_email
```

For extra layer of security, also add a passphrase to your key when prompted.

Then send the public key to your VM

```bash
ssh-copy-id -i ~/.ssh/id_ed25519.pub <username>@<servername>
```

Note that for windows you need to use WSL or git bash to use ssh-copy-id.

Now try to ssh into your VM and you should not need any password to log. Note that if you added passphrase to the key during ssh-keygen step, then you need that passphrase everytime you use your key.

## Disable password authentication

This reduces the attack surface as the key much longer than a password and thus is much safer than password.

Open sshd_config and update `PasswordAuthentication no`

```bash
sudo nano /etc/ssh/sshd_config
```

Then do

```bash
sudo sshd -t
```

to test that the ssh server configuration for errors. If there was no output then it is fine.

Now restart the sshd (ssh daemon)

```bash
sudo systemctl restart sshd
```

## Copying files with scp

Use `scp` to securely transfer files from client to server

```bash
# base syntax
scp [options] source destination

# example of moving a file from the client to oracle_yt into the path /home/kokchun/Desktop
scp file_client.txt kokchun@oracle_yt:/home/kokchun/Desktop

# copy directories with files from client to server
scp -r dir1 dir2 kokchun@oracle_yt:/home/kokchun/Desktop

# copy directories with files from server to client
scp -r kokchun@oracle_yt:/home/kokchun/Desktop/dir1 .
```

So scp is a single command copy in and out from remote server.

## Interactive session with sftp

The command sftp instead opens up an interactive session with the server. You have access to both your local machine and the remote machine. The local commands precedes with an `l`

```bash
# local
lpwd
lcd
lls

# remote
pwd
cd
ls

# download files remote -> local
get file.txt
get -r dir
get -P dir # preserve permission
mget file1.txt file2.txt
get rmote.txt local-name.txt

# upload files local -> remote
put file.txt
put -r dir
mput file1.txt file2.txt
put local.txt remote-name.txt

# end session
bye
```

## Other videos 📹

## Read more 👓

From LabEx

- [SSH](https://labex.io/tutorials/linux-linux-ssh-command-with-practical-examples-422931)
