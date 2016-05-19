
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

ننتقل الان لكيفية استخدام  الاداة 
مثلا نريد تحميل سورة الاعلى .mp3 نفتح الطرفية من المكان الدي نريد التحميل فيه ثم

sudo wget http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3

في هده الحالة سوف يتم التحميل بالسرعة القصوى ،وإذا اردنا تحديد مثلا في 200K السرعة يجب اضافة هاته الخاصية

  sudo wget -c --limit-rate=200k http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3
