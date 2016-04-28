---



copyright:

  years: 2015, 2016



---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Gestion de l'environnement {{site.data.keyword.Bluemix_notm}} local et de l'environnement {{site.data.keyword.Bluemix_notm}} dédié
{: #mng}
*Dernière mise à jour : 18 février 2016*

Si vous disposez d'un accès administrateur pour l'environnement {{site.data.keyword.Bluemix_notm}} local ou {{site.data.keyword.Bluemix_notm}} dédié, accédez à la page **Administration** pour gérer les ressources, surveiller l'utilisation des quotas, administrer des droits d'utilisateur, planifier des notifications de mise à niveau, afficher des rapports de sécurité et des journaux, etc. Vous pouvez gérer vos organisations en créant des espaces et en définissant des rôles utilisateur et des droits d'accès, voir [Gestion de vos organisations](../admin/adminpublic.html#orgmng).
{:shortdesc}

*Table 1. Tâches d'administration permettant de gérer une instance {{site.data.keyword.Bluemix_notm}} locale ou dédiée*

| Que puis-je faire ? | Détails |    
|----------------|---------|
|Surveiller l'utilisation du système | Cliquez sur **ADMINISTRATION &gt; UTILISATION**. Affichez vos informations système, surveillez
l'utilisation de l'unité centrale et planifiez l'utilisation afin de prendre les meilleures décisions pour votre entreprise. Voir [Affichage des informations relatives à l'utilisation](index.html#oc_resource).|
|Gérer votre catalogue | Cliquez sur **ADMINISTRATION &gt; GESTION DES CATALOGUES** afin de gérer les services que vos utilisateurs et
organisations peuvent voir. Voir [Gestion de votre catalogue](index.html#oc_catalog).|
|Administrer des organisations | Cliquez sur **ADMINISTRATION &gt; ADMINISTRATION DES ORGANISATIONS** afin de créer des organisations,
surveiller les quotas pour les organisations et prendre des décisions rapidement en fonction des besoins. Voir
[Administration des organisations](index.html#oc_organizations).|
|Créer des espaces et affecter des rôles utilisateur | Cliquez sur l'icône **Compte et support**
![Compte et support](../support/images/account_support.svg), puis sélectionnez **Gérer les organisations** afin de
créer des espaces dans vos organisations. Ajoutez des utilisateurs et affectez des organisations et des espaces aux utilisateurs. Voir
[Gestion de vos organisations](../admin/adminpublic.html#orgmng). |
|Gérer les droits d'administrateur | Cliquez sur **ADMINISTRATION &gt; ADMINISTRATION DES UTILISATEURS** pour ajouter des utilisateurs,
retirer des utilisateurs et ajuster les droits des utilisateurs. Voir [Gestion des utilisateurs et des droits](index.html#oc_user). |
|Consulter les rapports et les journaux | Cliquez sur **ADMINISTRATION &gt; RAPPORTS ET JOURNAUX** afin d'afficher des rapports de
sécurité et des journaux d'audit pour votre instance. Voir [Affichage des rapports](index.html#oc_report). |
|Afficher les informations système | Cliquez sur **ADMINISTRATION &gt; INFORMATIONS SYSTEME** afin d'afficher des informations système,
telles que les mises à jour en attente, le nom et la version de votre instance, la région, l'adresse URL de l'API, l'adresse URL de l'interface de ligne de
commande, les détails de la configuration LDAP, les mappages des groupes et des utilisateurs, des statistiques et les domaines partagés.
Vous pouvez aussi accéder aux abonnements à des événements et au flux de calendrier afin d'étendre vos notifications dans la section Mises à jour en
attente. Voir
[Affichage des informations système](index.html#oc_system). |
|Etendre des notifications et configurer des abonnements à des événements  | Cliquez sur **ADMINISTRATION &gt; INFORMATIONS SYSTEME &gt;
*Nombre* mises à jour en attente **. Vous pouvez utiliser des webhooks pour l'intégration à un service Web de votre choix afin de configurer un abonnement à une notification d'événement pour une mise à jour ou un incident. Voir [Notifications et
abonnements à des événements](index.html#oc_eventsubscription). |


## Notifications et abonnements à des événements 
{: #oc_eventsubscription}

Vous pouvez prendre connaissance à tout moment du statut de votre environnement en consultant la page Statut. {{site.data.keyword.Bluemix_notm}}
envoie également des notifications dans la zone Notifications de la page Administration concernant des événements tels que la maintenance et les mises à
niveau prévues. Les incidents sont signalés dans la page Statut. 

### Notifications

Vous pouvez afficher les notifications d'IBM pour votre environnement local ou dédié et surveiller le statut de votre environnement. Reportez-vous au
tableau ci-dessous pour des informations sur les différents types de notification et les emplacements auxquels les notifications sont publiées.


| **Type d'événement** | **Méthode de notification** |       
|-----------------|-------------------|
| Mises à jour de maintenance | Vous êtes prévenu en cas de mises à jour de maintenance prévues dans la zone Notifications de la page Administration. Accédez
à la page **Administration**, puis sélectionnez l'icône **Notifications** ![Notifications](images/icon_announcement.svg). Pour
afficher la liste complète ainsi que l'historique de vos notifications en attente et consultées, cliquez sur **ADMINISTRATION &gt;
INFORMATIONS SYSTEME** &gt; *Nombre* **mises à jour en attente**. Vous pouvez étendre la capacité de
notification en configurant un abonnement à un événement qui intègre les alertes relatives aux mises à jour de maintenance de la page Administration à un
service Web de votre choix afin d'acheminer les messages vers l'adresse électronique d'un centre d'assistance ou afin d'envoyer un message SMS à un
numéro de téléphone de votre choix.  |
| Incidents critiques | Vous êtes prévenu en cas d'incident critique dans la page Statut. Cliquez sur l'icône **Compte et support**
![Compte et support](../support/images/account_support.svg), puis sélectionnez **Statut**. Vous pouvez étendre la
capacité de notification en configurant un abonnement à un événement qui intègre les alertes relatives aux incidents de la page
Statut à un service Web de votre choix afin d'acheminer les messages vers l'adresse électronique d'un centre d'assistance ou afin d'envoyer un
message SMS à un numéro de téléphone de votre choix.  |  
| Statut | Vous pouvez afficher le statut le plus récent de la plateforme, des services et de votre instance {{site.data.keyword.Bluemix_notm}}. 
Cliquez sur l'icône **Compte et support** ![Compte et support](../support/images/account_support.svg), puis
sélectionnez **Statut**.   |

*Tableau 2. Types d'événement et méthodes de notification*

### Configuration d'abonnements à des événements 

Vous pouvez étendre la fonctionnalité des notifications qui sont envoyées dans la page Administration et dans la page Statut en utilisant des
abonnements à des événements qui utilisent des webhooks. Les webhooks routent vos notifications directement vers une destination de votre choix, par
exemple l'adresse électronique d'un centre d'assistance (par courrier électronique) ou un numéro de téléphone (par message SMS). Vous pouvez personnaliser
le type de notification, notamment les alertes relatives aux mises à jour de maintenance ou aux incidents critiques, ainsi que les informations qui sont
incluses dans la notification.


Pour utiliser des webhooks afin de configurer un abonnement à un événement spécifique, procédez comme suit : 

1. Accédez à la page **ADMINISTRATION** : 

- Pour les notifications relatives aux mises à jour de maintenance, accédez à **INFORMATIONS SYSTEME** &gt;
*Nombre* **mises à jour en attente**, puis cliquez sur l'icône **S'abonner**
![S'abonner](images/icon_subscribe.svg).
- Pour les notifications d'alerte relatives aux incidents, cliquez sur l'icône **Compte et support**
![Compte et support](../support/images/account_support.svg) &gt; **Statut**, puis cliquez sur l'icône
**S'abonner** ![S'abonner](images/icon_subscribe.svg).

**Remarque** : vous pouvez accéder à la page des abonnements à des événements pour les deux types de notification en appliquant
l'une des deux méthodes décrites. 

2. Cliquez sur **Ajouter un abonnement**.

3. Remplissez le formulaire d'abonnement à un événement. Pour des informations sur les zones du formulaire, reportez-vous au tableau suivant :


| **Zone** | **Description** |
|-----------------|-------------------|
| Type | Sélectionnez un webhook.  |
| Méthode | Sélectionnez GET ou POST.  |
| Evénement | Choisissez de vous abonner aux notifications relatives aux mises à jour ou aux incidents.  |
| URL | Entrez l'adresse URL afin d'ancrer votre service Web.  |
| Description | Ajoutez une description pour l'abonnement à un événement que vous créez.  |
| Nom d'utilisateur | Entrez votre nom d'utilisateur pour votre service Web. Si vous ne voulez pas utiliser vos données d'identification personnelles, vous
pouvez configurer un ID fonctionnel à utiliser spécifiquement avec {{site.data.keyword.Bluemix_notm}}. |
| Mot de passe | Entrez le mot de passe pour votre service Web.  |
| Contenu | Si vous avez sélectionné la méthode POST, entrez les propriétés propres au service Web que vous utilisez, associées aux valeurs
appliquées pour
la notification IBM. Par exemple, pour afficher le titre, le message et la gravité dans la notification émise par votre service Web, vous devez définir les
valeurs {{site.data.keyword.Bluemix_notm}} avec la propriété correspondante pour votre service Web. Vous pouvez utiliser les valeurs suivantes pour
extraire des informations depuis la notification {{site.data.keyword.Bluemix_notm}}, comme le titre de la notification, le corps du
message et le niveau de gravité : `"{{title}}`, `"{{message}},"` et `"{{severity}}"`. Si
vous n'entrez pas d'informations dans cette section, vous recevrez la notification sans information supplémentaire.   |

Tableau 3. Zones du formulaire d'abonnement à un événement 

Une fois votre abonnement à un événement sauvegardé, vous recevez des notifications via la méthode que vous avez configurée par le biais de votre
service Web. Les notifications continuent d'être publiées dans la page Statut pour les incidents et dans la zone Notifications de la page Administration
pour les mises à jour de maintenance. 

Vous pouvez sélectionner n'importe quel abonnement à un événement et afficher l'activité récente. Vous pouvez cliquer pour développer toute entrée
d'activité récente afin d'afficher les détails. Les valeurs IBM pour la notification que vous pouvez utiliser dans la section du contenu sont incluses
dans les détails. Pour afficher ces valeurs, développez l'entrée d'activité récente, développez **Evénement**, puis développez **Objet**.


## Affichage des informations système
{: #oc_system}

Pour afficher les informations système, cliquez sur **ADMINISTRATION &gt; INFORMATIONS SYSTEME**.

Vous pouvez développer et afficher diverses sections sur les mises à jour en attente, les informations système générales et les détails de
la configuration LDAP.

### Mises à jour en attente et notifications 

La section Mises à jour affiche le nombre de notifications relatives à des mises à jour en attente qui requièrent une intervention de votre part. Afin d'effectuer une action pour une mise à jour spécifique, procédez comme suit :

<ol>
<li>Cliquez sur <strong><em>Nombre</em> mises à jour en attente</strong> pour afficher toutes les mises à jour en attente.</li>
<li>Sélectionnez une mise à jour pour effectuer une action ou afficher les détails de la mise à jour, qui incluent la fenêtre de mise à jour, la date
planifiée ou le statut d'interruption.</li>
<li>Cliquez sur <strong>SELECTIONNER LES DATES D'INDISPONIBILITE</strong> pour définir des jours
spécifiques dans la fenêtre de mise à jour qui ne vous conviennent pas pour
l'application de la mise à jour. Si vous définissez des dates d'indisponibilité, IBM approuve et planifie votre mise à jour en fonction de vos sélections. Vous
recevez une notification lorsque la mise à jour est approuvée et planifiée.</li>
<li>Cliquez sur <strong>Approuver la mise à jour</strong> pour approuver la mise à jour si toutes les dates vous conviennent. Si vous approuvez la mise à jour, celle-ci est appliquée au cours de la fenêtre de mise à jour planifiée. IBM envoie une notification au début et à la fin
du déploiement de la mise à jour.</li>
</ol>

**Remarque** : si vous ne définissez pas de date d'indisponibilité ou si vous n'approuvez pas la mise à jour, celle-ci est
appliquée à la fin d'une fenêtre de 21 jours pour garantir que votre plateforme reste à jour.


Dans la page Mises à jour en attente, vous pouvez choisir d'effectuer le suivi du planning des mises à jour en cliquant
sur l'icône **Calendrier** ![Calendrier](images/icon_calendar.svg) et en téléchargeant le fichier
`.ics` afin d'importer les mises à jour planifiées dans une application de calendrier de votre choix :


<ol>
<li>Ouvrez votre application de calendrier.</li>
<li>Téléchargez le fichier de calendrier en cliquant sur l'icône **Calendrier**
![Calendrier](images/icon_calendar.svg), puis importez-le dans votre application de calendrier en utilisant le fichier
`.ics`. </li>
<li>Entrez vos données d'identification.</li>
<li>Affichez vos mises à jour planifiées.</li>
</ol>

Vous pouvez également étendre la fonctionnalité de notification pour la page Administration à l'aide d'abonnements à des événements en vue de
l'intégration à un service Web de votre choix. Pour configurer un abonnement à des notifications d'événement relatives à une mise à jour ou un incident,
voir [Notifications et abonnements à des événements](index.html#oc_eventsubscription).

### Informations système générales 

Dans la section Informations générales, vous pouvez consulter les informations suivantes :

- Des informations de base sur la génération {{site.data.keyword.Bluemix_notm}}.
- Des informations sur les API, notamment la version, l'adresse URL, la région et un lien vers la documentation de l'interface de ligne de commande.
- Des informations sur le domaine partagé concernant votre système et votre service.
- Des statistiques sur le nombre total d'applications, d'utilisateurs et d'organisations.

### Détails de la configuration LDAP 

Dans la section Détails de la configuration LDAP, vous pouvez sélectionner le serveur LDAP et afficher des informations sur les mappages des
utilisateurs et des groupes. Si vous utilisez un ID Web {{site.data.keyword.IBM}}, il est indiqué dans cette section. 

## Affichage des informations relatives à l'utilisation
{: #oc_resource}

Vous pouvez afficher différents types d'informations sur l'utilisation pour votre instance locale ou dédiée et pour votre compte
{{site.data.keyword.Bluemix_notm}} :


- Des informations sur les ressources, notamment l'espace disque, l'utilisation de l'unité centrale, l'utilisation du réseau et les temps de réponse
moyens. Voir [Utilisation des ressources](index.html#resourceusage).
- L'utilisation du compte par organisation, notamment le nombre d'applications de contexte d'exécution et leur utilisation, le nombre
total de Go/heure consommé par les contextes d'exécution, ainsi que le nombre d'instances de service et leur utilisation. Voir
[Utilisation du compte](index.html#accountusage).
- L'utilisation du quota de mémoire des organisations, la mémoire allouée aux applications en fonction du quota de mémoire utilisé total, et une
vue de la consommation de Go/heure par application pour une organisation spécifique. Vous pouvez aussi afficher l'utilisation du quota pour toutes les
organisations dans la page Administration des organisations, dans la section Surveillance des quotas. Voir
[Administration des organisations](../admin/index.html#orgusage).


### Utilisation des ressources
{: #resourceusage}

Pour afficher les informations relatives aux ressources, cliquez sur **ADMINISTRATION &gt; UTILISATION**.

Dans la section Surveillance des ressources, vous pouvez consulter les informations suivantes :

- Des informations relatives à l'utilisation des ressources, par exemple le nombre de gigaoctets de mémoire et le nombre de gigaoctets d'espace
disque qui sont utilisés. Vous pouvez afficher l'utilisation moyenne de l'unité centrale par tous les agents DEA (Droplet Execution Agent). Cliquez sur la vignette
de l'**UC** afin d'afficher l'utilisation de l'unité centrale pour chaque agent DEA. L'agent DEA associé à l'utilisation la plus élevée est répertorié en
premier, et chaque agent est identifié par son travail et son adresse IP. L'utilisation de l'unité centrale est exprimée dans trois catégories : la quantité d'unité centrale
utilisée pour les processus système, la quantité d'unité centrale utilisée pour les processus utilisateur et la quantité d'unité centrale utilisée pour les processus en attente.
- Des informations relatives à l'utilisation du réseau pour la bande passante entrante et la bande passante sortante, pour le jour précédent, la
semaine précédente ou le mois précédent.
Les données affichées dépendent de la somme du trafic entrant et sortant pour les réseaux publics et privés.
- Le temps de réponse moyen pour {{site.data.keyword.Bluemix_notm}} au cours des dix
minutes précédentes, de l'heure précédente ou du jour précédent.
- Le nombre moyen de transactions par seconde pour {{site.data.keyword.Bluemix_notm}} au
cours des dix minutes précédentes, de l'heure précédente ou du jour précédent.

### Utilisation du compte 
{: #accountusage}

Vous pouvez afficher l'utilisation mensuelle pour votre compte, pour votre environnement dédié ou local. Vous pouvez utiliser ces données afin
de déterminer les frais à facturer à des organisations spécifiques en fonction de leur consommation.


<ol>
<li>Cliquez sur l'icône <strong>Compte et support</strong> ![Compte et support](../support/images/account_support.svg) &gt;
<strong>Compte</strong> &gt; <strong>Détails sur l'utilisation</strong>.</li>
<li>Sélectionnez l'organisation pour laquelle afficher les données. </li>
<li>Vous pouvez afficher des détails sur l'utilisation pour les catégories suivantes :
<ul>
<li>Les applications de contexte d'exécution qui sont utilisées </li>
<li>L'utilisation totale des applications de contexte d'exécution en Go/heure </li>
<li>Les instances de service qui sont utilisées </li>
</ul>
</li>
<li>Facultatif : affichez vos données pour un mois spécifique en utilisant le menu <strong>Votre activité de cloud</strong> pour sélectionner le mois de
votre choix. </li>
<li>Facultatif : cliquez sur <strong>EXPORTER DES DONNEES</strong> et sélectionnez <strong>CSV</strong> ou <strong>JSON</strong> afin d'exporter vos
données pour le mois sélectionné dans un fichier <code>CSV</code> ou <code>JSON</code>. </li>
</ol>

Vous pouvez aussi afficher l'utilisation mensuelle et les frais associés au niveau du compte pour vos contextes d'exécution, vos applications et vos
services qui sont mis à disposition depuis l'environnement {{site.data.keyword.Bluemix_notm}} public. Vous pouvez utiliser ces données afin de
déterminer les frais à facturer à des organisations spécifiques en fonction de leur consommation.


<ol>
<li>Cliquez sur l'icône <strong>Compte et support</strong> ![Compte et support](../support/images/account_support.svg) &gt;
<strong>Compte</strong> &gt; <strong>Détails sur l'utilisation</strong>.</li>
<li>Cliquez sur <strong>Public</strong>.</li>
<li>Sélectionnez l'organisation pour laquelle afficher les données ou sélectionnez <strong>Toutes les organisations</strong> afin d'afficher les données
simultanément pour toutes les organisations.
</li>
<li>Vous pouvez afficher des détails sur l'utilisation pour les catégories suivantes :
<ul>
<li>Les applications de contexte d'exécution qui sont utilisées </li>
<li>L'utilisation totale des applications de contexte d'exécution en Go/heure </li>
<li>Les instances de service qui sont utilisées </li>
<li>Un récapitulatif des frais pour tous les contextes d'exécution, tous les services et toutes les applications qui sont mis à disposition
</li>
</ul>
</li>
<li>Facultatif : affichez vos données pour un mois spécifique en sélectionnant le mois de votre choix dans le graphique à barres. Les données pour le mois
en cours s'affichent par défaut.
</li>
<li>Facultatif : cliquez sur <strong>EXPORTER DES DONNEES</strong> et sélectionnez <strong>CSV</strong> ou <strong>JSON</strong> afin d'exporter vos
données pour le mois sélectionné dans un fichier <code>CSV</code> ou <code>JSON</code>. </li>
</ol>


### Utilisation des organisations 
{: #orgusage}

Pour afficher l'utilisation par organisation, cliquez sur **ADMINISTRATION &gt; ADMINISTRATION DES ORGANISATIONS**, puis
sélectionnez une organisation dans **Liste des organisations**. La page **Gérer les organisations** de l'organisation
sélectionnée affiche les informations suivantes sur l'utilisation :


- Le nombre de services utilisés 
- Le nombre de routes utilisées 
- Un graphique du quota de mémoire qui représente le quota utilisé et le quota non utilisé 
- Un graphique de l'allocation des applications qui indique quelles sont les applications incluses dans le quota de mémoire utilisé 
- Un graphique de l'utilisation des applications mesurée qui représente un rapport sur trois mois du nombre de Go/heure consommé par application
déployée. Vous pouvez sélectionner **Vue de liste** afin d'afficher des données pour toutes les applications, notamment l'allocation de
mémoire par application et la consommation de Go/heure mesurée pour les trois derniers mois.


Pour plus d'informations sur l'affichage de l'utilisation par organisation, l'ajustement des plans d'établissement des quotas et la gestion de vos
organisations, voir [Administration des organisations](../admin/index.html#oc_organizations).

## Affichage des rapports
{: #oc_report}

Vous pouvez afficher des journaux et des rapports de sécurité, tels que des rapports DataPower&trade;, de pare-feux et d'audit de connexion,
pour votre instance {{site.data.keyword.Bluemix_notm}}.

Pour afficher les rapports et les journaux, cliquez sur **ADMINISTRATION &gt; RAPPORTS ET JOURNAUX**.

Effectuez l'une des opérations suivantes :

- Vous pouvez sélectionner des dates de début et de fin dans les zones afin de filtrer les rapports et les journaux à afficher.
- Vous pouvez développer et afficher divers rapports depuis le panneau de navigation.
- Vous pouvez effectuer une recherche dans votre collection de rapports et de journaux. La recherche s'applique aux noms de rapport ainsi qu'au
contenu textuel des rapports et des journaux. Vous pouvez aussi choisir de filtrer votre recherche par **événements d'administration**,
**rapports DataPower**, **pare-feu** et **audit de connexion**.
- Lors de l'affichage d'un rapport ou d'un journal, vous pouvez cliquer sur l'icône ![Télécharger](images/icon_download.png) pour télécharger le rapport.

Le tableau ci-dessous présente la liste des rapports de sécurité qui sont générés pour l'environnement {{site.data.keyword.Bluemix_notm}}
local et l'environnement {{site.data.keyword.Bluemix_notm}} dédié.

| **Catégorie** | **Rapport** | **Description** |      
|-----------------|-------------------|---------------------|
| Pare-feu | Connexions au pare-feu | Evénements liés à la connexion de l'administrateur aux unités de pare-feu Vyatta. |
| Pare-feu | Refus du pare-feu | Evénements générés par les unités de pare-feu Vyatta lorsqu'une demande d'accès est refusée selon les règles de
pare-feu appliquées. |
| Evénements de connexion d'administrateur {{site.data.keyword.Bluemix_notm}} | Connexion des
administrateurs {{site.data.keyword.Bluemix_notm}} | Evénements générés par le système d'exploitation lorsqu'un administrateur démarre une
session SSH sur chaque système {{site.data.keyword.Bluemix_notm}}. |
| Evénements de connexion de développeur d'applications {{site.data.keyword.Bluemix_notm}} | Connexion
des développeurs d'applications {{site.data.keyword.Bluemix_notm}} | Evénements générés par le composant
de connexion à la plateforme {{site.data.keyword.Bluemix_notm}} lorsqu'un utilisateur de la plateforme {{site.data.keyword.Bluemix_notm}}
démarre une session via la ligne de commande, les API REST ou l'interface utilisateur {{site.data.keyword.Bluemix_notm}}. |
| Evénements d'administration d'administrateur {{site.data.keyword.Bluemix_notm}} | Evénements
d'administration du système d'exploitation des administrateurs {{site.data.keyword.Bluemix_notm}} | Evénements générés par le système
d'exploitation lorsqu'un administrateur effectue une action dans une session de travail en cours. |
| Evénements d'administration de développeur d'applications {{site.data.keyword.Bluemix_notm}} | Evénements
d'administration (Cloud Foundry) {{site.data.keyword.Bluemix_notm}} | Evénements liés aux opérations effectuées par l'utilisateur de la plateforme
{{site.data.keyword.Bluemix_notm}} via la ligne de commande, les API REST ou l'interface utilisateur {{site.data.keyword.Bluemix_notm}}. |
| Evénements d'administration de base de données d'administrateur {{site.data.keyword.Bluemix_notm}} | Evénements d'administration de base
de données | Evénements liés aux opérations effectuées par un administrateur de base de données sur les bases de données internes
{{site.data.keyword.Bluemix_notm}}. |
| Evénements d'administration | Evénements de gestion des utilisateurs | Evénements liés aux actions de gestion des utilisateurs effectuées dans la page
Administration. |
| Evénements d'administration | Catalogue | Evénements liés aux modifications du catalogue des services. |
| Evénements d'administration | Evénements de gestion des rapports de sécurité | Evénements liés aux actions de gestion des rapports de sécurité effectuées
dans la page Administration. |
| Révisions d'accès | Rapport sur les révisions d'accès | Révisions pour les accès privilégiés. |
| Gestion des modifications | Gestion des modifications logicielles | Activité de gestion des modifications. |
| Gestion des clés | Gestion des certificats SSL personnalisés | Certifications SSL personnalisées qui ont été téléchargées et stockées. |
| Chiffrement | Chiffrement des données en transit | Chiffrement des données en transit configuré. |
| Antivirus | Rapport d'analyse antivirus | Logiciel antivirus installé. |
| Gestion des correctifs logiciels | Rapport d'application des correctifs | Correctifs logiciels appliqués. |
| Gestion des incidents de sécurité | Rapport de résolution des incidents de sécurité | Preuve des incidents de sécurité pour la gestion des
incidents de sécurité. |

*Tableau 4. Liste des rapports de sécurité*

## Affichage du statut
{: #oc_status}

Vous pouvez surveiller le statut de votre instance {{site.data.keyword.Bluemix_notm}} à l'aide de la page Statut de {{site.data.keyword.Bluemix_notm}}. 
Cliquez sur l'icône **Compte et support** ![Compte et support](../support/images/account_support.svg), puis
sélectionnez **Statut**. 

La page Statut est l'emplacement central pour rechercher des notifications et des annonces sur les événements clés affectant la plateforme {{site.data.keyword.Bluemix_notm}} et les principaux services dans {{site.data.keyword.Bluemix_notm}}.

Vous pouvez vous abonner à un flux RSS pour recevoir les notifications automatiquement et ne pas avoir à les rechercher. Pour plus d'informations sur la page Statut et la configuration du flux RSS, voir [Affichage de {{site.data.keyword.Bluemix_notm}}](../support/index.html#viewing-bluemix-status).

## Gestion de votre catalogue
{: #oc_catalog}

Vous pouvez choisir les services et les modules de démarrage {{site.data.keyword.Bluemix_notm}} que les utilisateurs peuvent voir dans
le catalogue {{site.data.keyword.Bluemix_notm}}. Cliquez sur **ADMINISTRATION &gt; GESTION DES CATALOGUES**.

Sélectionnez une vignette de service ou de module de démarrage afin d'éditer la visibilité du plan de service ou de module de démarrage. Pour éditer
la visibilité, sélectionnez l'une des options suivantes :

- Pour afficher un service ou un module de démarrage masqué de sorte que vos utilisateurs puissent le voir dans le catalogue, sélectionnez
**ACTIVER TOUS LES PLANS**.
- Pour masquer un service ou un module de démarrage de sorte que vos utilisateurs ne le voient pas dans le catalogue
{{site.data.keyword.Bluemix_notm}}, sélectionnez **DESACTIVER TOUS LES PLANS**.
- Pour contrôler la visibilité d'un plan individuel, sélectionnez le nom du plan, puis utilisez le menu déroulant afin de sélectionner
**Activer pour toutes les organisations**, **Désactiver pour toutes les organisations** ou **Activer le plan pour des organisations spécifiques**.

<!-- staging only start -->

### Enregistrement d'un courtier de services 
{: #servicebrokerui}

Si vous voulez afficher un service particulier dans votre catalogue {{site.data.keyword.Bluemix_notm}}, vous devez implémenter et enregistrer
un courtier de services. Une fois votre courtier enregistré, vous pouvez choisir les organisations qui peuvent accéder au service dans votre instance
locale ou dédiée.


Les méthodes d'utilisation du courtier de services varient selon le nombre de services qu'il gère ou selon qu'il a déjà été enregistré dans {{site.data.keyword.Bluemix_notm}}.

- Si votre courtier de services gère un service, vous pouvez vous servir de l'interface utilisateur pour l'enregistrer après avoir implémenté
l'[API de courtier de services](http://docs.cloudfoundry.org/services/api.html){: new_window}. Voir
[Enregistrement d'un courtier de services qui gère un service](index.html#registerbrokerui).
- Si votre courtier de services gère plusieurs services, à ce stade, vous ne pouvez pas l'enregistrer après avoir implémenté l'API de courtier de
services. A la place, utilisez l'interface de ligne de
commande cf avec le plug-in d'[interface de ligne de commande
d'administration {{site.data.keyword.Bluemix_notm}}](../cli/plugins/bluemix_admin/index.html) (sous-commande ba) ou utilisez
l'[API de service personnalisé](index.html#servicebrokerapi).
- Si votre courtier de services est déjà enregistré et que vous voulez le mettre à jour ou le supprimer, utilisez l'interface de ligne de commande
cf avec le plug-in d'[interface de ligne de commande
d'administration {{site.data.keyword.Bluemix_notm}}](../cli/plugins/bluemix_admin/index.html) (sous-commande ba) ou utilisez
l'[API de service personnalisé](index.html#servicebrokerapi).

#### Enregistrement d'un courtier de services qui gère un service 
{: #registerbrokerui}

Procédez comme suit pour enregistrer votre courtier de services : 

1\. [Implémentez l'API de courtier de services Cloud Foundry](http://docs.cloudfoundry.org/services/api.html){: new_window}
pour permettre la communication entre votre service et {{site.data.keyword.Bluemix_notm}}. L'API de courtier de services est un ensemble de noeuds
finaux REST consommés par {{site.data.keyword.Bluemix_notm}}.

Lorsque vous implémentez le courtier de services, dans la réponse JSON de `GET /v2/catalog`, vous devez fournir les définitions pour
vos service et vos plans de service, notamment les informations relatives au service que vous voulez afficher. Par exemple, appuyez-vous sur le modèle
de fichier JSON suivant de réponse de catalogue (GET) :


```
"services": [
   {
      "bindable":true,
      "description":"Cool Service est une solution d'analyse et d'entreposage de données.",
      "id":"cool-service-id",
      "name":"coolservice",
      "tags":[
         "customer_dedicated"
      ],
      "metadata":{
         "displayName":"Cool Service",
         "serviceMonitorApi":"https://myservicesstatus.mybluemix.net/healthcheck/",
         "providerDisplayName":"Société Cool",
         "longDescription":"Cool Service est une solution d'analyse et d'entreposage des données. Vous pouvez placer rapidement vos données dans une base de
données structurant les données en colonne en mémoire, de génération suivante, et commencer à exécuter des requêtes
analytiques complexes.,
         "bullets":[
            {
               "title":"Rapide et simple",
               "description":"Cool Service utilise des innovations et la technologie structurant les données en colonne en mémoire, comme le traitement vectoriel parallèle et la compression afin d'analyser et de renvoyer rapidement les données pertinentes."
            },
            {
               "title":"Connectivité",
               "description":"Cool Service a été conçu pour vous permettre de vous connecter facilement à tous vos services et à toutes vos applications. Vous pouvez
commencer à analyser vos données immédiatement à l'aide d'outils familiers."
            }
         ],
         "featuredImageUrl":"http://chemin/icon_64x64.png",
         "imageUrl":"http://chemin/icon_50x50.png",
         "mediumImageUrl":"http://chemin/icon_32x32.png",
         "smallImageUrl":"http://chemin/icon_24x24.png",
         "documentationUrl":"http://chemin/documentation.html",
         "instructionsUrl":"http://chemin/servicesample.md",
         "termsUrl":"http://chemin/terms_of_agreement.pdf",
         "media":[
            {
               "type":"youtube",
               "thumbnailUrl":"http://chemin/thumbnail.png",
               "url":"http://chemin/youtube/video",
               "caption":"Apprendre à utiliser Cool Service en 60 secondes"
            },
            {
               "type":"image",
               "thumbnailUrl":"http://chemin/thumbnail.png",
               "url":"http://chemin/image_file.png",
               "caption":"Cool Service connecte des applications"
            },
            {
               "type":"video",
               "thumbnailUrl":"http://chemin/thumb.png",
               "caption":"Cool Service fonctionne avec des tableaux",
               "source":[
                  {
                     "type":"video/mp4",
                     "url":"http://chemin/video_file.mp4"
                  },
                  {
                     "type":"video/ogg",
                     "url":"http://chemin/video_file.ogg"
                  }
               ]
            }
         ]
      },
      "plans":[
         {
            "name":"smallplan",
            "description":"Schéma et espace table dédiés par instance de service sur un serveur partagé. 1 Go et 10 Go de stockage de données compressées peuvent correspondre respectivement à 5 Go et 50 Go de données non compressés selon des taux de compression typiques.",
            "free":false,
            "id":"cool-service-plan-id",
            "metadata":{
               "bullets":[
                  "1 Go minimum par instance. 10 Go maximum par instance."
               ],
               "costs":[
                  {
                     "unitId":"INSTANCES_PAR_MOIS",
                     "unit":"PAR MOIS",
                     "partNumber":"D15UTLL"
                  }
               ],
               "displayName":"Petit"
            }
         }
      ]
   }
]
}
```
{: codeblock}

**Remarque** : lorsque vous créez un courtier de services pour un environnement local ou dédié, vous devez spécifier
`customer_dedicated` dans la zone "tags" dans votre fichier JSON de définition de service. 

2\. Une fois l'API de courtier de services implémentée, accédez à **ADMINISTRATION &gt; GESTION DES CATALOGUES**.

3\. Cliquez sur **Enregistrement d'un courtier de services**.

4\. Remplissez le formulaire en entrant des valeurs dans les zones suivantes :

- Nom du courtier de services
- Adresse URL du courtier de services
- Nom d'utilisateur du courtier de services
- Mot de passe du courtier de services

5\. Cliquez sur **CONNECTER**.

6\. Passez en revue les informations relatives à votre service, notamment les plans disponibles, l'icône et la description du service.


**Remarque** : si vous devez changer les informations de catalogue pour le service, mettez à jour votre courtier de services et
lancez à nouveau le processus d'enregistrement en remplissant le formulaire.


7\. Cliquez sur **ENREGISTRER**.

8\. Choisissez d'activer tous les plans ou des plans spécifiques seulement pour le service. Tous les plans sont désactivés par défaut. 

9\. Activez l'instance de service pour toutes les organisations ou pour des organisations spécifiques.


A présent, votre service apparaît dans la catégorie Services personnalisés de votre catalogue {{site.data.keyword.Bluemix_notm}}. Accédez à
**ADMINISTRATION &gt; GESTION DES CATALOGUES** et sélectionnez la vignette dans le catalogue. Vous pouvez activer différents plans et
éditer la visibilité d'un plan pour vos organisations à tout moment.


## Administration des organisations
{: #oc_organizations}

Vous pouvez gérer vos organisations en créant et en supprimant des organisations, en ajoutant ou en retirant des responsables pour les
organisations, et en surveillant l'utilisation des quotas afin de prendre les meilleures décisions pour votre entreprise.


Cliquez sur **ADMINISTRATION &gt; ADMINISTRATION DES ORGANISATIONS**.

Vous pouvez développer et afficher diverses sections. Vous pouvez aussi passer en revue et gérer les plans d'établissement des quotas pour vos
organisations.

### Création d'organisations

Pour créer une organisation et ajouter des responsables, procédez comme suit : 

1. Cliquez sur <strong>CREATION D'ORGANISATION</strong>.
2. Entrez un nom pour l'organisation. 
3. Entrez le nom ou l'adresse électronique de la personne à ajouter en tant que responsable. Vous pouvez ajouter plusieurs responsables en entrant et en sélectionnant plusieurs noms.
4. Cliquez sur <strong>CREATION D'ORGANISATION</strong> pour sauvegarder vos modifications et créer l'organisation.

### Surveillance des quotas 

Vous pouvez développer la section Surveillance des quotas pour afficher les informations suivantes :

- Utilisation de la mémoire de l'environnement. Cette section détaille l'utilisation de la mémoire pour l'intégralité de l'environnement système.
	Le graphique fournit diverses informations, notamment la quantité de mémoire système utilisée, la quantité de mémoire système totale, le quota utilisé et
le quota total alloué. La liste de termes suivante définit les types d'utilisation de la mémoire qui sont affichés dans le graphique :

	<dl>
	<dt><strong>Mémoire système utilisée</strong></dt>
	<dd>Quantité de mémoire physique utilisée par votre environnement.</dd>
	<dt><strong>Mémoire système totale</strong></dt>
	<dd>Quantité de mémoire physique totale qui est disponible dans votre environnement.</dd>
	<dt><strong>Quota déployé</strong></dt>
	<dd>Quantité de mémoire allouée à toutes les applications déployées dans toutes les organisations. La somme du quota déployé peut dépasser la quantité de
mémoire système totale physique pour votre environnement. Par exemple, si la quantité de mémoire système totale est de 16 Go et que vous allouez 4 Go de mémoire à chaque organisation pour cinq organisations
différentes, le quota total est supérieur à la quantité de mémoire système totale qui vous a été allouée pour toutes les organisations. Cependant, dans la plupart des cas, les organisations n'utilisent pas le quota total qui leur est alloué individuellement. De plus, les organisations
n'utilisent pas toutes la totalité de leur quota d'allocation de mémoire simultanément. </dd>
	<dt><strong>Total quota</strong></dt>
	<dd>Quantité de mémoire totale qui est allouée dans toutes les organisations.</dd>
	</dl>

- Utilisation de la mémoire de l'organisation. Cette section détaille l'utilisation de la mémoire au niveau de l'organisation. Vous pouvez afficher le quota total et le
quota déployé pour chaque organisation. Le graphique fournit des informations triées en fonction de l'utilisation de la mémoire la plus élevée par
organisation ; par défaut, l'organisation qui utilise la quantité de mémoire la plus élevée est répertoriée en premier. Vous pouvez effectuer un tri en
fonction du paramètre **Utilisation de la mémoire la plus élevée** et du paramètre **Allocation de mémoire
superflue**. 

	<dl>
	<dt><strong>Utilisation de la mémoire la plus élevée</strong></dt>
	<dd>Utilisez cette option pour identifier l'organisation qui utilise la quantité de mémoire la plus élevée. Effectuez un tri par utilisation de la mémoire la plus élevée pour identifier les organisations qui utilisent la quantité de mémoire la plus élevée. La liste est triée par quota déployé. </dd>
	<dt><strong>Allocation de mémoire superflue</strong></dt>
	<dd>Utilisez cette option pour identifier les organisations dont le plan d'établissement des quotas est supérieur aux besoins.
	Effectuez un tri par allocation de mémoire superflue pour identifier les organisations qui utilisent la quantité de mémoire la plus faible par rapport au
quota qui leur a été alloué. </dd>
	</dl>

### Ajustement des plans d'établissement des quotas 

Afin de changer le plan d'établissement des quotas pour une organisation, procédez comme suit : 

<ol>
<li>Cliquez dans le graphique sur la barre correspondant à l'organisation que
vous voulez éditer dans la section Utilisation de la mémoire de l'organisation ou sélectionnez le nom de l'organisation dans la section Liste des
organisations. </li>
<li>Dans la page Gérer l'organisation, vous pouvez changer le plan d'établissement des quotas, modifier le nom de l'organisation, et ajouter ou retirer des responsables. <br />
<p><strong>Remarque</strong> : vous recevez un message si vous sélectionnez un plan d'établissement des quotas qui n'est pas suffisant pour l'utilisation en
cours pour l'organisation. </p>
</li>
<li>Pour sauvegarder les modifications que vous avez apportées dans la page Gérer l'organisation, cliquez sur <strong>SAUVEGARDER</strong>.</li>
</ol>

### Gestion de vos organisations depuis la liste des organisations 

Dans la section Liste des organisations, vous pouvez afficher toutes les organisations de l'environnement
{{site.data.keyword.Bluemix_notm}}, et vous pouvez effectuer des actions pour des organisations individuelles en cliquant sur le nom de
l'organisation. 

- Pour supprimer une organisation, cliquez sur l'icône **Supprimer** ![Supprimer](images/icon_trash.svg) dans
la colonne Actions. 
- Afin d'afficher le plan d'établissement des quotas et l'utilisation pour une organisation, cliquez sur le nom de l'organisation dans la liste.
La page **Gérer les organisations** de l'organisation sélectionnée affiche les informations suivantes sur l'utilisation :


  - Le nombre de services utilisés 
  - Le nombre de routes utilisées 
  - Un graphique du quota de mémoire qui représente le quota utilisé et le quota non utilisé 
  - Un graphique de l'allocation des applications qui indique quelles sont les applications incluses dans le quota de mémoire utilisé 
  - Un graphique de l'utilisation des applications mesurée qui représente un rapport sur trois mois du nombre de Go/heure consommé par application
déployée. Vous pouvez sélectionner **Vue de liste** afin d'afficher les données pour toutes les applications, notamment l'allocation de
mémoire par application et la consommation de Go/heure mesurée pour les trois derniers mois.


- Pour éditer le nom de l'organisation et ajouter ou retirer des responsables, cliquez sur le nom de l'organisation dans la liste et suivez les
invites à l'écran. 

## Gestion des utilisateurs et des droits
{: #oc_useradmin}

Vous pouvez ajouter des utilisateurs à votre instance {{site.data.keyword.Bluemix_notm}} depuis le registre d'utilisateurs de votre société via
LDAP. Vous pouvez ajouter des utilisateurs individuels ou des groupes d'utilisateurs et
afficher les droits d'utilisateur. Si vous disposez du droit `Admin`, vous pouvez également définir et gérer les droits des autres
utilisateurs. Cliquez sur **ADMINISTRATION &gt; USER ADMINISTRATION**.

La page User Administration affiche tous les utilisateurs pour l'instance locale ou dédiée.
Les droits de chaque utilisateur sont affichés. Les droits peuvent être les suivants : aucun, `Admin`, `Catalogue`,
`Connexion`, `Rapports` et `Utilisateurs`. Ils peuvent être activés, ou l'utilisateur peut se voir attribuer l'accès
`view` (afficher) ou `write` (écrire) pour le droit, comme représenté par les icônes. Voir [Droits](#permissions) pour la description de chaque type et l'explication des icônes.

Effectuez l'une des opérations suivantes :

* Localisez des utilisateurs. Vous pouvez localiser des utilisateurs dans le tableau à l'aide de la zone **Rechercher**.
* Ajoutez des utilisateurs. Si vous disposez du droit `Admin` ou du droit `Utilisateurs` avec l'accès
`write` (écrire), vous pouvez ajouter des utilisateurs. Pour ajouter un utilisateur ou un groupe d'utilisateurs, cliquez sur
**Ajouter un seul utilisateur** ou **Ajouter un groupe d'utilisateurs**. Dans la zone
**Rechercher**, entrez un nom d'utilisateur ou un nom de groupe à rechercher et sélectionnez
l'organisation à laquelle ajouter l'utilisateur ou le groupe d'utilisateurs dans la liste des **organisations**. Lorsque vous trouvez l'utilisateur ou
le groupe à ajouter, cliquez sur le nom d'utilisateur, puis cliquez sur **Ajouter un utilisateur** ou **Ajouter des utilisateurs**.
Les
groupes de plus de 50 utilisateurs sont ajoutés via un travail par lots en arrière-plan. Lorsque l'opération d'ajout aboutit, l'utilisateur ou le groupe est ajouté à la table pour que vous puissiez l'afficher et le rechercher. Lorsque des utilisateurs sont ajoutés, aucun droit ne leur est affecté.
* Editez les droits et les organisations. Si vous disposez du droit `Admin`, vous pouvez éditer les droits et les organisations
pour d'autres utilisateurs. Pour éditer les droits, localisez l'utilisateur et cliquez sur son nom. Pour activer ou désactiver des droits, sélectionnez
l'une des options suivantes dans la fenêtre qui s'ouvre :
	* Sélectionnez **Activé** dans la liste pour activer un droit.
	* Sélectionnez **Read** dans la liste pour que l'utilisateur dispose de l'accès `view` (afficher en lecture
seule) pour ce droit ou **Write** pour qu'il dispose de l'accès `write` (écrire, c'est-à-dire éditer, ajouter
ou
supprimer) pour ce droit.
	* Sélectionnez **désactivé** pour désactiver le droit.
Pour éditer des organisations, choisissez l'une des options
suivantes :
	* Ajoutez l'utilisateur à une organisation en utilisant la zone de recherche afin de localiser une organisation, puis en sélectionnant les options de
votre choix et en cliquant sur **Ajouter**.
	* Retirez un utilisateur d'une organisation en cliquant sur l'icône ![Retirer, représentée par le signe moins](images/icon_remove.svg).
Une fois que vous avez terminé, cliquez sur
**Sauvegarder**.
* Retirez des utilisateurs. Si vous disposez du droit `Admin` ou du droit `Utilisateurs` avec l'accès `write` (écrire), vous pouvez retirer des utilisateurs.
Pour supprimer un utilisateur, localisez-le et cliquez sur l'icône ![Supprimer](images/icon_trash.svg) puis sur
**Retirer**.

### Droits
{: #permissions}

Les droits suivants peuvent être accordés aux utilisateurs :

| **Droit d'utilisateur** | **Description** |       
|-----------------|-------------------|
| Admin | Les utilisateurs disposant du droit `Admin` peuvent éditer les droits des autres utilisateurs. |
| Catalogue | Les utilisateurs disposant du droit `Catalogue` peuvent afficher (accès `view`) ou modifier (accès `write`) les services qui sont disponibles dans l'instance locale ou dédiée. |  
| Connexion | Les utilisateurs disposant du droit `Connexion` sont autorisés à voir la page Administration. Sans ce droit, les utilisateurs ne peuvent pas voir l'option de menu Administration. |
| Rapports | Les utilisateurs disposant du droit `Rapports` peuvent afficher (accès `view`) ou modifier
(accès `write`) les rapports de sécurité. |
| Utilisateurs  | Les utilisateurs disposant du droit `Utilisateurs` peuvent afficher (accès `view`) la liste des
utilisateurs ou
ajouter ou retirer (accès `write`) des utilisateurs. Ce droit ne vous permet pas de définir des droits pour d'autres utilisateurs.|

*Tableau 5. Droits*

Les droits peuvent être activés, ou l'utilisateur peut se voir attribuer l'accès `view` (afficher) ou `write`
(écrire) pour ces droits, comme représenté par les icônes suivantes :

* L'icône ![Activé, représentée par une coche](images/icon_enabled.svg) à côté d'un droit signifie que le droit est activé.
* L'icône ![Afficher, représentée par un oeil](images/icon_read.svg) signifie que l'utilisateur dispose de l'accès `view` (afficher en lecture seule) pour ce droit.
* L'icône ![Ecrire, représentée par un crayon](images/icon_write.svg) signifie que l'utilisateur dispose de l'accès `write` (écrire, c'est-à-dire éditer, ajouter ou supprimer) pour ce droit.

## Gestion des utilisateurs avec l'API REST Admin
{: #usingadminapi}

Vous pouvez utiliser l'API REST `Admin` afin d'ajouter et de retirer des utilisateurs pour votre instance
{{site.data.keyword.Bluemix_notm}}.
Les noeuds finaux de l'API REST
`Admin` et les réponses JSON sont fournis sur une base expérimentale afin de permettre des opérations de base depuis une ligne de
commande. Les noeuds finaux et les adresses URL qui figurent dans les exemples de cette documentation peuvent changer ou être abandonnés dans un délai
court.

Les outils ci-après sont requis pour l'utilisation des exemples qui suivent. Vous pouvez également choisir d'utiliser d'autres outils.
* cURL, pour entrer les demandes d'API REST sous forme de commandes. cURL est un utilitaire gratuit que vous pouvez utiliser pour envoyer des
demandes HTTP à un serveur
et recevoir les réponses du serveur via une interface de ligne de commande. Vous pouvez le télécharger depuis le
[site de téléchargement cURL](http://curl.haxx.se/download.html){: new_window}.
* Python, pour utiliser l'outil JSON de formatage de Python. Cet outil facultatif transforme le texte JSON en entrée en sortie facile à lire. Vous pouvez télécharger Python depuis le [site des téléchargements Python](https://www.python.org/downloads){: new_window}.

### Connexion à la console d'administration

Pour pouvoir exécuter des requêtes d'API `Admin`, vous devez vous connecter à la console d'administration. Si vous disposez du droit
`Admin` ou du droit `Utilisateurs` avec l'accès `write` (écrire), vous pouvez ajouter ou retirer des
utilisateurs. Vous devez disposer du droit `Admin` pour éditer les droits des autres utilisateurs.

Pour vous connecter à la console d'administration, vous pouvez utiliser l'authentification d'accès de base sur le noeud final
`https://<votre_hôte>.ibm.com/login`. Le serveur renvoie un cookie avec votre session. Vous utilisez ce cookie pour toutes les opérations avec la console d'administration.

**Remarque :** la session n'est plus valide si elle n'est pas utilisée pendant quelques heures.

Pour vous connecter à la console d'administration, exécutez la commande suivante :

`curl --user <id_utilisateur>:<mot_de_passe> -c ./cookies.txt --header "Accept: application/json"
https://<votre_hôte>.ibm.com/login | python -m json.tool`
{: codeblock}

<dl class="parml">

<dt class="pt dlterm">--user <em>id_utilisateur</em>:<em>mot_de_passe</em></dt>
<dd class="pd">Accepte l'ID utilisateur et le mot de passe et envoie un en-tête d'autorisation de base.</dd>


<dt class="pt dlterm">-c <em>nom_fichier</em></dt>
<dd class="pd">Stocke l'ID utilisateur et le mot de passe spécifiés sous forme de cookie dans le fichier spécifié.</dd>


<dt class="pt dlterm">--header</dt>
<dd class="pd">Envoie un en-tête Accept.</dd>

</dl>

Voici un exemple de sortie pour
cette commande :
```
{
    "message": "Logged in",
    "name": {
        "familyName": "*nom*",
        "givenName": "*prénom*"
    }
}
```
{: screen}

### Liste des organisations
{: #listingorg}

Lorsque vous ajoutez un utilisateur, vous devez spécifier une organisation. Vous pouvez utiliser l'API REST `Admin` pour
répertorier toutes les organisations. Vous devez disposer du droit `Utilisateurs` avec l'accès `read` (lire) pour
pouvoir
répertorier les organisations. Pour répertorier toutes les organisations, exécutez la commande suivante :

`curl -b ./cookies.txt https://<votre_hôte>.ibm.com/codi/v1/organizations | python -m json.tool`
{: codeblock}

<dl class="parml">

<dt class="pt dlterm">-b <em>nom_fichier</em></dt>
<dd class="pd">Transmet l'ID utilisateur et le mot de passe stockés précédemment avec l'option <samp class="ph codeph">-c</samp> dans le fichier sur le serveur HTTP sous forme
de cookie.</dd>

</dl>

Pour chaque organisation, les résultats incluent les informations suivantes :
* `"guid"`, identificateur global unique de l'organisation
* `"name"`, nom de l'organisation

Voici un exemple de sortie pour
cette commande :
```
{
     "resources": [
         {
             "guid": "05af098d-d476-4fb0-8b87-a84350e72af3",
             "name": "org-1"
         },
         {
             "guid": "5129a5a8-37c2-4ee4-a9b2-bebae3531db5",
             "name": "org-2"
         },

		 		 ....

		 ],
		 "total_results": 284
}
```
{: screen}

### Liste des utilisateurs
{: #listingusr}

Vous pouvez déterminer si un utilisateur a déjà été ajouté à votre environnement {{site.data.keyword.Bluemix_notm}} en utilisant l'API
REST `Admin` afin de répertorier les utilisateurs enregistrés. Vous devez disposer du droit `Utilisateurs` avec
l'accès `read` (lire) pour pouvoir répertorier les utilisateurs enregistrés. Pour répertorier tous les utilisateurs, exécutez la commande
suivante :

`curl -b ./cookies.txt https://<votre_hôte>.ibm.com/codi/v1/users | python -m json.tool`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-b <em>nom_fichier</em></dt>
<dd class="pd">Transmet l'ID utilisateur et le mot de passe stockés précédemment avec l'option <samp class="ph codeph">-c</samp> dans le fichier sur le serveur HTTP sous forme
de cookie.</dd>
</dl>

Pour chaque utilisateur enregistré, les résultats incluent les informations suivantes :
* `"first_name"` (prénom) et `"last_name"` (nom)
* `"user_id"`, ID utilisateur et adresse électronique
* `"guid"`, identificateur global unique de l'organisation.
* `"permissions"`, droits qui sont affectés à l'utilisateur pour la console d'administration.

Voici un exemple de sortie pour
cette commande :

```
{
    "next_url": "/codi/v1/users?results_per_page=100&amp;page=2",
    "prev_url": "",
    "resources": [
        {
            "active": true,
            "created_at": "2015-04-08T17:38:51.788Z",
            "created_by": "",
            "first_name": "un prénom",
            "guid": "5d5268cf-39c0-48d3-96ae-7afe928e5dd7",
            "last_name": "un nom",
            "permissions": [
                {
                    "display": "ops.admin"
                },
                {
                    "display": "ops.catalog.write"
                },
                {
                    "display": "ops.reports.write"
                },
                {
                    "display": "ops.catalog.read"
                },
                {
                    "display": "ops.users.write"
                },
                {
                    "display": "ops.reports.read"
                },
                {
                    "display": "ops.login"
                },
                {
                    "display": "ops.users.read"
                }
            ],
            "user_id": "un_id@us.ibm.com"
        },
		 		 ...


     }
    ],
    "total_pages": 395,
    "total_results": 39421
}

```
{: screen}

### Ajout d'un utilisateur

Vous pouvez utiliser l'API REST `Admin` pour ajouter des utilisateurs à l'instance {{site.data.keyword.Bluemix_notm}}. Vous
devez disposer du droit `Utilisateurs` avec l'accès `write` (écrire) pour pouvoir ajouter des utilisateurs.

Vous pouvez ajouter un utilisateur ou une liste d'utilisateurs. Vous pouvez ajouter des utilisateurs à une seule organisation ou à plusieurs
organisations. Pour ajouter un utilisateur, vous devez fournir les informations suivantes :

* Prénom et nom de l'utilisateur. Indiquez les valeurs `"first_name"` et `"last_name"` figurant dans
[Liste des utilisateurs](index.html#listingusr).
* Adresse électronique et ID utilisateur. Indiquez la valeur `"user_id"` figurant dans [Liste des
utilisateurs](index.html#listingusr) pour l'adresse électronique et l'ID utilisateur.
* `"guid"`. Indiquez l'identificateur global unique de l'organisation figurant dans [Liste des organisations](index.html#listingorg).

Vous
fournissez les informations dans un fichier JSON.

`curl -b ./cookies.txt https://<votre_hôte>.ibm.com/codi/v1/users | python -m json.tool`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-b <em>nom_fichier</em></dt>
<dd class="pd">Transmet l'ID utilisateur et le mot de passe stockés précédemment avec l'option <samp class="ph codeph">-c</samp> dans le fichier sur le serveur HTTP sous forme
de cookie.</dd>
</dl>

<ol>
<li>Créez un fichier JSON qui contient les informations dans un format JSON correct.
<p>Par exemple, créez un fichier appelé `user.json` dont le contenu est le suivant :</p>
<pre>
{
    "members": [
        {
            "emails": [
                "un_id_utilisateur@domaine.com"
            ],
            "first_name": "Un_prénom",
            "last_name": "Un_nom",
            "user_id": "un_id_utilisateur@domaine.com"
        }
    ],
    "organization_roles": [
        {
            "id": "7a891f9c-e4e7-46c7-8b4e-dffaa7eb3bcd"
        }
    ]
}
</pre>
</li>
<li>Envoyez le contenu du fichier JSON au noeud final de l'utilisateur en exécutant la commande suivante :<br/><br/>
<code>
curl -v -b ./cookies.txt -X POST -H "Content-Type: application/json" -d @./user.json https://<votre_hôte>.ibm.com/codi/v1/users
</code>
</li>
</ol>

<dl class="parml">

<dt class="pt dlterm">-v </dt>
<dd class="pd">Spécifie la sortie prolixe.</dd>


<dt class="pt dlterm">-X POST</dt>
<dd class="pd">Spécifie une demande POST, qui remplace la demande GET par défaut.</dd>


<dt class="pt dlterm">-H "Content-Type: application/json"</dt>
<dd class="pd">Spécifie l'en-tête content-type, qui dans ce cas est JSON.</dd>


<dt class="pt dlterm">-d *données*</dt>
<dd class="pd">Spécifie les données, dans ce cas le fichier `user.json`, à envoyer dans la demande POST au serveur HTTP.</dd>

</dl>



Voici un exemple de sortie pour
cette commande :

```
* Connected to localhost (127.0.0.1) port 3000 (#0)
 > POST /codi/v1/users HTTP/1.1
 > User-Agent: curl/7.37.1
 > Host: localhost:3000
 > Accept: */*
 > Cookie: opsConsole.sid=s%3AHLcwKGumyEb3IxREmikDOG3ATKD5xYMe.jfjWAa1tJC0rGghpeV8RPHqE2JaFVL4ZFIJbQpSC%2FAI
 > Content-Type: application/json
 > Content-Length: 333
 >
 * upload completely sent off: 333 out of 333 bytes
 < HTTP/1.1 201 Created
 < x-powered-by: Express
 < vary: X-HTTP-Method-Override
 < content-type: application/json
 < date: Wed, 22 Apr 2015 19:32:54 GMT
 < connection: close
 < transfer-encoding: chunked
 < X-Time_Check: Proxy Time: 5612 msec
 ```
{: screen}

### Retrait d'un utilisateur

Vous pouvez utiliser l'API REST `Admin` pour retirer des utilisateurs de l'instance {{site.data.keyword.Bluemix_notm}}. Vous
devez disposer du droit `Utilisateurs` avec l'accès `write` (écrire) pour pouvoir retirer des utilisateurs.

Pour retirer un utilisateur, vous devez
fournir l'ID de l'utilisateur. Exécutez la commande suivante :

`curl -v -b ./cookies.txt -X DELETE
https://<votre_hôte>.ibm.com/codi/v1/users?user_id=<un_id_utilisateur@domaine.com>`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-X DELETE</dt>
<dd class="pd">Spécifie une demande DELETE.</dd>
</dl>

Voici un exemple de sortie pour
cette commande :

```
 * connect to ::1 port 3000 failed: Connection refused
 *   Trying 127.0.0.1...
 * Connected to localhost (127.0.0.1) port 3000 (#0)
 > DELETE /codi/v1/users?user_id=exampleuser@domain.com HTTP/1.1
 > User-Agent: curl/7.37.1
 > Host: localhost:3000
 > Accept: */*
 > Cookie: opsConsole.sid=s%3AHLcwKGumyEb3IxREmikDOG3ATKD5xYMe.jfjWAa1tJC0rGghpeV8RPHqE2JaFVL4ZFIJbQpSC%2FAI
 >
 < HTTP/1.1 201 Created
 < x-powered-by: Express
 < content-type: application/json
 < date: Wed, 22 Apr 2015 21:01:09 GMT
 < connection: close
 < transfer-encoding: chunked
 < X-Time_Check: Proxy Time: 1922 msec
 <
 ```
{: screen}


## API de service personnalisée
{: #servicebrokerapi}

Vous pouvez utiliser trois interfaces de programmation (API) pour enregistrer ou créer un nouveau service, mettre à jour un service et supprimer un service.

Toutes les API sont relatives à <code>https://console.&lt;sous-domaine&gt;.bluemix.net/</code>.

<dl>
<dt><strong>&lt;sous-domaine&gt;</strong></dt>
<dd>Cette valeur est le nom de votre instance locale ou dédiée. Le nom de sous-domaine pour votre instance {{site.data.keyword.Bluemix}} a été affecté au cours du processus
d'intégration.</dd>
</dl>

## Enregistrement d'un nouveau service

Utilisez l'API et les exemples de code suivants pour enregistrer un nouveau service.

### Route
{: #registerroute}

```
POST /codi/v1/serviceBrokers
```
{: screen}

### Demande
{: #registerrequest}

| **Nom** | **Description** |
|-----------------|-------------------|
| name | Nom du courtier de services. |
| auth_username | Nom d'utilisateur utilisé pour se connecter au courtier de services. |
| auth_password | Mot de passe utilisé pour se connecter au courtier de services. |
| broker_url | URL utilisée pour se connecter au courtier de services. |
| owningOrganization | Organisation initiale avec laquelle enregistrer le service sur la liste blanche. |

*Tableau 6. Zones*

#### Corps
{: #registerbody}

```
{
  "name" : "Nom du courtier de services",
  "auth_username" : "nom d'utilisateur",
  "auth_password" : "mot de passe",
  "broker_url" : "https://broker.comp.com",
  "owningOrganization" : "ORG"
}
```
{: screen}

#### En-têtes
{: #registerheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### Réponse
{: #registerresponse}

#### Statut
{: #registerstatus}

```
201 Created
```
{: screen}

#### Corps
{: #registerbody2}

```
{
  "entity": {
    "name": "Nom du courtier de services",
    "broker_url": "https://provision-broker.comp.bluemix.net/bmx/provisioning/brokers/2063580064-8f23230c-7f36-4ce5-a298-2ab4108f1120",
    "auth_username": "nom d'utilisateur",
    "space_guid": null
  },
  "warnings": [],
  "metadata": {
    "guid": "49f3adcc-ecc2-46fa-83c1-03322f04b3b1",
    "created_at": "2015-12-07T19:51:50Z",
    "updated_at": null,
    "url": "/v2/service_brokers/49f3adcc-ecc2-46fa-83c1-03322f04b3b1"
  }
}
```
{: screen}

## Mise à jour d'un service

Utilisez l'API et les exemples de code suivants pour mettre à jour un service.

### Route
{: #updateroute}

`PUT /codi/v1/serviceBrokers`
{: screen}

### Demande
{: #updaterequest}

| **Nom** | **Description** |
|-----------------|-------------------|
| name | Nom du courtier de services. Ce nom ne peut pas varier du nom avec lequel a été créé le service. |
| auth_username | Nom d'utilisateur utilisé pour se connecter au courtier de services. |
| auth_password | Mot de passe utilisé pour se connecter au courtier de services. |
| broker_url | URL utilisée pour se connecter au courtier de services. |
| owningOrganization | Organisation initiale avec laquelle enregistrer le service sur la liste blanche. |

*Tableau 7. Zones*

#### Corps
{: #updatebody}

```
{
  "name" : "Nom du courtier de services",
  "auth_username" : "nom d'utilisateur",
  "auth_password" : "nouveau mot de passe",
  "broker_url" : "https://broker.comp.com",
  "owningOrganization" : "ORG"
}
```
{: screen}

#### En-têtes
{: #updateheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### Réponse
{: #updateresponse}

#### Statut
{: #updatestatus}

```
201 Created
```
{: screen}

#### Corps
{: #updatebody2}

```
{
  "entity": {
    "name": "Nom du courtier de services",
    "broker_url": "https://provision-broker.dys0.bluemix.net/bmx/provisioning/brokers/2063580064-d11bdd84-7556-469f-858d-2098b531f7f2",
    "auth_username": "nom d'utilisateur",
    "space_guid": null
  },
  "warnings": [],
  "metadata": {
    "guid": "2cbdb812-d37f-443b-894a-a96de31e5c38",
    "created_at": "2015-12-07T20:11:08Z",
    "updated_at": "2015-12-07T20:11:19Z",
    "url": "/v2/service_brokers/2cbdb812-d37f-443b-894a-a96de31e5c38"
  }
}
```
{: screen}

## Suppression d'un service

Utilisez l'API et les exemples de code suivants pour supprimer un service.

| **Nom** | **Description** |
|-----------------|-------------------|
| name | Nom du courtier de services. Ce nom ne peut pas varier du nom avec lequel a été créé le service. |

*Tableau 8. Paramètre*

### Route

```
DELETE /codi/v1/serviceBrokers?name=nom du courtier de services
```
{: screen}

### Demande
{: #deleterequest}

#### En-têtes
{: #deleteheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### Réponse
{: #deleteresponse}

#### Statut
{: #deletestatus}

```
204 No Content
```
{: screen}

## Gestion des utilisateurs avec l'interface de ligne de commande cf
{: #usingadmincli}

Vous pouvez gérer les utilisateurs pour votre environnement {{site.data.keyword.Bluemix_notm}} via l'interface de ligne de commande
Cloud Foundry, avec le plug-in d'interface de ligne de commande d'administration {{site.data.keyword.Bluemix_notm}}. Par exemple, vous pouvez ajouter des utilisateurs depuis
un registre LDAP.

Avant de commencer, installez l'interface de ligne de commande cf. Le plug-in d'interface de ligne de commande d'administration {{site.data.keyword.Bluemix_notm}} requiert cf version 6.11.2 ou ultérieure. [Télécharger l'interface de ligne de commande Cloud Foundry](https://github.com/cloudfoundry/cli/releases){: new_window}

**Restriction :** l'interface de ligne de commande Cloud Foundry n'est pas prise en charge par Cygwin. Utilisez-la dans une fenêtre de ligne de commande autre que Cygwin.

### Ajout du plug-in d'interface de ligne de commande d'administration {{site.data.keyword.Bluemix_notm}}

Une fois l'interface de ligne de commande cf installée, vous pouvez ajouter le plug-in d'interface de ligne de commande d'administration
{{site.data.keyword.Bluemix_notm}}.

**Remarque** : si vous avez déjà installé le plug-in d'administration {{site.data.keyword.Bluemix_notm}}, il peut être
nécessaire de le désinstaller, de supprimer le référentiel, puis de réinstaller le plug-in afin de bénéficier des mises à jour les plus récentes.


Procédez comme suit pour ajouter le référentiel et installer le plug-in :

<ol>
<li>Pour ajouter le référentiel de plug-in d'administration {{site.data.keyword.Bluemix_notm}}, exécutez la commande suivante :
<br/><br/> <code> cf add-plugin-repo BluemixAdmin https://console.&lt;sous-domaine&gt;.bluemix.net/cli </code><br/><br/>
<dl class="parml">
<dt class="pt dlterm">&lt;sous-domaine&gt;</dt>
<dd class="pd">Sous-domaine de l'adresse URL pour votre instance {{site.data.keyword.Bluemix_notm}}.</dd>
</dl>
</li>
<li>Pour installer le plug-in d'interface de ligne de commande d'administration {{site.data.keyword.Bluemix_notm}}, exécutez la commande suivante :<br/><br/> <code>
cf install-plugin bluemix-admin-cli -r BluemixAdmin
</code>
</li>
</ol>

Pour afficher la liste des commandes, exécutez la
commande suivante :

`cf plugins`
{: codeblock}

Pour obtenir de l'aide supplémentaire sur une commande, utilisez l'option `-help`.

Pour plus d'informations sur l'utilisation du plug-in d'interface de ligne de commande d'administration {{site.data.keyword.Bluemix_notm}}, voir [Administration {{site.data.keyword.Bluemix_notm}}](../cli/plugins/bluemix_admin/index.html).
