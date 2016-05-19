
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

ننتقل الان لكيفية استخدام  الاداة  :
مثلا نريد تحميل سورة الاعلى .mp3 نفتح الطرفية من المكان الدي نريد التحميل فيه ثم :
sudo wget http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3 
في هده الحالة سوف يتم التحميل بالسرعة القصوى ،وإذا اردنا تحديد مثلا في 200K السرعة يجب اضافة هاته الخاصية :   
  sudo wget -c --limit-rate=200k http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3
الخيار c  يعني الاستمرار التحميل في اخر نقطة وقوف دون البداء من الصفر
و الخيار limit-rate=200  تعني تحديد السرعة في 200k كيلو بايت 
الحرف K يعني كيلوبيت يمكنك تغيره الى M ان اردنا مكابيت  او G ان اردنا ان نعني الجيكابيت وان لم تحدد انت فإن السرعة ستكون بالبايت 
وإذا اردنا تغيير مجلد التحميل مثلا من مجلد البيت الى مجلد اخر دالك فقط ب :
 wget -c http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3 -P /home/abedo-fx/quran 
مما لا شك فيه انه عند التشغيل العادي لااداة فانه لا يمكنك عمل اي شيىء في الطرفية التي يشتغل عليها البرنامج حتى انتهاء التحميل لجعل التحميل في الخلفية والستمرار على استخدامك اللطرفية يمكنك اضافة b  هكذا :
sudo wget -c -b http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3 
الخيار -b يعني الخلفي (f(background
يمكنك ايضا تحميل مجموعة من الروابط  محفوضة في ملف نص مثال quran.txt الان نقوم بي التعروف على هاته الروابط عن طريق الامر cat والذي يظهر لنا محتويات ملف نصي ما
cat quran.txt
و النتيجة:

http://www.mp3quran.net/newMedia.php?id=97&file=http://server8.mp3quran.net/afs_dori/097.mp3
http://www.mp3quran.net/newMedia.php?id=14&file=http://server8.mp3quran.net/afs_dori/014.mp3
http://www.mp3quran.net/newMedia.php?id=25&file=http://server8.mp3quran.net/afs_dori/025.mp3
http://www.mp3quran.net/newMedia.php?id=99&file=http://server8.mp3quran.net/afs_dori/099.mp3
http://www.mp3quran.net/newMedia.php?id=87&file=http://server8.mp3quran.net/afs_dori/087.mp3
ولتحميل الروابط الموجودة بهذا الملف نسستعمل خيار i  بعد الاداة هكدا :   
sudo wget -c-i quran.txt
ننتقل الان الى طريقة التحميل الحلقي او الدورية فمثلا نريد تحميل مدونة ثورة اللينكس 
   http://www.com  
      sudo wget -c -r -k http://www.com
ولتحميل ملفات دات امتداد معين ناخد على سبيل المتال  ملفات دات امتدات pdf فقط ودالك من الموقع   http://www.4kotob.com  
sudo wget -c -r -k -A.pdf http://www.com
وللاضافة امتداد اخرى مختلفة نفصل بينهما بفاصلة , مثلا pdf و zip و tar : 
                          sudo wget -c -r -k -A.pdf,zip,tar http://www.com
ادا اردنا تحميل محتواى مجلد واحد من الموقع دون تحميل مجلد الاب مثلا نريد تحميل هدا الموقع الدي يحتوي على العديد من التوزيعات والبرامج اللنيكس :                                                http://mirror.aarnet.edu.au/pub/
ونريد تحميل جميع محتوى مجلد fedora ودون تحميل الموقع كاملا نستعمل خاصية -np وتعني لااب (no parent) 
sudo wget -c-r-k-np http://mirror.aarnet.edu.au/pub/fedora
