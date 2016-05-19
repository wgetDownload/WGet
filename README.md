
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

There is no doubt that when the normal operation of the instrument, it can not work any cheesed off at the terminal, which runs the program until the download is completed to make the download in the background and continue to use Allpartyah so you can add your b

sudo wget -c -b http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3

-b Option means the rear (f (background
You can also download a set of links in the text of the Reserved example quran.txt file now we Altarov my links to these circumstances by it and the cat who shows us what the contents of a text file

cat quran.txt

و النتيجة

http://www.mp3quran.net/newMedia.php?id=97&file=http://server8.mp3quran.net/afs_dori/097.mp3
http://www.mp3quran.net/newMedia.php?id=14&file=http://server8.mp3quran.net/afs_dori/014.mp3
http://www.mp3quran.net/newMedia.php?id=25&file=http://server8.mp3quran.net/afs_dori/025.mp3
http://www.mp3quran.net/newMedia.php?id=99&file=http://server8.mp3quran.net/afs_dori/099.mp3
http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3

To download the links on this file we use i option after Hecda tool:

sudo wget -c-i quran.txt

We now turn to cyclic loading or periodic mode For example, we want to upload a blog Linux revolution

http://to-linux.blogspot.com

sudo wget -c -r -k http://to-linux.blogspot.com

To download a certain DAT along Nakhadd files on the matter does not fill the DAT files Amtdat pdf only Dalk from the site http://www.4kotob.com

sudo wget -c -r -k -A.pdf http://www.4kotob.com

To add various other along separate them with a comma, for example, pdf and zip and tar:

sudo wget -c -r -k -A.pdf, zip, tar http://www.4kotob.com

Ada We wanted to upload my content one folder from the site without downloading Father folder, for example, want to download this site my father has many distributions and programs Allnieks: http://mirror.aarnet.edu.au/pub/
We want to download all the content fedora folder and site without downloading the full use property -np means for CAP (no parent)

sudo wget -c-r-k-np http://mirror.aarnet.edu.au/pub/fedora
