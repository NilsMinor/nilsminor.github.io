---
layout: post
title: Smart-Mirror mit dem Raspberry Pi
bigimg: img/post-smart-mirror/img1.png
image: img/post-smart-mirror/img1.png
layout: post
tags: [raspberry-pi, altium-designer]
---

# Einleitung
Vor einiger Zeit hatte ich mir bei Ebay ein neuwertiges Notebook Display (Display für HP 625 Notebook Laptop) gekauft. 
Für 11 € ein echtes Schnäppchen. Passend dazu gab es ein Display-Controllerboard (HDMI DVI VGA LCD Controller Board Driver
n156b6-l0a n156b6-loa LED) auf Ebay für 24 €. Leider bringt es wenig einen Link einzufügen(Da diese Produkte immer nur für 
kurze Zeit angeboten werden), deshalb habe ich zwei Fotos hochgeladen. Bei Ebay werden eine Vielzahl von Displays mit 
passenden Controllern angeboten. Für den Smart-Mirror ist es prinzipiell egal welchen Monitor man verwendet.

![img2](/img/post-smart-mirror/img2.png)

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


