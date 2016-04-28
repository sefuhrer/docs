{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:download: .download}

# Codierung mit Git starten
*Letzte Aktualisierung: 8. Dezember 2015*  

Sie können ein gehostetes Git-Repository erstellen, das für {{site.data.keyword.Bluemix}} automatisch bereitgestellt wird.
Sie können dann den in Ihrer App ausgeführten Code ändern, indem Sie für Änderungen eine Push-Operation an das Git-Repository durchführen. 
{:shortdesc}

1. Um zu beginnen, klicken Sie auf der Übersichtsseite der App auf **GIT HINZUFÜGEN**.   
2. Stellen Sie im Fenster, das geöffnet wird, sicher, dass das Kontrollkästchen zum Auffüllen des Repository mit dem Starteranwendungspaket und zum Aktivieren der Delivery Pipeline (Build & Deploy) aktiviert ist. Das Git-Repository wird erstellt. Wenn Startercode verfügbar ist, wird er in das Repository geladen. Die Anwendung wird zudem vom in {{site.data.keyword.jazzhub}} ausgeführten Service
'Delivery Pipeline' bereitgestellt.   
3. Sie können die App über die Befehlszeile oder die Web-IDE aktualisieren. **Bei Verwendung der Befehlszeile:**
   a. Klonen Sie das Git-Repository aus der Git-URL auf der Übersichtsseite der App.
   b. Aktualisieren Sie den Code in Ihrem bevorzugten Editor.
   c. Übertragen Sie Ihre Änderungen per Push-Operation über die Git-Befehlszeilenschnittstelle.  
	    
   **Bei Verwendung der Web-IDE:**  
   a. Klicken Sie auf der Übersichtsseite der App auf **CODE BEARBEITEN**. Ihr Projekt wird in der Web-IDE geöffnet.   
   b. Nehmen Sie die gewünschten Änderungen vor und führen Sie dann mithilfe der integrierten Git-Unterstützung eine Push-Operation durch.   
		
Die aktualisierte Anwendung wird erneut in {{site.data.keyword.Bluemix_notm}} bereitgestellt.  

Schrittweise Anweisungen finden Sie unter [Set up Git integration and auto-deploy in DevOps Services](https://hub.jazz.net/tutorials/jazzeditor/#git_integration_and_autodeployment).   

## Haben Sie Git hinzugefügt? Testen Sie {{site.data.keyword.Bluemix_notm}} Live Sync.  

Wenn Sie eine Node.js-App erstellen, können Sie mit {{site.data.keyword.Bluemix_notm}} Live Sync die App-Instanz in {{site.data.keyword.Bluemix_notm}} schnell aktualisieren und Ihren Anforderungen entsprechend auf dem Desktop entwickeln.   

Weitere Informationen zu {{site.data.keyword.Bluemix_notm}} Live Sync finden Sie unter [{{site.data.keyword.Bluemix_notm}} Live Sync](../develop/bluemixlive.html). Weitere Details zu den Befehlen finden Sie in der [Dokumentation zur {{site.data.keyword.Bluemix_notm}} Live Sync-Befehlszeilenschnittstelle](../cli/reference/bl/index.html). Informationen zur Verwendung von {{site.data.keyword.Bluemix_notm}} Live Sync mit der Web-IDE finden Sie unter [Live Edit](../develop/bluemixlive.html).  

1. Laden Sie die Befehlszeile 'bl' für {{site.data.keyword.Bluemix_notm}} Live Sync herunter und installieren Sie sie.  

<p>
<a class="xref" href="http://livesyncdownload.ng.bluemix.net/downloads/blive_setup.msi" target="_blank" title="(Wird in einer neuen Registerkarte oder in einem neuen Fenster geöffnet)"><img class="image" src="images/bl_gs_icons_windows_b.png" alt="Schaltfläche zum Herunterladen der Windows-Befehlszeile 'bl'" /> </a>
<a class="xref" href="http://livesyncdownload.ng.bluemix.net/downloads/BluemixLive.pkg" target="_blank" title="(Wird in einer neuen Registerkarte oder in einem neuen Fenster geöffnet)"><img class="image" src="images/bl_gs_icons_mac-osx_b.png" alt="Schaltfläche zum Herunterladen der Mac-Befehlszeile 'bl'" /> </a>
</p>

**Wichtig:** Das Befehlszeilentool 'bl' ist nur für Windows 7 und 8
sowie für Mac OS X ab Version 10.9 verfügbar.  

2. Melden Sie sich in einer Befehlszeile mit dem folgenden Befehl an. Sie werden zur Eingabe Ihrer IBM® ID und des entsprechenden Kennworts aufgefordert. ```
bl login
```

3. Zeigen Sie die Liste der für die {{site.data.keyword.Bluemix_notm}} Live Sync-Synchronisation verfügbaren Projekte an, indem Sie den folgenden Befehl eingeben: ```
bl projects
```
Suchen Sie in der Liste nach dem Projektnamen, der Ihrer Anwendung entspricht. Der Projektname weist das Format
*eigener Alias* | *Name der eigenen Anwendung* auf.
 

4. Synchronisieren Sie die lokale Umgebung mit dem Projekt in {{site.data.keyword.Bluemix_notm}}, indem Sie den folgenden Befehl eingeben. Wenn Sie der Eigner des Projekts sind, müssen Sie für 'projectName' nur den Namen Ihrer eigenen Anwendung angeben.  
<!--- this command needs italicized parameters projectName localDirectory and yellow on 'local' -->
```
bl sync projectName -d localDirectory --verbose
```
Dieser Befehl (und die Synchronisation) wird solange ausgeführt, bis Sie ein "q" eingeben. Mit der Option '--verbose' werden die Protokollierungs- und Statusinformationen angezeigt. Wenn eines der Argumente ein Leerzeichen enthält, müssen Sie den Namen in Anführungszeichen setzen. 5. Stellen Sie in einem weiteren Befehlszeilenfenster in Ihrem lokalen Verzeichnis die Anwendung für {{site.data.keyword.Bluemix_notm}} im Live Edit-Modus bereit, indem Sie den folgenden Befehl eingeben: ```
bl start
```  

Wenn Sie die Dateien in Ihrem lokalen Verzeichnis ändern, werden die Änderungen automatisch in der aktiven Anwendung in {{site.data.keyword.Bluemix_notm}} und im Cloud-Arbeitsbereich des Projekts bereitgestellt. Wenn Sie die Node-Anwendung erneut starten müssen, können Sie den folgenden Befehl verwenden: ```
bl start --restart 
```
