{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

#{{site.data.keyword.Bluemix_notm}} Local
{: #local}
*Letzte Aktualisierung: 15. Januar 2016*

{{site.data.keyword.Bluemix}} Local bringt das Leistungsstärke und Beweglichkeit (der Geschäftsabläufe) der cloudbasierten {{site.data.keyword.Bluemix_notm}}-Plattform in Ihr Rechenzentrum. Mit {{site.data.keyword.Bluemix_notm}} Local können Sie die hochsensiblen Verarbeitungsprozesse hinter der Firewall des Unternehmens schützen und gleichzeitig eine sichere Verbindung und Synchronisation mit {{site.data.keyword.Bluemix_notm}} Public gewährleisten.
{:shortdesc}

IBM® verwendet Cloudoperationen als Service zum Überwachen und Verwalten Ihrer Umgebung, damit Sie sich auf das Erstellen von Apps und Services konzentrieren können, die in dieser Umgebung ausgeführt werden. IBM führt zudem Plattformaktualisierungen aus, während Sie sich um Ihre Geschäftsabläufe kümmern.

{{site.data.keyword.Bluemix_notm}} Local umfasst einen privaten, syndizierten Katalog, in dem die lokalen Services angezeigt werden, die ausschließlich Ihnen zur Verfügung stehen. Er umfasst außerdem zusätzliche Services, die aus {{site.data.keyword.Bluemix_notm}} Public syndiziert werden und die Sie verwenden können. Der syndizierte Katalog bietet die Funktion zum Erstellen von Hybridanwendungen, die aus öffentlichen und privaten Services bestehen. Sie können auf der Basis Ihrer Kriterien für Datenschutz und Sicherheit entscheiden, welche öffentlichen Services die Anforderungen Ihres Unternehmens erfüllen.

{{site.data.keyword.Bluemix_notm}} Local befindet sich auf einer virtuellen Maschine hinter der Firewall Ihres Unternehmens. Das bedeutet, dass Ihnen eine besonders leistungsfähige und sichere Cloudinfrastruktur zur Verfügung steht. Mit seiner Relay-Technologie installiert und verwaltet IBM {{site.data.keyword.Bluemix_notm}} Local in Ihrem Rechenzentrum und führt eine Fernüberwachung durch.

![Übersicht über {{site.data.keyword.Bluemix_notm}} Local](images/bluemixlocalarchitecture.png "Übersicht über Bluemix Local")

*Abbildung 1. Detaillierte Übersicht über {{site.data.keyword.Bluemix_notm}} Local*

{{site.data.keyword.Bluemix_notm}} Local-Umgebungen besitzen in Hinblick auf die Betriebssicherheit dieselben Sicherheitsstandards wie die öffentliche {{site.data.keyword.Bluemix_notm}}-Plattform. Sie stellen die Hardware und Infrastruktur bereit und erhalten so die Kontrolle über die Infrastruktur und physische Sicherheit. Der Zugriff von Entwicklern auf die lokale {{site.data.keyword.Bluemix_notm}}-Plattform wird durch Ihre LDAP-Richtlinien gesteuert, die bei der Einrichtung Ihrer Umgebung durch das {{site.data.keyword.Bluemix_notm}}-Team konfiguriert werden können. Sie können innerhalb der lokalen Umgebung über die Administrationskonsole Benutzerrollen und Berechtigungen verwalten.

{{site.data.keyword.Bluemix_notm}} Local wird mit vollständig integrierten {{site.data.keyword.Bluemix_notm}}-Laufzeiten und 64 GB Rechenspeicher ausgeliefert.

Des Weiteren gibt es eine Reihe verfügbarer Services für {{site.data.keyword.Bluemix_notm}} Local.

| **Typ** | **Name** | **Beschreibung** |    
|----------|----------|-----------------|
|Inbegriffen | {{site.data.keyword.Bluemix_notm}}-Laufzeiten | Machen Sie mit Laufzeiten Ihre App schnell betriebsbereit, ohne VMs und Betriebssysteme einrichten und verwalten zu müssen. Alle {{site.data.keyword.Bluemix_notm}}-Laufzeiten stehen Ihnen zur Verwendung in Ihrer {{site.data.keyword.Bluemix_notm}} Local-Instanz zur Verfügung.|
|Inbegriffen | {{site.data.keyword.autoscaling}}| Dynamisches Erhöhen oder Verringern der Rechenleistung Ihrer Anwendung basierend auf Richtlinien. Mit diesem Service können Sie Ihre {{site.data.keyword.Bluemix}} Local-Umgebung unbegrenzt nutzen.|
|Optional |{{site.data.keyword.datacshort}}| Dieser Service bietet ein speicherinternes Datengitter, durch das Szenarios mit verteiltem Caching für Ihre Apps unterstützt werden. Umfasst 50 GB speicherinternen Cache. |
|Optional | {{site.data.keyword.APIM}} | Verwenden Sie den {{site.data.keyword.APIMfull}}-Service zum Erstellen, Verwalten und Mitteilen von APIs. Sie können mit einer Proxy-URL oder durch Zusammenstellen von Daten aus HTTP-Datenquellen neue APIs mit Ressourcen importieren. Die Verwendung des {{site.data.keyword.APIM}}-Service bietet den Vorteil, dass Sie steuern können, wie Ihre APIs genutzt werden. |

*Tabelle 1. Lokale Services*

### Relay

Relay ist eine in {{site.data.keyword.Bluemix_notm}} Local integrierte Zustellungsfunktion, mit der IBM automatisch und konsistent die neuesten Aktualisierungen für alle lokalen Implementierungen bereitstellt und Sie somit stets ein aktuelles und sicheres System haben. Relay erreicht eine sichere Konnektivität mittels eines offenen VPN-Tunnels mit ausgehender SSL, der von der lokalen, virtuellen Konzeptionsmaschine stammt. Dabei werden die entsprechenden Zertifikate der einzelnen {{site.data.keyword.Bluemix_notm}} Local-Instanzen verwendet. Alle ersten {{site.data.keyword.Bluemix_notm}}-Releases sind in der virtuellen Konzeptionsmaschine verfügbar, die auch als Automatisierungsagentenmaschine für Bereitstellungen und Aktualisierungen fungiert. Die SSL-Verbindung stammt von der virtuellen Konzeptionsmaschine; sobald eine sichere Verbindung zum Automation Server von {{site.data.keyword.Bluemix_notm}} eingerichtet wurde, können wir die Aktualität und Konsistenz von {{site.data.keyword.Bluemix_notm}}-Releases prüfen und mit der Bereitstellung von Aktualisierungen beginnen.

Bei dem Datenverkehr über diesen Tunnel handelt es sich um eine Automatisierung zum Bereitstellen und Verwalten der Plattform, Rechenressourcen und Services für Ihre Instanz. Der eingehende Web-Port 443 wird für diese Verbindung verwendet. Auf Relay kann nur von Automatisierungsagenten zugegriffen werden. IBM nutzt die Relay-Funktionalität, um Plattformaktualisierungen über einen konsistenten Test- und Validierungsprozess bereitzustellen und so sicherzustellen, dass alle Bereitstellungen, die per Push-Operation an Ihre lokalen Umgebungen übertragen werden, stabil und sicher sind.

Als Administrator haben Sie einen umfassenden Überblick über die Umgebung für die Verwaltung von Vorfällen, Problemen, der Kapazität und der Sicherheit. Administratoren greifen über die Administrationskonsole auf die Informationen zu ihrer Umgebung zu. Dank Relay-Technologie enthält die Administrationskonsole immer die aktuellen Daten. Weitere Informationen zum Benutzerzugriff, zu Sicherheitsprotokollen, zur Kontrolle des syndizierten Katalogs und zur Kommunikation bezüglich Aktualisierungen und Problemlösungen finden Sie unter [{{site.data.keyword.Bluemix_notm}} Local und {{site.data.keyword.Bluemix_notm}} Dedicated verwalten](../admin/index.html#mng).

##{{site.data.keyword.Bluemix_notm}} Local-Instanz einrichten
{: #setuplocal}

{{site.data.keyword.Bluemix_notm}} Local wurde konzipiert, um eine private Version des Produktangebots {{site.data.keyword.Bluemix_notm}} Public bereitzustellen, die auf Ihrer eigenen, von Ihnen verwalteten Hardware gehostet ist. Sie können {{site.data.keyword.Bluemix_notm}}-Services und -Laufzeiten verwenden, um Ihre Datenverarbeitungsanforderungen in einer sicheren, vom Kunden gehosteten und verwalteten Cloudumgebung zu unterstützen.

IBM bietet Ihnen über eine kennwortgesicherte Anmeldung Zugriff auf {{site.data.keyword.Bluemix_notm}} Local. Sie können auf die Services, Laufzeiten und zugehörigen Ressourcen zugreifen und {{site.data.keyword.Bluemix_notm}}-Apps bereitstellen und entfernen. Überprüfen Sie die folgenden Schritte zur Arbeit mit Ihrem IBM Ansprechpartner zum Einrichten Ihrer lokalen Instanz von {{site.data.keyword.Bluemix_notm}}.

Gehen Sie wie folgt vor, um Ihre private Version von {{site.data.keyword.Bluemix_notm}} einzurichten:

<ol>
<li>Prüfen Sie die <a href="index.html#localinfra">Infrastrukturanforderungen für {{site.data.keyword.Bluemix_notm}} Local</a> für die Einrichtung der lokalen Instanz.</li>
<li>Wenden Sie sich an Ihren zugewiesenen IBM Kundenbeauftragten oder wenden Sie sich an <a href="https://console.ng.bluemix.net/?direct=classic/#/contactUs/cloudOEPaneId=contactUs" target="_blank">{{site.data.keyword.Bluemix_notm}}</a>, um mit der Arbeit zu beginnen.</li>
<li>Erstellen Sie Ihre Vereinbarung zu {{site.data.keyword.Bluemix_notm}} Local einschließlich Meilensteindaten für die Bereitstellung mit IBM.
<ol type="a">
	<li>Erarbeiten Sie mit IBM Ihre Gebühren für Ihre {{site.data.keyword.Bluemix_notm}} Local-Instanz. Die monatlich fällige Gebühr basiert auf den lokalen Services, die Sie nutzen möchten. Hinzu kommt ein Abonnement für alle {{site.data.keyword.Bluemix_notm}} Public-Services. Sie erhalten dann eine Rechnung für alle Nutzungen, die über die Abonnementvereinbarung hinausgehen.</li>
	<li>Ermitteln Sie die Fristen für die einzelnen Einrichtungsphasen Ihrer {{site.data.keyword.Bluemix_notm}} Local-Instanz.</li>
	</ol>
	</li>
<li>Nach dem Erstellen der Plattform und des Kontos ermitteln Sie die Personen in Ihrer Organisation für die Rollen, die benötigt werden, um Ihre lokale Instanz betriebsbereit zu machen. Weitere Informationen zu den Rollen, die Sie zuweisen, finden Sie unter <a href="index.html#rolesresponsibilities" target="_blank">{{site.data.keyword.Bluemix_notm}}</a> Local-Rollen und -Zuständigkeiten. </li>
<li>Sie stellen die Hardware bereit und IBM hilft Ihnen beim Definieren und Festlegen der Netzkonnektivität zwischen Ihrem Unternehmensnetz und Ihrer {{site.data.keyword.Bluemix_notm}} Local-Instanz. Weitere Informationen zu Infrastrukturanforderungen finden Sie unter <a href="index.html#localinfra">Infrastrukturanforderungen für {{site.data.keyword.Bluemix_notm}} Local</a>.
<ol type="a">
	<li>IBM konfiguriert den Netzzugriff und LDAP Ihren Angaben entsprechend. Die von Ihnen bestimmten Ansprechpartner erhalten Verwaltungszugriff. Sie müssen auch einen Ansprechpartner für die Unterstützung und die Abrechnung bestimmen.</li>
	<li>IBM richtet in Ihrer lokalen Umgebung einen syndizierten Katalog ein, um Ihnen Ihre lokalen Services und viele der öffentlichen {{site.data.keyword.Bluemix_notm}}-Services zu zeigen.</li>
	<li>Sie überprüfen die Netz- und Firewallkonfiguration sowie den LDAP-Endpunkt und -Zugriff.</li>
	</ol>
</li>
</ol>

Für die Erstbereitstellung und Erstkonfiguration Ihrer Umgebung können Sie einen Prozess wie in der folgenden Liste dargestellt erwarten. Details dazu, wer für die einzelnen Tasks verantwortlich ist, finden Sie unter [Rollen und Zuständigkeiten](../local/index.html#rolesresponsibilities).

<ol>
<li>Sie stellen die VMware-Konfiguration bereit, die die Spezifikationen für Rechenressourcen, Netzbetrieb und Speicher erfüllt. Weitere Informationen zu den Infrastrukturanforderungen finden Sie unter <a href="../local/index.html#localinfra">Infrastrukturanforderungen für {{site.data.keyword.Bluemix_notm}} Local</a>.</li>
<li>Sie stellen die Berechtigungsnachweise für den vCenter-Cluster bereit, die von der virtuellen Konzeptionsmaschine verwendet werden sollen. Sie müssen die folgenden Informationen angeben:
<ul>
<li>Name des VMware-Clusters</li>
<li>Berechtigungsnachweise für den vCenter-Cluster aus Benutzer-ID und Kennwort</li>
<li>Datenspeichername bzw. -namen (LUN-Name für den Speicher)</li>
<li>VLAN ID-/VMware-Portgruppe</li>
<li>Name für den Ressourcenpool</li>
</ul>
</li>
<li>Sie und IBM arbeiten zusammen, um die Berechtigungsnachweise zu validieren, die Sie in der vorherigen Task bereitgestellt haben.</li>
<li>Sie stellen sieben IP-Adressen in Ihrem Netz bereit. Wenn Sie einen gesicherten Web-Proxy haben, um ausgehenden Zugriff auf das Internet für interne {{site.data.keyword.Bluemix_notm}}-Komponenten zuzulassen, müssen Sie die Berechtigungsnachweise für die entsprechende Verbindung bereitstellen.
<p>**Hinweis:** Wenn Ihr Web-Proxy nicht geschützt wird, brauchen Sie die Berechtigungsnachweise nicht bereitzustellen. Beachten Sie außerdem, dass nicht alle {{site.data.keyword.Bluemix_notm}} Local-Kunden einen Web-Proxy verwenden.</p></li>
<li>IBM stellt eine Whitelist von URLs bereit, die über Ihren Web-Proxy zugelassen werden müssen, bevor die Bereitstellung beginnt.</li>
<li>Sie geben die Domänennamen für die Bereitstellung und die gewünschten IDs an. Sie erhalten zwei teilweise definierte Domänen, wenn Sie Ihre lokale Instanz einrichten, und wählen das Präfix für die beiden Domänen aus. Beispiel: Sie wählen das Präfix für <code>*mycompany*.bluemix.net</code> und <code>*mycompany*.mybluemix.net</code> aus. Anschließend können Sie auch einen vollständigen Domänennamen auswählen, um eine angepasste Domäne zu erstellen.
<p>Sie können so viele angepasste Domänen wählen, wie Sie möchten. Sie sind jedoch für die Zertifikate für die angepassten Domänen verantwortlich. Informationen zur Erstellung einer angepassten Domäne finden Sie unter <a href="../manageapps/updapps.html#domain">Angepasste Domäne erstellen und verwenden</a>.</p></li>
<li>Sie wählen die Technologie (IPSec- oder OpenVPN-Tunnel) aus, die zur Konfiguration von Relay für die Rückverbindung zum IBM Operations Center verwendet wird.</li>
<li>IBM installiert und startet die virtuelle Konzeptionsmaschine im {{site.data.keyword.Bluemix_notm}}-Cluster. Wenn Sie ein eigenes VMware bereitstellen, wird Ihr Kundenvertreter von einem IBM Ansprechpartner bei der Ausführung dieser Task unterstützt.</li>
<li>IBM konfiguriert Relay für die Kommunikation mit dem IBM Operations Center.</li>
<li>Das Repository für die virtuelle Konzeptionsmaschine extrahiert die aktualisierten Buildartefakte.</li>
<li>Sie stellen IBM die Berechtigungsnachweise für die Verbindung zur unternehmenseigenen LDAP-Verzeichnisinstanz zur Verfügung.</li>
<li>IBM arbeitet mit einer Automatisierung, um die zentrale {{site.data.keyword.Bluemix_notm}}-Plattform bereitzustellen.</li>
<li>IBM stellt die zentrale Plattform bereit, die elastische Laufzeiten, Konsolen, Verwaltungsfunktionen und Überwachung umfasst.</li>
<li>IBM konfiguriert Ihren Verwaltungszugriff auf die Umgebung.</li>
<li>IBM verlinkt Ihren syndizierten Katalog aus Ihrer lokalen Bereitstellung mit einer öffentlichen {{site.data.keyword.Bluemix_notm}}-Instanz für die Verwendung öffentlicher Services. Eine Gruppe öffentlicher Services ist standardmäßig in Ihrer lokalen Instanz verfügbar. Sie können die Verwaltungsseite für die Katalogverwaltung verwenden, um die Services für Ihre lokale Instanz zu aktivieren oder zu inaktivieren.</li>
<li>Sie können mit der Verwendung Ihrer lokalen Instanz beginnen, die vom IBM Operationsteam überwacht wird, um auf Alerts zu reagieren.</li>
</ol>

Nach der Einrichtung Ihrer {{site.data.keyword.Bluemix_notm}}-Instanz können Sie die Ihre {{site.data.keyword.Bluemix_notm}}-Instanz über die Verwaltungsseite ('Administration') überwachen und verwalten. Weitere Informationen finden Sie unter [{{site.data.keyword.Bluemix_notm}} Local und Dedicated verwalten](../administer/index.html#mng). Weitere Informationen zu Upgrades und Wartung finden Sie unter [Lokale Instanz warten](index.html#maintainlocal).

##Rollen und Zuständigkeiten
{: #rolesresponsibilities}

Wenn Sie ein {{site.data.keyword.Bluemix_notm}} Local-Konto einrichten, ermitteln Sie die Personen in Ihrer Organisation für die Rollen, die benötigt werden, um Ihre lokale Instanz betriebsbereit zu machen.

###Rollen

In der folgenden Liste sind die Kundenrollen und -zuständigkeiten enthalten, die Sie zuweisen:

<dl>
<dt>**Zentraler Ansprechpartner für das Beschaffungswesen**</dt>
<dd>Arbeitet mit dem IBM Ansprechpartner zusammen an der Einrichtung
Ihrer {{site.data.keyword.Bluemix_notm}} Local-Umgebung. Dazu gehört
das Ermitteln geeigneter Personen in Ihrer Organisation für die Arbeit an den einzelnen Aspekten des Projekts. Die Person, die dieser Rolle zugewiesen ist, überwacht die Musterauswahl, die geschäftlichen Vereinbarungen und die Regelung für den Zugang zu Kundenressourcen. Dieser zentrale Ansprechpartner ist der allgemeine Ansprechpartner für die Einrichtung der lokalen Instanz.</dd>
<dt>**Compliance-Manager**</dt>
<dd>Arbeitet mit dem IBM Ansprechpartner zusammen, um eine Topologie
und eine Bereitstellungsoption auszuwählen, die Ihren Sicherheitsanforderungen entsprechen. Die Person, die dieser Rolle zugewiesen ist, legt gemeinsam mit dem IBM Compliance-Berater fest, mit welchen Implementierungsmustern die Compliance-Ziele erreicht werden. </dd>
<dt>**Netzspezialist**</dt>
<dd>Arbeitet mit dem IBM Ansprechpartner zusammen an den Netzplänen für die {{site.data.keyword.Bluemix_notm}}-Bereitstellung. Die Person, die dieser Rolle zugewiesen ist, überprüft die von IBM vorausgesetzten Netzspezifikationen und arbeitet gemeinsam mit IBM an einem Implementierungsplan. Am Ende der Installations- und Verifizierungsphase prüft die Person, die dieser Rolle zugewiesen ist, dass die Netzkonfiguration im Einklang mit den Unternehmensstandards ist. </dd>
<dt>**Zentraler DevOps-Ansprechpartner**</dt>
<dd>Arbeitet mit dem IBM Ansprechpartner zusammen, um die für die {{site.data.keyword.Bluemix_notm}}-Plattform, -Services und -Laufzeiten benötigten Wartungsaktualisierungen zu planen und anzuwenden. Die Person, die dieser Rolle zugewiesen ist, arbeitet auch mit dem
IBM Ansprechpartner an der Konfiguration Ihrer {{site.data.keyword.Bluemix_notm}} Local-Instanz. </dd>
<dt>**IaaS-Spezialist**</dt>
<dd>Arbeitet mit den IBM Ansprechpartnern an dem Bereitstellungsplan für VMware. Typischerweise handelt es sich hierbei um einen VMware-Administrator im Rechenzentrum. Die Person, die dieser Rolle zugewiesen ist, überprüft die <a href="../local/index.html#localinfra">Infrastrukturanforderungen für {{site.data.keyword.Bluemix_notm}} Local</a> und arbeitet gemeinsam mit IBM an einem Implementierungsplan. Am Ende der Installationsphase prüft die Person, die dieser Rolle zugewiesen ist, dass die Implementierung im Einklang mit den Unternehmensstandards auf der IaaS-Ebene ist. </dd>
</dl>

Ihre Ansprechpartner beim Kunden arbeiten mit einem dedizierten Client Success Manager (CSM) und anderen IBM Spezialisten zusammen, um sicherzustellen, dass Sie immer die benötigte Unterstützung erhalten. Der CSM steht Ihnen 6 Monate lang kostenlos zur Verfügung. Er führt die folgenden Tasks aus:

<ul>
<li>Technische Koordination zwischen Ihnen und IBM.</li>
<li>Koordination von Aktualisierungen, Upgrades, kompetenter Hilfe von IBM und Erstaktivierung durch einen {{site.data.keyword.Bluemix_notm}}-Supportmitarbeiter.</li>
<li>Bereitstellen von Informationen zu den verfügbaren Typen von Support.</li>
<li>Ggf. Fungieren als erster Eskalationspunkt.</li>
</ul>

Das {{site.data.keyword.Bluemix_notm}}-Support- und -Operationsteam, das gemeinsam mit Ihnen an der {{site.data.keyword.Bluemix_notm}}-Instanz arbeitet, kann auf die lokale Umgebung zugreifen, tut dies aber nur unter den folgenden Umständen.

<ul>
<li>Zum Antworten auf Alerts und zum Durchführen einer Betriebswartung</li>
<li>Zum Reproduzieren eines Problems, das in einem Supportticket berichtet wurde</li>
</ul>

###Zuständigkeiten

Von der Einrichtung Ihrer Umgebung bis hin zur kontinuierlichen Wartung müssen von Ihnen und von IBM eine Vielfalt von Tasks abgeschlossen werden. Die folgenden Tabellen beschreiben grob die erforderlichen Tasks und die Eigner zum Abschließen der Task in den Phasen der Konzeption, des Fortschritts und der Fertigstellung.

In der Konzeptionsphase wird die {{site.data.keyword.Bluemix_notm}} Local-Umgebung eingerichtet. Zu diesem Zeitpunkt haben Sie sich bereits mit den [Infrastrukturanforderungen für Local](../local/index.html#localinfra) vertraut gemacht. Die primären Ziele dieser Phase sind unter anderem:

- Überprüfung der finanziellen Vereinbarung und Festlegung der Meilensteindaten für die Bereitstellung.
- Erstellung der {{site.data.keyword.Bluemix_notm}}-Plattform und Bereitstellung von Zugriff auf Laufzeiten und Services.
- Definition und Einrichtung der Netzkonnektivität zwischen Ihrem Unternehmensnetz und {{site.data.keyword.Bluemix_notm}}-Operationen.
- Ermittlung und Zuweisung von Rollen für Ihr Verwaltungsteam.

*Tabelle 1. Tasks in der Konzeptionsphase*

| **Task** | **Taskdetails** | **Zuständiges Team** |
|----------|------------------|-----------------------|
|Festlegen von Konformitätsstandards | Ermitteln Sie Behörden-, Branchen- und proprietäre Unternehmensstandards, die für die Umgebung erforderlich sind. | Kunde |
|Erstellen eines Sicherheits- und Konformitätsintegrationsplans | Erstellen Sie einen Sicherheits- und Integrationsplan, der Kosten, Planung und Ressourcen einbezieht, die für die Einhaltung von Sicherheitsbestimmungen erforderlich sind. | IBM |
|Genehmigen des Konformitätsplans | Genehmigen Sie den Konformitätsplan. | Kunde |
|Dimensionieren der Umgebung |  	Dimensionieren Sie die Umgebung auf der Basis von vordefinierten Optionen, die die Hochverfügbarkeits- und Disaster-Recovery-Ziele sowie den ursprünglichen DEA und die Servicebereitstellung berücksichtigen, die zur Unterstützung der mit der Plattform erstellten Apps erforderlich sind. Gemeinsam mit IBM definieren Sie beispielsweise, welche Datenbanken erforderlich sind, welche Services im syndizierten Katalog des Benutzers angeboten werden und vieles mehr. | IBM und Kunde |
|Auswählen der Architektur | Wählen Sie die Architektur auf der Basis vordefinierter Optionen aus, die Hochverfügbarkeits- und Disaster-Recovery-Anforderungen berücksichtigen. | IBM |
|Definieren von Disaster-Recovery-Zielen | Definieren Sie die Disaster-Recovery-Anforderungen für die Umgebung. | Kunde |
|Erstellen eines Disaster-Recovery-Plans | Konsultieren und definieren Sie den Disaster-Recovery-Plan. IBM erstellt ein Disaster-Recovery-Modell und berät mit Ihnen, wo Sie Feedback bereitstellen und den Plan genehmigen. | IBM und Kunde |
|Erstellen eines Sicherungs- und Wiederherstellungsplans | Erstellen Sie einen Sicherungs- und Wiederherstellungsplan, der die Häufigkeit und die Anforderungen einer zentralen bzw. dezentralen Verteilung der Sicherung definiert. IBM sichert Fabric-Komponenten, IBM Services, Servicemetadaten wie Benutzerrollen und vieles mehr. Sie sichern alle anwendungsspezifischen Daten, für die Sie verantwortlich sind. | IBM und Kunde |
|Angeben von Tools für Ereigniserkennung und Problembestimmung | Geben Sie IBM Tools und Tools von Drittanbietern für die Ereigniserkennung und Problembestimmung auf der {{site.data.keyword.Bluemix_notm}}-Plattformebene an. | IBM |
|Definieren eines Eskalationsplans | Definieren Sie den Eskalationsplan zur Klassifizierung und Auflösung von Ereignissen, die von Überwachungskomponenten erkannt werden. | IBM |
|Unterzeichnen von Infrastruktur-, Plattform- und Supportvereinbarungen | Unterzeichnen Sie die Abonnementvereinbarung, einschließlich der finanziellen Vertragsbedingungen für die Umgebung. Unterzeichnen Sie eine Vereinbarung zur Netz- und Sicherheitsüberwachung. Unterzeichnen Sie ein Supportabonnement. | Kunde |
|Beschaffen einer Umgebung | Beschaffen Sie Rechen-, Netz- und Speicherressourcen. Weitere Informationen zu den Infrastrukturanforderungen für die Umgebung finden Sie unter [ Local-Infrastrukturanforderungen](../local/index.html#localinfra).  | Kunde |
|Installieren einer VPN-Lösung | Installieren Sie eine bidirektionale VPN-Lösung. | IBM |
|Installieren von Fabric-, Anwendungs- sowie Überwachungs- und Verwaltungskomponenten | Installieren, konfigurieren und überprüfen Sie Fabric-Komponenten wie BOSH Director, Cloud-Controller, Statusmanager, Messaging, Routers, DEAs und Service-Provider sowie die Überwachungskomponenten, die im Eskalations- und Problemerkennungsplan definiert sind. | IBM |
|Installieren und Konfigurieren von Sicherheitskomponenten | Installieren und konfigurieren Sie Sicherheitskomponenten, die in den Überwachungs- und Eskalationsplan eingebunden sind, darunter IBM QRadar, Vault für Berechtigungsnachweise, Abwehrsystem gegen Angriffe von außen, IBM BigFix und IBM Security Privileged Identity Management. | IBM |
|Konfigurieren eines Anmeldungsservers | Konfigurieren Sie den Anmeldungsserver für die Verwendung mit dem unternehmensweiten LDAP. | IBM |
|Installieren und Konfigurieren von angepassten Komponenten |  	Installieren und konfigurieren Sie angepasste Komponenten, die sich außerhalb des Geltungsbereichs des {{site.data.keyword.Bluemix_notm}}-Produkts und der -Services befinden. | Kunde |
|Verbinden einer {{site.data.keyword.Bluemix_notm}}-Pipeline | Verbinden Sie eine {{site.data.keyword.Bluemix_notm}}-Pipeline für kontinuierliche Integration und Bereitstellung mit IBM Repositorys. | IBM |
|Anpassen externer Lösungskomponenten | Passen Sie Lastausgleichsfunktionen für Disaster-Recovery-Szenarios an. | Kunde |
|Verfolgen des Status von Sicherheits-, Konformitäts- und Prüfungsmaßnahmen  | Verfolgen Sie den Status bis zu dem Zeitpunkt, an dem alle Tools und Prozesse zum Erzielen der gewünschten Konformität vorhanden und einsatzbereit sind. | Kunde |
|Überprüfen der physischen Infrastruktur | Überprüfen Sie die Orte, an denen die Lösungskomponenten für Bedrohungen gehostet werden, und überprüfen Sie die Sicherheitsmaßnahmen zum Schutz des Rechenzentrums. | Kunde |
|Untersuchen der Überwachungssoftware | Untersuchen Sie Überwachungs- und Verwaltungskomponenten, wie im Eskalations- und Problembestimmungsplan definiert. | Kunde |
|Untersuchen des Betriebssystems | Stellen Sie sicher, dass das Betriebssystemimage Konfomitätsstandards entspricht. IBM stellt Zugriff auf das Betriebssystemimage bereit. | IBM und Kunde |

Als nächstes folgt die Fortschrittsphase. Die Fortschrittsphase beschreibt die laufende, interaktive Beziehung zwischen Ihnen und IBM. Die primären Ziele dieser Phase sind unter anderem:

- Überprüfen der Kapazität und Koordinieren von erforderlichen Anpassungen.
- Überprüfen von Wartungs- und Plattformverbesserungen.
- Koordinieren der Aktivitäten für Fehlerbehebung und Ursachenanalyse.

*Tabelle 2. Tasks in der Fortschrittsphase*

| **Task** | **Taskdetails** | **Zuständiges Team** |
|----------|------------------|-----------------------|
|Überprüfen von wöchentlichen Kapazitätsberichten | Überprüfen Sie die wöchentlichen Kapazitätsberichte und ergreifen Sie ggf. Korrekturmaßnahmen. | Kunde |
|Erstellen von monatlichen Projektionen | Erfassen Sie Informationen und erstellen Sie eine monatliche Projektion von Kapazität und Nutzung. | IBM und Kunde |
|Überprüfen von Kapazitätsprojektionen | Überprüfen Sie die Kapazitätsprojektionen hinsichtlich externer Ereignisse, die sich sowohl auf die Kapazität als auch auf geplante neue Implementierungen von Apps auswirken können. Arbeiten Sie gemeinsam mit IBM an der Überprüfung der Projektionen und der entsprechenden Planung. | IBM und Kunde |
|Anpassen der Kapazität |  Fügen Sie Kapazität hinzu oder entfernen Sie Kapazität nach Bedarf. | IBM |
|Veröffentlichen zukünftiger Aktualisierungen und Wartungen | Erstellen Sie eine Dokumentation für die erforderliche Wartung von IBM Komponenten. | IBM |
|Durchführen einer Wartung | Planen Sie gemeinsam mit IBM die erforderliche Wartung in einem 30-tägigen Zeitraum. Sie können innerhalb des 30-tägigen Zeitraums Daten angeben, an denen keine Arbeit ausgeführt wird, und IBM bemüht sich, die Wartung entsprechend zu planen. | IBM und Kunde |
|Adressieren von Bereitstellungsfehlern | Beheben Sie ggf. auftretende Bereitstellungsfehler für vom Kunden erstellte Services, die im Katalog implementiert werden. | IBM |
|Durchführen von Netz- und IP-Scans | Führen Sie tägliche und monatliche Netz- und IP-Scans durch. | IBM und Kunde |
|Bereitstellen von Zugriff auf Prüfprotokolle | Stellen Sie Zugriff auf alle Sicherheits- und Verwaltungsprüfprotokolle bereit.   | IBM und Kunde |
|Durchführen von Tests | Führen Sie regelmäßige Kontrollen für Operationstests und Penetrationstests von Drittanbietern durch. | IBM und Kunde |
|Statusberichterstattung, Prüfungskoordination und Konformitätsbesprechungen  | Führen Sie eine Statusberichterstattung, eine externe Prüfungskoordination und eine Präsentation bei Statusbesprechungen zur Konformitätsprüfung aus. | IBM |
|Prüfung der Beschäftigungssituation und Geschäftsanforderungen | Führen Sie eine vierteljährliche Prüfung der Beschäftigungssituation sowie eine Prüfung kontinuierlicher Geschäftsanforderungen für IBM Ansprechpartner aus, die Zugriff auf die Umgebung des Kunden haben. | IBM |
|Beheben von Sicherheitslücken | Beheben Sie berichtete Sicherheitslücken in der Plattform. | IBM |

Die finale Phase der Fertigstellung stellt das Ende der Beziehung zwischen Ihnen und IBM {{site.data.keyword.Bluemix_notm}} dar. Die primären Tasks in dieser Phase sind unter anderem:

* Beenden der finanziellen Vereinbarung
* Entfernen aller Netzverbindungen
* Recyceln der Infrastruktur

*Tabelle 3. Tasks in der Fertigstellungsphase*

| **Task** | **Taskdetails** | **Zuständiges Team** |
|----------|------------------|-----------------------|
|Beenden der finanziellen Vereinbarung | Erörtern und vereinbaren Sie ein Ende der finanziellen Vereinbarung. | IBM und Kunde |
|Stilllegen der Umgebung | Inaktivieren Sie den Zugriff auf und die Berechtigungsnachweise für die Umgebung. | IBM und Kunde |
|Beenden von Relay | Beenden Sie die Relay-Verbindung. | IBM |
|Recyceln der Infrastruktur | Recyceln Sie Ihre Infrastruktur im Einklang mit Unternehmensrichtlinien. | Kunde |

##Infrastrukturanforderungen für {{site.data.keyword.Bluemix_notm}} Local
{: #localinfra}

Bei
{{site.data.keyword.Bluemix_notm}} Local
entscheiden Sie über die physische Sicherheit und die Hosting-Infrastruktur
für die lokale Instanz. Die Anforderungen für das Einrichten von {{site.data.keyword.Bluemix_notm}}
Local sind von IBM wie im Folgenden angegeben festgelegt.
###Hardware
Während es feste Anforderungen für Typ und Größe der verfügbaren Hardware gibt, können Sie sich
für eine beliebige Kombination entscheiden, die
die definierten
Gesamtressourcenanforderungen erfüllt.
<dl>
<dt>**VMware ESXi-Hardware**</dt>
<dd>
Bei ESXi handelt es sich um eine Virtualisierungsebene, die auf physischen Servern ausgeführt
wird und auf abstrakter Ebene Prozessor, Hauptspeicher, Speicher und Ressourcen in mehreren virtuellen
Maschinen bereitstellt. Wählen Sie eine beliebige Kombination, die dem folgenden Gesamtumfang an
Ressourcen entspricht. Berücksichtigen Sie dabei, dass die Mindestanzahl an physischen Kernen pro
ESXi-Server
bei 8 liegt. Die folgenden Spezifikationen beziehen sich nur auf die {{site.data.keyword.Bluemix_notm}}-Kernlaufzeit.
<ul>
<li>48 physische Kerne mit jeweils mindestens 2,0 GHz</li>
<li>756 GB physischer Arbeitsspeicher</li>
</li>Gesamtdatenspeichergröße von 7,5 TB
<ul>
<li>7 TB Datenspeicher für {{site.data.keyword.Bluemix_notm}}</li>
<li>500 GB Datenspeicher für die virtuelle Anfangsmaschine</li>
</ul>
</ul>
<p><strong>Hinweis:</strong> Wenn Sie mehrere
Datenspeicher verwenden, muss das Präfix bei diesen Datenspeichern übereinstimmen.</p>
</dd>
<dt>**Hochverfügbarkeit**</dt>
<dd>
Um den Ausfall eines einzelnen Knotens auffangen zu können, müssen Sie über
n+1
ESXi-Server verfügen. Werden beispielsweise zwei ESXi-Server mit jeweils 16 Kernen verwendet,
wird ein
dritter ESXi-Server benötigt.
<p><strong>Hinweis:</strong> Der VMware-Administrator beim Kunden kann über ein striktes
Durchsetzen
der automatischen Funktionsübernahme für hohe Verfügbarkeit im Cluster entscheiden, die
die Verfügbarkeit von Ressourcen garantiert.</p>
</dd>
<dt>**Netz**</dt>
<dd>
Zu den empfohlenen Voraussetzungen gehört eine für den Kunden zugängliche Portgruppe mit sieben IP-Adressen des Kundennetzes, die einen abgehenden Internetzugriff im selben Teilnetz ermöglichen. Zwei Ports werden von der virtuellen Konzeptionsmaschine verwendet, drei Ports sind virtuelle IP-Adresse, die für die Domänen verwendet werden, und die letzten beiden Ports sind öffentliche IP-Adressen für DataPower-Systeme. Anschließend definieren Sie ein zweites privates VLAN, das auf die ESXi-Server beschränkt ist, die für {{site.data.keyword.Bluemix_notm}} Local verwendet werden. Dieses VLAN wird in VMware als Portgruppe angezeigt. {{site.data.keyword.Bluemix_notm}} Local verwendet dieses VLAN für das private Teilnetz, das sicherer ist und Probleme bei der Weiterleitung verringern kann.<br />
<p>Die folgenden Ports werden verwendet:</p>
<ul>
<li>Port 443 für die Relay-Verbindung
<p>**Hinweis:** Wenn Sie einen IPSec-Tunnel anstelle eines OpenVPN-Tunnels auswählen, öffnen Sie einen Kundenport für diese Verbindung. </p></li>
<li>Port 389 oder SSL 636 für die LDAP- oder Active Directory-Verbindung</li>
</ul>
<p>**Hinweis:** IBM kann erkennen, ob die Netzverbindung verloren geht. Falls die Netzverbindung verloren geht, nimmt IBM mit Ihnen Kontakt auf, um das Problem zusammen mit Ihrem Netzspezialisten zu beheben.</p>
</dd>
</dl>

###vCenter Server-Konfiguration
Informieren Sie sich über die folgenden
Anforderungen in Bezug auf Version, Rechenzentrum, Ressourcenpool und Datenspeicher.
<dl>
<dt>**Unterstützte VMware-Versionen**</dt>
<dd>vCenter und ESXi 5.1 sowie 5.5</dd>
<dt>**Unterstützte VMware-Typen**</dt>
<dd>vSphere Enterprise<br />
vSphere Enterprise plus, wenn Sie beabsichtigen, verteilte virtuelle Switches zu verwenden</dd>
<dt>**Rechenzentrum**</dt>
<dd>Erstellen Sie ein Rechenzentrum, soweit noch nicht vorhanden.</dd>
<dt>**Ordner für Rechenzentrum**</dt>
<dd>Erstellen Sie einen VM-Ordner mit dem Namen des Clusters, wenn nicht geplant ist, das
ein Administratorzugriff erteilt werden soll, der über das Rechenzentrum weitergegeben wird.</dd>
<dt>**Cluster**</dt>
<dd>Erstellen Sie speziell für
{{site.data.keyword.Bluemix_notm}} Local einen Cluster. Wählen Sie als Namen für den Cluster beispielsweise den Namen `bluemix`.</dd>
<dt>**Ressourcenpool**</dt>
<dd>Erstellen Sie einen Ressourcenpool für den
{{site.data.keyword.Bluemix_notm}} Local-Cluster. Wählen Sie als Namen für den Ressourcenpool beispielsweise den Namen
`local`.</dd>
</dt>**Datenspeicher**</dt>
<dd>Erfordert 7,5 TB für die Erstbereitstellung von {{site.data.keyword.Bluemix_notm}}.<br />
<br />
**Hinweis**: Wenn
Sie mehrere Datenspeicher verwenden, müssen Sie sicherstellen, dass alle Datenspeicher mit
demselben Präfix beginnen. Die Datenspeicher könnten z. B. als `bluemix_datastore_01` und `bluemix_datastore_02` bezeichnet werden.</dd>
</dl>

###Netzbandbreite
Der empfohlene Durchsatz liegt bei 5
Mbps (Hochladen) und 5 Mbps (Herunterladen). Es ist im Schnitt mit einer monatlichen Datennutzung im
Umfang
von 10 GB zu rechnen. IBM richtet vereinbarte Fenster
ein, wenn umfangreiche Datenpakete eingehen, die bis zu 3 GB groß sein können.
###VMware-Berechtigungen
Legen Sie die im Folgenden beschriebenen Rollen und
Berechtigungen fest. Für alle Berechtigungen ist eine Weitergabe eingerichtet. Wird eine Berechtigung
weitergegeben, wird sie bis in die unterste Objekthierarchie durchgereicht. Berechtigungen für
untergeordnete Objekte setzen Berechtigungen eines übergeordneten Objekts jedoch immer außer
Kraft.
<dl>
<dt>**v Center Server**</dt>
<dd>Definieren Sie die Rolle als Nur-Lese-Berechtigung
ohne Weitergabe.<br />
<br />
**Note**: Diese Rolle wird benötigt,
um den Taskstatus für bestimmte Plattenoperationen abzurufen.</dd>
<dt>**Rechenzentrum**</dt>
<dd>Erstellen Sie die Rolle '{{site.data.keyword.Bluemix_notm}}' und erteilen Sie Berechtigungen für
den Datenspeicher (untergeordnete Dateioperationen und das Aktualisieren von Dateien virtueller Maschinen eingeschlossen).<br />
<br />
**Hinweis**: Diese Rolle wird zur Unterstützung von Dateisendungen an die Datenspeicher benötigt.</dd>
<dt>**Cluster**</dt>
<dd>Definieren Sie die Rolle als Administratorrolle mit Weitergabe.</dd>
<dt>**Datenspeicher**</dt>
<dd>Definieren Sie die Administratorberechtigung und eine Weitergabe an alle
{{site.data.keyword.Bluemix_notm}}-Datenspeicher.</dd>
<dt>**Netz**</dt>
<dd>Definieren Sie öffentliche und private Portgruppen mit Administratorberechtigung ohne
Weitergabe.</dd>
</dl>

###Droplet Execution Agent-Pool
Jeder DEA (Droplet Execution Agent) ist wie folgt konfiguriert:
- 16 bis 32 GB RAM
- 2 - 4 vCPU
- 150 - 300 GB Speicher

Ist z. B. der ESXi-Host mit 256 GB Hauptspeicher und 16 Kernen ausgestattet, werden
acht DEA hinzugefügt. Sind für den ESXi-Host 64 GB Hauptspeicher und 8 Kerne vorgesehen, werden zwei
ESXi-Server benötigt und es müssen vier DEA hinzugefügt werden. Weitere 1,5 TB Speicher werden für
jeweils vier DEA benötigt. Bei diesem Beispiel wird davon ausgegangen, dass ein DEA mit 32 GB RAM, 4
vCPUs und 300 GB Speicher konfiguriert ist.

##Lokale Instanz warten
{: #maintainlocal}

IBM wartet und installiert Aktualisierungen und Fixes, sofern IBM dies für die Bluemix Local-Plattform, -Laufzeiten und
-Services für angemessen hält. Es kann vorkommen, dass Services während Wartungszeiten nicht verfügbar sind.

**Wichtig**: IBM behält sich das Recht vor,
Services zu unterbrechen, um im Bedarfsfall Notfallwartungen vorzunehmen. IBM
kann die geplanten Wartungszeiten ändern, wird Sie aber über solche Änderungen sowie über eventuelle
Notfallwartungen benachrichtigen.

Die folgenden Wartungsarten sind für {{site.data.keyword.Bluemix_notm}} Local erforderlich:
<dl>
<dt>**Standardwartungsfenster**</dt>
<dd>Die Services verwenden vordefinierte Standardwartungsfenster, die dazu führen können, dass die Services nicht verfügbar sind. IBM benötigt nicht die Genehmigung des Kunden, um Wartungsarbeiten durchzuführen, versucht jedoch, die Auswirkungen auf Ihre Services so gering wie möglich zu halten.<br />
<br />
IBM übermittelt per E-Mail, Telefon oder über andere Medien Rundsendungen zu den jeweils für ein Wartungsfenster
geplanten Änderungen.<br />
<br />
**Wichtig**: Einige Services stehen Ihnen während des Wartungszeitraums möglicherweise nicht zur Verfügung.</dd>

<dt>**Monatliches Änderungsfenster**</dt>
<dd>Das monatliche Änderungsfenster wird basierend auf der entsprechenden Koordination zwischen Ihnen und IBM innerhalb eines 21-tägigen Fensters angewendet. Sie können IBM bestimmte Daten oder Zeiten innerhalb dieses 21-tägigen Zeitfensters mitteilen, die für Sie ungünstig sind. IBM wird sich bemühen, Aktualisierungen außerhalb dieser angegebenen Daten oder Zeiten zu planen. Basierend auf den Anfragen teilt Ihnen IBM das Wartungsfenster mit. Monatliche Änderungsfenster haben für gewöhnlich keinerlei Auswirkungen auf die aktive Bluemix Local-Umgebung.<br />
<br />
**Hinweis:** Wenn Sie für die Aktualisierung keine bestimmte Zeit anfordern, wird die Wartung automatisch am Ende des Zeitfensters durchgeführt.<br />
<br />
Wechseln Sie zu **ADMINISTRATION > SYSTEM INFORMATION**, um anstehende Aktualisierungen anzuzeigen, nicht verfügbare Daten festzulegen und Aktualisierungen zu genehmigen. Weitere Informationen zu Benachrichtigungen und zum Planen anstehender Aktualisierungen finden Sie unter <a href="../admin/index.html#oc_system">Systeminformationen anzeigen</a>.</dd>

<dt>**Sonstige**</dt>
<dd>IBM beabsichtigt, alle Wartungstätigkeiten, die Ihre Services beeinträchtigen, insbesondere die Verfügbarkeit Ihrer Bluemix Local-Umgebung, -Laufzeiten und -Services auf die monatlichen und Standardaktualisierungen zu beschränken. In Ausnahmefällen können andere Änderungsfenster für die Verwaltung der Umgebung verwendet werden. IBM
wird sich in angemessenem Maße bemühen, die Auswirkungen auf Sie während solcher Änderungsfenster zu minimieren
und Sie im Voraus benachrichtigen.</dd>
</dl>

Arbeiten Sie mit Ihrem von IBM zugewiesenen Kundenbeauftragten zusammen, um die Wartung Ihrer lokalen
Instanz festzulegen und sich auf ein Fenster für die Standardwartung zu einigen.

Falls nach einer Wartungsaktualisierung ein Problem berichtet wird, entscheiden Sie gemeinsam mit Ihrem IBM Ansprechpartner, ob es sinnvoll wäre, dass IBM die Aktualisierung rückgängig macht. Nachdem Sie sich geeinigt haben, macht IBM die Aktualisierung rückgängig und stellt die Umgebung in ihrem ursprünglichen Zustand wieder her.

## Disaster-Recovery
{: #dr}

{{site.data.keyword.Bluemix_short}} Public stellt eine kontinuierlich verfügbare Plattform für Innovation bereit. Mehrere Sicherheitsmaßnahmen garantieren, dass Ihre Organisationen, Bereiche und Apps immer verfügbar sind. Durch das Bereitstellen von Apps in mehreren geografischen Regionen lässt sich eine kontinuierliche Verfügbarkeit realisieren, die vor einem ungeplanten, gleichzeitigen Ausfall mehrerer Hardware- und Softwarekomponenten bzw. dem Ausfall eines gesamten Rechenzentrums schützt. Auf diese Weise sind selbst im Fall einer Naturkatastrophe an einem spezifischen Standort die verteilten Instanzen der {{site.data.keyword.Bluemix_notm}} Public-App an anderen Standorten weiterhin verfügbar.
{: shortdesc}

Disaster-Recovery für {{site.data.keyword.Bluemix_short}} Local ist aufgrund einer kontinuierlichen Verfügbarkeit für Ihre Apps, der integrierten Hochverfügbarkeit der Plattform und der Möglichkeit, Ihre Instanz im Fall eines Fehlers wiederherzustellen, möglich. Ihre Aufgabe ist es, eine kontinuierliche Verfügbarkeit für Ihre Apps zu ermöglichen, indem Sie die Apps in mehreren Regionen bereitstellen. Hochverfügbarkeit ist über Technologien in Cloud Foundry und anderen Komponenten auf Plattformebene integriert. Und Sie können gemeinsam mit IBM sicherstellen, dass Ihre Daten ordnungsgemäß gesichert werden, falls Sie Ihre Instanz zu einem beliebigen Zeitpunkt wiederherstellen müssen.

### Kontinuierliche Verfügbarkeit für {{site.data.keyword.Bluemix_notm}} Local aktivieren
{: #enabling}

Standardmäßig wird {{site.data.keyword.Bluemix_notm}} Public an mehreren Standorten bereitgestellt. Sie müssen jedoch folgende Schritte ausführen, um global verteilte {{site.data.keyword.Bluemix_notm}} Local-Instanzen zu ermöglichen:

* Stellen Sie entweder manuell oder mithilfe eines automatisierten Prozesses sicher, dass Ihre Entwickler Apps in mehr als einer Region bereitstellen. Die ausgewählten Regionen sollten mehr als 200 km auseinander liegen, damit sichergestellt ist, dass eine Naturkatastrophe nicht beide Standorte betrifft.
* Konfigurieren Sie eine globale Lastausgleichsfunktion wie Akamai oder Dyn, um auf Apps in mindestens zwei unterschiedlichen Regionen zu verweisen.

**Hinweis**: Nicht alle {{site.data.keyword.Bluemix_notm}}-Services unterstützen eine regionale Verteilung. Wenn Sie eine App erstellen, müssen Sie, falls Sie eine geografische Verteilung erzielen möchten, sicherstellen, dass die von dieser App verwendeten Services über eine Datensynchronisation als Schlüsselfunktion verfügen.

#### {{site.data.keyword.Bluemix_notm}} Local-Apps an mehreren Standorten bereitstellen
{: #deploying}

Für eine Bereitstellung an einem zweiten Standort bzw. an mehreren Standorten müssen Sie einen Prozess ganz ähnlich dem zur Aktivierung Ihres primären Standorts ausführen:

1. Aktivieren Sie eine neue lokale Umgebung, in der zusätzliche Instanzen Ihrer Anwendungen gehostet werden sollen. Wenden Sie sich zum Erstellen einer neuen Umgebung an Ihr IBM Vertriebsteam, das den Prozess einleitet. Weitere Informationen zum Einrichten einer lokalen Instanz finden Sie unter [{{site.data.keyword.Bluemix_notm}} Local einrichten](../local/index.html#setuplocal). Für den Zugriff auf die einzelnen Umgebungen müssen Sie sich bei jeder Umgebung separat anmelden. Die Standorte für die gehosteten Umgebungen sollten mindestens 200 km entfernt von dem ursprünglichen Standort liegen, damit ihre Verfügbarkeit sichergestellt werden kann.
2. Rufen Sie den eindeutigen Namen der Domäne ab, in der Ihre neue bereitgestellte App gehostet wird. Beispiel: Wenn Ihre ursprüngliche Domäne *mycompany.east.bluemix.net* ist, können Sie eine neue lokale Umgebung mit einer neuen Domäne wie *mycompany.west.bluemix.net* erstellen und die App in der neuen Domäne bereitstellen.
3. Stellen Sie Ihre ursprüngliche App jedes Mal auch an dem neuen Standort bereit. Weitere Informationen zur Bereitstellung finden Sie unter [Anwendung hochladen](../starters/upload_app.html).


#### Globale Lastausgleichsfunktion für {{site.data.keyword.Bluemix_notm}} Local aktivieren
{: #glb}

Eine globale Lastausgleichsfunktion stellt nicht nur eine kontinuierliche Verfügbarkeit sicher und ist für eine Disaster-Recovery unverzichtbar, sie hat auch diverse andere Vorteile:

* Standardmäßige Weiterleitung von Benutzern zur nächstgelegenen {{site.data.keyword.Bluemix_notm}}-Region.
* Leistungsabhängige Weiterleitung.
* Gezielte Übertragung eines Prozentsatzes des Datenverkehrs an eine neue Anwendungsversion.
* Bereitstellung von Failover für einen Standort auf der Basis einer Regionsdiagnose.
* Bereitstellung von Failover für einen Standort auf der Basis einer Anwendungsdiagnose.
* Gewichtete Weiterleitung zwischen Endpunkten.

Sie können eine globale Lastausgleichsfunktion wie Akamai oder Dyn auswählen. Weitere Informationen zur Verwendung von Akamai als globaler Lastausgleichsfunktion finden Sie unter [Global Traffic Management](https://www.akamai.com/us/en/solutions/products/web-performance/global-traffic-management.jsp){: new_window}. Weitere Informationen zur Verwendung von Dyn als globaler Lastausgleichsfunktion finden Sie unter [4 Reasons Businesses Are Taking Global Load Balancing to the Cloud](http://dyn.com/blog/4-reasons-businesses-are-taking-global-load-balancing-to-the-cloud/){: new_window}.

### Hochverfügbarkeit
{: #ha}

Zusätzlich zur Aktivierung einer kontinuierlichen Verfügbarkeit stellt {{site.data.keyword.Bluemix_notm}} durch den Einsatz von Technologien, die in Cloud Foundry, Docker und andere Komponenten integriert sind, auch eine plattformübergreifende Hochverfügbarkeit bereit.

Zu diesen Technologien zählen die folgenden:

<dl>
<dt>Skalierbarkeit in Cloud Foundry</dt>
<dd>Ein Cloud Foundry <a href="https://docs.cloudfoundry.org/concepts/architecture/execution-agent.html" target="_blank">Droplet Execution Agent (DEA)</a> führt Diagnosen der integrierten Apps aus. Falls ein Problem mit der App oder dem DEA selbst auftritt, werden zusätzliche Instanzen der App in einem alternativen DEA bereitgestellt, um das Problem zu beheben. Weitere Informationen finden Sie unter <a href="https://docs.cloudfoundry.org/concepts/high-availability.html" target="_blank">Configuring CF for High Availability with Redundancy</a>.
</dd>
<dt>Metadatensicherung</dt>
<dd>Metadaten werden an einem sekundären Standort, typischerweise einer lokalen virtuellen Maschine, gesichert. Falls möglich, sollten Sie die Sicherung in Ihrer eigenen Umgebung, die mindestens 200 km entfernt liegt, replizieren.</dd>
</dl>

##Lokale Instanz wiederherstellen
{: #restorelocal}

{{site.data.keyword.Bluemix_notm}} Local-Einstellungen, -Metadaten und -Konfigurationen werden für den Fall ungeplanter Ausfälle in der Umgebung regelmäßig gesichert. Zu den Daten, für deren Sicherung Sie zuständig sind, zählen Anwendungsdaten, Daten aus Clouddatenbankservices und Objektspeicher.

Im Rahmen der Datensicherung, die Systemmetadaten und Konfigurationen umfasst, führt IBM die folgenden Tasks aus:

<ul>
<li>Verschlüsselung aller Sicherungskopien und Verwaltung von Verschlüsselungsschlüsseln</li>
<li>Überwachung und Verwaltung der Sicherungsaktivität</li>
<li>Bereitstellung der verschlüsselten Sicherungsdateien</li>
<li>Wiederherstellen der angeforderten Daten</li>
<li>Beheben von Planungskonflikten bei Optionen des Sicherungs- und Fixmanagements</li>
</ul>

Da der Schutz privater Daten kritisch ist, ist IBM beim Umgang mit dem Sicherungsdateimanagement auf Ihre Kooperation angewiesen, damit die Dateien nicht an einen Ort außerhalb der Rechenzentren verschoben werden können. Deswegen fordert Sie IBM auf, die folgenden Tasks auszuführen:

<ul>
<li>Lagern Sie eine Kopie Ihrer verschlüsselten Sicherungsdaten analog zur Vorgehensweise für alle anderen von Ihnen verwalteten Sicherungsdaten aus.</li>
<li>Stellen Sie die Sicherungsdateien für den IBM Operator bereit, falls eine Wiederherstellung erforderlich sein sollte.</li>
</ul>

# Zugehörige Links
## Allgemein
* [Entdecken Sie: {{site.data.keyword.Bluemix_notm}} Local](http://www.ibm.com/cloud-computing/bluemix/hybrid/local/)
* [{{site.data.keyword.Bluemix_notm}} Local und {{site.data.keyword.Bluemix_notm}} Dedicated verwalten](../admin/index.html#mng)
* [Support kontaktieren](../troubleshoot/getting_customer_support.html#bluemix_support)
