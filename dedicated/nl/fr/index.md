---

 

copyright:

  years: 2015, 2016

 

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

#{{site.data.keyword.Bluemix_notm}} dédié
{: #dedicated}

*Dernière mise à jour : 7 mars 2016*


{{site.data.keyword.Bluemix}} est une plateforme à normes ouvertes reposant sur le cloud qui permet de construire, d'exécuter et de gérer des applications. Avec l'environnement {{site.data.keyword.Bluemix_notm}} dédié, vous bénéficiez de la puissance et de la simplicité de {{site.data.keyword.Bluemix_notm}}&mdash;et ce, dans votre propre environnement SoftLayer dédié, connecté de façon sécurisée à l'environnement {{site.data.keyword.Bluemix_notm}} public et à votre propre réseau.
{:shortdesc}

Tous les déploiements dédiés de {{site.data.keyword.Bluemix_notm}} incluent les fonctions et les avantages suivants gratuitement : réseau
privé virtuel (VPN), réseau local virtuel (VLAN) privé, connectivité avec votre protocole LDAP, possibilité d'optimiser des applications et des bases de
données sur
site existantes, sécurité sur site 24 heures sur 24 et 7 jours sur 7, matériel dédié et support standard. 

L'environnement {{site.data.keyword.Bluemix_notm}} dédié inclut un catalogue privé qui affiche les services dédiés disponibles exclusivement pour vous. Il
inclut également des services supplémentaires qui sont à votre disposition depuis l'environnement {{site.data.keyword.Bluemix_notm}} public.

L'environnement {{site.data.keyword.Bluemix_notm}} dédié est fourni avec tous les contextes d'exécution
{{site.data.keyword.Bluemix_notm}} et 64 Go de mémoire pour les ressources de traitement. 

De plus, vous disposez d'un ensemble de services et de composants inclus ou facultatifs.



| **Type**        | **Nom **            | **Description** |      
|-----------------|-------------------|-------------------|
|Inclus | Contextes d'exécution {{site.data.keyword.Bluemix_notm}} | Utilisez des contextes d'exécution pour que votre application soit
opérationnelle rapidement, sans qu'il soit nécessaire de configurer et de gérer des machines et des systèmes d'exploitation. Vous pouvez utiliser tous les
contextes d'exécution {{site.data.keyword.Bluemix_notm}} dans votre instance {{site.data.keyword.Bluemix_notm}} dédiée.|
| Inclus | {{site.data.keyword.autoscaling}} | Augmentez ou diminuez dynamiquement la capacité de traitement de votre application en fonction de règles. Avec ce service, vous bénéficiez d'une utilisation illimitée dans votre environnement {{site.data.keyword.Bluemix_notm}} dédié. |
| Facultatif | {{site.data.keyword.datacshort}} | Ce service fournit une grille de données en mémoire qui prend en charge des scénarios de mise en cache distribuée pour vos applications. Il inclut 50 Go de mémoire cache interne. |
| Facultatif | {{site.data.keyword.mql}} | {{site.data.keyword.mqlfull}} for {{site.data.keyword.Bluemix_notm}} est un service de messagerie reposant sur le cloud qui fournit une messagerie souple et facile à utiliser pour les applications {{site.data.keyword.Bluemix_notm}}. {{site.data.keyword.mql}} constitue une solution d'administration simple pour la messagerie. Vous pouvez utiliser {{site.data.keyword.mql}} pour rendre vos applications plus réactives et plus évolutives, et vous pouvez partager et décharger le travail entre des applications à l'aide d'une API puissante et simple. |
| Facultatif | {{site.data.keyword.dashdbshort}} | Utilisez dashDB pour stocker les données relationnelles, notamment les types spéciaux tels que les données géospatiales. Ensuite, analysez ces données avec l'analyse intégrée avancée ou SQL, comme l'analyse prédictive et l'exploration de données, l'analyse avec R et l'analyse géospatiale. |
|Facultatif | {{site.data.keyword.APIM}} | Utilisez le service {{site.data.keyword.APIMfull}} pour composer des API, les gérer et les diffuser sur les réseaux sociaux. Vous pouvez importer des API avec des ressources en utilisant une adresse URL de proxy ou en assemblant des données à partir de sources de données HTTP. L'avantage avec le service {{site.data.keyword.APIM}} est que vous pouvez gérer la façon dont vos API sont utilisées. |
|Facultatif | {{site.data.keyword.SecureGateway}} | Le service {{site.data.keyword.SecureGateway}} fournit un moyen sécurisé pour connecter des applications {{site.data.keyword.Bluemix_notm}} à des emplacements distants sur site ou dans le cloud.  |
|Facultatif | {{site.data.keyword.cloudant}} | {{site.data.keyword.cloudant}} fournit l'accès à une couche de données JSON NoSQL
entièrement gérée toujours active. Ce service est compatible avec CouchDB et accessible via une interface HTTP facile à utiliser pour les modèles
d'application mobile et Web. |

*Tableau 1. Services dédiés*

## Architecture de l'environnement {{site.data.keyword.Bluemix_notm}} dédié 
{: #dedicatedarch}

L'environnement {{site.data.keyword.Bluemix_notm}} dédié s'appuie sur SoftLayer pour que vous puissiez bénéficier de l'infrastructure de cloud la plus performante. Chaque centre de données applique des contrôles rigoureux de sécurité 24 heures sur 24, 7 jours sur 7. Vous et IBM accédez à votre instance {{site.data.keyword.Bluemix_notm}} dédiée via un tunnel de réseau privé virtuel et un réseau local virtuel privé.

{{site.data.keyword.Bluemix_notm}} dédié réside sur votre réseau via une connexion de réseau privé virtuel ou
une connexion réseau directe. Votre matériel à service exclusif peut être configuré dans n'importe quel centre de données SoftLayer, n'importe où dans le
monde. {{site.data.keyword.IBM_notm}} gère la plateforme dédiée et les services dédiés pour que vous puissiez vous consacrer à la construction d'applications personnalisées. De plus, {{site.data.keyword.IBM_notm}} se charge de l'intégralité de la maintenance des instances dédiées au cours d'une fenêtre de maintenance
que vous choisissez.

![{{site.data.keyword.Bluemix_notm}} dédié](images/dedicated.png "{{site.data.keyword.Bluemix_notm}} dédié")

*Figure 1. Diagramme détaillé de l'environnement {{site.data.keyword.Bluemix_notm}} dédié*

Les environnements {{site.data.keyword.Bluemix_notm}} dédiés appliquent les mêmes normes de sécurité que l'environnement {{site.data.keyword.Bluemix_notm}} public en termes d'infrastructure, de fonctionnement et de sécurité physique. Toutefois, l'accès des développeurs à l'environnement {{site.data.keyword.Bluemix_notm}} dédié est contrôlé par vos stratégies LDAP, qui peuvent être configurées par l'équipe {{site.data.keyword.Bluemix_notm}} lorsqu'elle configure votre environnement. Dans l'environnement dédié, vous pouvez gérer les rôles utilisateur et les droits. Voir [Gestion des utilisateurs et des droits](../admin/index.html#oc_useradmin) pour des détails.


##Configuration de l'environnement {{site.data.keyword.Bluemix_notm}} dédié
{: #setupdedicated}

L'environnement {{site.data.keyword.Bluemix_notm}} dédié a été conçu pour fournir une version privée de l'offre d'environnement {{site.data.keyword.Bluemix_notm}} public. Vous pouvez utiliser les services et les contextes d'exécution {{site.data.keyword.Bluemix_notm}} pour répondre à vos besoins informatiques dans un compte SoftLayer hébergé par IBM.

IBM fournit l'accès à l'environnement {{site.data.keyword.Bluemix_notm}} dédié par le biais d'une connexion sécurisée par mot de passe. Vous pouvez accéder aux services, aux contextes d'exécution et aux ressources associées, et déployer et retirer des applications {{site.data.keyword.Bluemix_notm}}. IBM utilise plusieurs emplacements SoftLayer afin de distribuer l'environnement {{site.data.keyword.Bluemix_notm}} dédié, pour que l'emplacement de votre version privée puisse être proche de vous.

Pour configurer votre version privée de {{site.data.keyword.Bluemix_notm}} :

<ol>
<li>Prenez contact avec votre représentant de compte IBM attitré ou <a href="https://console.ng.bluemix.net/?direct=classic/#/contactUs/cloudOEPaneId=contactUs" target="_blank">avec {{site.data.keyword.Bluemix_notm}}</a> pour commencer.</li>
<li>Décidez avec IBM du tarif correspondant à votre instance {{site.data.keyword.Bluemix_notm}} dédiée. Le prix mensuel dépend des services dédiés que vous voulez utiliser, et comprend un abonnement à tous les services {{site.data.keyword.Bluemix_notm}} publics. Vous recevez ensuite une facture pour tous les éléments que vous utilisez au-delà de ce contrat d'abonnement.</li>
<li>Identifiez les échéances pour chaque phase de configuration de votre instance {{site.data.keyword.Bluemix_notm}} dédiée. Pour obtenir des informations sur chaque phase et les tâches concernées, voir <a href="index.html#rolesresponsibilities" target="_blank">Rôles et responsabilités de l'environnement {{site.data.keyword.Bluemix_notm}} dédié</a>.</li>
<li>Sélectionnez l'<a href="http://www.softlayer.com/data-centers" target="_blank">emplacement du centre de données SoftLayer</a> pour votre instance dédiée. Ensuite, votre plateforme dédiée et votre compte sont créés. Pour votre compte, vous identifiez les personnes de votre organisation à affecter aux rôles nécessaires à la configuration et à l'exécution de votre instance dédiée. Pour obtenir des informations sur les rôles que vous attribuez, voir <a href="index.html#rolesresponsibilities" target="_blank">Rôles et responsabilités de l'environnement {{site.data.keyword.Bluemix_notm}} dédié</a>.
</li>
<li>Définissez et établissez la connectivité du réseau entre votre réseau d'entreprise et votre instance {{site.data.keyword.Bluemix_notm}} dédiée.
	<ol type="a">
	<li>IBM installe une infrastructure de surveillance et de sécurité pour l'instance dédiée.</li>
	<li>IBM installe les services dédiés exclusifs que vous avez sélectionnés.</li>
	<li>Vous fournissez la configuration réseau et des noeuds finaux pour des éléments, tels que les adresses IP ou les pare-feux, et l'accès à LDAP pour l'intégration à {{site.data.keyword.Bluemix_notm}}.</li>
	</ol>
</li>
<li>Identifiez et affectez des rôles pour votre équipe d'administration pour l'environnement.
	<ol type="a">
	<li>IBM configure l'accès réseau et LDAP en fonction des éléments que vous avez fournis. L'accès administrateur est accordé aux contacts que vous désignez. Vous devez également désigner un contact pour le support et la facturation.</li>
	<li>IBM configure un catalogue mixte dans votre environnement dédié qui répertorie vos services dédiés. Ce catalogue comprend des services supplémentaires qui sont à votre disposition depuis l'environnement {{site.data.keyword.Bluemix_notm}} public. Vous pouvez choisir les services publics qui satisfont les exigences pour votre activité selon vos critères de sécurité et de confidentialité des données.</li>
	<li>Vous validez la configuration du réseau et du pare-feu ainsi que l'accès et le noeud final LDAP.</li>
	</ol>
</li>
</ol>

Vous pouvez vous attendre à obtenir un processus similaire à la liste suivante pour le déploiement initial et la configuration de votre environnement. Pour obtenir des détails sur les responsables de chaque tâche, voir [Rôles et responsabilités](../dedicated/index.html#rolesresponsibilities).

<ol>
<li>Vous sélectionnez le centre de données à utiliser pour héberger votre instance dédiée. Pour plus d'informations sur les options de centre de données, voir <a href="http://www.softlayer.com/data-centers" target="_blank">Emplacement du centre de données SoftLayer</a>.</li>
<li>Vous spécifiez les noms de domaine pour le déploiement et les ID que vous souhaitez utiliser. Vous obtenez trois domaines lorsque vous configurez votre instance {{site.data.keyword.Bluemix_notm}}. Vous sélectionnez le préfixe pour <code>*masociété*.*région*.bluemix.net</code> et <code>*masociété*.*région*.mybluemix.net</code>. Puis vous choisissez le nom complet du troisième domaine.<br />
<p>Vous pouvez choisir autant de domaines personnalisés que vous le souhaitez. Cependant, vous êtes chargé des certificats de ces domaines personnalisés. Pour plus d'informations sur la création d'un domaine personnalisé, voir <a href="../manageapps/updapps.html#domain">Création et utilisation d'un domaine personnalisé</a>.</p></li>
<li>Vous identifiez un propriétaire du compte public utilisé pour représenter votre société dans l'environnement {{site.data.keyword.Bluemix_notm}} public. IBM utilise ce compte pour le suivi de l'utilisation des services mixtes.</li>
<li>Vous sélectionnez le type de connexion sécurisée à votre centre de données. Vous pouvez effectuer votre sélection entre SoftLayer VPN, SoftLayer Direct Link et AT&T Net Bond.</li>
<li>Vous décidez s'il y aura un accès à votre environnement dédié à partir de l'Internet public.</li>
<li>Vous sélectionnez le type d'authentification qui sera utilisé. Vous pouvez sélectionner ID IBM ou Active Directory. Pour plus d'informations sur l'utilisation et l'enregistrement d'un ID IBM, voir la page <a href="https://www.ibm.com/account/profile/us?page=regfaqhelp#4">Help and FAQ</a>.
</li>
<li>Vous identifiez et affectez des rôles pour votre équipe d'administration pour l'environnement. Pour obtenir des informations sur les rôles que vous devez attribuer, voir <a href="index.html#rolesresponsibilities" target="_blank">Rôles et responsabilités de l'environnement {{site.data.keyword.Bluemix_notm}} dédié</a>.</li>
<li>IBM déploie la plateforme de base qui comprend les environnements d'exécution élastiques, la console, les fonctions d'administration et de surveillance.</li>
<li>IBM configure votre accès administrateur à l'environnement.</li>
<li>Vous pouvez commencer à utiliser votre instance dédiée surveillée par l'équipe IBM chargée des opérations pour répondre aux alertes.</li>
</ol>

Une fois votre instance {{site.data.keyword.Bluemix_notm}} configurée, vous pouvez surveiller et gérer votre instance {{site.data.keyword.Bluemix_notm}} via la page Administration. Pour plus d'informations, voir [Gestion de l'environnement {{site.data.keyword.Bluemix_notm}} local et de l'environnement Bluemix dédié](../administer/index.html#mng). Pour plus d'informations sur les mises à niveau et la maintenance, voir [Gestion de votre instance dédiée](index.html#maintaindedicated).

##Rôles et responsabilités
{: #rolesresponsibilities}

Si vous configurez un compte {{site.data.keyword.Bluemix_notm}} dédié, vous identifiez les personnes de votre organisation à affecter aux rôles nécessaires à la configuration et à l'exécution de votre instance.

###Rôles

La liste suivante répertorie les rôles et les responsabilités des clients que vous attribuez :

<dl>
<dt>**Contact du service Achats (Procurement focal)**</dt>
<dd>Collabore avec l'interlocuteur IBM afin d'établir votre environnement {{site.data.keyword.Bluemix_notm}} dédié, notamment pour identifier les
personnes autorisées dans votre organisation à travailler sur un aspect du projet. La personne disposant de ce rôle assume un rôle de gestion de projet et supervise la sélection de pattern, les accords commerciaux et les accords relatifs à l'accès aux ressources du client. Le contact du service Achats est le contact général pour la configuration de l'instance dédiée et le suivi du processus de déploiement.</dd>
<dt>**Agent de conformité (Compliance officer)**</dt>
<dd>Collabore avec l'interlocuteur IBM pour sélectionner une topologie et une option de déploiement répondant à vos exigences en matière de sécurité. La
personne disposant de ce
rôle collabore avec le consultant en conformité d'IBM pour déterminer quels sont les patterns de déploiement qui permettent d'atteindre les
objectifs de conformité.</dd>
<dt>**Spécialiste réseau (Network specialist)**</dt>
<dd>Collabore avec l'interlocuteur IBM sur les plans de réseau pour le déploiement {{site.data.keyword.Bluemix_notm}}. La personne disposant de ce rôle passe en revue les spécifications de réseau requises par IBM et collabore avec IBM afin d'établir un plan
d'implémentation. A la fin de la phase d'installation et de vérification, elle confirme que la configuration du réseau est conforme aux standard
d'entreprise.</dd>
<dt>**Contact DevOps (DevOps focal)**</dt>
<dd>Collabore avec l'interlocuteur IBM afin de planifier et d'appliquer les mises à jour de maintenance nécessaires pour la plateforme, les services et
les contextes d'exécution {{site.data.keyword.Bluemix_notm}}. La personne disposant de ce rôle collabore également avec l'interlocuteur IBM sur la
configuration de votre instance {{site.data.keyword.Bluemix_notm}} dédiée.</dd>
</dl>

Vos ingénieurs commerciaux collaborent avec votre interlocuteur IBM désigné pour le compte Bluemix dédié et d'autres spécialistes IBM pour s'assurer
que vous disposez toujours du support
dont vous avez besoin. Votre interlocuteur IBM désigné pour le compte Bluemix dédié est votre point de contact unique au sein de l'équipe de
support de développement {{site.data.keyword.Bluemix_notm}} et il effectue les tâches suivantes :

<ul>
<li>Il permet l'adoption rapide de votre environnement {{site.data.keyword.Bluemix_notm}} dédié.</li>
<li>Il distribue des ressources d'activation et de formation utiles permettant d'améliorer votre autonomie.</li>
<li>Il entretient une relation à long terme entre vous et le développement {{site.data.keyword.Bluemix_notm}}, le support et les services que
vous utilisez.</li>
</ul>

L'équipe en charge des opérations et du support {{site.data.keyword.Bluemix_notm}} qui travaille avec vous sur votre instance
{{site.data.keyword.Bluemix_notm}} peut accéder à votre environnement local, mais n'utilise cette possibilité que pour les
raisons suivantes :

<ul>
<li>Pour répondre à des alertes et effectuer une maintenance opérationnelle</li>
<li>Pour tenter de reproduire un problème qui a été signalé dans un ticket d'incident</li>
</ul>

###Responsabilités

De la configuration de votre environnement à la maintenance permanente, diverses tâches doivent être effectuées. Le tableau ci-dessous répertorie les
tâches requises ainsi que le propriétaire pour l'exécution de la tâche au cours des phases de création, de progression et d'achèvement.

La phase de création permet d'établir l'environnement {{site.data.keyword.Bluemix_notm}} dédié. Les objectifs principaux de cette phase
sont les suivants :

- Réviser l'accord financier et établir les dates de jalon pour la distribution.
- Créer la plateforme {{site.data.keyword.Bluemix_notm}} et fournir l'accès aux contextes d'exécution et aux services.
- Définir et établir la connectivité du réseau entre votre réseau d'entreprise et les opérations {{site.data.keyword.Bluemix_notm}}.
- Identifier et affecter des rôles pour votre équipe d'administration.

*Tableau 1. Tâches de la phase de création*

| **Tâche** | **Détails de la tâche** | **Partie responsable** |
|----------|------------------|-----------------------|
|Définir les normes de conformité | Identifier les normes du gouvernement, de l'industrie et de l'entreprise propriétaire qui sont requises pour
l'environnement. | Client |
|Créer un plan d'intégration de conformité et de sécurité | Créer un plan d'intégration et de sécurité qui inclut les coûts, la planification et les
ressources qui sont nécessaires pour assurer la conformité et la sécurité. | IBM |
|Approbation du plan de conformité | Approbation du plan de conformité. | Client |
|Créer la taille de l'environnement |  	Créer la taille de l'environnement en fonction de choix prédéfinis qui prennent en compte les objectifs de haute
disponibilité et de reprise après incident, ainsi que la mise à disposition initiale des services et de l'agent DEA nécessaires pour la prise en charge des
applications créées avec la plateforme. Vous collaborez avec IBM pour définir par exemple les bases de données qui sont nécessaires, les services qui sont proposés dans le catalogue mixte du
client, etc. | IBM et le client partagent la
responsabilité |
|Sélectionner une architecture | Sélectionner une architecture en fonction de choix prédéfinis qui prennent en compte les exigences de haute disponibilité
et de reprise après incident. | IBM |
|Définir les objectifs de reprise après incident | Définir les exigences de reprise après incident pour l'environnement. | Client |
|Créer un plan de reprise après incident | Définir le plan de reprise après incident et vous consulter. IBM crée un modèle de reprise après incident et vous
consulte pour que vous puissiez donner votre feedback et approuver le plan. | IBM et le client partagent la
responsabilité |
|Créer un plan de sauvegarde et de reprise | Créer un plan de sauvegarde et de reprise qui définit la fréquence et les exigences pour une distribution sur
site et hors site de la sauvegarde. IBM sauvegarde des composants de plateforme, des services IBM, des métadonnées de service incluant des rôles
utilisateur, etc. Vous sauvegardez les données propres à l'application desquelles vous êtes en charge. | IBM et le client partagent la
responsabilité |
|Identifier les outils pour la détection d'événements et l'identification des problèmes. | Identifier les outils IBM et tiers utilisés pour la
détection d'événements et l'identification des problèmes au niveau de la plateforme {{site.data.keyword.Bluemix_notm}}. | IBM |
|Définir un plan d'escalade | Définir le plan d'escalade pour analyser les besoins et résoudre les événements détectés depuis les composants de
surveillance. | IBM |
|Signer des accords relatifs à l'infrastructure, la plateforme et le support | Signer le contrat d'abonnement incluant les dispositions financières
pour l'environnement. Signer l'accord de surveillance du réseau et de la sécurité. Signer le contrat d'assistance. | Client |
|Procurer l'environnement | Procurer les ressources de traitement, le réseau et le stockage, notamment le réseau local virtuel des services et de base
pour héberger {{site.data.keyword.Bluemix_notm}}, des services non virtualisés pour héberger Data Power, et le pare-feu SoftLayer. Fournir
l'infrastructure pour autoriser un tunnel de réseau privé virtuel. | Client |
|Installer les composants de plateforme, d'application, de surveillance et de gestion | Installer, configurer et vérifier les composants de plateforme,
comme BOSH Director, le contrôleur de cloud, le gestionnaire de santé, la messagerie, les routeurs, les agents DEA et les fournisseurs de services, ainsi
que les composants de surveillance qui sont définis dans le plan d'escalade et de détection des problèmes.
 | IBM |
|Installer et configurer les composants de sécurité | Installer et configurer les composants de sécurité qui sont liés dans le plan de surveillance et
d'escalade, notamment IBM QRadar, le coffre des identifications, le système de prévention des intrusions, IBM BigFix et IBM Security
Privileged Identity
Management. | IBM |
|Installer et configurer des composants personnalisés |  	Installer et configurer des composants personnalisés qui se trouvent hors de la portée du
produit
et des services {{site.data.keyword.Bluemix_notm}}. | Client |
|Etablir la configuration réseau initiale | Etablir la configuration réseau initiale, notamment les pare-feux, DataPower, Fortigate et le serveur
DNS. | IBM |
|Connecter le pipeline {{site.data.keyword.Bluemix_notm}} | Connecter le pipeline de distribution continue et l'intégration continue
{{site.data.keyword.Bluemix_notm}} avec des référentiels IBM. | IBM |
|Personnaliser les composants externes de la solution | Personnaliser les équilibreurs de charge pour les scénarios de reprise après incident. | Client |
|Installer la solution de réseau privé virtuel | Installer la solution de réseau privé virtuel bidirectionnelle. | IBM |
|Configurer le serveur de connexion | Configurer le serveur de connexion en vue de son utilisation avec l'annuaire LDAP d'entreprise. | IBM |
|Effectuer le suivi du statut des contrôles de sécurité, de conformité et d'audit  | Effectuer le suivi du statut jusqu'à ce que tous les outils et
processus soient en place pour que la conformité identifiée soit assurée. | Client |
|Réviser l'infrastructure physique | Réviser les locaux physiques qui hébergent les composants de la solution afin d'identifier d'éventuelles menaces et
réviser les contrôles de sécurité pour la protection du centre de données. | Client |
|Inspecter le logiciel de surveillance | Inspecter les composants de surveillance et de gestion tels que définis dans le plan d'escalade et
d'identification des problèmes. | Client |
|Inspecter le système d'exploitation | Vérifier que l'image de système d'exploitation satisfait les normes de conformité. IBM fournit l'accès à l'image de
système d'exploitation. | IBM et le client partagent la
responsabilité |

Ensuite vient la phase de progression. Elle décrit la relation de collaboration qui existe entre vous et le cloud IBM. Les objectifs principaux de
cette phase sont les suivants :

- Réviser la capacité et coordonner les ajustements nécessaires.
- Réviser les améliorations de la maintenance et de la plateforme.
- Coordonner les activités relatives à la résolution des problèmes et à l'analyse de la cause première.

*Tableau 2. Tâches de la phase de progression*

| **Tâche** | **Détails de la tâche** | **Partie responsable** |
|----------|------------------|-----------------------|
|Réviser les rapports de capacité hebdomadaire | Réviser les rapports de capacité hebdomadaires et prendre des mesures correctives, si nécessaire. | Client |
|Créer des projections sur une base mensuelle | Collecter des informations et créer une projection sur une base mensuelle pour la capacité et la
consommation. | IBM et le client partagent la
responsabilité |
|Réviser les projections de capacité | Réviser les projections de capacité car elle sont liées à des événements externes pouvant avoir un impact sur
la capacité ainsi que sur de nouveaux déploiements anticipés des applications. Collaborer avec IBM pour réviser les projections et le plan en conséquence. | IBM et le client partagent la
responsabilité |
|Réviser les projections | Réviser les projections de capacité car elles sont liées à des événements externes pouvant avoir un impact sur la capacité. | Client |
|Ajuster la capacité |  Ajouter ou retirer de la capacité au fur et à mesure que vos besoins changent. | IBM |
|Publier la maintenance et les mises à jour entrantes | Créer une documentation pour la maintenance requise des composants IBM. | IBM |
|Assurer la maintenance | Collaborer avec IBM pour planifier la maintenance requise dans une fenêtre de 30 jours. Vous pouvez fournir les dates qui ne
vous conviennent pas dans la fenêtre de 30 jours ; IBM s'arrangera pour planifier la maintenance en conséquence. | IBM et le client partagent la
responsabilité |
|Echecs de mise à disposition d'adresse | Corriger les échecs de mise à disposition, le cas échéant, pour les services créés par le client qui sont
déployés dans le catalogue. | IBM |
|Effectuer une analyse réseau et IP | Effectuer des analyses réseau et IP quotidiennement et mensuellement. | IBM et le client partagent la
responsabilité |
|Fournir l'accès aux journaux d'audit | Fournit l'accès à tous les journaux d'audit de sécurité et d'administration   | IBM et le client partagent la
responsabilité |
|Mener le test | Tester régulièrement les contrôles clés des opérations et effectuer un test de pénétration tiers. | IBM et le client partagent la
responsabilité |
|Génération de rapports sur le statut, coordination de l'audit et réunions sur la conformité  | Assurer la génération de rapports sur le statut, la
coordination d'audit externe et la représentation dans des réunions sur le statut des examens de conformité. | IBM |
|Attestation d'emploi et vérification des besoins d'affaires | Effectuer l'attestation d'emploi trimestrielle et la vérification des besoins d'affaires continus
pour les interlocuteurs IBM qui ont accès à l'environnement client. | IBM |
|Résolution des vulnérabilités en matière de sécurité | Résoudre les vulnérabilités signalées en matière de sécurité sur la plateforme. | IBM |

L'étape finale d'achèvement représente la fin de la relation entre vous et {{site.data.keyword.Bluemix_notm}}. Les tâches principales de
cette phase sont les suivantes :

* Fin de l'accord financier
* Suppression de toutes les connexions réseau
* Recyclage de l'infrastructure

*Tableau 3. Tâches de la phase d'achèvement*

| **Tâche** | **Détails de la tâche** | **Partie responsable** |
|----------|------------------|-----------------------|
|Mettre fin à l'accord financier | Discuter et convenir de la fin de l'accord financier. | IBM et le client partagent la
responsabilité |
|Mettre l'environnement hors service | Désactiver l'accès à l'environnement et les données d'identification. | IBM et le client partagent la
responsabilité |
|Supprimer les connexions réseau du client | Supprimer les connexions réseau entre IBM et l'environnement client. | IBM et le client partagent la
responsabilité |
|Recycler l'infrastructure | Votre environnement est recyclé selon les processus définis par SoftLayer. | IBM |

##Gestion de votre instance dédiée
{: #maintaindedicated}

IBM gère et installe les mises à jour et les correctifs qu'elle juge nécessaires pour la plateforme, les contextes d'exécution et les services de
l'environnement {{site.data.keyword.Bluemix_notm}} dédié.

**Important** : IBM se réserve le droit d'interrompre des services afin de procéder à une maintenance d'urgence si nécessaire. IBM
peut changer les heures de maintenance planifiées et vous fera part de tels changements et de toute information relative à la maintenance d'urgence.

Les types suivants de maintenance sont requis pour l'environnement {{site.data.keyword.Bluemix_notm}}
dédié :
<dl>
<dt>**Fenêtres de maintenance standard**</dt>
<dd>Les services utilisent des fenêtres de maintenance standard prédéfinies qui peuvent entraîner leur indisponibilité. IBM n'exige pas l'approbation du client avant de procéder à la maintenance, mais tente de réduire
l'impact sur vos services.<br />
<br />
IBM envoie des messages de diffusion concernant les changements qui sont planifiés pour chaque fenêtre de maintenance par courrier électronique, par
téléphone ou par d'autres moyens.<br />
<br />
**Important** : certains services peuvent ne pas être disponibles au cours de la période de maintenance.</dd>

<dt>**Fenêtre de maintenance mensuelle**</dt>
<dd>La fenêtre de maintenance mensuelle est convenue entre vous et IBM dans une fenêtre de 21 jours. Vous pouvez fournir à IBM des dates ou des heures
spécifiques qui ne vous conviennent pas dans la fenêtre de 21 jours. IBM tente de planifier les mises à jour en dehors de ces dates ou de ces heures. En
fonction des demandes, IBM vous communique la fenêtre de maintenance planifiée. Les fenêtres de maintenance mensuelle n'ont généralement pas d'impact
sur l'environnement Bluemix dédié en cours d'exécution.
<p>L'image suivante représente le processus, de la réception d'une notification relative à une mise à jour en attente à la définition de dates ne convenant
pas, jusqu'à la réception de la notification relative à la date planifiée :
</p>
<p><img src="../local/images/maintenance_dates.png" alt="Processus de définition des dates d'indisponibilité pour une mise à jour de maintenance"></p>
<br />
**Remarque** : si vous n'avez pas besoin de définir de dates d'indisponibilité pour la mise à jour, vous pouvez l'approuver. IBM vous
signale la date planifiée pour la maintenance. <br />
<p>L'image suivante représente le processus, de la réception d'une notification relative à une mise à jour en attente à l'approbation de la mise à jour,
jusqu'à la réception de la date planifiée pour la mise à jour :
</p>
<p><img src="../local/images/maintenance_nodates.png" alt="Processus d'approbation de la mise à jour sans date d'indisponibilité"></p>
<br />
Accédez à **ADMINISTRATION > SYSTEM INFORMATION** pour afficher les mises à jour en attente, définir des dates d'indisponibilité et
approuver des mises à jour. Pour plus d'informations sur les notifications et la planification des mises à jour en attente, voir
<a href="../admin/index.html#oc_system">Affichage des informations système</a>.</dd>

<dt>**Autre**</dt>
<dd>IBM entend regrouper les maintenances pouvant avoir un impact sur vos services, en particulier la disponibilité de votre environnement
{{site.data.keyword.Bluemix_notm}} dédié, de vos
contextes d'exécution et de vos services, dans les mises à jour standard et mensuelles. D'autres fenêtres de maintenance peuvent être utilisées exceptionnellement pour la gestion de l'environnement. IBM fera de son mieux pour limiter l'impact
sur vos activités pendant ces fenêtres de maintenance et vous avertira à l'avance.</dd>
</dl>

Pour configurer la maintenance de votre instance dédiée, collaborez avec votre représentant de compte IBM afin de convenir d'une fenêtre pour la
maintenance standard.

Si un problème est signalé suite à une mise à jour de maintenance, vous décidez avec votre interlocuteur IBM s'il est judicieux pour vous qu'IBM
annule la mise à jour. Si vous parvenez à un accord, IBM annule la mise à jour afin de restaurer l'état précédent de l'environnement.

## Réponse aux incidents et support
{: #incidentresponse}

### Problèmes détectés par le client 

Si vous identifiez un problème nécessitant l'attention du centre des opérations et du support IBM, vous pouvez prendre contact avec le support de
plusieurs façons. Pour des informations sur la façon de contacter le support, voir
[Contacter le support](../support/index.html#contacting-bluemix-support-local). Selon le problème, vous et IBM travaillerez ensemble ou
individuellement pour le résoudre.


### Incidents critiques détectés par IBM 

Les incidents critiques sont des problèmes dont la résolution est urgente, comme des indisponibilités de service inattendues ou des problèmes de
stabilité ayant un impact sur votre environnement ou vos utilisateurs. Si IBM détecte un incident critique dans votre environnement, elle vous envoie une
notification sur la page **Statut**. Vous pouvez également rechercher dans la page Statut les problèmes connus pour la plateforme ou vos
services. Si vous voulez intégrer vos notifications à un service Web qui prend en charge les webhooks, voir
[Notifications et abonnements à des événements](../admin/index.html#oc_eventsubscription) pour des informations sur l'extension de vos
fonctions de notification.


![Processus de réponse à un incident](../local/images/incidentresponseprocess.png "Processus de réponse à un incident")

*Figure 2. Processus de réponse à un incident*

Selon le problème, vous et IBM travaillerez ensemble ou individuellement pour le résoudre.
En cas de question relative à l'incident ou si vous avez besoin de l'aide d'un interlocuteur IBM pour résoudre le problème, vous pouvez ouvrir un ticket de
demande de service. Pour des informations sur la façon de contacter le support, voir
[Contacter le support](../support/index.html#contacting-bluemix-support-local). 

**Remarque** : les tickets de demande de service de gravité 1 sont surveillés 24 heures sur 24, 7 jours sur 7. Les autres tickets
sont traités du dimanche 22:00 GMT au samedi 12:00 GMT. Pour plus d'informations sur la gravité des tickets de demande de service et la collaboration avec
le support, voir <a href="../support/index.html#contacting-bluemix-support-local">Contacter le support</a>.


## Reprise après incident
{: #dr}

L'environnement {{site.data.keyword.Bluemix_short}} public fournit une plateforme d'innovation disponible en permanence. Plusieurs
mesures de sécurité garantissent que vos organisations, vos espaces et vos applications sont toujours disponibles. Le déploiement d'applications dans
plusieurs zones géographiques permet une disponibilité continue qui constitue une protection contre la perte simultanée et non planifiée de plusieurs
composants matériels ou logiciels, ou la perte d'un centre de données entier, de sorte que même en cas de catastrophe naturelle dans une zone géographique,
les instances d'application {{site.data.keyword.Bluemix_notm}} publiques qui se trouvent dans d'autres zones géographiques restent disponibles.
{: shortdesc}

La reprise après incident pour l'environnement {{site.data.keyword.Bluemix_short}} dédié est possible grâce à la disponibilité continue de
vos applications, la haute disponibilité inhérente à la plateforme, et la possibilité de restaurer votre instance en cas d'échec. Vous êtes en charge de
la disponibilité continue de vos applications et pouvez la configurer en procédant au déploiement dans plusieurs régions. La haute disponibilité est
intégrée au niveau de la plateforme via des technologies incluses dans Cloud Foundry et d'autres composants. De plus, vous pouvez collaborer avec IBM pour
vous assurer que les données sont sauvegardées correctement au cas où vous auriez besoin de restaurer votre instance.

### Configuration de la disponibilité continue pour l'environnement {{site.data.keyword.Bluemix_notm}} dédié
{: #enabling}

Par défaut, l'environnement {{site.data.keyword.Bluemix_notm}} public procède au déploiement dans plusieurs zones géographiques. Toutefois,
vous devez effectuer les opérations suivantes pour activer les instances {{site.data.keyword.Bluemix_notm}} dédiées distribuées globalement :

* Assurez-vous que vos développeurs déploient les applications dans plusieurs régions, via un processus manuel ou automatisé. Les régions
doivent être séparées d'au moins 200 kilomètres pour éviter qu'une catastrophe naturelle n'ait d'impact sur deux zones géographiques.
* Configurez un équilibreur de charge global, comme Akamai ou Dyn, pour désigner des applications dans deux régions différentes au moins.

**Remarque** : les services {{site.data.keyword.Bluemix_notm}} ne prennent pas tous en charge la distribution
régionale. Lorsque vous construisez une application, si vous voulez procéder à une distribution géographique, vous devez aussi vérifier que les services
qui sont utilisés par cette application proposent la synchronisation des données comme fonction principale.

#### Déploiement des applications {{site.data.keyword.Bluemix_notm}} dédiées dans plusieurs zones géographiques
{: #deploying}

Pour procéder au déploiement dans une deuxième zone ou dans plusieurs zones, vous devez suivre un processus similaire à celui que vous avez appliqué
pour activer votre zone géographique principale :

1. Activez un nouvel environnement dédié pour héberger des instances supplémentaires de vos applications. Pour créer un environnement, prenez
contact avec votre équipe commerciale IBM afin d'initier le processus. Pour plus d'informations sur la configuration d'une instance dédiée, voir
[Configuration d'un environnement {{site.data.keyword.Bluemix_notm}} dédié](../dedicated/index.html#setupdedicated). Vous devez
vous connecter séparément pour accéder à chaque environnement. Chaque zone physique pour les environnements hébergés doit se trouver à au moins
200 kilomètres de la zone d'origine pour que la disponibilité soit assurée.
2. Procurez-vous le nom de domaine unique dans lequel votre nouvelle application déployée va être hébergée.  Par exemple, si votre domaine d'origine
est *masociété.est.bluemix.net*, vous pouvez créer un environnement local avec un nouveau domaine tel que
*masociété.ouest.bluemix.net* et procéder au déploiement dans le nouveau domaine.
3. A chaque fois que vous déployez votre application d'origine, déployez-la également dans la nouvelle zone. Pour plus d'informations sur le déploiement, voir [Téléchargement de votre application](../starters/upload_app.html).


#### Activation d'un équilibreur de charge global pour l'environnement {{site.data.keyword.Bluemix_notm}} dédié
{: #glb}

Un équilibreur de charge global assure non seulement la disponibilité continue et est requis pour la reprise après incident, mais présente également
de nombreux avantages :

* Il achemine les utilisateurs vers la région {{site.data.keyword.Bluemix_notm}} la plus proche par défaut
* Il procède à l'acheminement en fonction des performances
* Il dirige de façon sélective un pourcentage du trafic vers une nouvelle version d'application
* Il fournit la reprise en ligne sur site en fonction du diagnostic d'intégrité de la région
* Il fournit la reprise en ligne sur site en fonction du diagnostic d'intégrité de l'application
* Il utilise le routage pondéré entre les noeuds finaux

Vous pouvez choisir un équilibreur de charge global tel qu'Akamai ou Dyn. Pour plus d'informations sur l'utilisation d'Akamai comme équilibreur de
charge global, voir [Global traffic management](https://www.akamai.com/us/en/solutions/products/web-performance/global-traffic-management.jsp){: new_window}. Pour
plus d'informations sur l'utilisation de Dyn comme équilibreur de charge global, voir [4 Reasons Businesses Are Taking Global Load Balancing to the Cloud](http://dyn.com/blog/4-reasons-businesses-are-taking-global-load-balancing-to-the-cloud/){: new_window}.

### Haute disponibilité
{: #ha}

En plus d'assurer la disponibilité continue, {{site.data.keyword.Bluemix_notm}} fournit également la haute disponibilité sur la plateforme en
utilisant des technologies intégrées dans Cloud Foundry, Docker et d'autres composants.

Ces technologies incluent les points suivants :

<dl>
<dt>L'évolutivité dans Cloud Foundry</dt>
<dd>Un agent <a href="https://docs.cloudfoundry.org/concepts/architecture/execution-agent.html" target="_blank">Droplet Execution Agent
(DEA)</a> Cloud Foundry effectue des diagnostics d'intégrité pour les applications qu'il exécute. S'il existe un problème lié à l'application ou à l'agent DEA lui-même, il déploie des instances supplémentaires de l'application dans un autre agent DEA
afin de traiter le problème. Pour plus d'informations, voir
la page relative à la <a href="https://docs.cloudfoundry.org/concepts/high-availability.html" target="_blank">configuration de CF pour la haute
disponibilité avec redondance</a>.
</dd>
<dt>Redondance SoftLayer</dt>
<dd>Avec SoftLayer dans les environnements dédiés, les données de chaque cluster de stockage en cloud sont écrites plusieurs fois et les clusters de
stockage sont configurés avec des capacités de rétablissement automatique en cas d'échec d'unité. En cas de problème lié à un serveur virtuel, SoftLayer
tente de redémarrer le serveur virtuel sur un autre hôte.
</dd>
<dt>Sauvegarde des métadonnées</dt>
<dd>Les métadonnées sont sauvegardées avec SoftLayer EVault Backup dans une zone qui se trouve à au moins 200 kilomètres.</dd>
</dl>

##Restauration de votre instance dédiée
{: #restorededicated}

Les paramètres, les métadonnées et les configurations de l'environnement {{site.data.keyword.Bluemix_notm}} dédié sont sauvegardés
régulièrement en vue d'une indisponibilité non planifiée dans l'environnement. Les données pour lesquelles vous êtes en charge de la
sauvegarde incluent des données d'application, des données de services de base de données de cloud et des magasins d'objets.

Dans le cadre de la sauvegarde des données, qui inclut les métadonnées système et les configurations, IBM effectue les tâches suivantes :

<ul>
<li>Elle chiffre toutes les copies de sauvegarde et gère les clés de chiffrement</li>
<li>Elle surveille et gère l'activité de sauvegarde</li>
<li>Elle fournit les fichiers de sauvegarde chiffrés</li>
<li>Elle restaure les données demandées</li>
<li>Elle gère les conflits de planification entre les opérations de sauvegarde et de gestion des correctifs</li>
</ul>

Etant donné que la protection des données privées est essentielle, IBM a besoin de votre aide pour la gestion des fichiers de sauvegarde, de sorte
que ceux-ci ne soit pas déplacés hors de vos centres de données. En particulier, IBM demande que vous effectuiez les tâches suivantes :

<ul>
<li>Vous devez déplacer une copie de vos données de sauvegarde chiffrées hors site, comme vous le feriez pour d'autres données de sauvegarde que vous gérez.</li>
<li>Vous devez fournir les fichiers de sauvegarde à l'opérateur IBM si la restauration est nécessaire.</li>
</ul>

# rellinks
## general
* [Discover: {{site.data.keyword.Bluemix_notm}} Dedicated](http://www.ibm.com/cloud-computing/bluemix/hybrid/dedicated/)
* [Nouveautés de {{site.data.keyword.Bluemix_notm}}](../whatsnew/index.html)
* [Glossaire {{site.data.keyword.Bluemix_notm}}](glossary/index.html)
* [Gestion de l'environnement {{site.data.keyword.Bluemix_notm}} local et de l'environnement {{site.data.keyword.Bluemix_notm}} dédié](../admin/index.html#mng)
* [Contacter le service de support](../troubleshoot/getting_customer_support.html#bluemix_support)
