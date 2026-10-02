
create login user (wilfrid) : sudo useradd -m -s /bin/bash wilfrid
create login (brenda) : sudo useradd -m -s /bin/bash brenda

create no login deploybot : sudo useradd -r -s /usr/sbin/nologin deploybot

create dev group : sudo groupadd devteam

create share folder : mkdir /projectX

secure projectX : chmod 770 /projectX

attribute folder to group dev : sudo chow :devteam /projectX
automatic attribut ownership to group when created : chmod 2770 /projectX
login user as dev : sudo usermod -aG devteam brenda or wilfrid

note : the 2 in '2770' indicate setgid that anable automatique ownership permissions


