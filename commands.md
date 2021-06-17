# grep files recursively

find . -iname "*.clj" | xargs grep defmacro

# who is listening port

lsof -nP -iTCP:$PORT | grep LISTEN
lsof -nP -iTCP:8800 | grep LISTEN

# show firewall rules

sudo iptables -L --line-numbers

# block outgoing port in firewall

sudo iptables -A OUTPUT -p tcp --destination-port 1521 -d 10.203.162.162 -j DROP

# drop firewall rule by number

sudo iptables -D INPUT 3

# test if port is open

nc -zv example.com 80

# view the latest log from the end

sudo journalctl -f

# View the log for reindexing.timer and reindexing.service from the end

journalctl -f -u reindexing

# list systemd timers

systemctl list-timers

# run ansible-playbook in check mode and tags filter

ansible-playbook -i inventory/test -vv detector.yml --tags "reindexing" --key-file "~/.ssh/detector-deploy.key" --check

# install detector to t3

ansible-playbook -i inventory/test -vv detector.yml --key-file "~/.ssh/detector-deploy.key" --limit "detector-app-t3.posti.fi" --check

# open root shell

sudo su -

# become deploy -user

sudo su - deploy

# download certficates

openssl s_client -connect lm-test.posti.com:443 -showcerts

# print certificate contents

openssl x509 -inform pem -text -in detector.pem

# find certificate revocation list url

openssl x509 -inform pem -text -in telia.crt | grep -A4 'CRL Distribution Points'

# find certificate revocation from crl

openssl crl -noout -inform DER -in telia.crl -text | grep -A4 01714F

# curl with oauth token

Run this command
curl -X POST "http://localhost:8080/v1/match/recipient" -H "accept: application/json" -H "Content-Type: application/json" -d @koe-30000-1.json -K-

and then paste the cookie to terminal like this:

--cookie "detector_oauth_token="

# splunk

index="detector-app002382-test"  | convert num(totalMillisecondsUsed) as totalMS | where totalMS > 4

index="detector-app002382-test"
| eval roundedms = round(totalMillisecondsUsed/10,1)
| chart count by roundedms

index="detector-app002382-test" | where hostname!="detector-app-t3.netti.infra.posti.fi"
| eval roundedms = round(totalMillisecondsUsed/10,1)
| chart count by roundedms

index="detector-app002382-test" | eval roundedms = round(totalMillisecondsUsed,1) | search roundedms="9.0" hostname="detector-app-t3.netti.infra.posti.fi"

index="detector-app002382-test" | eval roundedms = round(totalMillisecondsUsed/10,1) | search roundedms="0.8" hostname="detector-app-t3.netti.infra.posti.fi"

## docker

docker build -t ct:1.0
docker container run --publish 8000:8800 --name ct ct:1.0

show how much disk volumes are taking
docker system df -v

start bash in ubuntu and mount a volume to /data
docker run --rm --volume d5b87f270408c7d56c69aa6f399505838b20761008530f90b23bb6a31716b008:/data -it ubuntu:bionic /bin/bash

open shell in running container
docker exec -it <container name> /bin/bash

open shell in running container as root
docker exec -it -u 0 <container name> /bin/bash

run a new temporary container with a given named volume and a folder mounted
docker run -it -v minecraft_mine:/mine -v /home/jukka/worlds:/worlds ubuntu /bin/bash

docker run -it -v minecraftjava_mcbig:/data -v /home/jukka/:/jukka ubuntu /bin/bash

docker stop <container name>

# update password stored by git

git config --global credential.helper osxkeychain

# print redhat version

cat /etc/redhat-release

# archive

rsync -vau /Volumes/BACKUP1/ /Volumes/BACKUP3/

# list volumes

rsync admin@192.168.10.55::
rsync admin@192.168.10.1::

>
# backup through daemon

rsync -vau /Volumes/Backup_3_1/ admin@192.168.10.55::Volume1/backup/  > rsync.output 2> rsync.error
rsync -vauP ../backup/ admin@192.168.10.46::volume1/backup2/  > rsync.output 2> rsync.error

# through ssh tunnel

ssh -L admin@nas -L 9999:localhost:873
rsync /Volumes/Backup_3_1/ rsync://localhost:9999/Volume1/backup/

# diff archive directories

diff -qrs /Volumes/BACKUP1/ /Volumes/BACKUP3/ > diff.txt

# list usb devices

ioreg -p IOUSB

# mounting fat32 disk

https://apple.stackexchange.com/questions/235309/external-drive-does-not-mount-after-plug-off-without-eject

ps aux | grep fsck
sudo kill <fsck pid>
diskutil list
diskutil mountDisk /dev/diskX

# Wake on lan

NAS326

wakeonlan -i 192.168.10.255 08:26:97:37:1D:96


NSA
wakeonlan -i 192.168.10.255 5C:F4:AB:E7:CD:AD

# screen

## start

export TERM=xterm-color
screen

## detach

Ctrl+a d

## resume

screen -r

## set date and time

sudo timedatectl set-timezone Europe/Helsinki
sudo timedatectl set-time 2020-10-04
sudo timedatectl set-time 07:14:00

# keytool
$JAVA\_HOME/bin/keytool -import -trustcacerts -noprompt -keystore "$CACERTS" -storepass ${KEYSTORE\_PASS} -alias "$ALIAS" -file $TEMP\_FILErm $TEMP\_FILE
  
  
# pgp
encrypt file with pass phrase
gpg -o output-file.gpg -c input-file.txt


