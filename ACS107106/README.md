#�Ĥ@�D
(1)uname -r�ݨ�3.xx��3.10�A���ۥ�echo $ver�]�w�ܼơA��ver="my kernel version is 3.10�A�M��A�Τ@��echo $ver�N�i�H��ܥX�ܼƪ��ȡC

(2)��echo $PATH�i��ܥX/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin:/root/bin�A��\�ά����t�γz�L PATH �o���ܼƸ̭������e�ҰO�������|���Ǩӷj�M���O�C

#�ĤG�D
(1)mail/�o���ɮת��s���Ƭ�3�A���ɮת��֦��̬�root(��rwx���v��)�A���ݸs�լ�mail(��rws���v��)�A��L�H�h�u��rx���v���A�ɮפj�p��4096�A�̫�@���ק諸�����2017/02/16

(2)�Ʀr�k:��chmod 777 script.sh
   �Ÿ��k:chmod u=rwx,g=rwx,o=rwx script.sh

#�ĤT�D

(1)����s���P�Ÿ��s�����t��:
�ϥι���s���A�ϺЪ��Ŷ��Pinode���ƥس����|���ܡA�u�O�b�ؿ��̥[�@��inode�P�ɦW�������C
�ϥβŸ��s���A�N�O�b�إߤ@�ӿW�ߪ��s���ɮסA�ҥH�|���ν�inode�Pblock�C

(2)��touch hosts.real�إ��ɮסA��ln ~/etc/hosts ~/hosts.real �b�a�ؿ��إ߹���s���C

(3)��touch hosts.symbo�إ��ɮסA��ln -s ~/etc/hosts ~/hosts.symbo�b�a�ؿ��إ߲Ÿ��s���C

#�ĥ|�D

(1)fdisk /dev/sdb�إ�1GB���ɮסA��mkfs.xfs /dev/sdb1�إ�xfs�ɮרt�ΡA��mount /dev/sdb1 /srv/maildir�A��df -T /srv/maildir��ܦ�1GB���ɮרt�Υ�������`/srv/maildir`�C

(2)��cat /etc/fstab�N����ܪ�UUID���@��g��vi /etc/fstab���A���s�}����N�|�۰ʱ����C

(3)��chgrp mailgroup /srv/maildir�A��chmod 770 /srv/maildir�A��ls -ld /srv/maildir�C

(4)��groupadd mailgroup�A��useradd -G mailgroup mailuser�A��id mailuser�i�ݨ�ϥΪ̦��b`mailgroup`�C

(5)��/etc/passwd | grep mailuser�C