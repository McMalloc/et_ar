Framework für Augmentierung des Emerging Technologies Exponats, Werkschau 2018/2 Magdeburg. Funktioniert laut Entwickler der ar.js-Bibliothek für iOS erst ab Version 11 wegen Beschränkungen in der webRTC-Implementierung von Apple.

# Marker

1. Marker [hier](https://webxr.io/marker-generator/) vorbereiten. Das Bild muss ohne den schwarzen Rand hochgeladen werden und sollte als Hintergrundfarbe `#f0f0f0` haben. Es sollte außerdem klare Linien enthalten, z.B. ist Text sehr gut geeignet.
2. Die `.patt`-Datei herunter laden und in den `/patterns`-Ordner schieben.
3. Die Bilddatei heurnterladen (diese ist jetzt mit schwarzem Rand versehen) und in den `/markers`-Ordner verschieben.

# 3D-Modell

1. Mögliche Formate sind FBX und glTF. glTF ist das neue Standardformate für 3D-Inhalte im Web, [hier](https://github.com/KhronosGroup/glTF-Blender-Exporter) gibt es beispielsweise einen Exporter für Blender.
2. Die 3D-Dateien in einem eigenen Ordner unter `/scenes` zusammenfassen.

# Integrieren

Siehe Beispiele in `index.html`. Grundsätzliche Vorgehensweise:

1. `<a-marker type="pattern" url="patterns/mein-pattern.patt">`-Tag für den Marker anlegen und die URL entsprechend abändern.
2. Im Tag kommt dann der gewünschte 3D-Inhalt, z.B. `<a-gltf-model>` mit entsprechendem `src`-Attribut. Diese Komponenten-Tags haben verschiedene Attribute wie `position`, `scale` und `rotation`, die relativ zum Marker zu verstehen sind.

# Inhalte

* Ein HUD, also eine UI, die sich stets mit der Kamera bewegt, kann durch Komponenten unter dem `<a-camera>`-Tag realisiert werden. Diese Komponenten liegen starr auf dem Bildschirm.
* Texttafeln, Bilder etc sind prinzipiell auch glTF- oder FBX-Modelle, eben texturierte Ebenen.
* [Videos](https://aframe.io/docs/0.8.0/primitives/a-video.html) und [Sound](https://aframe.io/docs/0.8.0/components/sound.html) sind grundsätzlich auch möglich. Bitte dazu die Anleitungen und vor allem Hinweise in den verlinkten Dokuabschnitten beachten.

