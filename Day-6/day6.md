
# LINUX ADMINISTARTION

## user mangement:

Here we want add user or groups. so we need to add admin. 

```bash
sudo su -         # To login as a admin
useradd <username>         # To crate user
id <username>              # To check whether the user is created or not. It will display the user information
```

In linux we have 2 types of groups  
1..Primary group (gid)  
2.secordary gruop (groups)  
when you create any user by deafault group also created.  
one primary group atleast one secondary group  

```bash
cat /etc/passwd       # It will show users list  
cat /etc/group        # It will show group list
```

```bash
groupadd <groupname>                # It will create groupname
usermod -g <groupname> <username>   # It will add user to particular group
usermod -aG <groupname> <username>  # It will add user to particular group 
```

- `-g` means primary group  
- `-aG` means secorndary group

```bash
userdel <username>     # It will delete the user
groupdel <groupname>   # It will delete the group
```

## set the password to user:

```bash
useradd <username>
passwd <username>
```

Try to login in another window with the latest user

first it will denied the permisssion beacuse we need to modigy the configuration file

```bash
vim /etc/ssh/sshd_config
```

Change the below line:

```
PasswordAuthentication yes
```

```bash
systemctl restart sshd
```

Now you can able to login

---

## Permissions:

```
r ----> READ    ----> 4  
w ----> Write   ----> 2  
x ----> Execute ----> 1
```

Example file permissions:

```
drwx r-x r-x-
```

- `d` ---> Directory/files  
- `rwx` ---> This is for user/admin/root ---> `u`  
- `r-x` ---> This is for groups             ---> `g`  
- `r-x` ---> This is for others             ---> `o`

```bash
chmod ugo+w         # It will write acess to all gruops users,and others
chmod ugo+rwx       # It will all acess to all users,gruops and other
```

By deafalut root can conatin write acess

```bash
chmod 700 <filename>       # It will all acess to user and remaing don't have any acess
chown <username> <filename>
```
