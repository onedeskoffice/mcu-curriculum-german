# Mac-Befehlszeilen-Anweisungen

## Sich mit der Kommandozeile vertraut machen

Bei den nächsten Aufgaben geht es um die Verwendung der Befehlszeile. Das Programm, das Sie auf dem Mac verwenden werden, heißt Terminal. Sie finden es unter Applications-->Utilities-->Terminal, oder Sie können es mit [spotlight](https://support.apple.com/en-us/HT204014) starten, indem Sie `cmd+space` drücken und dann `Terminal` eingeben.

![](images/section_0/terminal.png)

Wir werden hier nur ein paar Befehle durchgehen. Wenn du mehr Details möchtest, schau dir [dieses Video](https://www.youtube.com/watch?v=5XgBd6rjuDQ "How to use the Command Line | Terminal Basics for Beginners") an.

Erstelle ein neues Verzeichnis in deinem Home-Verzeichnis für deine Minecraft U Level 5 Arbeit und gehe in dieses Verzeichnis. Benutze den `mkdir` Befehl, um die Verzeichnisse zu erstellen und dann den `cd` Befehl, um in dieses Verzeichnis zu wechseln:

``bash
mkdir mcu
cd mcu
mkdir level5
cd level5
```

![](images/section_0/mkdir.png)

### Brew installieren

Nun müssen wir einige Entwicklungssoftware auf unserem Computer installieren. Als erstes müssen wir ein Programm namens Homebrew installieren, das uns wiederum dabei helfen wird, weitere Entwicklungssoftware zu installieren. Befolgen Sie die Anweisungen auf [https://brew.sh/](https://brew.sh/). Die Installation von Homebrew sollte in etwa so aussehen:

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

...aber stellen Sie sicher, dass Sie den Anweisungen auf der Website selbst folgen.

### Git installieren

Jetzt können wir Homebrew's `brew` Befehl benutzen, um andere Anwendungen zu installieren. Die erste, die wir brauchen, ist `git`.

>Git ist ein verteiltes Versionskontrollsystem zur Verfolgung von Änderungen am Quellcode während der Softwareentwicklung

-- [Wikipedia](https://en.wikipedia.org/wiki/Git)

Führen Sie diesen Befehl im Terminal aus:

`brew install git`

### Gradle installieren

Als nächstes brauchen wir Gradle. Gradle hilft uns bei der Erstellung unseres Softwareprojekts.

In den [Gradle-Installationsanweisungen] (https://gradle.org/install/) für Mac steht eigentlich, dass man Homebrew verwenden soll. Um Gradle mit Homebrew zu installieren, führen Sie aus:

`brew install gradle`

## Erstellen Sie eine Kopie des Example Mod GitHub Repository

### Erstellen Sie ein Github-Konto

>[GitHub](https://github.com/) ist ein webbasierter Hosting-Dienst für die Versionskontrolle mit Git

Auf GitHub wird unser Lehrplan gehostet, sowie einige andere Modifizierungscodes, auf die wir in Level 5 Bezug nehmen werden.

Gehen Sie zu GitHub und erstellen Sie ein neues Konto. Sie benötigen dieses Konto, um Kopien des Beispielcodes zu erstellen und um Ihre Änderungen in der Cloud zu speichern.

### Fork the Example Mod Repository

Die ersten Beispiel-Mods, die wir erforschen werden, stammen von [MinecraftByExample] (https://github.com/MinecraftU/MinecraftByExample). Wir beginnen mit dem Forken des Repositorys. Es gibt einen `Fork` Knopf oben rechts in jedem GitHub Repository. Gehe zu MinecraftByExample und klicke `Fork`

![](images/section_0/fork.png)

### Klone deine Kopie der Beispiel-Mods

Als nächstes werden wir das Repository "klonen", was bedeutet, dass wir eine lokale Kopie des Codes auf unserem Computer erstellen, basierend auf der Kopie, die auf GitHub gespeichert ist. Später werden wir lernen, wie wir unsere GitHub-Kopie anhand der Änderungen, die wir auf unserem Computer vornehmen, aktualisieren können.

Zuerst klickst du auf deiner geforkten Kopie des MinecraftByExample Repository auf "Klonen oder Herunterladen". Klicke dann auf den Link "HTTPS verwenden". Klicke dann auf die Schaltfläche "In die Zwischenablage kopieren".

![](images/section_0/clone.png)

`git clone ...`

(Tippen Sie nicht `...`, sondern fügen Sie den Link `https://github.com...`, den Sie gerade in die Zwischenablage kopiert haben, an dieser Stelle ein).

Du musst deinen GitHub-Benutzernamen und dein Passwort eingeben.

Du solltest nun ein MinecraftByExample Verzeichnis in deinem `Level5` Ordner haben. Du kannst diesen Ordner im Finder ansehen, indem du eintippst:

`open .`

## Erstelle die Beispiel-Mods

Benutze in der Kommandozeile des Terminals `cd`, um in den MinecraftByExample Ordner zu wechseln. Dann führe aus:

`./gradlew setupDecompWorkspace`

...dann:

`./gradlew build`

...dann:

`./gradlew runClient`

Dies wird Minecraft mit den geladenen Beispielmods starten.

Starte eine neue kreative Welt. Sobald du in deiner neuen Welt bist, öffne das Kreativ-Inventar und scrolle auf der Registerkarte "Blöcke" nach unten. Du wirst die modifizierten Beispielblöcke sehen:

![](images/section_0/modded_blocks_inventory.png)

Lege einen `MBE01 Block Simple` ab:

![](images/section_0/simple_block_placed.png)

Du hast nun erfolgreich eine Mod von Grund auf mit Beispielcode und Texturen erstellt!

Beenden Sie Minecraft, bevor Sie mit dem nächsten Abschnitt fortfahren.

## Das Projekt für IntelliJ einrichten

Nun müssen wir das Projekt für ItelliJ konfigurieren. Führen Sie von der Kommandozeile aus:

`./gradlew idea`

Öffnen Sie dann die Datei `MinecraftByExample.ipr` im Finder.

Ein kleines Benachrichtigungsfenster wird unten rechts erscheinen. Klicken Sie auf den Link "Gradle-Projekt importieren" in diesem Benachrichtigungsfenster.

![](images/section_0/import_gradle.png)

Am unteren Rand des Fensters erscheint ein Fenster und nach ein paar Sekunden wird der Build abgeschlossen:

![](images/section_0/gradle_build.png)

Als nächstes müssen wir den Debug-Build konfigurieren.

Beenden Sie IntelliJ und gehen Sie zurück zu Ihrem Terminal. Ausführen:

`./gradlew genIntellijRuns`

Starten Sie IntelliJ neu. Im oberen Teil des Fensters befindet sich die Run-Symbolleiste:

![](images/section_0/run_bar.png)

Klicken Sie auf die Schaltfläche run. (Der, der wie ein Play-Button aussieht.) Wenn ein Fenster mit dem Titel "edit configuration" erscheint, wähle im Dropdown-Menü "Use classpath of module" "MinecraftByExample.main".

![](images/section_0/classpath.png)

Dies wird Minecraft mit den geladenen Mods starten, genau wie bei der Ausführung von `./gradlew runClient` zuvor.

Sie sind nun bereit, diese Beispiel-Mods zu modifizieren und in IntelliJ auszuführen und zu debuggen.
