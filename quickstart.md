	 	 	
# Nette Framework Quickstart - első applikációm
## A hivatalos dokumentáció fordítása cseh nyelvről, kezdőbarát megjegyzésekkel kiegészítve és senior fejlesztők által lektorálva (nagyon nagy köszi mindenkinek :) )

### Első lépések

* A legelső teendő indulás előtt egy gyors ellenőrzés, hogy a használt szerverünk teljesíti-e a Nette Framework futtatásához szükséges feltételeket (minimum 5.6.0-s PHP, a teljes feltételrendszer itt található: [Nette Requirements](https://doc.nette.org/en/2.4/requirements). Valószínűleg minden rendben lesz vele, de a biztonság kedvéért ellenőrizzük le, megéri.
* A Nette Framework letöltéséhez a hivatalosan javasolt és ajánlott letöltési módszer a Composerrel való letöltés https://doc.nette.org/en/2.4/composer. Ha még nem találkoztunk a Composerrel, szánjunk rá pár percet, hogy megismerjük használatát. A Composer egy kifejezetten egyszerű és hasznos eszköz, ez a legelterjedtebb külső függőségeket kezelő program PHP-ra (PHP dependency manager). Mindent szükséges infót megtalálunk róla a [dokumentációjában]( https://getcomposer.org/doc/). Ha már a Composer dokumentációja alapján installáltuk a Composert a gépünkre (kezdők inkább globálisan installálják), akkor 
	* Megkeressük a webszerverünk gyökérkönyvtárát (ez általában ott van, ahova az apache vagy az nginx webszervert is telepítettük, ha nem tudjuk hol van, akkor keressük ki az interneten. A kereséshez ajánlott kulcsszavak: webserver root directory, document root vagy web root. (pl. /var/www, vagy C:/InetPub is lehet). 
	* Megnyitjuk a parancssort (Windowsnál Accesoires->Command Prompt, Macnél Terminal ) 
	* Belépünk a gyökérkönyvtárba és beírjuk a következő utasítást:

	`composer create-project nette/web-project nette-blog`

	Ez a parancs azt jelenti, hogy a Composer a saját [Packagist könyvtárából](https://packagist.org/packages/nette/web-project) letölti a nette/web-projectet és azt minden függőségével (dependency) és körülményével együtt bemásolja az általunk megadott nette-blog mappába. Vagy ha nincs még ilyen mappa a gyökérkönyvtárban (pl /var/www vagy C:/InetPub), akkor elkészíti. Igazából bármilyen nevet adhatnánk a projektnek, most nette-blognak nevezzük. 

*Megjegyzés 1: Ha valami miatt nem tudunk Composert használni, letölthetjük manuálisan is a [githubról a Nette Web Projectet](https://github.com/nette/web-project/archive/preloaded.zip). Ezt letöltés után kicsomagoljuk, bemásoljuk a gyökérkönyvtárunkba és átnevezzük "nette-blog"-ra.* 

*Megjegyzés 2: Ha szeretnénk egy [parancssor gyorstalpalót](https://lifehacker.com/5633909/who-needs-a-mouse-learn-to-use-the-command-line-for-almost-anything), mert mondjuk nem tudunk belépni a parancssor használatával a gyökérkönyvtárba, akkor keressünk egy tutorialt az interneten. Kulcsszavak: command line basics, getting to know the command line*

* Ha Unix alapú rendszeren dolgozunk (pl. Mac OS X vagy Linux), akkor módosítanunk kell a webszerver jogait is: engedélyezni kell a temp és a log file-ok írását.

```cd nette-blog && chmod -R a+rw temp log```

*Megjegyzés 1: egyes Linuxokon (Fedora, CentOs,…) alapból be van kapcsolva a SELinux. Ezért módosítani kell a SELinux policiest, vagy be kell állítani a megfelelő SELinux security context-et a temp és log fájloknak.*



### Főoldal

Ha letöltöttük a gépünkre a Nette Quickstartot a fentiek szerint és beírjuk a böngészőnkbe a http://localhost/nette-blog/www/ címet, és a "Congratulations!" ablakot látjuk, akkor már jók vagyunk, működik a Nette applikációnk :)

![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)
