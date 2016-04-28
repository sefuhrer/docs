---

 

copyright:

  years: 2015, 2016

 

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}

#{{site.data.keyword.Bluemix_notm}} dedicado
{: #dedicated}

*Última actualización: 7 de marzo de 2016*


{{site.data.keyword.Bluemix}} es una plataforma de estándares abiertos basada en la nube para crear, ejecutar y gestionar apps. Con {{site.data.keyword.Bluemix_notm}} Dedicado, obtendrá la potencia y la simplicidad de {{site.data.keyword.Bluemix_notm}}&mdash; en su propio entorno dedicado de SoftLayer, que se conecta de forma segura tanto al entorno público de {{site.data.keyword.Bluemix_notm}} como a su propia red.
{:shortdesc}

Los despliegues dedicados de {{site.data.keyword.Bluemix_notm}} incluyen los siguientes beneficios y características sin ningún coste adicional: VPN, red de área local virtual (VLAN) privada, cortafuegos, conectividad con LDAP, optimización de las apps y bases de datos locales existentes, seguridad local 24 horas al día/7 días por semana, hardware dedicado y soporte estándar. 

{{site.data.keyword.Bluemix_notm}} dedicado incluye un catálogo privado que muestra los servicios dedicados que tiene disponibles de forma exclusiva. También incluye servicios adicionales sindicados disponibles que puede utilizar desde {{site.data.keyword.Bluemix_notm}} público.

{{site.data.keyword.Bluemix_notm}} dedicado se suministra con todos los tiempos de ejecución de {{site.data.keyword.Bluemix_notm}} incluidos y a los 64 GB de memoria de recursos de cálculo. 

Además, hay un conjunto de servicios y componentes que se incluyen o son opcionales. 


| **Tipo**        | **Nombre**            | **Descripción** |      
|-----------------|-------------------|-------------------|
|Incluido | Tiempos de ejecución de {{site.data.keyword.Bluemix_notm}}  | Utilice los tiempos de ejecución para que su app esté activa y en funcionamiento con rapidez, sin necesidad de configurar y gestionar las máquinas ni los sistemas operativos. Todos los tiempos de ejecución de {{site.data.keyword.Bluemix_notm}} están disponibles para utilizarlos en la instancia de {{site.data.keyword.Bluemix_notm}} dedicada. |
| Incluido | {{site.data.keyword.autoscaling}} | Aumente o reduzca de forma dinámica la capacidad de cálculo de la app en función de políticas. Con este servicio, dispone de un uso ilimitado del entorno {{site.data.keyword.Bluemix_notm}} dedicado. |
| Opcional | {{site.data.keyword.datacshort}} | Este servicio proporciona una cuadrícula de datos en memoria que da soporte a casos de ejemplo de memoria caché distribuidos para las apps. Incluye 50 GB de memoria caché en memoria. |
| Opcional | {{site.data.keyword.mql}} | {{site.data.keyword.mqlfull}} for {{site.data.keyword.Bluemix_notm}} es un servicio de mensajería basado en la nube que proporciona mensajería flexible y fácil de usar para apps {{site.data.keyword.Bluemix_notm}}. {{site.data.keyword.mql}} proporciona una solución fácil de administrar para la mensajería. Puede utilizar {{site.data.keyword.mql}} para aumentar el nivel de respuesta y de escalado de sus apps y puede compartir y descargar trabajo entre apps con una sencilla y potente API. |
| Opcional | {{site.data.keyword.dashdbshort}} | Utilice dashDB para almacenar datos relacionales, que incluye tipos especiales como datos geoespaciales. A continuación, analice esos datos con SQL o análisis integrados avanzados como análisis predictivo y minería de datos, análisis con R y análisis geoespaciales. |
|Opcional | {{site.data.keyword.APIM}} | Utilice el servicio de {{site.data.keyword.APIMfull}} para componer, gestionar y socializar API. Puede importar API con recursos utilizando un URL de proxy o ensamblando datos de fuentes de datos HTTP. La ventaja de utilizar el servicio de {{site.data.keyword.APIM}} es que puede gestionar cómo se utilizan las API. |
|Opcional | {{site.data.keyword.SecureGateway}} | El servicio {{site.data.keyword.SecureGateway}} proporciona una forma segura para conectar las aplicaciones de {{site.data.keyword.Bluemix_notm}} a ubicaciones remotas locales o en la nube.  |
|Opcional | {{site.data.keyword.cloudant}} | {{site.data.keyword.cloudant}} proporciona acceso a una capa de datos JSON de NoSQL
completamente gestionada que siempre está activa. Este servicio es compatible con CouchDB y se puede acceder a través de una interfaz HTTP fácil de utilizar para los modelos de aplicación web y móvil. |

*Tabla 1. Servicios dedicados*

## Arquitectura de {{site.data.keyword.Bluemix_notm}} dedicado
{: #dedicatedarch}

{{site.data.keyword.Bluemix_notm}} dedicado se basa en SoftLayer para ofrecerle una infraestructura de nube de alto rendimiento. Cada centro de datos dispone de servicios de seguridad 24 horas, 7 días `por semana y rigurosos controles. El cliente e IBM acceden a la instancia dedicada de {{site.data.keyword.Bluemix_notm}} a través de un túnel VPN y de una VLAN privada.

{{site.data.keyword.Bluemix_notm}} dedicado forma parte de su red con una conexión de red directa o VPN. El hardware de un solo arrendatario se puede configurar en cualquier centro de datos de SoftLayer que exista. {{site.data.keyword.IBM_notm}} gestiona la plataforma dedicada y los servicios dedicados, de esta manera puede centrarse en crear apps personalizadas. Además, {{site.data.keyword.IBM_notm}} realiza todo el mantenimiento a instancias dedicadas durante una ventana de mantenimiento que haya seleccionado.

![{{site.data.keyword.Bluemix_notm}} dedicado](images/dedicated.png "{{site.data.keyword.Bluemix_notm}} dedicado")

*Figura 1. Diagrama detallado de {{site.data.keyword.Bluemix_notm}} dedicado*

Los entornos de {{site.data.keyword.Bluemix_notm}} dedicado tiene los mismos estándares de seguridad que {{site.data.keyword.Bluemix_notm}} público en la infraestructura y en la seguridad física y operativa. Sin embargo, el acceso de desarrollador a {{site.data.keyword.Bluemix_notm}} dedicado está controlado por políticas de LDAP, que las pueden configurar el equipo de {{site.data.keyword.Bluemix_notm}} al configurar el entorno. En el entorno dedicado, puede gestionar los roles y permisos de usuarios. Consulte [Gestión de usuarios y permisos](../admin/index.html#oc_useradmin) para ver más detalles.


##Configuración de {{site.data.keyword.Bluemix_notm}} dedicado
{: #setupdedicated}

{{site.data.keyword.Bluemix_notm}} dedicado se ha diseñado para proporcionar una versión privada del producto {{site.data.keyword.Bluemix_notm}} público. Puede utilizar los servicios y tiempos de ejecución de {{site.data.keyword.Bluemix_notm}} para satisfacer sus requisitos de cálculo en una cuenta SoftLayer alojada en IBM.

IBM le proporciona acceso a {{site.data.keyword.Bluemix_notm}} dedicado mediante un inicio de sesión protegido por contraseña. Puede acceder a los servicios, tiempos de ejecución y recursos asociados, y desplegar y eliminar apps {{site.data.keyword.Bluemix_notm}}. IBM se beneficia de varias ubicaciones de SoftLayer para ofrecer {{site.data.keyword.Bluemix_notm}} dedicado, de modo que puede obtener su versión privada en una ubicación cercana.

Para configurar su versión privada de {{site.data.keyword.Bluemix_notm}}:

<ol>
<li>Póngase en contacto con el representante designado de la cuenta de IBM o con el contacto de <a href="https://console.ng.bluemix.net/?direct=classic/#/contactUs/cloudOEPaneId=contactUs" target="_blank"> {{site.data.keyword.Bluemix_notm}}</a> para empezar a trabajar.</li>
<li>Trabaje con IBM, a cargo del cliente, para configurar la instancia de {{site.data.keyword.Bluemix_notm}} dedicado. El cargo mensual se basa en los servicios dedicados que desee utilizar, más una suscripción a todos los servicios públicos de {{site.data.keyword.Bluemix_notm}}. Recibirá una factura por todo lo que utilice por encima del acuerdo de suscripción.</li>
<li>Identifique plazos límite para cada fase de la configuración de la instancia de {{site.data.keyword.Bluemix_notm}} dedicado. Para obtener información sobre cada fase y las tareas implicadas, consulte <a href="index.html#rolesresponsibilities" target="_blank">Roles y responsabilidades de {{site.data.keyword.Bluemix_notm}} dedicados</a>.</li>
<li>Seleccione la <a href="http://www.softlayer.com/data-centers" target="_blank">ubicación del centro de datos SoftLayer</a> para su instancia dedicada. A partir de aquí se crea la plataforma dedicada y la cuenta. Para la cuenta, identifique las personas de la organización para los roles necesarios para configurar y activar la instancia dedicada. Para obtener información sobre los roles que asigne, consulte <a href="index.html#rolesresponsibilities" target="_blank">Roles y responsabilidades de {{site.data.keyword.Bluemix_notm}} dedicados</a>.
</li>
<li>Defina y establezca la conectividad de red entre su red corporativa y la instancia de {{site.data.keyword.Bluemix_notm}} dedicado.
	<ol type="a">
	<li>IBM instala la infraestructura de supervisión y seguridad para la instancia dedicada.</li>
	<li>IBM instala los servicios dedicados de arrendatario único que seleccione.</li>
	<li>El cliente proporciona la configuración de la red y puntos finales para elementos tales como direcciones IP o cortafuegos y acceso a LDAP para la integración en {{site.data.keyword.Bluemix_notm}}.</li>
	</ol>
</li>
<li>Identifique y asigne roles para el equipo de administración del entorno.
	<ol type="a">
	<li>IBM configura el acceso a la red y LDAP en función de lo que proporcione el usuario. Se ofrece acceso de administración a los contactos que designe el cliente. También debe designar un contacto para soporte y facturación.</li>
	<li>IBM configura un catálogo sindicado en el entorno dedicado para mostrar los servicios dedicados. El catálogo sindicado incluye servicios adicionales sindicados y disponibles para que los utilice el usuario a partir de {{site.data.keyword.Bluemix_notm}} público. Tiene la opción de decidir qué servicios públicos cumplen los requisitos de su empresa en función de sus criterios de privacidad de datos y de seguridad.</li>
	<li>El cliente debe validar la configuración de la red y del cortafuegos, además del punto final LDAP y el acceso.</li>
	</ol>
</li>
</ol>

Puede prever un proceso similar a la siguiente lista para el despliegue y la configuración iniciales de su entorno. Para obtener detalles sobre la persona responsable de cada tarea, consulte [Roles y responsabilidades](../dedicated/index.html#rolesresponsibilities).

<ol>
<li>Se selecciona el centro de datos a utilizar para que aloje la instancia dedicada. Para obtener información sobre las opciones del centro de datos, consulte <a href="http://www.softlayer.com/data-centers" target="_blank">Ubicación del centro de datos SoftLayer</a>.</li>
<li>Debe especificar los nombres de dominio para el despliegue, y los ID que desea utilizar. Obtendrá tres dominios al configurar la instancia de {{site.data.keyword.Bluemix_notm}}. Seleccione el prefijo para <code>*mycompany*.*region*.bluemix.net</code> y <code>*mycompany*.*region*.mybluemix.net</code>. Y puede elegir el nombre completo del tercer dominio.<br />
<p>Puede elegir tantos dominios personalizados como desee. Sin embargo, el usuario es responsable de los certificados para los dominios personalizados. Para obtener información sobre cómo crear el dominio personalizado, consulte <a href="../manageapps/updapps.html#domain">Creación y utilización de un dominio personalizado</a>.</p></li>
<li>Debe identificar un propietario para la cuenta pública que se utiliza para representar la empresa en {{site.data.keyword.Bluemix_notm}} público. IBM utiliza esta cuenta para realizar el seguimiento del uso de los servicios sindicados.</li>
<li>Seleccione el tipo de conexión segura en el centro de datos. Puede seleccionar desde SoftLayer VPN, SoftLayer Direct Link y AT&T Net Bond.</li>
<li>Decida si habrá acceso al entorno dedicado desde la Internet pública.</li>
<li>Seleccione el tipo de autenticación que se utilizará. Puede seleccionar desde el ID de IBM o Active Directory. Para obtener información sobre cómo utilizar y registrarse para un ID de IBM, consulte la página <a href="https://www.ibm.com/account/profile/us?page=regfaqhelp#4">Ayuda y preguntas frecuentes</a>.
</li>
<li>Identifique y asigne roles para el equipo de administración del entorno. Para obtener información sobre los roles que debe asignar, consulte <a href="index.html#rolesresponsibilities" target="_blank">Roles y responsabilidades de {{site.data.keyword.Bluemix_notm}} dedicados</a>.</li>
<li>IBM despliega la plataforma principal que incluye los tipos de ejecución elásticos, la consola, la función de administración y la supervisión.</li>
<li>IBM configura el acceso administrativo al entorno.</li>
<li>Puede empezar utilizando la instancia dedicada que está supervisada por el equipo de operaciones de IBM para responder a las alertas.</li>
</ol>

Una vez que se configure la instancia de {{site.data.keyword.Bluemix_notm}}, puede supervisar y gestionar la instancia de {{site.data.keyword.Bluemix_notm}} utilizando la página Administración. Para obtener más información, consulte [Gestión de {{site.data.keyword.Bluemix_notm}} local y dedicado](../administer/index.html#mng). Para obtener información sobre las actualizaciones y el mantenimiento, consulte [Mantenimiento de la instancia dedicada](index.html#maintaindedicated).

##Roles y responsabilidades
{: #rolesresponsibilities}

Si establece una cuenta de {{site.data.keyword.Bluemix_notm}} dedicado, puede identificar a las personas de su organización para los roles necesarios para configurar y activar la instancia.

###Roles

La lista siguiente muestra los roles y responsabilidades de cliente que se asignan:

<dl>
<dt>**Contacto de suministro**</dt>
<dd>Trabaja con el representante de IBM en el establecimiento del entorno de {{site.data.keyword.Bluemix_notm}} dedicado, incluida la identificación de las personas adecuadas de la organización que trabajarán en cualquier aspecto del proyecto. La persona asignada a este rol toma un rol de gestión de proyectos y supervisa la selección del patrón, las formas comerciales y la disposición de acceso a los recursos del cliente. El contacto de suministro es el contacto general para configurar la instancia dedicada y para rastrear el proceso del despliegue.</dd>
<dt>**Responsable de suministro**</dt>
<dd>Trabaja con el representante de IBM para seleccionar una topología y opción de despliegue que se ajuste a sus requisitos de seguridad. La persona asignada a este rol trabaja con el asesor de suministro de IBM para determinar qué patrones de despliegue consiguen los objetivos y las metas de conformidad.</dd>
<dt>**Especialista en redes**</dt>
<dd>Trabaja con el representante de IBM en los planes de red para el despliegue de {{site.data.keyword.Bluemix_notm}}. La persona asignada a este rol revisa las especificaciones de red necesarias para IBM y trabaja conjuntamente con IBM en un plan de implementación. Al final de la fase de instalación y de verificación, la persona asignada a este rol concluirá que la configuración de red está en conformidad con los estándares corporativos.</dd>
<dt>**Contacto de DevOps**</dt>
<dd>Trabaja con el representante de IBM para planificar y aplicar las actualizaciones de mantenimiento necesarias para la plataforma, servicios y tiempos de ejecución de {{site.data.keyword.Bluemix_notm}}. La persona asignada a este rol también trabaja con el representante de IBM en la configuración de la instancia de {{site.data.keyword.Bluemix_notm}} dedicado.</dd>
</dl>

Los representantes de los clientes trabajan con su abogado especializado y con otros especialistas de IBM, que trabajan conjuntamente para asegurarse de que siempre tenga el soporte que necesita. Su abogado especializado es su único punto de contacto dentro del equipo de soporte de desarrollo de {{site.data.keyword.Bluemix_notm}}, que lleva a cabo las siguientes tareas:

<ul>
<li>Permite una adopción rápida del entorno {{site.data.keyword.Bluemix_notm}} dedicado.</li>
<li>Entrega valiosos materiales de formación y capacitación para mejorar su autosuficiencia.</li>
<li>Establece una relación duradera entre usted y el desarrollo, el soporte y los servicios de {{site.data.keyword.Bluemix_notm}} que utilice.</li>
</ul>

El equipo de soporte y operaciones de {{site.data.keyword.Bluemix_notm}} que trabaja con usted en la instancia de {{site.data.keyword.Bluemix_notm}} puede acceder a su entorno local, pero solo por los siguientes motivos:

<ul>
<li>Para responder a las alertas y realizar tareas de mantenimiento operativo</li>
<li>Para intentar reproducir un problema notificado en una incidencia de soporte</li>
</ul>

###Responsabilidades

Desde configurar su entorno hasta efectuar tareas de mantenimiento continuado, hay una gran variedad de tareas que deben llevarse a cabo. En la tabla siguiente se describen las tareas necesarias, así como el encargado de llevar a cabo la tarea durante la fase inicial, de progresión y de finalización.

La fase inicial se utiliza para establecer el entorno de {{site.data.keyword.Bluemix_notm}} dedicado. Los objetivos principales de dicha fase son los siguientes:

- Revisar el acuerdo financiero y establecer las fechas objetivo para la entrega.
- Crear la plataforma {{site.data.keyword.Bluemix_notm}} y proporcionar acceso a tiempos de ejecución y servicios.
- Definir y establecer la conectividad de red entre su red corporativa y las operaciones de {{site.data.keyword.Bluemix_notm}}.
- Identificar y asignar roles al equipo de administración.

*Tabla 1. Tareas de fases iniciales*

| **Tarea** | **Detalles de la tarea** | **Parte responsable** |
|----------|------------------|-----------------------|
|Establecer estándares de conformidad | Identificar estándares gubernamentales, sectoriales y de propiedad corporativa necesarios para el entorno. | Cliente |
|Crear un plan de seguridad y de integración de conformidad | Crear un plan de seguridad e integración que incluya costes, planificación y recursos necesarios para conseguir la conformidad de seguridad. | IBM |
|Aprobación de un plan de conformidad | Aprobar el plan de conformidad. | Cliente |
|Crear una variación de tamaño para los entornos |  	Crear una variación de tamaño de los entornos en función de opciones predefinidas que tengan en cuenta los objetivos de alta disponibilidad y la recuperación en caso de error, así como el DEA inicial y el suministro de servicios necesario para dar soporte a las apps creadas con la plataforma. Usted e IBM trabajan conjuntamente para definir, por ejemplo, qué bases de datos son necesarias, qué servicios se ofrecen en el catálogo sindicado del cliente, entre otros. | Responsabilidad compartida de IBM y el cliente |
|Seleccionar una arquitectura | Seleccionar una arquitectura basada en opciones predefinidas que tengan en cuenta requisitos de alta disponibilidad y de recuperación en caso de desastre. | IBM |
|Definir objetivos de recuperación en caso de error | Definir los requisitos de recuperación en caso de error para el entorno. | Cliente |
|Crear un plan de recuperación en caso de error | Consultar y definir el plan de recuperación en caso de error. IBM crea un modelo de recuperación en caso de error y le consulta donde debe proporcionar comentarios y aprobar el plan. | Responsabilidad compartida de IBM y el cliente |
|Crear un plan de copia de seguridad y recuperación | Crear un plan de copia de seguridad y recuperación que defina la frecuencia y los requisitos para la distribución interna y externa de la copia de seguridad. IBM realiza una copia de seguridad de componentes de plataforma, servicios de IBM, metadatos de servicios (roles de usuarios), etc. Debe realizar una copia de seguridad de todos los datos específicos de app de los que sea responsable. | Responsabilidad compartida de IBM y el cliente |
|Identificar herramientas para la detección de sucesos y la determinación de problemas | identificar herramientas de IBM y de terceros utilizadas para la detección de sucesos y la determinación de problemas en el nivel de plataforma de {{site.data.keyword.Bluemix_notm}}. | IBM |
|Definir un plan de escalamiento | Definir el plan de escalamiento para seleccionar y resolver sucesos detectados desde los componentes de supervisión. | IBM |
|Firmar acuerdos de infraestructuras, plataformas y soporte | Firmar el acuerdo de suscripción, incluidos los términos y condiciones financieros del entorno. Firmar un acuerdo de supervisión de seguridad y redes. Firmar una suscripción de soporte. | Cliente |
|Obtener un entorno | Obtener recursos informáticos, redes y almacenamiento, incluyendo VLAN principales y de servicios para alojar servicios nativos de {{site.data.keyword.Bluemix_notm}}, y alojar Data Power y el cortafuegos de SoftLayer. Proporcionar una infraestructura para el túnel VPN. | Cliente |
|Instalar componentes de plataforma, app y supervisión y gestión | Instalar, configurar y verificar componentes de plataforma, como BOSH Director, Cloud Controller, Health Manager, mensajería, routers, DEA y proveedores de servicios y los componentes de supervisión definidos en el plan de escalamiento y detección de problemas.  | IBM |
|Instalar y configurar componentes de seguridad | Instalar y configurar componentes de seguridad enlazados con el plan de supervisión y escalamiento, incluyendo IBM QRadar, almacén de credenciales, sistema de prevención de intrusión, IBM BigFix e IBM Security Privileged Identity Management. | IBM |
|Instalar y configurar componentes personalizados |  	Instalar y configurar componentes personalizados que residen fuera del ámbito del producto y los servicios de {{site.data.keyword.Bluemix_notm}}. | Cliente |
|Establecer una configuración inicial de red | Establecer una configuración inicial de red incluyendo cortafuegos, DataPower, Fortigate y DNS. | IBM |
|Conectar el conducto de {{site.data.keyword.Bluemix_notm}} | Conectar la integración continua y el conducto de entrega continua de {{site.data.keyword.Bluemix_notm}} con repositorios de IBM. | IBM |
|Personalizar componentes de soluciones externas | Personalizar equilibradores de carga para escenarios de recuperación en caso de error. | Cliente |
|Instalar una solución VPN | Instalar una solución VPN bidireccional. | IBM |
|Configurar un servidor de inicio de sesión | Configurar el servidor de inicio de sesión para utilizarlo con el LDAP corporativo. | IBM |
|Hacer un seguimiento del estado de la seguridad, la conformidad y los controles de auditoría  | Hacer un seguimiento del estado hasta el punto en que todas las herramientas y procesos estén en regla para conseguir la conformidad identificada. | Cliente |
|Revisar la infraestructura física | Revisar las instalaciones físicas que alojan los componentes de la solución para detectar amenazas y revisar los controles de seguridad para proteger el centro de datos. | Cliente |
|Inspeccionar el software de supervisión | Inspeccionar los componentes de supervisión y gestión, como se define en el plan de escalamiento y determinación de problemas. | Cliente |
|Inspeccionar el SO | Inspeccionar y asegurarse de que la imagen del sistema operativo cumple los estándares de conformidad. IBM proporciona acceso a la imagen del SO. | Responsabilidad compartida de IBM y el cliente |

A continuación tenemos la fase de progresión. En la fase de progresión se describe la relación de colaboración entre usted e IBM Cloud. Los objetivos principales de esta fase son los siguientes:

- Revisar la capacidad y coordinar los ajustes necesarios.
- Revisar el mantenimiento y las mejoras en la plataforma.
- Coordinar las actividades para la resolución de problemas y analizar las causas originarias.

*Tabla 2. Tareas de la fase de progresión*

| **Tarea** | **Detalles de la tarea** | **Parte responsable** |
|----------|------------------|-----------------------|
|Revisar informes de capacidad semanalmente | Revisar los informes de capacidad semanalmente y tomar acciones de corrección, si procede. | Cliente |
|Crear proyecciones mes a mes | Recopilar información y crear una proyección mes a mes de la capacidad y el consumo. | Responsabilidad compartida de IBM y el cliente |
|Revisar las proyecciones de capacidad | Revisar las proyecciones de capacidad relacionadas con sucesos externos que puedan afectar a la capacidad, así como la previsión de nuevos despliegues de apps. Trabajar con IBM para revisar las proyecciones y efectuar una planificación según convenga. | Responsabilidad compartida de IBM y el cliente |
|Revisar las proyecciones | Revisar las proyecciones de capacidad con relación a los sucesos externos que puedan afectar a la capacidad. | Cliente |
|Ajustar la capacidad |  Añadir o eliminar capacidad a medida que cambien sus necesidades. | IBM |
|Publicar actualizaciones venideras y realizar mantenimiento | Crear documentación para el mantenimiento necesario de los componentes de IBM. | IBM |
|Realizar tareas de mantenimiento | Trabajar con IBM para planificar tareas de mantenimiento necesarias en un intervalo de 30 días. Puede proporcionar fechas que no le vayan bien en dicho período de 30 días, e IBM trabajará para planificar el mantenimiento según convenga. | Responsabilidad compartida de IBM y el cliente |
|Abordar fallos de aprovisionamiento | Corregir fallos de aprovisionamiento, si se producen, de los servicios creados por el cliente desplegados en el catálogo. | IBM |
|Realizar exploraciones de red y de IP | Realizar exploraciones diarias y mensuales de red y de IP. | Responsabilidad compartida de IBM y el cliente |
|Proporcionar acceso a los registros de auditoría | Proporcionar acceso a todos los registros de auditoría de seguridad y administración.   | Responsabilidad compartida de IBM y el cliente |
|Realizar pruebas | Realizar pruebas Key Controls over Operations (KCO) periódicas y pruebas de penetración de terceros. | Responsabilidad compartida de IBM y el cliente |
|Informes de estado, coordinación de auditorías y reuniones de conformidad  | Efectuar informes de estado, coordinación de auditorías externas y representación en reuniones de estado de revisión de conformidad. | IBM |
|Verificación de necesidades empresariales y de ocupación | Efectuar verificaciones de ocupación trimestrales y verificaciones de necesidades empresariales continuadas para los representantes de IBM que tienen acceso al entorno del cliente. | IBM |
|Resolución de vulnerabilidades de seguridad | Resolver vulnerabilidades de seguridad notificadas en la plataforma. | IBM |

La etapa final de la finalización representa el final de la relación entre usted e IBM {{site.data.keyword.Bluemix_notm}}. Las tareas principales de esta fase son las siguientes:

* Finalización del acuerdo financiero
* Eliminación de todas las conexiones de red
* Reciclaje de la infraestructura

*Tabla 3. Tareas de la fase de finalización*

| **Tarea** | **Detalles de la tarea** | **Parte responsable** |
|----------|------------------|-----------------------|
|Finalizar el acuerdo financiero | Debatir y acordar el contrato del acuerdo financiero. | Responsabilidad compartida de IBM y el cliente |
|Retirar el entorno | Cerrar el acceso y retirar las credenciales del entorno. | Responsabilidad compartida de IBM y el cliente |
|Eliminar las conexiones de red del cliente | Eliminar las conexiones de red entre IBM y el entorno del cliente. | Responsabilidad compartida de IBM y el cliente |
|Reciclar la infraestructura | El entorno se recicla a partir de procesos definidos con SoftLayer. | IBM |

##Mantenimiento de la instancia dedicada
{: #maintaindedicated}

IBM mantiene e instala actualizaciones y arreglos como cambios de IBM adecuados para la plataforma de {{site.data.keyword.Bluemix_notm}} dedicado, tiempos de ejecución y servicios.

**Importante**: IBM se reserva el derecho de interrumpir servicios para aplicar mantenimiento emergencia si es necesario. IBM puede modificar las horas de mantenimiento planificadas, pero le notificará cualquier cambio, así como la información de mantenimiento de emergencia.

Se requieren los siguientes tipos de mantenimiento para {{site.data.keyword.Bluemix_notm}} dedicado:
<dl>
<dt>**Ventanas de mantenimiento estándar**</dt>
<dd>Los servicios utilizan ventanas de mantenimiento estándar y predefinidas, lo cual podría hacer que los servicios no estén disponibles. IBM no requiere aprobación del cliente para realizar el mantenimiento, pero intenta minimizar el impacto en los servicios.<br />
<br />
IBM envía mensajes de difusión general de los cambios planificados para cada ventana de mantenimiento, por correo electrónico, por teléfono o mediante otros métodos.<br />
<br />
**Importante**: Es posible que algún servicio no esté disponible durante el periodo de mantenimiento.</dd>

<dt>**Ventana de cambio mensual**</dt>
<dd>La ventana de mantenimiento mensual se aplica en función de la coordinación entre el usuario y IBM dentro de una ventana de 21 días. Puede proporcionar a IBM horas o fechas específicas dentro de la ventana de 21 días que puede que no funcionen para el usuario. IBM intenta planificar actualizaciones alrededor de esas horas. En función de las solicitudes, IBM se comunicará con la ventana de mantenimiento planificada. No se espera que las ventanas de cambio mensual produzcan un impacto en la ejecución del entorno dedicado de Bluemix.
<p>La imagen siguiente muestra el proceso desde la recepción de una notificación sobre una actualización pendiente para establecer fechas que
pudieran no venirle bien, y luego recibir finalmente la notificación sobre la fecha de planificación: </p>
<p><img src="../local/images/maintenance_dates.png" alt="Proceso para el establecimiento de fechas no disponibles para una actualización de mantenimiento"></p>
<br />
**Nota**: si no necesita establecer ninguna fecha no disponible para la actualización, puede aprobar la actualización. IBM
le notifica de la fecha de planificación para la aplicación del mantenimiento. <br />
<p>La imagen siguiente muestra el proceso desde la recepción de una notificación sobre una actualización pendiente, la probación de la actualización y la posterior recepción de la fecha planificada de la actualización: </p>
<p><img src="../local/images/maintenance_nodates.png" alt="Proceso para la aprobación de la actualización sin fechas no disponibles"></p>
<br />
Vaya a **ADMINISTRACIÓN > INFORMACIÓN DEL SISTEMA** para ver las actualizaciones pendientes, establecer fechas no disponibles y aprobar actualizaciones. Para obtener más información sobre las notificaciones y la planificación de actualizaciones pendientes, consulte <a href="../admin/index.html#oc_system">Visualización de información del sistema</a>.</dd>

<dt>**Otro**</dt>
<dd>IBM intenta limitar todo el mantenimiento que pueda afectar a los servicios, en particular a la disponibilidad del entorno {{site.data.keyword.Bluemix_notm}} dedicado, los tiempos de ejecución y los servicios, a las actualizaciones estándar y mensuales. Es posible que, de forma excepcional, se utilicen otras ventanas de cambios para la gestión del entorno. IBM hará todo lo posible para minimizar el impacto en su entorno durante estas ventanas de cambios y se lo notificará por adelantado.</dd>
</dl>

Para configurar el mantenimiento de la instancia dedicada, póngase en contacto con el representante designado de su cuenta de IBM para identificar una ventana acordada para el mantenimiento estándar.

Si hay un problema después de una actualización de mantenimiento, acuerda con el representante de IBM si le conviene permitir que IBM retrotraiga la actualización. Si se acuerda, IBM retrotrae la actualización para restaurar el entorno al estado anterior.

## Respuesta y soporte de incidencias
{: #incidentresponse}

### Problemas detectados por el cliente

Si detecta un problema que necesite la atención de operaciones y soporte de IBM puede ponerse en contacto con el soporte mediante diversos
métodos. Para obtener información sobre cómo contactar con el soporte, consulte [Cómo obtener soporte](../support/index.html#contacting-bluemix-support-local). Según la naturaleza del problema, el usuario, IBM o ambos pueden trabajar para solucionarlo. 

### Incidencias críticas detectadas por IBM

Las incidencias críticas son urgentes, cortes de servicio inesperados y problemas de estabilidad que afectan a su
entorno o sus usuarios. Si IBM detecta una incidencia crítica en su entorno, se le envía una notificación en la página
**Estado**. También se puede revisar la página Estado para buscar problemas conocidos para la plataforma o
sus servicios. Si quiere integrar sus notificaciones con un servicio web que admita ganchos (hooks), consulte
[Notificaciones y suscripciones de sucesos](../admin/index.html#oc_eventsubscription) para obtener información sobre
cómo ampliar las funciones de notificación. 

![Proceso de respuesta de incidencias](../local/images/incidentresponseprocess.png "Proceso de respuesta de incidencias")

*Figura 2. Proceso de respuesta de incidencias*

Según la naturaleza del problema, el usuario, IBM o ambos pueden trabajar para solucionarlo. Si tiene alguna pregunta relativa a la incidencia, o si necesita que un representante de IBM le ayude a resolver el problema, puede abrir una incidencia de soporte. Para obtener información sobre cómo contactar con el soporte, consulte [Cómo obtener soporte](../support/index.html#contacting-bluemix-support-local). 

**Nota**: Las incidencias de soporte de gravedad 1 se supervisan 24 horas al día, 7 días por semana. Otras incidencias
se procesan desde las 22:00 del domingo (GMT) hasta las 00:00 del sábado (GMT). Para obtener más información sobre la gravedad de
las incidencias de soporte y cómo trabajar con soporte, consulte <a href="../support/index.html#contacting-bluemix-support-local">Contacto
con soporte</a>. 


## Recuperación en caso de siniestro
{: #dr}

{{site.data.keyword.Bluemix_short}} público proporciona una plataforma disponible de forma continuada para la innovación. Las diversas medidas a prueba de errores le garantizan que las organizaciones, espacios y apps siempre estén disponibles. El despliegue de apps en varias regiones geográficas permite la disponibilidad continua, que protege frente a la pérdida no planificada y simultánea de varios componentes de hardware o software, o la pérdida de todo un centro de datos, de modo que, incluso en el caso de un desastre natural en una ubicación geográfica, las instancias distribuidas de la app de {{site.data.keyword.Bluemix_notm}} público, situadas en ubicaciones geográficas alternativas, seguirán estando disponibles.
{: shortdesc}

La recuperación en caso de error de {{site.data.keyword.Bluemix_short}} dedicado es posible gracias a la disponibilidad continua de sus apps, la alta disponibilidad inherente de la plataforma y la capacidad de restaurar la instancia en caso de error. Es responsable de habilitar una disponibilidad continua de sus apps desplegándolas en varias regiones. La alta disponibilidad está integrada en el nivel de la plataforma mediante tecnologías incluidas en Cloud Foundry y otros componentes. También puede trabajar conjuntamente con IBM para asegurarse de que se ha hecho una copia de seguridad correcta de sus datos en el caso de que necesite restaurar su instancia en cualquier momento.

### Habilitación de la disponibilidad continua para {{site.data.keyword.Bluemix_notm}} dedicado
{: #enabling}

De forma predeterminada, {{site.data.keyword.Bluemix_notm}} público se despliega en varias ubicaciones geográficas. Sin embargo, debe llevar a cabo lo siguiente para habilitar las instancias de {{site.data.keyword.Bluemix_notm}} dedicado distribuidas globalmente:

* Asegúrese de que los desarrolladores están desplegando apps en más de una región, ya sea a través de un proceso manual o automatizado. Las regiones deben estar a una distancia de más de 200 km entre ellas para garantizar que, en caso de desastre natural, ambas ubicaciones geográficas no se vean afectadas.
* Configure un equilibrador de carga global, como Akamai o Dyn, para que apunten a apps en al menos dos regiones distintas.

**Nota**: No todos los servicios de {{site.data.keyword.Bluemix_notm}} admiten la distribución regional. Al construir una app, si desea lograr la distribución geográfica, también debe asegurarse de que los servicios que se utilizan en la app tienen la sincronización de datos como característica clave.

#### Despliegue de apps de {{site.data.keyword.Bluemix_notm}} dedicado en varias ubicaciones geográficas
{: #deploying}

Para efectuar un despliegue en una segunda ubicación o en varias ubicaciones, debe seguir un proceso similar al que siguió para habilitar la ubicación geográfica primaria:

1. Habilite un nuevo entorno dedicado para alojar instancias adicionales de las apps. Para crear un nuevo entorno, póngase en contacto con el equipo de ventas de IBM para iniciar el proceso. Para obtener más información sobre la configuración de una instancia dedicada, consulte [Configuración de {{site.data.keyword.Bluemix_notm}} dedicado](../dedicated/index.html#setupdedicated). Debe iniciar sesión por separado para acceder a cada entorno. Cada ubicación física de los entornos alojados debe estar a una distancia mínima de 200 km de la ubicación original para garantizar la disponibilidad.
2. Obtenga el nombre de dominio exclusivo en el que se alojará la nueva app desplegada.  Por ejemplo, si el dominio original es *mycompany.east.bluemix.net*, puede crear un nuevo entorno local con un nuevo dominio como *mycompany.west.bluemix.net* y desplegarlo en el nuevo dominio.
3. Cada vez que despliegue la app original, también la desplegará en la nueva ubicación. Para obtener más información sobre el despliegue, consulte [Carga de una app](../starters/upload_app.html).


#### Habilitación de un equilibrador de carga global para {{site.data.keyword.Bluemix_notm}} dedicado
{: #glb}

Un equilibrador de carga global no solo garantiza una disponibilidad continua y es necesario para la recuperación en caso de error, sino que también presenta varias ventajas adicionales:

* Dirige a los usuarios a la región más próxima de {{site.data.keyword.Bluemix_notm}} de forma predeterminada
* Efectúa un enrutamiento en función del rendimiento
* Dirige de forma selectiva un porcentaje de tráfico a una nueva versión de una app
* Proporciona migración tras error de sitio en función de la comprobación del estado de la región
* Proporciona migración tras error de sitio en función de la comprobación del estado de la app
* Utiliza un direccionamiento ponderado entre los puntos finales

Puede elegir un equilibrador de carga global como Akamai o Dyn. Para obtener más información sobre cómo utilizar Akamai como equilibrador de carga global, consulte [Gestión de tráfico global](https://www.akamai.com/us/en/solutions/products/web-performance/global-traffic-management.jsp){: new_window}. Para obtener más información sobre cómo utilizar Dyn como equilibrador de carga global, consulte [4 Reasons Businesses Are Taking Global Load Balancing to the Cloud](http://dyn.com/blog/4-reasons-businesses-are-taking-global-load-balancing-to-the-cloud/){: new_window}.

### Alta disponibilidad
{: #ha}

Además de habilitar una disponibilidad continua, {{site.data.keyword.Bluemix_notm}} también proporciona alta disponibilidad en la plataforma mediante tecnologías integradas en Cloud Foundry, Docker y otros componentes.

Estas tecnologías incluyen:

<dl>
<dt>Escalabilidad en Cloud Foundry</dt>
<dd>Un <a href="https://docs.cloudfoundry.org/concepts/architecture/execution-agent.html" target="_blank">agente de ejecución de gotas (DEA)</a> de Cloud Foundry efectúa comprobaciones de estado en las apps que se ejecutan en él. Si se produce algún problema con la app o con el propio DEA, despliega instancias adicionales de la app en un DEA alternativo para solucionar el problema. Para obtener más información, consulte <a href="https://docs.cloudfoundry.org/concepts/high-availability.html" target="_blank">Configuración de CF para la alta disponibilidad con redundancia</a>.
</dd>
<dt>Redundancia SoftLayer</dt>
<dd>Con SoftLayer en los entornos dedicados, los datos de cada clúster de almacenamiento en la nube se graban varias veces y los clústeres de almacenamiento se configuran con capacidades de solución automática en caso de error en la unidad. Si hay un problema con
un servidor virtual, SoftLayer intenta reiniciar el servidor virtual en otro host. </dd>
<dt>Copia de seguridad de metadatos</dt>
<dd>Se realiza una copia de seguridad de los metadatos mediante SoftLayer EVault Backup en una ubicación a una distancia mínima de 200 km.</dd>
</dl>

##Restauración de la instancia dedicada
{: #restorededicated}

Se hace una copia de seguridad de forma regular de los valores, los metadatos y las configuraciones de {{site.data.keyword.Bluemix_notm}} dedicado para prepararse ante cualquier interrupción no planificada del entorno. Los datos de cuya copia de seguridad es responsable incluyen datos de app, datos de servicios de bases de datos en la nube y almacenes de objetos.

Como parte de la copia de seguridad de los datos, que incluye metadatos del sistema y configuraciones, IBM lleva a cabo las tareas siguientes:

<ul>
<li>Cifra todas las copias de seguridad y gestiona las claves de cifrado</li>
<li>Supervisa y gestiona la actividad de copia de seguridad</li>
<li>Proporciona los archivos de copia de seguridad cifrados</li>
<li>Restaura los datos solicitados</li>
<li>Gestiona conflictos de planificación entre operaciones de copia de seguridad y de gestión de arreglos</li>
</ul>

Puesto que la protección de datos privados es crítica, IBM necesita su colaboración cuando se trabaja con la gestión de archivos de copia de seguridad, de modo que los archivos no se traspasen fuera de sus centros de datos. Específicamente, IBM le solicita que complete las tareas siguientes:

<ul>
<li>Mover una copia de los datos de copia de seguridad cifrados fuera del sitio, como lo haría para cualesquiera otros datos de copia de seguridad que gestione.</li>
<li>Proporcionar los archivos de copia de seguridad para el operador de IBM en caso de cualquier necesidad de restauración.</li>
</ul>

# rellinks
## general
* [Descubrir: {{site.data.keyword.Bluemix_notm}} dedicado](http://www.ibm.com/cloud-computing/bluemix/hybrid/dedicated/)
* [Novedades de {{site.data.keyword.Bluemix_notm}}](../whatsnew/index.html)
* [{{site.data.keyword.Bluemix_notm}} glosario](glossary/index.html)
* [Gestión de {{site.data.keyword.Bluemix_notm}} local y {{site.data.keyword.Bluemix_notm}} dedicado](../admin/index.html#mng)
* [Cómo obtener soporte](../troubleshoot/getting_customer_support.html#bluemix_support)
