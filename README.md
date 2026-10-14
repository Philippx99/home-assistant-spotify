# Spotify Browser für Home Assistant

Das Add-on zeigt den Spotify-Webplayer in einer Browser-App im Home-Assistant-Seitenmenü. Melde dich dort mit deinem Spotify-Konto an. Chromium gibt seinen Ton auf einen virtuellen PulseAudio-Ausgang aus; das Add-on nimmt diesen Ton auf und stellt ihn als MP3-Livestream bereit. Über **Player verbinden** weist du einen Home-Assistant-Media-Player an, diesen Audiostream abzuspielen.

## Installation

1. Füge dieses Repository unter **Einstellungen → Apps → App-Store → ⋮ → Repositories** hinzu.
2. Installiere **Spotify Browser** und starte das Add-on.
3. Setze in den Add-on-Optionen `stream_base_url` auf eine für den Media-Player erreichbare Adresse, z. B. `http://192.168.1.20:8099`. Port 8099 ist für den Livestream freigegeben.
4. Öffne **Spotify** in der Home-Assistant-Seitenleiste, melde dich an, wähle einen Player und drücke **Player verbinden**. Starte anschließend die Musikwiedergabe im Browser.

## Grenzen

- Der Player muss den Livestream unter `stream_base_url` erreichen und MP3-Livestreams wiedergeben können.
- Spotify kann abhängig von Browser, DRM-Unterstützung, Konto und Region die Wiedergabe einschränken. Ein erfolgreicher Login garantiert nicht, dass der Webplayer in dieser Add-on-Umgebung Audio abspielen kann.
- Der Stream wird live aus dem Browser-Audio erzeugt. Verbinde den Player zuerst und starte danach den Titel; der Stream hat keine Such- oder Rücksprungfunktion.
- Der Browser gibt den Ton über den virtuellen Audioausgang aus und nicht zusätzlich über Computerlautsprecher.
- Der Image-Build benötigt Internetzugriff.

