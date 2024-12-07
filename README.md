# e-solat
Sistem E-Solat 

Sistem ini base kepada API yang disediakan oleh pihak jakim dalam https://www.e-solat.gov.my/

ada beberapa api yang disediakan oleh www.e-solat.gov.my sebagaimana di bawah 

1.  https://www.e-solat.gov.my/index.php?r=esolatApi/TakwimSolat&period=today&zone=
    boleh lihat zone di https://github.com/hardyweb/e-solat/blob/main/zone.json
    
2.  https://www.e-solat.gov.my/index.php?r=esolatApi/SirimTime ( 
3.  https://www.e-solat.gov.my/index.php?r=esolatApi/tarikhtakwim&period=today&datetype=miladi ( tarikh milinium/ tarikh Melayu )
4.  https://www.e-solat.gov.my/index.php?r=esolatApi/takwimsolat&period=date&zone="+zone+"&date="+nexDate ( tarikh berikutnya pada zone tertentu )


Catatan 
1. jika baca terus dari API e-solat, akan ada latency sekitar 1000 milisaat ke 1300 milisaat bergantung kepada jaringan internet kita.
2. boleh juga guna cronjob untuk dapatkan attribute dari API esolat kemudian simpan ke dalam database kita sendiri. dengan cara ini, latensy semasa mendapatkan maklumat dapat dikurangkan.
   2.1  Jika lihat json yang disediakan ada dua table, table utama yang menunjukkan zone, servertime, longitut dan latithut diikuti dengan  table waktu solat

   ```json
{"prayerTime":[{"hijri":"1446-06-06","date":"08-Dec-2024","day":"Sunday","imsak":"05:41:00","fajr":"05:51:00","syuruk":"07:05:00","dhuhr":"13:02:00","asr":"16:23:00","maghrib":"18:55:00","isha":"20:10:00"}],"status":"OK!","serverTime":"2024-12-08 04:04:27","periodType":"today","lang":"ms_my","zone":"TRG01","bearing":"291&#176; 23&#8242; 2&#8243;"}
   ```
 
 

