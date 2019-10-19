---
layout: post
title: Smart-Mirror mit dem Raspberry Pi
bigimg: img/post-smart-mirror/img1.jpg
image: img/post-smart-mirror/img1.jpg
layout: post
tags: [raspberry-pi, smart-mirror, home]
---

# Einleitung
Vor einiger Zeit hatte ich mir bei Ebay ein neuwertiges Notebook Display (Display für HP 625 Notebook Laptop) gekauft. 
Für 11 € ein echtes Schnäppchen. Passend dazu gab es ein Display-Controllerboard (HDMI DVI VGA LCD Controller Board Driver
n156b6-l0a n156b6-loa LED) auf Ebay für 24 €. Leider bringt es wenig einen Link einzufügen(Da diese Produkte immer nur für 
kurze Zeit angeboten werden), deshalb habe ich zwei Fotos hochgeladen. Bei Ebay werden eine Vielzahl von Displays mit 
passenden Controllern angeboten. Für den Smart-Mirror ist es prinzipiell egal welchen Monitor man verwendet.

![img2](/img/post-smart-mirror/img2.png)
![img21](/img/post-smart-mirror/img2_1.png)

Eigentlich habe ich Display + Controller nur gekauft, weil beides sehr günstig war. 
Damit hatte ich sozusagen einen 15.6″ HDMi Monitor für nur 35€ gekauft. Als ich auf das 
[mirr.OS](https://glancr.de/mirr-os/) Projekt gestoßen bin, konnte ich endlich Verwendung für  für das Display finden 🙂.


[Mirr.OS](https://glancr.de/mirr-os/) ist eine Erweiterung von Raspbian und wurde extra für die Smart-Mirror Anwendung entwickelt. 
Ein Alternative zu mirr.OS ist [MagicMirror2](https://github.com/MichMich/MagicMirror) was mir jedoch zu groß und komplex war. Ich wollte weder mit 
meinem Spiegel reden, noch ihn anfassen und konnte somit auf die Touchfunktion verzichten.

# Vorbereitung

##Software
Das Betriebssystem [mirr.OS](https://glancr.de/mirr-os/) lud ich hier herunter. Da ich OS X verwende habe ich 
[Etcher](https://etcher.io/) genutzt um das Image auf die SD Karte zu spielen. Schneller und einfacher geht es nicht.

## Hardware
Neben dem Display und dem Display-Controller (35€) benötigte ich noch folgende Sachen:

- Raspberry Pi 3 (35€)
- HDMI Kabel (lag noch bei mir herum)
- [Flaches 12V 3A Netzteil](https://www.pollin.de/p/schaltnetzteil-ad6660lf-12-v-3-33-a-gebraucht-351901)  (4€)
- Ich hatte mich, nach einiger Recherche im Netz für den [Mirropane™ Chrome Spy](http://brigla-shop.de/spionspiegel-329.html) 
entschieden. Inklusive Versand kostete der Spiegel (68€). Nicht günstig aber ideal für diese Anwendung. Und ich wollte mich nicht im Nachhinein ärgern 20€ gespart zu haben, um danach ein schlechtes Ergebnis zu erhalten.
- Eichenholz für den Rahmen (15€)
- Klebeband, Holzleim, Pappe und Kleber (hatte ich alles noch)
- Winkel zur Stabilisierung des Rahmens (ca. 2€)
- Alu-Schiene und Wandhalterung (ca. 5€)

Die Kosten lagen somit insgesamt bei ca.  170€.

## Bau des Spiegels

Die Spiegelkonstruktion aus Holz wirkte zunächst recht simpel, stellte sich jedoch als gar nicht so einfach heraus. 
Das Eichenholz hatte ich vom [Holzhändler aus der Nähe](http://www.holz-schwarz.de/), der mich auch bei der Auswahl sehr gut unterstützte. 
Der Spiegel war so konzipiert, dass von der Spiegelfläche (60cm x 40cm) rundum jeweils 1cm hinter dem Holz verschwinden 
sollte. Der Zentimeter diente als Klebefläche für das Spiegelglas. Die 6cm breiten Holzleisten für die Front wurden 
jeweils auf 45 ° geschnitten. Auf die Rückseite kamen 4cm dicke Leisten. Diese Stärke war mindestens notwendig, 
um die Elektronik im inneren des Spiegels gut zu verbauen. Der erster Versuch das Holz zu schneiden scheiterte 
leider kläglich, da die Bretter der Front keine 45 ° hatten und somit nicht verklebt werden konnten. 
Deshalb hat mein Vater, der geübter mit der Kapp-Säge ist, die Bretter nachgeschnitten und verklebt. 
Dann passte das Ganze auch :D. Bevor die Bretter verleimt wurden (schliff ich sie noch ab). Das macht einen 
deutlichen Unterschied. Ich kann diesen Arbeitsschritt nur empfehlen, da sich das abgeschliffene 
Eichenholz klasse anfühlt.

![img3](/img/post-smart-mirror/img3.jpg)

Anschließend habe ich die Außenflächen mit “Möbel Regenerator” bestrichen. Dafür nimmt man einfach ein Tuch oder ein 
Fetzen Stoff und reibt die Holzoberfläche mit etwas vom Regenerator ein. Der Regenerator sorgt dafür, dass die 
Oberfläche unempfindlicher gegen Schmutz und Flecken ist. So kann man die Oberfläche nun auch mit Wasser säubern, 
ohne das Wasserflecken auf dem Holz entstehen. Des Weiteren sorgt der Regenerator dafür, dass die Holzmaserung des 
Eichenholzes besser zum Vorschein kommt und das Holz insgesamt etwas dunkler wird.

![img4](/img/post-smart-mirror/img4.jpg)

Den Unterschied kann man auf den nachfolgenden Bildern  sehen, in der Mitte vor der Behandlung mit dem Regenerator 
und rechts danach.


![img5](/img/post-smart-mirror/img5.jpg)
![img6](/img/post-smart-mirror/img6.jpg)
![img7](/img/post-smart-mirror/img7.jpg)

Zur zusätzlichen Stabilisierung des Rahmens habe ich noch Winkel auf die Innenseite geschraubt. 
Weil das Eichenholz extrem hart ist sollte man immer vorbohren.

Anschließend habe ich das Spiegelglas vorbereitet. Das Display klebte ich mit Panzer-Tape auf die Rückseite des 
Spiegelglases. Man sollte darauf achten, dass alle Leuchtelemente/Leuchtflächen verklebt sind. So ist beim 
Display beispielsweise auf der Vorderseite ein Schlitz im Gehäuse aus dem Licht von der Hintergrundbeleuchtung scheint.
Das Licht aus dem Schlitz würde man ebenfalls auf der Spiegelvorderseite sehen, was die Schrift auf dem Display jedoch 
stören würde. Deshalb alles was leuchtet zukleben! Die restliche Spiegelfläche habe ich mit Pappe und ebenfalls 
Panzer-Tape blickdicht zugeklebt. Auf die Pappe wurde mit doppelseitigem Klebeband die Elektronik befestigt. 
Da ich nur eine Stromversorgung habe (12V), greife ich die 5V für den Raspberry Pi direkt vom HDMI Converter Board ab. 
Dafür nutze ich den Anschluss der eigentlich für ein IR-LED gedacht war. Beim verwendeten Stecker handelt es sich um 
einen JST-XXX den ich noch zufällig hatte. Auf Pin 1 ist 5V auf pin 2 GND. Auf die andere Seite des Kabels habe ich 
ein USB Kabel gelötet. Bei USB ist rot 5V und weiß ist GND. Das USB Kabel habe ich dann einfach in den USB Power-Eingang 
vom PI gesteckt und festgeklebt. Der Vorteil davon ist, dass ich ein 5V Netzteil spare, der Nachteil dass der RPI 5.1V 
benötigt und mir ein Unterspannung signalisiert, welche man im Spiegel sehen kann. Diese Warnung kann man jedoch ausstellen.

![img8](/img/post-smart-mirror/img8.jpg)
![img9](/img/post-smart-mirror/img9.jpg)
![img10](/img/post-smart-mirror/img10.jpg)

Die Bilder zeigen die Anordnung der Elektronik im Inneren des Spiegels. Das Netzteil das ich “gebraucht” bei Pollen 
gekauft hatte war interessanter Weise ein ausrangiertes Netzteil von einem SKY Receiver. Das Netzteil musste ich noch 
anpassen und einen 12V Holsteiner dran löten. Auf die Netzseite  habe ich lediglich ein Kabel mit Lüsterklemme gesteckt 
und dieses am Rahmen befestigt. Hier wurden später die 230V angeschlossen.

Um den Spiegel an die Wand zu hängen hatte ich eine 60cm Alu-Leiste auf die Rückseite geschraubt. An die Wand wurden 
Halterungen aus dem Baumarkt  angebracht, in die man den Spiegel anschließend einhängen konnte. Zum Glück war eine 
Abzweigdose über dem Spiegel. In dieser wurden die Schalter im Flur verdrahtet und glücklicherweise konnte ich den 
Spiegel einfach an die Zuleitung anschließen :). Für das Kabel hatte ich noch ein Loch auf die Oberseite des Spiegels 
gebohrt und das Kabel durchgezogen.

![img11](/img/post-smart-mirror/img11.jpg)

# Update vom 11.03.2018
Leider war die Idee, das Spiegelglas mit doppelseitigem Klebeband zu befestigen, nicht die beste. Das Spiegelglas 
hatte sich vom Holzrahmen gelöst. Im Baumarkt habe ich einen Kleber von Pattex (Montage Kleber Special) geholt. 
Mal schauen wie lange dieser die Scheibe hält :D.

# Einrichten von mirr.OS
Nachdem ich mirr.OS auf eine SD Karte gespielt und den PI gebootet hatte, startete das Betriebssystem erst mit dem 
mirr.OS Logo und anschließend mit dem Herzlich-Willkommen Screen. Ich hatte vorher versucht mirr.OS mit einem PI Zero 
und einem WLAN Stick zu benutzen. Leider war der WLAN Stick nicht für Linux und ich hatte keinen anderen zur Hand. 
Deshalb hatte ich mich für den RPI 3 entschieden, der kommt direkt mit WLAN on Board.

Die Konfiguration von mirr.OS ist recht unkompliziert und auch gut beschrieben. Der RPI macht ein WLAN Access Point 
auf (**GlancrAP**). Mit diesem verbindet man sich und bekommt das Passwort auf dem Bildschirm angezeigt. 
Im Browser öffnet man **http://glancr.conf/** und nimmt dort alle Einstellungen wie Name, Stadt, Emailadresse 
und Zugang zum Heimnetzwerk/WLAN vor.  Das wars im Grunde auch schon. Mirr.OS sendet eine Email wenn alles geklappt hat.

![img12](/img/post-smart-mirror/img12.png)

Das coole an mirr.OS ist die einfache Konfiguration über den Browser. Dafür gibt man nur die IP/config 
(z.B. **http://192.168.2.106/config/**) im Browser ein und kann mirr.OS konfigurieren. Die Aufteilung der Module kann 
man wie auf der Abbildung zu sehen ist frei wählen. Aktuell sieht meine Auswahl wie auf der nebenstehenden Abbildung aus. 
Die [Module](/https://glancr.de/module/) werden kostenlos auf der mirr.OS Seite zum Download angeboten. Dabei sollte 
man darauf achten, dass der Browser die ZIP Datei nicht entpackt. Mein Safari macht dies leider und auch anschließendes 
Komprimieren als Zip bringt nichts. Deshalb musste ich Firefox nutzen. In mirr.OS kann man die Module als ZIP 
anschließend einfach hochladen.

Beim konfigurieren der einzelnen Module ist mir folgendes aufgefallen. Ich denke das wird in Zukunft gefixt.

- Beim Einstellen des Api-Keys von OpenWeather musste ich die letzte Ziffer des Keys löschen und wieder hinschreiben. 
Mirr.OS hatte mir sonst immer angezeigt das der Api-Key ungültig sei, wenn ich diesen nur CMD+V eingefügt hatte.
- Beim Einstellen meines iCloud Kalenders musste ich “webcal” durch “https” ersetzen. Das wird aber auch im 
Modul-tutorial beschrieben.

Generell finde ich mirr.OS durchdacht und leicht zu bedienen. Zu jedem Modul gibt es eine Anleitung und sogar bei der 
Konfiguration im Browser findet man Links in den Modulen, die einen direkt dahin bringen wo man hin muss. Zum Beispiel 
auf die OpenWeather Seite um sich den Api-Key zu besorgen. Das macht Spaß und man merkt, dass die Jungs von mirr.OS 
sich Zeit genommen haben das System extrem anwenderfreundlich zu gestalten.

# Anpassen des Raspberry Pi
## Unterspannungsanzeige ausschalten

![img13](/img/post-smart-mirror/img13.jpg)

Was ich noch störend fand war das “Undervoltage” Zeichen in Form eines kleinen Blitzes, welchen der PI auf dem 
Display anzeigte. Da ich kein PI Netzteil mit 5.1V verwende, sondern wie vorher beschrieben die 5V vom HDMI-Converter 
Board abgreife, meckert der PI und meint er würde eine zu geringe Spannung bekommen. Zum abstellen des Blitzen bin ich 
wie folgt vorgegangen.

Anmelden per ssh über das Terminal auf meinem Macbook:
```
ssh pi@192.168.0.106
Passwort: glancr!2017
```

Auf dem Pi muss man die config.txt anpassen und folgende Zeile einfügen:
```
sudo nano /boot/config.txt
```
Folgende Zeile am Ende der Datei ergänzen. Danach speichern und neu starten.
```
avoid_warnings=1
```

HDMI Monitor zeitgesteuert an/aus schalten

Da wir wochentags arbeiten sind, soll der Raspberry Pi und dementsprechend auch der HDMI-Monitor ausgeschaltet werden. 
Dafür eignen sich cronjobs. Der [Cron-Daemon](https://de.wikipedia.org/wiki/Cron) ist ein Dienst, der automatisch Skripte und Programme zu vorgegebenen 
Zeiten starten kann.

Wie oben beschrieben greift man wieder per ssh auf den PI zu. Um die Root Cron-Tabelle zu öffnen gibt man 
folgenden Befehl ein:
```
sudo crontab -e
```

Meine Einstellung sieht vor, dass von Montag bis Freitag (1-5) jeweils um 10:00 Uhr der HDMI Ausgang des PIs 
ausgeschaltet und um 16:00 wieder eingeschaltet wird. Um den Cronjob zu editieren muss man nur die beiden 
nachfolgenden Zeilen einfügen.
```
# Turn off hdmi monitor from monday to friday at 10:00 o'clock
0 10 * * 1-5 tvservice --off
# Turn hdmi monitor on from monday to friday at 16:00 o'clock
0 16 * * 1-5 tvservice -p
```
