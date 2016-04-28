---

copyright:
  years: 2015, 2016

---

{:new_window: target="_blank"}
{:codeblock: .codeblock}

# Aggiornamenti più recenti al pacchetto di build Liberty
{: #latest_updates}

## Un elenco degli aggiornamenti più recenti nel pacchetto di build Liberty.

*Ultimo aggiornamento: 23 marzo 2016*

### 25 marzo 2016: pacchetto di build Liberty aggiornato v2.7-20160321-1358
* Il pacchetto di build contiene una versione aggiornata di WebSphere Liberty basata sul [beta di marzo](https://developer.ibm.com/wasdev/blog/2016/03/18/new-websphere-liberty-features-march-2016/). La versione aggiornata di Liberty rende disponibile la funzione beta cloudant-1.0 in Bluemix.
* Il pacchetto di build contiene anche le versioni aggiornate di IBM JRE: 8 SR2 FP12 e 7.1 SR3 FP32. 
* Il pacchetto di build fornisce una versione aggiornata dell'agent per il [servizio Auto-Scaling](../../services/Auto-Scaling/index.html). 
* Il pacchetto di build viene ora fornito con un nuovo raccoglitore di dati per il [servizio Monitoring and Analytics](../../services/monana/index.html#monana_oview). Il nuovo raccoglitore abilita la configurazione delle soglie di monitoraggio e contiene delle correzioni di bug.
* Il pacchetto di build fornisce una versione driver DB2® JDBC 4.19.49 aggiornata. 
* Il runtime Node.js utilizzato dai [programmi di utilità devconsole e shell di Gestione applicazioni](../../manageapps/app_mng.html#app_management) è stato aggiornato alla versione 0.12.12 più recente.

### 7 marzo 2016: pacchetto di build Liberty aggiornato v2.6-20160225-1649
* Il pacchetto di build aggiunge il supporto per l'applicazione di monitoraggio Dynatrace. Consulta [Utilizzo di Dynatrace](dynatrace.html) per i dettagli.
* Il pacchetto di build aggiunge il supporto per [DynamicPULSE](www.fujitsu.com/jp/group/fsweb/products/dynamic-pulse/).

### 10 febbraio 2016: pacchetto di build Liberty aggiornato v2.5-20160209-1336
* Il pacchetto di build contiene una versione aggiornata di WebSphere Liberty basata sul [beta di febbraio](https://developer.ibm.com/wasdev/blog/2016/02/12/beta-websphere-liberty-and-tools-february/). La versione aggiornata del profilo Liberty rende disponibile la funzione apiDiscovery-1.0 GA in Bluemix.

### 4 febbraio 2016: pacchetto di build Liberty aggiornato v2.4-20160127-1437
* Il pacchetto di build contiene una versione aggiornata di WebSphere Liberty basata sul beta di gennaio. Con questo aggiornamento, la funzione Liberty scim-1.0, precedentemente disponibile come una funzione beta, è ora disponibile come una funzione pronta per la produzione. La versione aggiornata di Liberty rende inoltre disponibile la funzione beta passwordUtilities-1.0 in Bluemix.
* Il pacchetto di build contiene anche un aggiornamento IBM JRE 7.1 SF3 FP20 e IBM JRE 8 SR2 FP10.
* Il pacchetto di build è stato aggiornato per scaricare l'ultimo 1.x [MariaDB Connector/J JDBC driver](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) quando di esegue la [configurazione automatica per il tipo MySQL dei servizi](autoConfig.html).

### 16 dicembre 2015: pacchetto di build Liberty aggiornato v2.3-20151208-1311
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sul [beta di dicembre](https://developer.ibm.com/wasdev/blog/2015/11/20/beta-was-liberty-beta-with-tools-december-2015/). La versione aggiornata del profilo Liberty rende disponibili le funzioni spnego-1.0 e wsSecuritySaml-1.1 GA e la funzione beta scim-1.0 in Bluemix.
* Il pacchetto di build contiene anche un IBM JRE 8 SR2 aggiornato.
* Il pacchetto di build è stato aggiornato per scaricare gli ultimi [9.4.x PostgreSQL JDBC driver](https://jdbc.postgresql.org/) e 1.2.x [MariaDB Connector/J JDBC driver](https://mariadb.com/kb/en/mariadb/about-mariadb-connector-j/) quando si esegue la [configurazione automatica](autoConfig.html) per il tipo PostgreSQL o MySQL dei servizi.

### 23 novembre 2015: pacchetto di build Liberty aggiornato v2.2-20151119-1720
* Il pacchetto di build contiene una versione aggiornata del runtime di profilo Liberty e WebSphere eXtreme
Scale Client con le correzioni per la protezione per la [vulnerabilità di Apache Commons Collection](http://www-01.ibm.com/support/docview.wss?uid=swg21971426).
* Il pacchetto di build contiene anche una versione aggiornata del [Java MongoDB Driver](https://docs.mongodb.org/ecosystem/drivers/java/), v2.13.3. Il nuovo driver è compatibile con MongoDB versione 2.4, 2.6 e 3.0.
* Il pacchetto di build fornisce anche una versione aggiornata del raccoglitore di dati per il [servizio Monitoring and Analytics](../../services/monana/index.html). Il raccoglitore di dati aggiornato offre delle funzionalità di traccia di metodo migliorate.

### 16 ottobre 2015: pacchetto di build Liberty aggiornato v2.1-20151006-0912
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sul [beta di ottobre](https://developer.ibm.com/wasdev/blog/2015/09/25/beta-was-liberty-beta-with-tools-october-2015/). Con questo aggiornamento, le funzioni Liberty bells-1.0, rtcomm-1.0, rtcommGateway-1.0, samlWeb-2.0, sipServlet-1.1 , precedentemente disponibili come beta, sono ora disponibili come funzioni pronte per la produzione.
* Il pacchetto di build contiene anche un IBM JRE 8 SR1 FP11 aggiornato.
* Il pacchetto di build fornisce anche diversi miglioramenti e ottimizzazioni delle prestazioni:
  * La funzione di scansione degli archivi di bean impliciti [CDI 1.2](optionsForPushing.html)
è disabilitata per impostazione predefinita quando si distribuiscono file WAR o EAR.
  * Per ridurre la dimensione del droplet, i [programmi di utilità di gestione applicazioni](../../manageapps/app_mng.html) evconsole e shell richiedono un'operazione di ripreparazione, invece di un riavvio.
  * La cache di classe condivisa di IBM JRE è disabilitata poiché non veniva riutilizzata nell'ambiente Bluemix.

### 18 settembre 2015: pacchetto di build Liberty aggiornato v2.0-20150914-1535
* Il pacchetto di build introduce due importanti modifiche:
  * La configurazione predefinita per i file WAR e EAR abilita le funzioni del profilo Web Java EE 7 anziché
le funzioni del profilo Web Java EE 6.
  * La versione Java predefinita è la versione 8 anziché la funzione 7.
* Fai riferimento a [Upcoming Liberty for Java buildpack changes](https://developer.ibm.com/bluemix/2015/09/08/upcoming-liberty-for-java-buildpack-changes/) per dettagli su queste modifiche e su come possono influire sulla tua applicazione.
* Il pacchetto di build introduce anche l'opzione di configurazione app_state per disabilitare la funzione appstate tramite la variabile di ambiente JBP_CONFIG_LIBERTY. La funzione appstate si integra con il processo di verifica dell'integrità di Cloud Foundry per garantire che l'applicazione Liberty venga inizializzata completamente prima di poter ricevere richieste HTTP. Per disabilitare la funzione appstate, puoi impostare la variabile di ambiente JBP_CONFIG_LIBERTY su “app_state: false”.

### 4 settembre 2015: pacchetto di build Liberty aggiornato v1.22-20150824-1104
* Il pacchetto di build supporta le [variabili di ambiente HTTP_PROXY e
HTTPS_PROXY](environmentVariables.html). Se impostate, il pacchetto di build utilizza il server proxy specificato da queste variabili di ambiente quando scarica i diversi componenti del pacchetto di build.

### 19 agosto 2015: pacchetto di build Liberty aggiornato v1.21-20150811-1342
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sul [beta di agosto](https://developer.ibm.com/wasdev/blog/2015/07/30/beta-was-liberty-beta-with-tools-august-2015/). La versione aggiornata del profilo Liberty rende disponibili le seguenti nuove [funzioni beta](usingBetaFeatures.html) in Bluemix: bells-1.0, rtcommGateway-1.0, samlWebSso-2.0.

### 31 luglio 2015: pacchetto di build Liberty aggiornato v1.20.1-20150729-1255
* Il pacchetto di build contiene versioni aggiornate dei JRE IBM: 7.1 SR1 FP10 r 8 SR1 FP10.
I JRE aggiornati
contengono le [ultime correzioni di sicurezza](http://www-01.ibm.com/support/docview.wss?uid=swg21964161) e altri miglioramenti.
* Il plug-in del servizio che fornisce il [supporto di configurazione automatica](autoConfig.html) per il servizio [Cloudant NoSQL Database](../../services/Cloudant/index.html#Cloudant) è stato aggiornato per garantire che le connessioni al servizio vengano stabilite su un canale sicuro.

### 21 luglio 2015: pacchetto di build Liberty aggiornato v1.20-20150713-1450
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sulla [release 8.5.5.6](https://developer.ibm.com/wasdev/blog/2015/06/25/java-ee-7-has-landed-in-was-liberty/). Con questa release, tutte le funzioni Liberty Java EE 7 precedentemente disponibili come funzioni beta sono ora disponibili come funzioni pronte per la produzione. A causa di limitazioni relative
alle porte e anche di altra natura esistenti in Bluemix, alcune funzioni come ad esempio gli EJB remoti non sono
pienamente supportati nella piattaforma.
* Il pacchetto di build riconosce ed esegue le applicazioni fornite in [distZip-style](https://docs.gradle.org/current/userguide/application_plugin.html).
* Il pacchetto di build contiene un raccoglitore di dati aggiornato per il servizio [Monitoring and Analytics](../../services/monana/index.html) e WebSphere eXtreme Scale Client che supporta la nuova versione di runtime di Liberty.

### 30 giugno 2015: pacchetto di build Liberty aggiornato v1.19.1-20150622-1509
* Questa versione del pacchetto di build contiene un IBM JRE aggiornato con una correzione per la protezione per la [vulnerabilità LogJam](http://www-01.ibm.com/support/docview.wss?uid=swg21961390).
* L'agent [New Relic](newRelic.html) è stato aggiornato alla versione 3.17. La nuova versione fornisce un'integrazione migliorata con il runtime di profilo Liberty.

### 14 giugno 2015: pacchetto di build Liberty aggiornato v1.19-20150608-1717
* Il pacchetto di build contiene diversi miglioramenti alla gestione delle applicazioni che includono il supporto per la console di
sviluppo e un accesso shell basato sul web. Per i dettagli, consulta [la documentazione Gestione applicazioni](../../manageapps/app_mng.html).
* Il pacchetto di build contiene anche una correzione per un problema a causa del quale non era possibile
trovare la funzione Liberty per il [servizio Monitoring and Analytics](../../services/monana/index.html).

### 27 maggio 2015: pacchetto di build Liberty aggiornato v1.18-20150519-1642
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sul [beta di maggio](https://developer.ibm.com/wasdev/blog/2015/05/08/beta-liberty-and-tools-may-2015/).

### 5 maggio 2015: pacchetto di build Liberty aggiornato v1.17-20150501-1729
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sul [beta di aprile](https://developer.ibm.com/wasdev/blog/2015/04/10/announcing-liberty-beta-with-tools-aprilmay-2015/). Con questo aggiornamento, le funzioni Liberty jsp-2.3, el-3.0 e jdbc-4.1, precedentemente disponibili come funzioni beta, sono ora disponibili come funzioni pronte per la produzione. Inoltre, le funzioni Java EE 7 come jsf-2.2, javaMail-1.5, webProfile-7.0 e javaee-7.0 sono ora disponibili come [funzioni beta](usingBetaFeatures.html).
* Il pacchetto di build fornisce anche un supporto iniziale per Java 8. IBM JRE 7.1 continua a essere il JRE predefinito ma è possibile abilitare IBM JRE 8 per un'applicazione impostando la variabile di ambiente JBP_CONFIG_IBMJDK. È anche supportata
la configurazione della versione di OpenJDK. Per tutti i dettagli, consulta [Personalizzazione del JRE](customizingJRE.html).
* Il pacchetto di build fornisce una nuova variabile di ambiente JBP_CONFIG_LIBERTY che può essere utilizzata per
sovrascrivere l'insieme predefinito di funzioni Liberty abilitato per un'applicazione quando distribuisce un
file WAR o EAR. Per ulteriori informazioni, consulta [Applicazioni autonome](optionsForPushing.html#stand_alone_apps).
* Il plug-in di servizio per il [servizio Monitoring and Analytics](../../services/monana/index.html) è stato aggiornato per ridurre la dimensione dei log generati per il servizio.
* Con questa versione del pacchetto di build, la modalità di disposizione dei file applicazione nel droplet è cambiata. La modifica nella struttura dei file ha eliminato la complessità correlata a mantenere i link simbolici e non dovrebbe aver alcun impatto sulle applicazioni.

### 15 aprile 2015: pacchetto di build Liberty aggiornato v1.16-20150407-1737
* Questa versione del pacchetto di build contiene un IBM JRE 7.1-2.11 aggiornato
con una [correzione per la sicurezza per la vulnerabilità Bar Mitzvah](http://www-01.ibm.com/support/docview.wss?uid=swg21882777).
* Quando vengono distribuiti file WAR autonomi, se forniti, il pacchetto di build utilizza ora la
root di contesto specificata nel file **ibm-web-ext.xml** incorporato
come root di contesto dell'applicazione. Con questa modifica, le applicazioni precedentemente
distribuite sotto la root di contesto potrebbero essere distribuite sotto un
contesto diverso sulla base delle impostazioni contenute nel file **ibm-web-ext.xml**.

### 3 aprile 2015: pacchetto di build Liberty aggiornato v1.15-20150402-1422
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sul [beta di marzo](https://developer.ibm.com/wasdev/blog/2015/03/13/announcing-liberty-beta-tools-march-2015/). La versione aggiornata dei profili Liberty rende disponibile la funzione beta jsf-2.2 in Bluemix.
* Il pacchetto di build contiene anche una versione aggiornata del raccoglitore di dati per il [servizio Monitoring and Analytics](../../services/monana/index.html).

### 20 marzo 2015: pacchetto di build Liberty aggiornato v1.14-20150319-1159
* Questa versione del pacchetto di build contiene un IBM JRE 7.1.2.11 aggiornato con una correzione per la protezione per la [vulnerabilità FREAK](http://www-01.ibm.com/support/docview.wss?uid=swg21699864).
* Il servizio [ SQL Database](services/SQLDB/index.html#SQLDB) offre dei piani pagati
che forniscono un'opzione per connettersi al server di database sul protocollo SSL. Il supporto della configurazione automatica del pacchetto di
build per il servizio SQL Database è stato aggiornato per configurare il runtime per connettersi al database su SSL, se sono
disponibili le informazioni di connessione SSL.
* Il pacchetto di build è stato aggiornato per segnalare un errore quando viene distribuito un file WAR o EAR autonomo che
contiene un file di configurazione **server.xml ** nella root dell'archivio dell'applicazione.
* Il pacchetto di build contiene una correzione per il plug-in del servizio di configurazione automatica
di MongoDB che, in alcuni casi, generava una configurazione **server.xml** non valida.

### 10 febbraio 2015: pacchetto di build Liberty aggiornato v1.13-20150209-1122
* Il pacchetto di build contiene delle correzioni per la sicurezza per gli [Apache HttpComponents e le vulnerabilità della funzione di overlay Java](https://www-304.ibm.com/connections/blogs/PSIRT/entry/ibm_security_bulletin_multiple_vulnerabilities_fixed_in_liberty_for_java_for_ibm_bluemix_cve_2012_6153_cve_2014_3577_cve_2015_0178?lang=en_us).
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sul [beta di febbraio](https://developer.ibm.com/wasdev/blog/2015/02/13/announcing-liberty-beta-tools-february-2015/). La versione aggiornata del profilo Liberty fornisce una versione aggiornata della funzione WebSocket GA websocket-1.1. Rende inoltre disponibili le seguenti funzioni beta Java EE 7 in Bluemix:
  * cdi-1.2, el-3.0, jsp-2.3,  jca-1.7, jacc-1.5 e jaspic-1.1
* Il pacchetto di build fornisce l'integrazione con lo [strumento JRebel di ZeroTurnaround](http://zeroturnaround.com/software/jrebel/). L'integrazione semplifica l'utilizzo di JRebel con le applicazioni Bluemix e l'esecuzione di aggiornamenti delle applicazioni istantanei senza ridistribuire o ripreparare l'applicazione. Sono supportate solo le applicazioni web autonome.

### 6 febbraio 2015: pacchetto di build Liberty aggiornato v1.12-20150130-1016
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty basata sul [beta di gennaio](https://developer.ibm.com/wasdev/blog/2015/01/16/announcing-liberty-beta-tools-january-2015/).
* Il pacchetto di build contiene una versione snellita del raccoglitore di dati per [servizio Monitoring and Analytics](../../services/monana/index.html#gettingstartedtemplate).

### 23 gennaio 2015: pacchetto di build Liberty aggiornato v1.11-20150119-1511
* Il pacchetto di build contiene un IBM JRE versione 7.1 SR2 FP1 aggiornato.
* Contiene anche un WebSphere eXterme Scale Client versione 8.6.0.6 aggiornato e un agent aggiornato per il servizio di scaling automatico.
* Il supporto del servizio [New Relic](newRelic.html) è stato migliorato per supportare i servizi definiti dall'utente.
* Il pacchetto di build è stato migliorato per segnalare versioni dettagliate del profilo Liberty e di IBM JRE.

### 19 dicembre 2014: pacchetto di build Liberty aggiornato v1.10-20141218-0103
* Questo pacchetto di build fornisce una modalità di sviluppo per le applicazioni. La modalità di sviluppo
è una modalità speciale che consente agli sviluppatori di condurre molte attività per un'istanza dell'applicazione
che prima non erano possibili. Utilizzando questa funzione, questa versione di IBM Eclipse Tools for Bluemix può ora supportare il debug remoto con gli aggiornamenti file incrementali su un'applicazione Liberty in esecuzione in Bluemix. Per uno sviluppatore, ciò rende conveniente l'utilizzo di Eclipse per eseguire il debug di un'applicazione nel cloud e applicare le modifiche a tale applicazione istantaneamente.
* Il pacchetto di build contiene anche una versione aggiornata del profilo Liberty basata sul [beta di dicembre](https://developer.ibm.com/wasdev/blog/2014/12/10/announcing-liberty-beta-december/).
* Inoltre, le seguenti quattro funzioni Liberty che erano in precedenza disponibili come funzioni beta sono ore pronte per la produzione:
  * concurrent-1.0
  * jsonp-1.0
  * servlet-3.1
  * websocket-1.0.
* Il pacchetto di build fornisce l'integrazione con il servizio New Relic. Dopo che è stato eseguito il bind di un'applicazione al servizio New Relic, il pacchetto di build
scarica e configura automaticamente il runtime con l'agent New Relic.
* Il pacchetto di build ha i seguenti limiti noti:
  * quando si è in modalità di sviluppo, non è possibile eseguire il bind di un servizio SessionCache.
  * quando si è in modalità di sviluppo, non è possibile creare un dump dei thread.
  * Quando si utilizza la funzione servlet-3.1 o websocket-v1.0, non è possibile eseguire il bind del
servizio Monitoring & Analytics.

### 5 dicembre 2014: pacchetto di build Liberty aggiornato v1.9-20141202-0947
* Il pacchetto di build fornisce un supporto migliorato delle opzioni JVM. Le opzioni JVM
possono ora essere applicate con un'operazione di riavvio. La ripreparazione dell'applicazione
non è necessaria. Inoltre, le opzioni JVM predefinite sono ottimizzate per il rilevamento rapido delle possibili
condizioni di errore (e preconfigurate con un'ubicazione comune che semplifica l'individuazione dei
dump generati. Ulteriori dettagli sono forniti nell'[articolo Custom Configuration of Java JVM for the Liberty Runtime](https://developer.ibm.com/bluemix/2014/12/12/custom-configurations-java-jvm-liberty-runtime/).
* Il pacchetto di build contiene un driver JDBC DB2 aggiornato versione 4.17.29.
* Contiene anche una correzione per un problema che impediva la raccolta delle informazioni sull'utilizzo del pool di thread Liberty per il servizio Monitoring & Analytics.

### 21 novembre 2014: pacchetto di build Liberty aggiornato v1.8-20141118-1610
* Il pacchetto di build contiene un IBM JRE aggiornato versione 7.1 SR2 che fornisce una correzione per la [vulnerabilità POODLE](http://www-01.ibm.com/support/docview.wss?uid=swg21687173).
* Contiene anche una versione aggiornata del profilo Liberty basata sul [beta di novembre](https://developer.ibm.com/wasdev/blog/2014/11/07/announcing-liberty-profile-beta-november/).

### 30 ottobre 2014: pacchetto di build Liberty aggiornato v1.7-20141020-1759
* Il pacchetto di build contiene un IBM JRE aggiornato versione 7.1 SR1 FP3.
* Fornisce anche una correzione per un problema che impediva la distribuzione di applicazioni
con una configurazione server che conteneva caratteri Unicode.

### 23 ottobre 2014: pacchetto di build Liberty aggiornato v1.6-20141013-1628
* Il pacchetto di build viene ora fornito con un nuovo raccoglitore di dati per [Monitoring and Analytics](../../services/monana/index.html). Il nuovo raccoglitore di dati raccoglie le informazioni approfondite di diagnostica,
che abilitano gli utenti del piano di diagnostica del servizio a diagnosticare
i problemi relativi alle loro applicazioni, con una precisione fino alla specifica riga di codice.
* Il pacchetto di build contiene delle versioni aggiornate degli agent di gestione e di
scaling automatico che includono correzioni di bug e miglioramenti secondari. Include anche una versione aggiornata del [profilo Liberty](https://developer.ibm.com/wasdev/) e di [Java MongoDB Driver](https://docs.mongodb.org/ecosystem/drivers/java/), v2.12.3.
* Nella funzione cloudAutowiring, un bug che causava degli errori di aggiunta di risorse in alcune applicazioni è stato corretto.

### 3 ottobre 2014: pacchetto di build Liberty aggiornato v1.5-20140923-1143
* Con il pacchetto di build aggiornato, le applicazioni possono ora utilizzare le funzioni beta di Liberty,
comprese WebSocket 1.0, Servlet 3.1 o JAX-RS 2.0. Per ulteriori informazioni, consulta [Utilizzo delle funzioni beta](usingBetaFeatures.html).

### 30 settembre 2014: pacchetto di build Liberty aggiornato v1.4-20140908-1803
* Il pacchetto di build fornisce ora il supporto per i servizi di terze parti ElephantSQL e ClearDB MySQL Database. Il supporto di configurazione
automatica funziona anche con i servizi sperimentali posgresql e mysql. Con il nuovo totale di 13 servizi, il supporto di configurazione automatica nel pacchetto di build Liberty rende più rapido e facile l'utilizzo di servizi Bluemix nelle applicazioni Liberty.
* Durante la preparazione dell'applicazione, il pacchetto di build visualizza dei messaggi di log migliorati relativi alla configurazione automatica e alle altre azioni che esegue.
* Il pacchetto di build contiene una versione aggiornata del profilo Liberty con correzioni e miglioramenti.
* Contiene anche una versione aggiornata di IBM JRE versione 7.1 che presenta dei miglioramenti delle prestazioni. Consulta la pagina [What's new](http://www-01.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.71.doc/diag/preface/changes_71/changes.html) per un insieme delle modifiche in dettaglio.

### 28 agosto 2014: pacchetto di build Liberty aggiornato v1.3-20140818-1538
* Il pacchetto di build contiene anche una versione aggiornata di [ Liberty Profile](https://developer.ibm.com/wasdev/) con le correzioni e i miglioramenti più recenti.
* Questa versione del pacchetto di build corregge il supporto per la variabile di ambiente JAVA_OPTS
per passare delle opzioni JVM aggiuntive al runtime dell'applicazione.
* Corregge anche un problema che impediva la distribuzione di applicazioni Jar basate su Spring autonome.
* È ora possibile generare e scaricare tracce di snap IBM JVM utilizzando l'interfaccia utente Bluemix. Consulta l'[argomento relativo alla risoluzione dei problemi](http://www-01.ibm.com/support/knowledgecenter/SSYKE2_7.0.0/com.ibm.java.lnx.70.doc/troubleshooting.html) nella documentazione di IBM JVM per saperne di più sulle tracce di snap e le altre informazioni di diagnostica generate dalla JVM.

### 29 luglio 2014: pacchetto di build Liberty aggiornato v1.1-20140725-1341
* La nuova versione di Liberty Bluemix Edition è ora disponibile!
  * Con questa versione di Liberty, disponiamo di correzioni e di nuove funzioni che ti consentono di utilizzare i servizi Bluemix in modo più efficiente!
  * Con la nuova funzione CouchDB disponibile il servizio Cloudant® può ora configurarla automaticamente in modo tale che un oggetto connettore sia prontamente disponibile! Analizzare
VCAP_SERVICES e fornire i jar client ektorp non è più necessario.
* La nuova versione di IBM SDK for Java è disponibile!
  * Quando ne verrà eseguito nuovamente il push, le tue applicazioni utilizzeranno IBM SDK for Java Versione 7.1-1.0. Questo si traduce in un notevole miglioramento delle prestazioni. La tua applicazione mostra ora una migliore
velocità effettiva e un utilizzo della memoria ridotto. Per ulteriori informazioni su IBM Java SDK fai clic [qui](http://www-01.ibm.com/support/docview.wss?uid=swg21671466).

  # rellinks
  ## general
  * [Runtime Liberty](index.html)
  * [Panoramica di Liberty Profile](http://www-01.ibm.com/support/knowledgecenter/SSAW57_8.5.5/com.ibm.websphere.wlp.nd.doc/ae/cwlp_about.html)
