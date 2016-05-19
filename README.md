
#**WGet**#

Wget Download 

wget -E -H -k -K -p -e robots=off -P /Downloads/

wget.exe -h

wget.exe -c

wget.exe -qO - 

tar zxvf wget-1.17.tar.gz
cd wget-1.17
./config
 make
su -c make install

We now turn to how to use the tool, for example, we want to download Al-Ala .mp3 open the terminal from my father's place, and then we want to download

sudo wget http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3

In this case load will be full speed, and if we want to determine, for example, at 200K speed must add these circumstances property

sudo wget -c --limit-rate=200k http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3

C option means to continue loading the last parking spot without our audit from scratch
And limit-rate = 200 option means the speed limit in kilobytes 200k
The letter K means Kilubit you can change it if we want to M or G Mkapet that we wanted to Algikapet mean that you did not specify the speed will be in bytes
If you want to change the download folder, for example, from home folder to another folder Dalk only b

wget -c http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3 -P /home/abedo-fx/quran


