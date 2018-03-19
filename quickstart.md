	 	 	
# Nette Framework Quickstart - első applikációm
## A hivatalos dokumentáció fordítása Cseh nyelvről, kiegészítve

### Első lépések

A legelső teendő indulás előtt egy gyors ellenőrzés, hogy a használt szerverünk teljesíti-e a Nette Framework futtatásához szükséges feltételeket (minimum 5.6.0-s PHP, a teljes feltételrendszer itt található: [Nette Requirements](https://doc.nette.org/en/2.4/requirements). Valószínűleg minden rendben lesz vele, de a biztonság kedvéért ellenőrizzük le, megéri.

A Nette Framework letöltéséhez a hivatalosan javasolt és ajánlott letöltési módszer a Composerrel való letöltés https://doc.nette.org/en/2.4/composer. Ha nem ismerjük a Composert, szánjunk rá pár percet, hogy megismerjük használatát. A Composer egy kifejezetten egyszerű és hasznos eszköz, mindent megtalálunk róla a [dokumentációjában]( https://getcomposer.org/doc/). Ha valami miatt nem tudunk Composert használni, letölthetjük akár manuálisan is, a [nette.org-downloadról](https://nette.org/cs/download). 

A Composerrel nagyon egyszerűen letölthetjük és installálhatjuk az applikációnk vázát (ezt hívjuk Web Projectnek), amely a  Nette Frameworkot is tartalmazza. Hogy működésbe hozhassuk, megkeressük a webszerverünk gyökérkönyvtárát (pl. /var/www, vagy C:/InetPub) és a parancssorba (Command Line) beírjuk a következő utasítást: ```composer create-project nette/web-project nette-blog```


