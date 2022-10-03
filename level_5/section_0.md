# Einrichtung

Für die Modifikation von Minecraft muss eine lokale Entwicklungsumgebung eingerichtet werden. Dies sind die gleichen Werkzeuge, die Softwareentwickler jeden Tag benutzen.

## Installieren Sie das Tooling

## MultiMC installieren

MultiMC ist der Minecraft Launcher, den wir in diesem Kurs verwenden werden. Er ermöglicht es uns, jede Version von Minecraft zu starten.

Gehen Sie zu [multimc.org] (https://multimc.org/) und folgen Sie den Download-Anweisungen für Ihr Betriebssystem.

## Installieren Sie das JDK und IntelliJ

Wir haben den Rest der Anleitung für Windows und Macs getrennt. Bitte folgen Sie den Anweisungen für das Betriebssystem, das Sie verwenden:

**[Weiter zu den Windows-Anweisungen](windows_instructions.md)**

**[Gehe zu den Mac-Anweisungen](mac_instructions.md)**

## Download des Beispielprojekts

Gehen Sie zu [github.com/MinecraftU/MinecraftByExample](https://github.com/MinecraftU/MinecraftByExample), klicken Sie auf "Clone or Download" und wählen Sie "Download ZIP".

![](images/section_0/download_project.png)

Entpacken Sie das Projekt an einem logischen Ort, z. B. auf Ihrem Desktop oder in Ihrem Heimatverzeichnis.

## Projekt in IntelliJ einrichten

Diese Anweisungen funktionieren sowohl für Mac als auch für Windows, aber wenn Sie fortgeschrittene Mac-Anweisungen wünschen oder Probleme mit den folgenden Anweisungen haben, [verweisen Sie hier auf die Mac-Befehlszeilenanweisungen](mac_cmd_line_instructions.md).

Öffnen Sie IntelliJ.

Akzeptieren Sie die Standardeinstellungen in den anfänglichen Setup-Bildschirmen.

Wählen Sie im nächsten Bildschirm "Import Project", navigieren Sie zu Ihrem Projektordner und wählen Sie die Datei `build.gradle`.

Warten Sie, bis das Projekt erstellt ist. Ein Bereich im unteren Teil des Fensters wird in etwa so aussehen:

![](images/section_0/gradle_build.png)

Klicken Sie nun auf der rechten Seite des Fensters auf die Registerkarte Gradle. Dann öffnen Sie den Baum Tasks-->forgegradle und doppelklicken auf `setupDecompWorkspace`.

![](images/section_0/gradle_tab.png)

Schließlich doppelklicken Sie auf `runClient`. Dies sollte Minecraft mit allen geladenen Beispielmods starten.
