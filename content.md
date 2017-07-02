<!-- .slide: data-background="linear-gradient(rgba(0, 0, 0, 0.3), rgba(0, 0, 0, 0.3)), url(media/img/beuth.png)" data-background-size="cover" -->

<div class="talk-title">
  <h1>Masterarbeit Verteidigung</h1>
  <p>Konzeption, Entwicklung und Evaluation einer
     interaktiven Virtual Reality Anwendungen mit
     Web-Technologien im Vergleich zu nativer Entwicklung</p>
  <p class="talk-info" style="margin-top: -100px">
    Sebastian Kasanzew | Beuth Hochschule | iconmobile
  </p>
</div>

<!-- NOTES -->

- Titel vorlesen

------

# Ziele

* Vergleich zwischen WebVR und nativen VR-Apps
* Entwicklung einer Test-App für beide Platformen
* Evaluation der Ergebnisse der Test-App durch Usertests

<!-- NOTES -->

- Ziele erläutern

------

## Entwickler Plattformen

<!-- .slide: data-transition="slide-in none" -->

<div class="image-row">
    <p>&nbsp;&nbsp;&nbsp;</p>
    <p>native<br/>Engines</p>
    <div><img style="padding-left: 15px" data-src="media/img/Unity.png" todo="Unity"></div>
    <div><img style="padding-left: 30px" height="200px" data-src="media/img/Unreal.png" todo="Unreal"></div>
    <div><img data-src="media/img/CryEngine.png" todo="CryEngine"></div>
</div>

<div class="image-row" style="height: 222.815px">

</div>

<div class="image-row" style="height: 10px; margin-top: -50px">

</div>

<!-- NOTES -->

---

## Entwickler Plattformen

<!-- .slide: data-transition="none slide-out" -->

<div class="image-row">
    <p>&nbsp;&nbsp;&nbsp;</p>
    <p>native<br/>Engines</p>
        <div><img style="padding-left: 15px" data-src="media/img/Unity.png" todo="Unity"></div>
        <div><img style="padding-left: 30px" height="200px" data-src="media/img/Unreal.png" todo="Unreal"></div>
        <div><img data-src="media/img/CryEngine.png" todo="CryEngine"></div>
</div>

<div class="image-row"  style="height: 222.815px">
    <p>&nbsp;&nbsp;&nbsp;</p>
    <p>WebVR</p>
    <div>
        <h2 style="margin-left: 280px">**das Web**</h2>
    </div>
</div>

<div class="image-row" style="height: 10px; margin-top: -50px">
    <p style="margin-left: 300px">HTML</p>
    <p style="margin-left: 70px">JavaScript</p>
    <p style="margin-left: 70px">WebGL</p>
</div>

<!-- NOTES -->

---

## Gewählte Plattformen/Frameworks <br> zum Vergleich

<div class="image-row">
    <div><img data-src="media/img/Unity.png"></div>
    <div><img data-src="media/img/aframe-logo.png"></div>
</div>

------

# Bewertung

<!-- NOTES -->

- unterteilt in technische Kriterien welche eher das Endprodukt beeinflussen
- und allgemeine Kriterien, die die Entwicklung beeinflussen

---

# Technische Kriterien

- Hardware
- Grafik-API
- Multimedia
- Lizensierung
- Performance

<!-- NOTES -->

- Hardware: Kompatibilität mit aktueller Hardware
- Lizensierung: Lizensmodell für Vertrieb
- Grafik-API: Möglichkeiten der gegebenen Grafikschnittstellen
- Multimedia: Unterstützung von verschiedenen Formaten (3D/Bild/Video)
- Performance: Anzahl/Komplexität dargestellter Elemente bei stabiler FPS

---

# Allgemeine Kriterien

- Dokumentation
- Community
- Verbreitung
- Implementierungsaufwand
- Paketmanager
- Wiederverwertbarkeit

<!-- NOTES -->

- Dokumentation: Umfang und Qualität der Dokumentation
- Community: Größe und Aktivität
- Verbreitung: Anzahl vertriebener Apps
- Implementierungsaufwand: Zeit der Entwicklung am Beispiel der Test-App
- Paketmanager: Anzahl und Qualität angebotener Pakete
- Wiederverwertbarkeit: Portierbarkeit von Code zwischen Projekten

------

# Technische Kriterien

---

# Hardware

<div class="image-row">
  <div><img data-src="media/img/google-cardboard.png"></div>
  <div><img data-src="media/img/google-daydream.png"></div>
  <div><img data-src="media/img/samsung-gearvr.png"></div>
</div>

<div class="image-row">
  <div><img data-src="media/img/oculus-rift.png"></div>
  <div><img data-src="media/img/playstation-vr.png"></div>
  <div><img data-src="media/img/htc-vive.png"></div>
</div>

<!-- NOTES -->
- Wird von großen Unternehmen weltweit investiert
- Hardware reicht von billig bis teuer, mit und ohne Kabel, Controller, verschiedene Tracking Technologien
- Die HTC Vive bietet mit Steam derzeit das umfangreichste Erlebnis auf dem freien Markt
- Es gibt also eine große Anzahl an Geräten, Systemen und Plattformen, die in Konkurenz zu einander stehen
- A-Frame

---

https://webvr.rocks

<div class="captioned-image-row small">
  <div>
    <img data-src="media/img/firefox-nightly.png">
    <i>Firefox Nightly</i>
  </div>
  <div>
    <img data-src="media/img/edge.jpg">
    <i>Microsoft Edge</i>
  </div>
  <div>
    <img data-src="media/img/chromium.png">
    <i>Chromium</i>
  </div>
</div>

<div class="captioned-image-row small">
  <div>
    <img data-src="media/img/chrome.png">
    <i>Chrome for Android</i>
  </div>
  <div>
    <img data-src="media/img/carmel.jpg">
    <i>Oculus Carmel</i>
  </div>
  <div>
    <img data-src="media/img/samsung-browser.png">
    <i>Samsung Internet</i>
  </div>
  <div>
    <img data-src="media/img/google-cardboard.png">
    <i>Mobile Polyfill</i>
  </div>
</div>

<!-- NOTES -->
- Firefox + Chrome WebVR 1.0 hits release channels by early 2017
- Currently behind Nightly, custom builds, and flags
- Mobile Polyfill: use device motion / orientation sensors to polyfill on smartphones
- With all the browsers behind it...

---

# Grafik-API

<table>
  <tr>
    <th>A-Frame</th>
    <th>Unity</th>
  </tr>
  <tr>
    <td>WebGL 1.0 (~OpenGLES 2.0)</td>
    <td>DirectX 9-12</td>
  </tr>
  <tr>
    <td>[WebGL 2.0 (~OpenGLES 3)]</td>
    <td>OpenGLCore</td>
  </tr>
  <tr>
    <td></td>
    <td>OpenGLES 2-3</td>
  </tr>
  <tr>
    <td></td>
    <td>Metal</td>
  </tr>
  <tr>
    <td></td>
    <td>Vulkan<br></td>
  </tr>
</table>

---

# Multimedia

<table>
  <tr>
    <th></th>
    <th>A-Frame</th>
    <th>Unity</th>
  </tr>
  <tr>
    <td rowspan="2">3D</td>
    <td>COLLADA, OBJ, JSON, Blend, glTF</td>
    <td>FBX, COLLADA, OBJ, </td>
  </tr>
  <tr>
    <td></td>
    <td>MAX, C4D, Maya, ...</td>
  </tr>
  <tr>
    <td>Bilder</td>
    <td>JPG, PNG, BMP, GIF, SVG</td>
    <td>JPG, PNG, BMP, TGA, TIF, PSD</td>
  </tr>
  <tr>
    <td>Videos</td>
    <td>Browserabhängig</td>
    <td>alle von Browsern unterstützen Formate</td>
  </tr>
</table>

---

# Lizensierung
<style type="text/css">
table {
    border-collapse:collapse;
    border-spacing:0;
    margin:0px auto;
}
</style>

<table>
  <tr>
    <th>&nbsp;</th>
    <th>A-Frame</th>
    <th>Unity</th>
  </tr>
  <tr>
    <td>&nbsp;</td>
    <td>Open Source (MIT)</td>
    <td>Closed Source</td>
  </tr>
  <tr>
    <td>&nbsp;</td>
    <td></td>
    <td>Lizenz abhängig von Umsatz und Unternehmensgröße</td>
  </tr>
</table>

---

# Performance

<img height="500px" src="media/img/FCAT.png">

------

# Allgemeine Kriterien

---

# Dokumentation

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/aframe-doc.png">
    <i>A-Frame</i>
  </div>
  <div>
    <img data-src="media/img/Unity-doc.png">
    <i>Unity</i>
  </div>
</div>

<!-- NOTES -->

- A-Frame hat eine sehr vollständige, versionierte Doku
- A-Frame scholar bietet eine Plattform zum Austausch und Tutorials
 
- Unity hat jedoch all das, aber in viel größerem Umfang (mehrsprachig)
- auch durch die höhere Komplexität und Funktionsumfang

---

<!-- .slide: data-background="media/img/header.png" -->

# Community

https://aframe.io/blog/

---

<!-- .slide: data-background="media/img/apainter.gif" -->

# A-Frame: *A-Painter*

@mozillavr

---

<!-- .slide: data-background-video="media/video/Star_Trek_Bridge_Crew.mp4" data-background-video-loop="true" data-background-video-muted="true" data-state="state--bg-dark" -->

# Unity:<br> *Star Trek:Bridge Crew*

@Ubisoft

<p class="talk-info">https://youtu.be/p_Rz_btMLR4</p>

---

# Implementierungsaufwand

<br><br>

| A-Frame     | Unity      |
|-------------|------------|
| ~90 Stunden | 35 Stunden |

---

# Paketmanager

| A-Frame                   | Unity VR             |
|---------------------------|----------------------|
| 350 000 npm Pakete        | 15 000 Pakete        |
| 100+ speziell für A-Frame | 1000 speziell für VR |

<!-- NOTES -->
- Open source
- Meiste Arbeit auf GitHub
- Aktive Community auf Slack um Projekte zu teilen, interagieren, um Hilfe bitten
- Featured projects on the `awesome-aframe` repository and *A Week of A-Frame* blog

---

# Wiederverwertbarkeit

| A-Frame                          | Unity VR                     |
|----------------------------------|------------------------------|
| Einfache Trennung in npm Pakete  | Modularer Code möglich       |
| Simples Updaten von Paketen      | Umstände bei Paket Update    |
| Versionsabhängigkeiten vorhanden | Keine Versionsabhängigkeiten |

<!-- NOTES -->

------

# Ergebnis

<!-- .slide: data-background-color="#fff" -->

<img src="media/img/Kriterien.png">

---

## User Tests

mit 20 Teilnehmern

<img src="media/img/umfrage/header.jpg">

---

## A-Frame App

<!--<div class="stretch" data-aframe-scene="scenes/Tool-Test-VR.html"></div>-->
<iframe width="800" height="500" src="http://webvr.kasanzew.de"></iframe>

<!-- NOTES -->
- Das ist die von mir erstellte A-Frame App, die innerhalb der Folie läuft 
- Funktioniert auf Desktops, Android, iOS, Samsung Gear VR, Oculus Rift und HTC Vive
- Could open up the DOM Inspector to change values live
- Since it's just HTML...

---

## Bewertung

<!-- .slide: data-background-color="#fff" -->

<img src="media/img/umfrage/Bewertung.png">A

---

## Gesamteindruck

<!-- .slide: data-background-color="#fff" -->

<img src="media/img/umfrage/Gesamteindruck.png">

------

# Sägen-Prototyp

<p><br><br><br><br><br><br><br><br><br><br><br><br></p>

<!-- .slide: data-background-video="media/video/saw.mp4" data-background-video-loop="true" data-state="state--bg-dark" -->

---

# Zusammenfassung

---

## Probleme von VR-Ökosystemen

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/gatekeeper.png">
    <i>Wächter</i>
  </div>
  <div>
    <img data-src="media/img/downloads-installs.png">
    <i>Installationen</i>
  </div>
  <div>
    <img data-src="media/img/closed-door.png">
    <i>Geschlossen</i>
  </div>
</div>

<!-- NOTES -->
- App stores and corporations control distribution: can take down or block content
- Downloads / installs are a barrier to consumption: small business pages
- Closed ecosystem: proprietary engines, steep learning curves, siloed experiences, fragmentation
- We want VR to be successful, so we want a platform without these points of friction. The answer is WebVR...

---

## WebVR

Eine offene VR-Plattform mit den Vorteilen des **Web**

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/web-is-open.png">
    <i>Offen</i>
  </div>
  <div>
    <img data-src="media/img/web-is-connected.png">
    <i>Verbunden</i>
  </div>
  <div>
    <img data-src="media/img/web-is-instant.png">
    <i>Unmittelbar</i>
  </div>
</div>

<!-- NOTES -->
WebVR is...virtual reality in the browser, powered by the Internet

Open:
- Anyone can publish
- Open source culture with open standards

Connected:
- Traverse worlds

Instant:
- Click a link on Twitter or Weibo, immediate VR experiences
- No installs
- Imagine for long tail experiences: shopping & personal spaces
- Great for long tail bite-sized experiences

Transition:
- Web has advantages that make it the best platform for the people
- Need to act to make it reality, can't wait for VR to bake and crystallize
- Get involved

---

<!-- .slide: data-background="media/img/Unity-Adam.jpg" data-state="state--bg-dark" -->

# Unity

- Performance
- Visuelle Qualität
- einfache Monetarisierung

------

# Vielen Dank
### für die Aufmerksamkeit

------

# Quellen

- https://aframevr.github.io/aframe-presentation-kit/
- Quellen im Literaturverzeichnis der Masterarbeit
