```bash
login as: ansible
Pre-authentication banner message from server:
| Ubuntu 20.04.6 LTS
End of banner message from server
ansible@10.64.112.72's password:
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 5.15.0-1077-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Fri Aug  1 10:21:03 CST 2025

  System load:  0.0                Processes:             175
  Usage of /:   39.0% of 48.27GB   Users logged in:       0
  Memory usage: 51%                IPv4 address for ens5: 10.64.112.72
  Swap usage:   0%

  => There is 1 zombie process.

 * Ubuntu 20.04 LTS Focal Fossa has reached its end of standard support on 31 Ma

   For more details see:
   https://ubuntu.com/20-04

Expanded Security Maintenance for Infrastructure is not enabled.

108 updates can be applied immediately.
84 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

42 additional security updates can be applied with ESM Infra.
Learn more about enabling ESM Infra service for Ubuntu 20.04 at
https://ubuntu.com/20-04

New release '22.04.5 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


Last login: Fri Aug  1 10:03:43 2025 from 10.237.53.237
ansible@ip-10-64-112-72:~$ sudo su
root@ip-10-64-112-72:/home/ansible# cd /cm
root@ip-10-64-112-72:/cm# ls
docker-storage
root@ip-10-64-112-72:/cm# cd docker-storage/
root@ip-10-64-112-72:/cm/docker-storage# ls
buildkit    engine-id  network   plugins   swarm  volumes
containers  image      overlay2  runtimes  tmp
root@ip-10-64-112-72:/cm/docker-storage# cd volumes/
root@ip-10-64-112-72:/cm/docker-storage/volumes# ls
072c6bcab08244330d8b0411eba06758a9f90a505ce88c4fa9147ef5ece6c502
472997f69616b52ab3484ebf12c0dfe2372ed1b14e5bd0fcc6777d62c0bc5b18
654c2f06e6270f9135e116429c2e1504e854b3db35c7254af1634041b2735b8d
696041ed8f2b3cacf9d151887197a9f81792170a9317ae13bf1dc1ef8695a48c
7769932dcc069f81237f37475cbc971152ffe1b48a551ab83ffc02743c1c7811
8c7fd4b54268b2983778a156e293a3d476a68e3c1ec22494f7d4e19765aede13
8dccbc5c9e88256e162c22d6e8721f0cfa731ebb5e6aef668f981e3fa4bf33a0
935d50976799d56d02f476b3a82f31ce58128e6e3c0891ac0d077fb992f3c93c
9e49d539edcc86732b2d44c93242db4733e5056d1a321e098c77953d44496a0a
backingFsBlockDev
ci-gerrit.sh
ci-training-jenkins-home
eks-test
f46dfba0cc338af977afd5d9cd9777595e60029ec2e37a5abdbe06396e5ad6fe
f4f028bd7b868a78537e2f0c0280ff54317f93596fdd8bf44f52281bbf6cf1e6
gerrit-cn-qa-cache
gerrit-cn-qa-data
gerrit-cn-qa-db
gerrit-cn-qa-etc
gerrit-cn-qa-git
gerrit-cn-qa-index
gerrit-cn-qa-lib
gerrit-cn-qa-logs
gerrit-cn-qa-plugins
gerrit-cn-qa-ssh
julia-gitlab-data
julia-gitlab-etc
julia-gitlab-log
julia-jenkins-home
maven-julia
metadata.db
swfcn-jenkins-qa-home
swfcn-jenkins-qa-training
swfcn-qa-home.bak-2024-02-29
tmp-julis
root@ip-10-64-112-72:/cm/docker-storage/volumes# cd gerrit-cn-qa-etc/
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc# ls
_data
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc# cd _data/
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ls
entrypoint.sh      gerrit.config.bak.20240911  samlKeystore.jks.old        ssh_host_ecdsa_521_key      ssh_host_ed25519_key
gerrit.config      jgit.config                 secure.config               ssh_host_ecdsa_521_key.pub  ssh_host_ed25519_key.pub
gerrit.config.aad  mail                        ssh_host_ecdsa_384_key      ssh_host_ecdsa_key          ssh_host_rsa_key
gerrit.config.bak  samlKeystore.jks            ssh_host_ecdsa_384_key.pub  ssh_host_ecdsa_key.pub      ssh_host_rsa_key.pub
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# docker ps
CONTAINER ID   IMAGE                            COMMAND                  CREATED         STATUS       PORTS                                                                                      NAMES
1254430023f3   gerritcodereview/gerrit:3.11.2   "/entrypoint.sh"         2 weeks ago     Up 2 weeks   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp, 0.0.0.0:29418->29418/tcp, :::29418->29418/tcp   ci-training-gerrit
453923bfcf01   jenkins/jenkins:2.504.1          "/usr/bin/tini -- /u…"   5 weeks ago     Up 2 weeks   0.0.0.0:50000->50000/tcp, :::50000->50000/tcp, 0.0.0.0:8082->8080/tcp, :::8082->8080/tcp   swfcn-jenkins-qa
263482287c38   gerritcodereview/gerrit:3.11.2   "/var/gerrit/etc/ent…"   2 months ago    Up 3 weeks   0.0.0.0:8083->8080/tcp, :::8083->8080/tcp, 0.0.0.0:29419->29418/tcp, :::29419->29418/tcp   gerrit-cn-qa
4b593cabf528   jenkins/jenkins:2.426.3          "/usr/bin/tini -- /u…"   16 months ago   Up 8 weeks   0.0.0.0:80->8080/tcp, :::80->8080/tcp, 0.0.0.0:50001->50000/tcp, :::50001->50000/tcp       ci-training-jenkins
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# docker exec -it -u root gerrit-cn-qa /bin/bash
[root@263482287c38 /]# pwd
/
[root@263482287c38 /]# ls
afs  bin  dev  entrypoint.sh  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
[root@263482287c38 /]# cd var
[root@263482287c38 var]# ls
adm  cache  db  empty  ftp  games  gerrit  kerberos  lib  local  lock  log  mail  nis  opt  preserve  run  spool  tmp  yp
[root@263482287c38 var]# cd lib
[root@263482287c38 lib]# ls
alternatives  dnf  flatpak  games  geoclue  misc  polkit-1  private  rpm  rpm-state  selinux  systemd  tpm2-tss
[root@263482287c38 lib]# cd ..
[root@263482287c38 var]# ls
adm  cache  db  empty  ftp  games  gerrit  kerberos  lib  local  lock  log  mail  nis  opt  preserve  run  spool  tmp  yp
[root@263482287c38 var]# cd gerrit/
[root@263482287c38 gerrit]# ls
bin  cache  data  db  etc  git  index  lib  logs  plugins  static  tmp
[root@263482287c38 gerrit]# cd etc
[root@263482287c38 etc]# ls
entrypoint.sh      gerrit.config.bak.20240911  samlKeystore.jks.old        ssh_host_ecdsa_521_key      ssh_host_ed25519_key
gerrit.config      jgit.config                 secure.config               ssh_host_ecdsa_521_key.pub  ssh_host_ed25519_key.pub
gerrit.config.aad  mail                        ssh_host_ecdsa_384_key      ssh_host_ecdsa_key          ssh_host_rsa_key
gerrit.config.bak  samlKeystore.jks            ssh_host_ecdsa_384_key.pub  ssh_host_ecdsa_key.pub      ssh_host_rsa_key.pub
[root@263482287c38 etc]# ls -l
total 84
-rwxr-xr-x 1 root   root    409 Aug  4  2023 entrypoint.sh
-rw-r--r-- 1 gerrit gerrit 2638 May 14 09:01 gerrit.config
-rw-r--r-- 1 gerrit gerrit 2397 Jun 14  2023 gerrit.config.aad
-rw-r--r-- 1 gerrit gerrit 1198 Jun 14  2023 gerrit.config.bak
-rw-r--r-- 1 gerrit gerrit 2490 Feb 23  2024 gerrit.config.bak.20240911
-rw-r--r-- 1 gerrit gerrit   26 Nov 21  2022 jgit.config
drwxr-xr-x 2 gerrit gerrit 4096 Jul  7 08:59 mail
-rw-r--r-- 1 gerrit gerrit 2557 Jun 14  2023 samlKeystore.jks
-rw-r--r-- 1 gerrit gerrit 2218 Jun 14  2023 samlKeystore.jks.old
-rw------- 1 gerrit gerrit   71 Jun 12  2023 secure.config
-rw------- 1 gerrit gerrit  634 Jun 12  2023 ssh_host_ecdsa_384_key
-rw-r--r-- 1 gerrit gerrit  237 Jun 12  2023 ssh_host_ecdsa_384_key.pub
-rw------- 1 gerrit gerrit  756 Jun 12  2023 ssh_host_ecdsa_521_key
-rw-r--r-- 1 gerrit gerrit  285 Jun 12  2023 ssh_host_ecdsa_521_key.pub
-rw------- 1 gerrit gerrit  525 Jun 12  2023 ssh_host_ecdsa_key
-rw-r--r-- 1 gerrit gerrit  193 Jun 12  2023 ssh_host_ecdsa_key.pub
-rw------- 1 gerrit gerrit  432 Jun 12  2023 ssh_host_ed25519_key
-rw-r--r-- 1 gerrit gerrit  113 Jun 12  2023 ssh_host_ed25519_key.pub
-rw------- 1 gerrit gerrit 2622 Jun 12  2023 ssh_host_rsa_key
-rw-r--r-- 1 gerrit gerrit  585 Jun 12  2023 ssh_host_rsa_key.pub
[root@263482287c38 etc]# exec
[root@263482287c38 etc]# exist
bash: exist: command not found
[root@263482287c38 etc]# exit
exit
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ls
entrypoint.sh      gerrit.config.bak.20240911  samlKeystore.jks.old        ssh_host_ecdsa_521_key      ssh_host_ed25519_key
gerrit.config      jgit.config                 secure.config               ssh_host_ecdsa_521_key.pub  ssh_host_ed25519_key.pub
gerrit.config.aad  mail                        ssh_host_ecdsa_384_key      ssh_host_ecdsa_key          ssh_host_rsa_key
gerrit.config.bak  samlKeystore.jks            ssh_host_ecdsa_384_key.pub  ssh_host_ecdsa_key.pub      ssh_host_rsa_key.pub
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ll
total 88
drwxr-xr-x 3 ubuntu ubuntu 4096 May 14 17:02 ./
drwx-----x 3 ubuntu ubuntu   19 Jun 12  2023 ../
-rwxr-xr-x 1 root   root    409 Aug  4  2023 entrypoint.sh*
-rw-r--r-- 1 ubuntu ubuntu 2638 May 14 17:01 gerrit.config
-rw-r--r-- 1 ubuntu ubuntu 2397 Jun 14  2023 gerrit.config.aad
-rw-r--r-- 1 ubuntu ubuntu 1198 Jun 14  2023 gerrit.config.bak
-rw-r--r-- 1 ubuntu ubuntu 2490 Feb 23  2024 gerrit.config.bak.20240911
-rw-r--r-- 1 ubuntu ubuntu   26 Nov 21  2022 jgit.config
drwxr-xr-x 2 ubuntu ubuntu 4096 Jul  7 16:59 mail/
-rw-r--r-- 1 ubuntu ubuntu 2557 Jun 14  2023 samlKeystore.jks
-rw-r--r-- 1 ubuntu ubuntu 2218 Jun 14  2023 samlKeystore.jks.old
-rw------- 1 ubuntu ubuntu   71 Jun 12  2023 secure.config
-rw------- 1 ubuntu ubuntu  634 Jun 12  2023 ssh_host_ecdsa_384_key
-rw-r--r-- 1 ubuntu ubuntu  237 Jun 12  2023 ssh_host_ecdsa_384_key.pub
-rw------- 1 ubuntu ubuntu  756 Jun 12  2023 ssh_host_ecdsa_521_key
-rw-r--r-- 1 ubuntu ubuntu  285 Jun 12  2023 ssh_host_ecdsa_521_key.pub
-rw------- 1 ubuntu ubuntu  525 Jun 12  2023 ssh_host_ecdsa_key
-rw-r--r-- 1 ubuntu ubuntu  193 Jun 12  2023 ssh_host_ecdsa_key.pub
-rw------- 1 ubuntu ubuntu  432 Jun 12  2023 ssh_host_ed25519_key
-rw-r--r-- 1 ubuntu ubuntu  113 Jun 12  2023 ssh_host_ed25519_key.pub
-rw------- 1 ubuntu ubuntu 2622 Jun 12  2023 ssh_host_rsa_key
-rw-r--r-- 1 ubuntu ubuntu  585 Jun 12  2023 ssh_host_rsa_key.pub
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# touch test
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ls -l
total 84
-rwxr-xr-x 1 root   root    409 Aug  4  2023 entrypoint.sh
-rw-r--r-- 1 ubuntu ubuntu 2638 May 14 17:01 gerrit.config
-rw-r--r-- 1 ubuntu ubuntu 2397 Jun 14  2023 gerrit.config.aad
-rw-r--r-- 1 ubuntu ubuntu 1198 Jun 14  2023 gerrit.config.bak
-rw-r--r-- 1 ubuntu ubuntu 2490 Feb 23  2024 gerrit.config.bak.20240911
-rw-r--r-- 1 ubuntu ubuntu   26 Nov 21  2022 jgit.config
drwxr-xr-x 2 ubuntu ubuntu 4096 Jul  7 16:59 mail
-rw-r--r-- 1 ubuntu ubuntu 2557 Jun 14  2023 samlKeystore.jks
-rw-r--r-- 1 ubuntu ubuntu 2218 Jun 14  2023 samlKeystore.jks.old
-rw------- 1 ubuntu ubuntu   71 Jun 12  2023 secure.config
-rw------- 1 ubuntu ubuntu  634 Jun 12  2023 ssh_host_ecdsa_384_key
-rw-r--r-- 1 ubuntu ubuntu  237 Jun 12  2023 ssh_host_ecdsa_384_key.pub
-rw------- 1 ubuntu ubuntu  756 Jun 12  2023 ssh_host_ecdsa_521_key
-rw-r--r-- 1 ubuntu ubuntu  285 Jun 12  2023 ssh_host_ecdsa_521_key.pub
-rw------- 1 ubuntu ubuntu  525 Jun 12  2023 ssh_host_ecdsa_key
-rw-r--r-- 1 ubuntu ubuntu  193 Jun 12  2023 ssh_host_ecdsa_key.pub
-rw------- 1 ubuntu ubuntu  432 Jun 12  2023 ssh_host_ed25519_key
-rw-r--r-- 1 ubuntu ubuntu  113 Jun 12  2023 ssh_host_ed25519_key.pub
-rw------- 1 ubuntu ubuntu 2622 Jun 12  2023 ssh_host_rsa_key
-rw-r--r-- 1 ubuntu ubuntu  585 Jun 12  2023 ssh_host_rsa_key.pub
-rw-r----- 1 root   root      0 Aug  1 10:38 test
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# chown ubuntu:ubuntu test
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ls -l
total 84
-rwxr-xr-x 1 root   root    409 Aug  4  2023 entrypoint.sh
-rw-r--r-- 1 ubuntu ubuntu 2638 May 14 17:01 gerrit.config
-rw-r--r-- 1 ubuntu ubuntu 2397 Jun 14  2023 gerrit.config.aad
-rw-r--r-- 1 ubuntu ubuntu 1198 Jun 14  2023 gerrit.config.bak
-rw-r--r-- 1 ubuntu ubuntu 2490 Feb 23  2024 gerrit.config.bak.20240911
-rw-r--r-- 1 ubuntu ubuntu   26 Nov 21  2022 jgit.config
drwxr-xr-x 2 ubuntu ubuntu 4096 Jul  7 16:59 mail
-rw-r--r-- 1 ubuntu ubuntu 2557 Jun 14  2023 samlKeystore.jks
-rw-r--r-- 1 ubuntu ubuntu 2218 Jun 14  2023 samlKeystore.jks.old
-rw------- 1 ubuntu ubuntu   71 Jun 12  2023 secure.config
-rw------- 1 ubuntu ubuntu  634 Jun 12  2023 ssh_host_ecdsa_384_key
-rw-r--r-- 1 ubuntu ubuntu  237 Jun 12  2023 ssh_host_ecdsa_384_key.pub
-rw------- 1 ubuntu ubuntu  756 Jun 12  2023 ssh_host_ecdsa_521_key
-rw-r--r-- 1 ubuntu ubuntu  285 Jun 12  2023 ssh_host_ecdsa_521_key.pub
-rw------- 1 ubuntu ubuntu  525 Jun 12  2023 ssh_host_ecdsa_key
-rw-r--r-- 1 ubuntu ubuntu  193 Jun 12  2023 ssh_host_ecdsa_key.pub
-rw------- 1 ubuntu ubuntu  432 Jun 12  2023 ssh_host_ed25519_key
-rw-r--r-- 1 ubuntu ubuntu  113 Jun 12  2023 ssh_host_ed25519_key.pub
-rw------- 1 ubuntu ubuntu 2622 Jun 12  2023 ssh_host_rsa_key
-rw-r--r-- 1 ubuntu ubuntu  585 Jun 12  2023 ssh_host_rsa_key.pub
-rw-r----- 1 ubuntu ubuntu    0 Aug  1 10:38 test
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# docker ps
CONTAINER ID   IMAGE                            COMMAND                  CREATED         STATUS       PORTS                                                                                      NAMES
1254430023f3   gerritcodereview/gerrit:3.11.2   "/entrypoint.sh"         2 weeks ago     Up 2 weeks   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp, 0.0.0.0:29418->29418/tcp, :::29418->29418/tcp   ci-training-gerrit
453923bfcf01   jenkins/jenkins:2.504.1          "/usr/bin/tini -- /u…"   5 weeks ago     Up 2 weeks   0.0.0.0:50000->50000/tcp, :::50000->50000/tcp, 0.0.0.0:8082->8080/tcp, :::8082->8080/tcp   swfcn-jenkins-qa
263482287c38   gerritcodereview/gerrit:3.11.2   "/var/gerrit/etc/ent…"   2 months ago    Up 3 weeks   0.0.0.0:8083->8080/tcp, :::8083->8080/tcp, 0.0.0.0:29419->29418/tcp, :::29419->29418/tcp   gerrit-cn-qa
4b593cabf528   jenkins/jenkins:2.426.3          "/usr/bin/tini -- /u…"   16 months ago   Up 8 weeks   0.0.0.0:80->8080/tcp, :::80->8080/tcp, 0.0.0.0:50001->50000/tcp, :::50001->50000/tcp       ci-training-jenkins
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# docker restart 26
26
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# docker ps
CONTAINER ID   IMAGE                            COMMAND                  CREATED         STATUS         PORTS                                                                                      NAMES
1254430023f3   gerritcodereview/gerrit:3.11.2   "/entrypoint.sh"         2 weeks ago     Up 2 weeks     0.0.0.0:8080->8080/tcp, :::8080->8080/tcp, 0.0.0.0:29418->29418/tcp, :::29418->29418/tcp   ci-training-gerrit
453923bfcf01   jenkins/jenkins:2.504.1          "/usr/bin/tini -- /u…"   5 weeks ago     Up 2 weeks     0.0.0.0:50000->50000/tcp, :::50000->50000/tcp, 0.0.0.0:8082->8080/tcp, :::8082->8080/tcp   swfcn-jenkins-qa
263482287c38   gerritcodereview/gerrit:3.11.2   "/var/gerrit/etc/ent…"   2 months ago    Up 4 seconds   0.0.0.0:8083->8080/tcp, :::8083->8080/tcp, 0.0.0.0:29419->29418/tcp, :::29419->29418/tcp   gerrit-cn-qa
4b593cabf528   jenkins/jenkins:2.426.3          "/usr/bin/tini -- /u…"   16 months ago   Up 8 weeks     0.0.0.0:80->8080/tcp, :::80->8080/tcp, 0.0.0.0:50001->50000/tcp, :::50001->50000/tcp       ci-training-jenkins
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# docker images
REPOSITORY                TAG       IMAGE ID       CREATED         SIZE
jenkins/jenkins           2.504.1   ed331f9d3352   3 months ago    466MB
gerritcodereview/gerrit   3.11.2    cc8d0ea5977a   4 months ago    899MB
jenkins/jenkins           2.492.1   82a2134e1742   5 months ago    468MB
jenkins/ssh-agent         latest    64421e0bc633   16 months ago   342MB
jenkins/jenkins           2.426.3   b29eae45bb8c   18 months ago   477MB
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# login as: ansible
Pre-authentication banner message from server:
| Ubuntu 20.04.6 LTS
End of banner message from server
ansible@10.64.112.72's password:
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 5.15.0-1077-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Fri Aug  1 10:21:03 CST 2025

  System load:  0.0                Processes:             175
  Usage of /:   39.0% of 48.27GB   Users logged in:       0
  Memory usage: 51%                IPv4 address for ens5: 10.64.112.72
  Swap usage:   0%

  => There is 1 zombie process.

 * Ubuntu 20.04 LTS Focal Fossa has reached its end of standard support on 31 Ma

   For more details see:
   https://ubuntu.com/20-04

Expanded Security Maintenance for Infrastructure is not enabled.

108 updates can be applied immediately.
84 of these updates are standard security updates.
To see these additional updates run: apt list --upgradable

42 additional security updates can be applied with ESM Infra.
Learn more about enabling ESM Infra service for Ubuntu 20.04 at
https://ubuntu.com/20-04

New release '22.04.5 LTS' available.
Run 'do-release-upgrade' to upgrade to it.


Last login: Fri Aug  1 10:03:43 2025 from 10.237.53.237
ansible@ip-10-64-112-72:~$ sudo su
root@ip-10-64-112-72:/home/ansible# cd /cm
root@ip-10-64-112-72:/cm# ls
docker-storage
root@ip-10-64-112-72:/cm# cd docker-storage/
root@ip-10-64-112-72:/cm/docker-storage# ls
buildkit    engine-id  network   plugins   swarm  volumes
containers  image      overlay2  runtimes  tmp
root@ip-10-64-112-72:/cm/docker-storage# cd volumes/
root@ip-10-64-112-72:/cm/docker-storage/volumes# ls
072c6bcab08244330d8b0411eba06758a9f90a505ce88c4fa9147ef5ece6c502
472997f69616b52ab3484ebf12c0dfe2372ed1b14e5bd0fcc6777d62c0bc5b18
654c2f06e6270f9135e116429c2e1504e854b3db35c7254af1634041b2735b8d
696041ed8f2b3cacf9d151887197a9f81792170a9317ae13bf1dc1ef8695a48c
7769932dcc069f81237f37475cbc971152ffe1b48a551ab83ffc02743c1c7811
8c7fd4b54268b2983778a156e293a3d476a68e3c1ec22494f7d4e19765aede13
8dccbc5c9e88256e162c22d6e8721f0cfa731ebb5e6aef668f981e3fa4bf33a0
935d50976799d56d02f476b3a82f31ce58128e6e3c0891ac0d077fb992f3c93c
9e49d539edcc86732b2d44c93242db4733e5056d1a321e098c77953d44496a0a
backingFsBlockDev
ci-gerrit.sh
ci-training-jenkins-home
eks-test
f46dfba0cc338af977afd5d9cd9777595e60029ec2e37a5abdbe06396e5ad6fe
f4f028bd7b868a78537e2f0c0280ff54317f93596fdd8bf44f52281bbf6cf1e6
gerrit-cn-qa-cache
gerrit-cn-qa-data
gerrit-cn-qa-db
gerrit-cn-qa-etc
gerrit-cn-qa-git
gerrit-cn-qa-index
gerrit-cn-qa-lib
gerrit-cn-qa-logs
gerrit-cn-qa-plugins
gerrit-cn-qa-ssh
julia-gitlab-data
julia-gitlab-etc
julia-gitlab-log
julia-jenkins-home
maven-julia
metadata.db
swfcn-jenkins-qa-home
swfcn-jenkins-qa-training
swfcn-qa-home.bak-2024-02-29
tmp-julis
root@ip-10-64-112-72:/cm/docker-storage/volumes# cd gerrit-cn-qa-etc/
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc# ls
_data
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc# cd _data/
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ls
entrypoint.sh      gerrit.config.bak.20240911  samlKeystore.jks.old        ssh_host_ecdsa_521_key      ssh_host_ed25519_key
gerrit.config      jgit.config                 secure.config               ssh_host_ecdsa_521_key.pub  ssh_host_ed25519_key.pub
gerrit.config.aad  mail                        ssh_host_ecdsa_384_key      ssh_host_ecdsa_key          ssh_host_rsa_key
gerrit.config.bak  samlKeystore.jks            ssh_host_ecdsa_384_key.pub  ssh_host_ecdsa_key.pub      ssh_host_rsa_key.pub
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# docker ps
CONTAINER ID   IMAGE                            COMMAND                  CREATED         STATUS       PORTS                                                                                      NAMES
1254430023f3   gerritcodereview/gerrit:3.11.2   "/entrypoint.sh"         2 weeks ago     Up 2 weeks   0.0.0.0:8080->8080/tcp, :::8080->8080/tcp, 0.0.0.0:29418->29418/tcp, :::29418->29418/tcp   ci-training-gerrit
453923bfcf01   jenkins/jenkins:2.504.1          "/usr/bin/tini -- /u…"   5 weeks ago     Up 2 weeks   0.0.0.0:50000->50000/tcp, :::50000->50000/tcp, 0.0.0.0:8082->8080/tcp, :::8082->8080/tcp   swfcn-jenkins-qa
263482287c38   gerritcodereview/gerrit:3.11.2   "/var/gerrit/etc/ent…"   2 months ago    Up 3 weeks   0.0.0.0:8083->8080/tcp, :::8083->8080/tcp, 0.0.0.0:29419->29418/tcp, :::29419->29418/tcp   gerrit-cn-qa
4b593cabf528   jenkins/jenkins:2.426.3          "/usr/bin/tini -- /u…"   16 months ago   Up 8 weeks   0.0.0.0:80->8080/tcp, :::80->8080/tcp, 0.0.0.0:50001->50000/tcp, :::50001->50000/tcp       ci-training-jenkins
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# docker exec -it -u root gerrit-cn-qa /bin/bash
[root@263482287c38 /]# pwd
/
[root@263482287c38 /]# ls
afs  bin  dev  entrypoint.sh  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
[root@263482287c38 /]# cd var
[root@263482287c38 var]# ls
adm  cache  db  empty  ftp  games  gerrit  kerberos  lib  local  lock  log  mail  nis  opt  preserve  run  spool  tmp  yp
[root@263482287c38 var]# cd lib
[root@263482287c38 lib]# ls
alternatives  dnf  flatpak  games  geoclue  misc  polkit-1  private  rpm  rpm-state  selinux  systemd  tpm2-tss
[root@263482287c38 lib]# cd ..
[root@263482287c38 var]# ls
adm  cache  db  empty  ftp  games  gerrit  kerberos  lib  local  lock  log  mail  nis  opt  preserve  run  spool  tmp  yp
[root@263482287c38 var]# cd gerrit/
[root@263482287c38 gerrit]# ls
bin  cache  data  db  etc  git  index  lib  logs  plugins  static  tmp
[root@263482287c38 gerrit]# cd etc
[root@263482287c38 etc]# ls
entrypoint.sh      gerrit.config.bak.20240911  samlKeystore.jks.old        ssh_host_ecdsa_521_key      ssh_host_ed25519_key
gerrit.config      jgit.config                 secure.config               ssh_host_ecdsa_521_key.pub  ssh_host_ed25519_key.pub
gerrit.config.aad  mail                        ssh_host_ecdsa_384_key      ssh_host_ecdsa_key          ssh_host_rsa_key
gerrit.config.bak  samlKeystore.jks            ssh_host_ecdsa_384_key.pub  ssh_host_ecdsa_key.pub      ssh_host_rsa_key.pub
[root@263482287c38 etc]# ls -l
total 84
-rwxr-xr-x 1 root   root    409 Aug  4  2023 entrypoint.sh
-rw-r--r-- 1 gerrit gerrit 2638 May 14 09:01 gerrit.config
-rw-r--r-- 1 gerrit gerrit 2397 Jun 14  2023 gerrit.config.aad
-rw-r--r-- 1 gerrit gerrit 1198 Jun 14  2023 gerrit.config.bak
-rw-r--r-- 1 gerrit gerrit 2490 Feb 23  2024 gerrit.config.bak.20240911
-rw-r--r-- 1 gerrit gerrit   26 Nov 21  2022 jgit.config
drwxr-xr-x 2 gerrit gerrit 4096 Jul  7 08:59 mail
-rw-r--r-- 1 gerrit gerrit 2557 Jun 14  2023 samlKeystore.jks
-rw-r--r-- 1 gerrit gerrit 2218 Jun 14  2023 samlKeystore.jks.old
-rw------- 1 gerrit gerrit   71 Jun 12  2023 secure.config
-rw------- 1 gerrit gerrit  634 Jun 12  2023 ssh_host_ecdsa_384_key
-rw-r--r-- 1 gerrit gerrit  237 Jun 12  2023 ssh_host_ecdsa_384_key.pub
-rw------- 1 gerrit gerrit  756 Jun 12  2023 ssh_host_ecdsa_521_key
-rw-r--r-- 1 gerrit gerrit  285 Jun 12  2023 ssh_host_ecdsa_521_key.pub
-rw------- 1 gerrit gerrit  525 Jun 12  2023 ssh_host_ecdsa_key
-rw-r--r-- 1 gerrit gerrit  193 Jun 12  2023 ssh_host_ecdsa_key.pub
-rw------- 1 gerrit gerrit  432 Jun 12  2023 ssh_host_ed25519_key
-rw-r--r-- 1 gerrit gerrit  113 Jun 12  2023 ssh_host_ed25519_key.pub
-rw------- 1 gerrit gerrit 2622 Jun 12  2023 ssh_host_rsa_key
-rw-r--r-- 1 gerrit gerrit  585 Jun 12  2023 ssh_host_rsa_key.pub
[root@263482287c38 etc]# exec
[root@263482287c38 etc]# exist
bash: exist: command not found
[root@263482287c38 etc]# exit
exit
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ls
entrypoint.sh      gerrit.config.bak.20240911  samlKeystore.jks.old        ssh_host_ecdsa_521_key      ssh_host_ed25519_key
gerrit.config      jgit.config                 secure.config               ssh_host_ecdsa_521_key.pub  ssh_host_ed25519_key.pub
gerrit.config.aad  mail                        ssh_host_ecdsa_384_key      ssh_host_ecdsa_key          ssh_host_rsa_key
gerrPassword:

Login incorrect
ip-10-64-112-72 login:         ssh_host_ecdsa_384_key.pub  ssh_host_ecdsa_key.pub      ssh_host_rsa_key.pub
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ll
total 88
drwxr-xr-x 3 ubuntu ubuntu 4096 May 14 17:02 ./
drwx-----x 3 ubuntu ubuntu   19 Jun 12  2023 ../
-rwxr-xr-x 1 root   root    409 Aug  4  2023 entrypoint.sh*
-rw-r--r-- 1 ubuntu ubuntu 2638 May 14 17:01 gerrit.config
-rw-r--r-- 1 ubuntu ubuntu 2397 Jun 14  2023 gerrit.config.aad
-rw-r--r-- 1 ubuntu ubuntu 1198 Jun 14  2023 gerrit.config.bak
-rw-r--r-- 1 ubuntu ubuntu 2490 Feb 23  2024 gerrit.config.bak.20240911
-rw-r--r-- 1 ubuntu ubuntu   26 Nov 21  2022 jgit.config
drwxr-xr-x 2 ubuntu ubuntu 4096 Jul  7 16:59 mail/
-rw-r--r-- 1 ubuntu ubuntu 2557 Jun 14  2023 samlKeystore.jks
-rw-r--r-- 1 ubuntu ubuntu 2218 Jun 14  2023 samlKeystore.jks.old
-rw------- 1 ubuntu ubuntu   71 Jun 12  2023 secure.config
-rw------- 1 ubuntu ubuntu  634 Jun 12  2023 ssh_host_ecdsa_384_key
-rw-r--r-- 1 ubuntu ubuntu  237 Jun 12  2023 ssh_host_ecdsa_384_key.pub
-rw------- 1 ubuntu ubuntu  756 Jun 12  2023 ssh_host_ecdsa_521_key
-rw-r--r-- 1 ubuntu ubuntu  285 Jun 12  2023 ssh_host_ecdsa_521_key.pub
-rw------- 1 ubuntu ubuntu  525 Jun 12  2023 ssh_host_ecdsa_key
-rw-r--r-- 1 ubuntu ubuntu  193 Jun 12  2023 ssh_host_ecdsa_key.pub
-rw------- 1 ubuntu ubuntu  432 Jun 12  2023 ssh_host_ed25519_key
-rw-r--r-- 1 ubuntu ubuntu  113 Jun 12  2023 ssh_host_ed25519_key.pub
-rw------- 1 ubuntu ubuntu 2622 Jun 12  2023 ssh_host_rsa_key
-rw-r--r-- 1 ubuntu ubuntu  585 Jun 12  2023 ssh_host_rsa_key.pub
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# touch test
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ls -l
total 84
-rwxr-xr-x 1 root   root    409 Aug  4  2023 entrypoint.sh
-rw-r--r-- 1 ubuntu ubuntu 2638 May 14 17:01 gerrit.config
-rw-r--r-- 1 ubuntu ubuntu 2397 Jun 14  2023 gerrit.config.aad
-rw-r--r-- 1 ubuntu ubuntu 1198 Jun 14  2023 gerrit.config.bak
-rw-r--r-- 1 ubuntu ubuntu 2490 Feb 23  2024 gerrit.config.bak.20240911
-rw-r--r-- 1 ubuntu ubuntu   26 Nov 21  2022 jgit.config
drwxr-xr-x 2 ubuntu ubuntu 4096 Jul  7 16:59 mail
-rw-r--r-- 1 ubuntu ubuntu 2557 Jun 14  2023 samlKeystore.jks
-rw-r--r-- 1 ubuntu ubuntu 2218 Jun 14  2023 samlKeystore.jks.old
-rw------- 1 ubuntu ubuntu   71 Jun 12  2023 secure.config
-rw------- 1 ubuntu ubuntu  634 Jun 12  2023 ssh_host_ecdsa_384_key
-rw-r--r-- 1 ubuntu ubuntu  237 Jun 12  2023 ssh_host_ecdsa_384_key.pub
-rw------- 1 ubuntu ubuntu  756 Jun 12  2023 ssh_host_ecdsa_521_key
-rw-r--r-- 1 ubuntu ubuntu  285 Jun 12  2023 ssh_host_ecdsa_521_key.pub
-rw------- 1 ubuntu ubuntu  525 Jun 12  2023 ssh_host_ecdsa_key
-rw-r--r-- 1 ubuntu ubuntu  193 Jun 12  2023 ssh_host_ecdsa_key.pub
-rw------- 1 ubuntu ubuntu  432 Jun 12  2023 ssh_host_ed25519_key
-rw-r--r-- 1 ubuntu ubuntu  113 Jun 12  2023 ssh_host_ed25519_key.pub
-rw------- 1 ubuntu ubuntu 2622 Jun 12  2023 ssh_host_rsa_key
-rw-r--r-- 1 ubuntu ubuntu  585 Jun 12  2023 ssh_host_rsa_key.pub
-rw-r----- 1 root   root      0 Aug  1 10:38 test
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# chown ubuntu:ubuntu test
root@ip-10-64-112-72:/cm/docker-storage/volumes/gerrit-cn-qa-etc/_data# ls -l
total 84
-rwxr-xr-x 1 root   root    409 Aug  4  2023 entrypoint.sh
-rw-r--r-- 1 ubuntu ubuntu 2638 May 14 17:01 gerrit.config
-rw-r--r-- 1 ubuntu ubuntu 2397 Jun 14  2023 gerrit.config.aad
-rw-r--r-- 1 ubuntu ubuntu 1198 Jun 14  2023 gerrit.config.bak
-rw-r--r-- 1 ubuntu ubuntu 2490 Feb 23  2024 gerrit.config.bak.20240911
-rw-r--r-- 1 ubuntu ubuntu   26 Nov 21  2022 jgit.config
drwxr-xr-x 2 ubuntu ubuntu 4096 Jul  7 16:59 mail
-rw-r--r-- 1 ubuntu ubuntu 2557 Jun 14  2023 samlKeystore.jks
-rw-r--r-- 1 ubuntu ubuntu 2218 Jun 14  2023 samlKeystore.jks.old
-rw------- 1 ubuntu ubuntu   71 Jun 12  2023 secure.config
-rw------- 1 ubuntu ubuntu  634 Jun 12  2023 ssh_host_ecdsa_384_key
-rw-r--r-- 1 ubuntu ubuntu  237 Jun 12  2023 ssh_host_ecdsa_384_key.pub
-rw------- 1 ubuntu ubuntu  756 Jun 12  2023 ssh_host_ecdsa_521_key
-rw-r--r-- 1 ubuntu ubuntu  285 Jun 12  2023 ssh_host_ecdsa_521_key.pub

```