# PS4 Server 9.00

This is a project designed for the <a href=https://www.wemos.cc/en/latest/d1/d1_mini.html>esp8266 D1 Mini</a> or the <a href=https://www.wemos.cc/en/latest/d1/d1_mini_pro.html>esp8266 D1 Mini PRO</a> to provide a wifi http server and dns server.



this is for the 9.00 exploit and the esp8266.

the exploit files and payloads will be cached on first load which will allow full offline operation, you will still need to plug in the usb drive manually but the ESP8266 will not be required in offline mode.

the firmware is updatable via http and the exploit files can be managed via http.

you can access the main page from the userguide or the consoles webbrowser.

</b>

<br>
<br>


<b>implemented internal pages</b>

* <b>admin.html</b> - the main landing page for administration.

* <b>index.html</b> - if no index.html is found the server will generate a simple index page and list the payloads automatically.

* <b>info.html</b> - provides information about the esp board.

* <b>format.html</b> - used to format the internal storage(<b>SPIFFS</b>) of the esp board.

* <b>upload.html</b> - used to upload files(<b>html</b>) to the esp board for the webserver.

* <b>update.html</b> - used to update the firmware on the esp board (<b>fwupdate.bin</b>).

* <b>fileman.html</b> - used to <b>view</b> / <b>download</b> / <b>delete</b> files on the internal storage of the esp board.

* <b>config.html</b> - used to configure wifi ap and ip settings.

* <b>reboot.html</b> - used to reboot the esp board


<br><br>


installation is simple you just use the arduino ide to flash the sketch/firmware to the esp8266 board.<br>
<br>
make sure you set the flash size to match the D1 board you are using.<br>
4M (3M SPIFFS) for the D1 Mini<br>
<img src=https://github.com/stooged/PS4-Server-900/blob/main/Images/4m3m_spiffs.jpg><br>
there is a storage limitation of <b>2.8mb</b> for the <b>D1 Mini</b> board.<br><br>

<b>16M (15M SPIFFS)</b> for the D1 Mini PRO<br>
<img src=https://github.com/stooged/PS4-Server-900/blob/main/Images/16m15m_spiffs.jpg><br>
there is a storage limitation of <b>14.2mb</b> for the <b>D1 Mini PRO</b> board.

<br><br>
next you connect to the wifi access point with a pc/laptop, <b>PS4_WEB_AP</b> is the default SSID and <b>password</b> is the default password.<br>
then use a webbrowser and goto http://10.1.1.1/admin.html <b>10.1.1.1</b> is the defult webserver ip.<br>
on the side menu of the admin page select <b>File Uploader</b> and then click <b>Select Files</b> and locate the <b>data</b> folder inside the <b>PS4_Server_900</b> folder in this repo and select all the files inside the <b>data</b> folder and click <b>Upload Files</b>
you can then goto <b>Config Editor</b> and change the password for the wifi ap.


alternatively you can upload the files to the esp8266 with the arduino ide by selecting <b>Tools > ESP8266 Sketch Data Upload</b>

<img src=https://github.com/stooged/PS4-Server-900/blob/main/Images/dataup.jpg><br><br>

the files uploaded using this method are found in the <b>data</b> folder inside the <b>PS4_Server_900</b> folder.
