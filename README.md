# Chessverse Studio

Eine kreative, browserbasierte 3D-Schachplattform – gebaut als statische Website für GitHub Pages.

## Features

- **3D-Schachbrett:** drehbare Three.js-Szene, räumliche Figuren, Beleuchtung und Kamerasteuerung.
- **Schachregeln:** Züge, Schlagzüge, Rochade, Umwandlung, Schach und Matt über chess.js.
- **Figuren-Werkstatt:** eigene PNG-, JPG- oder WebP-Bilder hochladen. Die Silhouette wird im Browser erkannt, als Mesh extrudiert und mit dem Bild texturiert.
- **Eigene Designs:** eine individuelle Figur pro Figurentyp und Farbe; Designs bleiben lokal im Browser speicherbar.
- **Chaos-Modus:** Figuren frei bewegen, ersetzen und zusätzliche Figuren platzieren. Der Modus ist sichtbar gekennzeichnet und wird im Multiplayer mitgeteilt.
- **Peer-to-Peer-Multiplayer:** privaten Raum erstellen, Raum-ID teilen und mit einer zweiten Person spielen.
- **Responsive Oberfläche:** Desktop und Mobilgeräte.

## Start

Einfach `index.html` über einen lokalen Webserver oder GitHub Pages bereitstellen. Für ES-Module, Three.js und PeerJS wird eine Internetverbindung benötigt.

## GitHub Pages

Der Workflow unter `.github/workflows/pages.yml` veröffentlicht die Website bei jedem Push auf `main`. Im Repository muss GitHub Pages einmalig unter **Settings → Pages → Build and deployment → Source → GitHub Actions** aktiviert werden. Danach veröffentlicht der Workflow neue Commits automatisch.

## Hinweise

- Die 2D-zu-3D-Funktion erzeugt eine echte extrudierte 3D-Silhouette mit Bildtextur. Sie ist keine KI-Fotogrammetrie und rekonstruiert keine verdeckten Seiten eines Fotos. Transparente PNG-Bilder liefern die saubersten Ergebnisse.
- Multiplayer verwendet PeerJS für die Peer-to-Peer-Signalisierung und Datenverbindung. Für einen größeren oder produktiven Dienst empfiehlt sich ein eigener PeerServer sowie ein Backend für Konten, Matchmaking und Persistenz.
- Eigene Figuren-Designs werden im Local Storage des jeweiligen Browsers gespeichert. Es gibt aktuell keine Benutzerkonten oder serverseitige Speicherung.
- Der Chaos-Modus ist ein offener Kreativmodus und kein unsichtbarer Cheat in regulären Partien.

## Verwendete Bibliotheken

- [Three.js](https://threejs.org/)
- [chess.js](https://github.com/jhlywa/chess.js)
- [PeerJS](https://peerjs.com/)
