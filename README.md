1.
root@shubham-Latitude-7480:~mkdir MyFile
root@shubham-Latitude-7480:~#cd MyFile
root@shubham-Latitude-7480:~# ls
dir1  MyFile  snap
2.
root@shubham-Latitude-7480:~# touch document.txt
root@shubham-Latitude-7480:~# ls
dir1  document.txt  MyFile  snap
root@shubham-Latitude-7480:~# cp document.txt MyFile
root@shubham-Latitude-7480:~# cd MyFile
root@shubham-Latitude-7480:~/MyFile# ls
documents  document.txt
root@shubham-Latitude-7480:~/MyFile# cp document.txt documents
root@shubham-Latitude-7480:~/MyFile# cd documents
root@shubham-Latitude-7480:~/MyFile/documents# ls
document.txt
root@shubham-Latitude-7480:~/MyFile/documents# 
3.
root@shubham-Latitude-7480:~/MyFile# touch notes.txt
root@shubham-Latitude-7480:~/MyFile# ls
document  documents  document.txt  notes.txt
root@shubham-Latitude-7480:~/MyFile# rm notes.txt
root@shubham-Latitude-7480:~/MyFile# ls
document  documents  document.txt
4.
root@shubham-Latitude-7480:~# ln document.txt MyFile/documents/hardlink.txt
root@shubham-Latitude-7480:~# ls
dir1  document.txt  MyFile  snap
root@shubham-Latitude-7480:~# cd MyFile
root@shubham-Latitude-7480:~/MyFile# ls
document  documents  document.txt
root@shubham-Latitude-7480:~/MyFile# ls -a
.  ..  document  documents  document.txt
root@shubham-Latitude-7480:~/MyFile# cd documents
root@shubham-Latitude-7480:~/MyFile/documents# ls
document.txt  hardlink.txt
5.
root@shubham-Latitude-7480:~/MyFile# ls
document  documents  document.txt
root@shubham-Latitude-7480:~/MyFile# touch arun.txt asdf.txt azxc.txt
root@shubham-Latitude-7480:~/MyFile# ls
arun.txt  asdf.txt  azxc.txt  document  documents  document.txt
root@shubham-Latitude-7480:~/MyFile# ls a*.txt
arun.txt  asdf.txt  azxc.txt
7.
root@shubham-Latitude-7480:~/MyFile# mkdir backup
root@shubham-Latitude-7480:~/MyFile# cd documents
root@shubham-Latitude-7480:~/MyFile/documents# ls
a.sh  a.txt  b.txt  c.txt  document.txt  d.txt  hardlink.txt
root@shubham-Latitude-7480:~/MyFile/documents# cp * ../backup
root@shubham-Latitude-7480:~/MyFile/documents# ls
a.sh  a.txt  b.txt  c.txt  document.txt  d.txt  hardlink.txt
root@shubham-Latitude-7480:~/MyFile/documents# cd ..
root@shubham-Latitude-7480:~/MyFile# cd backup
root@shubham-Latitude-7480:~/MyFile/backup# ls
a.sh  a.txt  b.txt  c.txt  document.txt  d.txt  hardlink.txt
8.
root@shubham-Latitude-7480:~/MyFile/backup# cd ..
root@shubham-Latitude-7480:~/MyFile# ls > file_list.txt
root@shubham-Latitude-7480:~/MyFile# cat file_list.txt
arun.txt
asdf.txt
azxc.txt
backup
document
documents
document.txt
file_list.txt
root@shubham-Latitude-7480:~/MyFile# cat file_list.txt |grep .txt
arun.txt
asdf.txt
azxc.txt
document.txt
file_list.txt
9.
root@shubham-Latitude-7480:~/MyFile# touch my_notes.txt
root@shubham-Latitude-7480:~/MyFile# vi my_notes.txt
root@shubham-Latitude-7480:~/MyFile# cat my_notes.txt
Hello world
I am shubham
10.
oot@shubham-Latitude-7480:~/MyFile# current_date=$(date)
root@shubham-Latitude-7480:~/MyFile# echo $current_date
Monday 05 February 2024 11:41:12 AM IST
root@shubham-Latitude-7480:~/MyFile# echo $current_date >> my_notes.txt
root@shubham-Latitude-7480:~/MyFile# cat my_notes.txt
Hello world
I am shubham

Monday 05 February 2024 11:41:12 AM IST
11.
12.
oot@shubham-Latitude-7480:~/MyFile# echo "I am adding new text" >> my_notes.txt
root@shubham-Latitude-7480:~/MyFile# cat my_notes.txt
Hello world
I am shubham

Monday 05 February 2024 11:41:12 AM IST
I am adding new text
13.
oot@shubham-Latitude-7480:~/MyFile# ls /etc |grep 'conf' >conf_files.txt
root@shubham-Latitude-7480:~/MyFile# ls
arun.txt  a.sh      backup          document   document.txt   my_notes.txt
asdf.txt  azxc.txt  conf_files.txt  documents  file_list.txt
root@shubham-Latitude-7480:~/MyFile# cat conf_files.txt
adduser.conf
apg.conf
appstream.conf
brltty.conf
ca-certificates.conf
ca-certificates.conf.dpkg-old
dconf
debconf.conf
deluser.conf
e2scrub.conf
fprintd.conf
fuse.conf
gai.conf
hdparm.conf
host.conf
insserv.conf.d
kernel-img.conf
kerneloops.conf
ld.so.conf
ld.so.conf.d
libao.conf
libaudit.conf
logrotate.conf
manpath.config
mke2fs.conf
netconfig
nftables.conf
nsswitch.conf
pam.conf
pnm2ppa.conf
resolv.conf
rsyslog.conf
rygel.conf
sensors3.conf
sudo.conf
sudo_logsrvd.conf
sysctl.conf
ucf.conf
usb_modeswitch.conf
xattr.conf
14.
oot@shubham-Latitude-7480:~/MyFile# vim my_notes.txt

![Screenshot from 2024-02-05 15-41-24](https://github.com/shubh-564738/Linux-assignment-4/assets/155716163/bc7a52c5-efe9-4eb7-a8c8-cf196d78f606)
15.
oot@shubham-Latitude-7480:~/MyFile# grep '^users:' /etc/group
users:x:100:
root@shubham-Latitude-7480:~/MyFile# sudo adduser --home /home/john_doe john_doe
Adding user `john_doe' ...
Adding new group `john_doe' (1006) ...
Adding new user `john_doe' (1004) with group `john_doe' ...
Creating home directory `/home/john_doe' ...
Copying files from `/etc/skel' ...
New password: 
BAD PASSWORD: The password is shorter than 8 characters
Retype new password: 
Sorry, passwords do not match.
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for john_doe
Enter the new value, or press ENTER for the default
	Full Name []: 
	Room Number []: 
	Work Phone []: 
	Home Phone []: 
	Other []: 
Is the information correct? [Y/n]  
root@shubham-Latitude-7480:~/MyFile# sudo usermod -aG users john_doe
root@shubham-Latitude-7480:~/MyFile# id john_doe
uid=1004(john_doe) gid=1006(john_doe) groups=1006(john_doe),100(users)
16.
root@shubham-Latitude-7480:~/MyFile# sudo usermod -aG users john_doe
root@shubham-Latitude-7480:~/MyFile# id john_doe
uid=1004(john_doe) gid=1006(john_doe) groups=1006(john_doe),100(users)
root@shubham-Latitude-7480:~/MyFile# su - john_doe
john_doe@shubham-Latitude-7480:~$ cd home/
17.
root@shubham-Latitude-7480:~/MyFile# sudo chsh -s /bin/bash john_doe
root@shubham-Latitude-7480:~/MyFile# sudo chage -E $(date -d "+1 month" +"%Y-%m-%d") john_doe
root@shubham-Latitude-7480:~/MyFile# finger john_doe
Command 'finger' not found, but can be installed with:
apt install finger
root@shubham-Latitude-7480:~/MyFile# sudo chage -ijohn_doe
chage: invalid option -- 'j'
Usage: chage [options] LOGIN

Options:
  -d, --lastday LAST_DAY        set date of last password change to LAST_DAY
  -E, --expiredate EXPIRE_DATE  set account expiration date to EXPIRE_DATE
  -h, --help                    display this help message and exit
  -i, --iso8601                 use YYYY-MM-DD when printing dates
  -I, --inactive INACTIVE       set password inactive after expiration
                                to INACTIVE
  -l, --list                    show account aging information
  -m, --mindays MIN_DAYS        set minimum number of days before password
                                change to MIN_DAYS
  -M, --maxdays MAX_DAYS        set maximum number of days before password
                                change to MAX_DAYS
  -R, --root CHROOT_DIR         directory to chroot into
  -W, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS
18.
oot@shubham-Latitude-7480:~/MyFile# grep development_team /etc/group
root@shubham-Latitude-7480:~/MyFile# sudo addgroup development_team
Adding group `development_team' (GID 1007) ...
Done.
root@shubham-Latitude-7480:~/MyFile# grep development_team /etc/group
development_team:x:1007:
root@shubham-Latitude-7480:~/MyFile# sudo adduser john_doe development_team
Adding user `john_doe' to group `development_team' ...
Adding user john_doe to group development_team
Done.
root@shubham-Latitude-7480:~/MyFile# id john_doe
uid=1004(john_doe) gid=1006(john_doe) groups=1006(john_doe),100(users),1007(development_team)
19.
root@shubham-Latitude-7480:~/MyFile# sudo gpasswd -d john_doe users
Removing user john_doe from group users
root@shubham-Latitude-7480:~/MyFile# sudo usermod -aG development_team john_doe
root@shubham-Latitude-7480:~/MyFile# groups john_doe
john_doe : john_doe development_team
20.
root@shubham-Latitude-7480:~/MyFile# id john_doe
id: ‘john_doe’: no such user
root@shubham-Latitude-7480:~/MyFile# ls /home/john_doe
ls: cannot access '/home/john_doe': No such file or directory
21.
root@shubham-Latitude-7480:~/MyFile# sudo delgroup development_team
Removing group `development_team' ...
Done.
root@shubham-Latitude-7480:~/MyFile# grep development_team /etc/group
22.
root@shubham-Latitude-7480:~/MyFile# sudo chage -M 90 -m 0 -W 7 -I 30 -E -1 $(cut -d: -f1 /etc/passwd)
Usage: chage [options] LOGIN

Options:
  -d, --lastday LAST_DAY        set date of last password change to LAST_DAY
  -E, --expiredate EXPIRE_DATE  set account expiration date to EXPIRE_DATE
  -h, --help                    display this help message and exit
  -i, --iso8601                 use YYYY-MM-DD when printing dates
  -I, --inactive INACTIVE       set password inactive after expiration
                                to INACTIVE
  -l, --list                    show account aging information
  -m, --mindays MIN_DAYS        set minimum number of days before password
                                change to MIN_DAYS
  -M, --maxdays MAX_DAYS        set maximum number of days before password
                                change to MAX_DAYS
  -R, --root CHROOT_DIR         directory to chroot into
  -W, --warndays WARN_DAYS      set expiration warning days to WARN_DAYS

root@shubham-Latitude-7480:~/MyFile# sudo sed -i '/^PASS_MAX_DAYS 90' /etc/login.defs
sed: -e expression #1, char 18: unterminated address regex
root@shubham-Latitude-7480:~/MyFile# sudo sed -i '/^PASS_MAX_DAYS/c\PASS_MAX_DAYS  90' /etc/login.defs
root@shubham-Latitude-7480:~/MyFile# sudo chage -l john_doe
chage: user 'john_doe' does not exist in /etc/passwd
root@shubham-Latitude-7480:~/MyFile# grep PASS_MAX_DAYS /etc/login.defs
#	PASS_MAX_DAYS	Maximum number of days a password may be used.
PASS_MAX_DAYS  90
23.
