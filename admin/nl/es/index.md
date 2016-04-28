---



copyright:

  years: 2015, 2016



---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Gestión de {{site.data.keyword.Bluemix_notm}} Local y {{site.data.keyword.Bluemix_notm}} Dedicado
{: #mng}
*Última actualización: 18 de febrero de 2016*

Si tiene acceso de administrador para {{site.data.keyword.Bluemix_notm}} Local o {{site.data.keyword.Bluemix_notm}} Dedicado, vaya a la página **Administración** para gestionar recursos, supervisar el uso de cuota, administrar permisos de usuarios, planificar las notificaciones de actualización, ver informes y registros de seguridad, etc. Puede gestionar sus organizaciones mediante la creación de espacios y la configuración de roles y permisos de usuarios; consulte [Gestión de las organizaciones](../admin/adminpublic.html#orgmng).
{:shortdesc}

*Tabla 1. Tareas administrativas para gestionar la instancia local o dedicada de {{site.data.keyword.Bluemix_notm}}*

| ¿Qué puedo hacer? | Detalles |    
|----------------|---------|
|Supervisar el uso del sistema | Pulse **ADMINISTRACIÓN &gt; USO**. Visualice la información del sistema, supervise el uso de la CPU y planifique el uso para tomar las mejores decisiones para su empresa. Consulte [Visualización de información de uso](index.html#oc_resource). |
|Gestionar el catálogo | Pulse **ADMINISTRATION &gt; CATALOG MANAGEMENT** para gestionar qué servicios están visibles a sus
usuarios y orgs. Consulte [Gestión de su catálogo](index.html#oc_catalog). |
|Administrar organizaciones | Pulse **ADMINISTRATION &gt; ORGANIZATION ADMINISTRATION** para crear organizaciones, supervisar cuotas para organizaciones y realizar rápidamente las decisiones basadas en necesidades. Consulte [Administración de organizaciones](index.html#oc_organizations).|
|Crear espacios y asignar roles de usuario | Pulse el icono **Cuenta y soporte** ![Cuenta y soporte](../support/images/account_support.svg) y, a continuación, seleccione **Gestionar
organizaciones** para crear espacios dentro de sus organizaciones. Añada usuarios y asigne roles de organización y de espacio a los usuarios. Consultar [Gestión de sus organizaciones](../admin/adminpublic.html#orgmng).  |
|Gestionar permisos de usuarios administrativos | Pulse **ADMINISTRATION &gt; USER ADMINISTRATION** para añadir usuarios,
eliminar usuarios y ajustar permisos de usuario. Consultar [Gestión de usuarios y permisos](index.html#oc_user).  |
|Revisar informes y registros | Pulse **ADMINISTRATION &gt; REPORTS AND LOGS** para ver informes de seguridad y
registros de auditoría para su instancia. Ver [Visualización de informes](index.html#oc_report). |
|Ver información del sistema | Pulse **ADMINISTRATION &gt; SYSTEM INFORMATION** para ver información del sistema como actualizaciones pendientes, el nombre y la versión de la instancia, la región, la URL de API, la URL de CLI, los detalles de configuración de LDAP, las correlaciones de usuario y de grupo, las estadísticas y los dominios compartidos. También puede acceder a suscripciones de sucesos e información de entrada de calendario
para la aplicación de sus notificaciones en la sección Actualizaciones pendientes. Consulte [Visualización de información del sistema](index.html#oc_system).  |
|Ampliar notificaciones y configurar suscripciones de sucesos | Pulse **ADMINISTRACIÓN &gt; INFORMACIÓN DEL SISTEMA &gt; *Número* de actualizaciones pendientes**. Puede usar webhooks para integrar con el servicio web que quiera para configurar la suscripción a notificación de sucesos para una actualización o incidencia. Consulte [Suscripción de notificaciones y sucesos](index.html#oc_eventsubscription).  |


## Suscripción de notificaciones y sucesos
{: #oc_eventsubscription}

Siempre pueda saber el estado de su entorno comprobando la página Estado. {{site.data.keyword.Bluemix_notm}} también envía
notificaciones al área Notificaciones para la página Administración para sucesos como actualizaciones y mantenimiento planificados. Las
incidencias se informan en la página Estado. 

### Notificaciones

Puede ver notificaciones de IBM para su entorno local o dedicado y supervisar el estado de su entorno. Revise la
tabla siguiente para obtener información sobre los distintos tipos de notificaciones y dónde se publican. 

| **Tipo de suceso** | **Método de notificación** |       
|-----------------|-------------------|
| Actualizaciones de mantenimiento | En las notificaciones de la página Administración se avisa de las próximas actualizaciones de mantenimiento. Acceda
a la página **Administración** y seleccione el icono **Notificaciones** ![Notificaciones](images/icon_announcement.svg). Para ver un listado completo y el historial de notificaciones pendientes y
completas, pulse **ADMNISTRACIÓN &gt; INFORMACIÓN DEL SISTEMA** &gt; *Número* **actualizaciones
pendientes**. Puede ampliar la posibilidad de notificación configurando una suscripción de sucesos que integra alertas de
actualización de mantenimiento desde la página Administración con el servicio web que elija para direccionar los mensajes
a una dirección de correo electrónico del centro de atención al cliente o un mensaje SMS al número de teléfono que elija.  |
| Incidencias críticas | Se aleta sobre incidencias críticas en la página Estado. Pulse el icono **Cuenta y soporte** ![Cuenta y soporte](../support/images/account_support.svg), y seleccione **Estado**. Puede ampliar la posibilidad de notificación configurando una suscripción de sucesos que integra alertas de incidencias
desde la página Estado con el servicio web que elija para direccionar los mensajes
a una dirección de correo electrónico del centro de atención al cliente o un mensaje SMS al número de teléfono que elija.  |  
| Estado | Puede ver el estado más reciente de la plataforma, servicios y de su instancia {{site.data.keyword.Bluemix_notm}}. Pulse el icono **Cuenta y soporte** ![Cuenta y soporte](../support/images/account_support.svg), y seleccione **Estado**.   |

*Tabla 2. Tipos de sucesos y métodos de notificación*

### Configuración de suscripciones de sucesos

Puede ampliar la funcionalidad de las notificaciones que se envía a las páginas Administración y Estado usando las
suscripciones de sucesos que implementan los webhooks. Los webhooks direccionan sus notificaciones directamente al destino que elija (por
correo electrónico) o a un número de teléfono (por mensaje SMS). Puede personalizar el tipo de notificación, específicamente
actualizaciones de mantenimiento o alertas de incidencias críticas, y la información que se incluye en la notificación. 

Para usar los webhooks para configurar una suscripción de sucesos específica, realice los pasos siguientes: 

1. Acceda a la página **ADMINISTRACIÓN**: 

- Para notificaciones de actualización de mantenimiento, acceda a **INFORMACIÓN DEL SISTEMA** &gt; *Número* **actualizaciones pendientes** y pulse el icono **Suscribir**
![Suscribir](images/icon_subscribe.svg). 
- Para notificaciones de alerta de incidencias, pulse el icono **Cuenta y soporte** ![Cuenta y soporte](../support/images/account_support.svg) &gt; **Estado**, y pulse el icono
**Suscribir** ![Suscribir](images/icon_subscribe.svg).

**Nota**: Puede acceder a la página de suscripción de sucesos para ambos tipos de notificaciones, utilizando
cualquiera de los dos métodos descritos. 

2. Pulse **Añadir suscripción**. 

3. Rellene el formulario de suscripción de sucesos. Para obtener información sobre los campos del formulario, revise la tabla siguiente: 

| **Campo** | **Descripción** |
|-----------------|-------------------|
| Tipo | Seleccionar el Webhook. |
| Método | Seleccionar GET o POST. |
| Suceso | Seleccionar la suscripción a notificaciones para actualizaciones o incidencias. |
| URL | Especificar el URL a la que enganchar su servicio web. |
| Descripción | Añadir una descripción para la suscripción de sucesos que está creando.  |
| Nombre de usuario | Especificar el nombre de usuario para su servicio web. Si no quiere usar sus credenciales personales, puede configurar
un ID funcional a usar específicamente con {{site.data.keyword.Bluemix_notm}}. |
| Contraseña | Especificar la contraseña de su servicio web. |
| Carga útil | Si ha seleccionado el método POST, especifique las propiedades específicas del servicio web que usa, junto con los valores utilizados para la notificación a IBM. Por ejemplo, si quiere mostrar el título, mensaje y gravedad en la notificación desde su servicio web, debe definir los valores de
{{site.data.keyword.Bluemix_notm}} con la propiedad coincidente para su servicio web. Los valores siguientes se pueden usar para
extraer información desde la notificación de {{site.data.keyword.Bluemix_notm}} para el título de notificación,
cuerpo del mensaje y nivel de gravedad: `"{{title}}`, `"{{message}},"` y
`"{{severity}}"`. Si no especifica información en esta sección, recibirá la notificación sin
información adicional.   |

Tabla 3. Campos de formulario de suscripción de sucesos

Cuando se guarda su suscripción de sucesos, recibe notificaciones a través del método que haya configurado por medio del servicio web. Las
notificaciones se siguen publicando en la página Estado para las incidencias y en el área Notificaciones de la página Administración para las actualizaciones de mantenimiento. 

Puede seleccionar cualquier suscripción de sucesos guardada y ver la actividad reciente. Puede pulsar para expandir cualquier entrada de actividad
reciente para ver los detalles. Incluidos en los detalles están los valores de IBM para la notificación que puede usar en la sección payload. Para
ver estos valores, expanda la entrada de actividad reciente, expanda **Suceso** y luego **Objeto**. 


## Visualización de la información del sistema
{: #oc_system}

Para ver información del sistema, pulse **ADMINISTRACIÓN &gt; INFORMACIÓN DEL SISTEMA**.

Puede expandir y visualizar diversas secciones sobre detalles de configuración de actualizaciones pendientes, información general del sistema y LDAP.

### Actualizaciones y notificaciones pendientes

En la sección Actualizaciones, puede ver el número de notificaciones de actualizaciones pendientes
que requieren acción por su parte. Para realizar una acción para una actualización específica, siga estos pasos:

<ol>
<li>Pulse <strong><em>Número</em> de actualizaciones pendientes</strong> para ver todas las actualizaciones pendientes.</li>
<li>Seleccione una actualización para realizar una acción o ver los detalles de la actualización, que incluyen la ventana de actualización,
el estado planificado o el estado de interrupción.</li>
<li>Pulse <strong>ESTABLECER FECHAS DE NO DISPONIBILIDAD</strong> para establecer días específicos en la ventana de actualización
que no son convenientes para que se aplique la actualización. Si establece fechas de no disponibilidad, IBM aprobará y planificará
la actualización en función de las selecciones. Recibirá una notificación cuando se apruebe y se planifique la actualización.</li>
<li>Pulse <strong>APROBAR</strong> para aprobar la actualización, si no tiene ninguna fecha no disponible. Si aprueba, la actualización se aplicará durante la ventana de actualización planificada. IBM enviará una
notificación cuando se inicie y se detenga el despliegue de actualización.</li>
</ol>

**Nota**: si no establece fechas no disponibles o aprueba la actualización, se aplica al final del plazo de 21 días
para asegurar que su plataforma permanece actualizada. 

En la página Actualizaciones pendientes, puede elegir el seguimiento de su planificación de actualizaciones pulsando en el icono
**Calendario** ![Calendario](images/icon_calendar.svg) y descargar el archivo `.ics` para importar sus actualizaciones
planificadas en la app de calendario que prefiera: 

<ol>
<li>Abra la app de calendario.</li>
<li>Descargue el archivo de calendario pulsando el icono **Calendario** ![Calendario](images/icon_calendar.svg), y luego impórtelo en su app de calendario usando el archivo `.ics`. </li>
<li>Escriba sus credenciales.</li>
<li>Visualice las actualizaciones planificadas.</li>
</ol>

También puede ampliar la funcionalidad de notificación para la página Administración usando las suscripciones de sucesos para
la integración con el servicio web que quiera. Para configurar una suscripción de notificación de sucesos para una actualización o incidencia,
consulte [Suscripciones de suceso y notificaciones](index.html#oc_eventsubscription). 

### Información general del sistema

En la sección Información general, puede ver la siguiente información:

- Información básica sobre el build de {{site.data.keyword.Bluemix_notm}}.
- Información de API (versión, URL, región y enlace a la documentación de CLI).
- Información de dominio compartido sobre el sistema y el servicio.
- Estadísticas sobre el número total de apps, usuarios y organizaciones.

### Detalles de configuración de LDAP

En la sección Detalles de la configuración de LDAP, puede seleccionar el servidor de LDAP
y ver información sobre las correlaciones de usuarios y grupos. Si utiliza el WebID de
{{site.data.keyword.IBM}}, se indica en esta sección. 

## Visualización de la información de uso
{: #oc_resource}

Puede ver distintos tipos de información de uso para su instancia local o dedicada y cuenta de
{{site.data.keyword.Bluemix_notm}}: 

- Información de recursos, incluyendo espacio en disco, uso de CPU, uso de red y tiempos de respuesta medios. Consulte [Uso de recursos](index.html#resourceusage). 
- Uso de cuenta por org, incluyendo el número de apps de tiempo de ejecución con uso, el número total de GB-horas de tiempo de ejecución y el número de instancias de servicio con uso. Consulte [Uso de la cuenta](index.html#accountusage).
- Uso de cuota de memoria de org, memoria de app asignada en base al total de la cuota de memoria usada y una vista del uso GB-hora por app para una org específica. También puede ver el uso de la cuota para todas las orgs de la página Administración de organización en la sección
Supervisión de cuota. Consultar [Administración de organización](../admin/index.html#orgusage). 


### Uso de recursos
{: #resourceusage}

Para ver información de recursos, pulse **ADMINISTRACIÓN &gt; USO**.

En la sección Supervisión de recursos, puede ver la siguiente
información:

- Información sobre uso del recurso, como el número de GB de memoria y el número de GB de espacio de disco utilizados. Puede ver el promedio de uso de la CPU de todos los agentes de ejecución de gotas (DEA). Pulse el mosaico **CPU** y verá el uso de CPU de cada DEA. El DEA que tiene el uso más alto aparece primero, y todos ellos están identificados con su trabajo y su dirección IP. El uso de CPU se divide
en tres categorías que incluyen la cantidad de CPU utilizada en los procesos del sistema, la cantidad de CPU
utilizada en los procesos de usuario y la cantidad de CPU utilizada en los procesos de espera.
- Información sobre uso de red correspondiente a entrada y salida de ancho de banda durante el último día, semana o mes.
Los datos que se muestran se basan en la suma del tráfico de entrada y de salida de las redes públicas y privadas.
- Tiempo medio de respuesta para {{site.data.keyword.Bluemix_notm}} en los últimos 10 minutos, hora y día.
- Promedio de transacciones por segundo para {{site.data.keyword.Bluemix_notm}} durante los últimos 10
minutos, hora y día.

### Uso de cuenta
{: #accountusage}

Puede ver el uso mensual de su cuenta para su entorno local o dedicado. Puede utilizar estos datos para identificar cuánto cargar
a organizaciones específicas según su uso. 

<ol>
<li>Pulse en el icono <strong>Cuenta y soporte</strong> ![Cuenta y soporte](../support/images/account_support.svg) &gt; <strong>Cuenta</strong> &gt; <strong>Detalles de uso</strong>. </li>
<li>Seleccione la organización para la que quiere ver los datos. </li>
<li>Puede ver los detalles de uso de las categorías siguientes:
<ul>
<li>Apps de tiempo de ejecución que tienen uso</li>
<li>Uso total de apps de tiempo de ejecución en GB-horas</li>
<li>Instancias de servicio que tienen uso</li>
</ul>
</li>
<li>Opcional: ver sus datos para un mes concreto usando el menú <strong>Su actividad de nube</strong> para seleccionar el mes que quiera. </li>
<li>Opcional: pulse <strong>EXPORT DATA</strong>, y seleccione <strong>CSV</strong> o <strong>JSON</strong> para exportar sus datos para el
mes seleccionado a un archivo <code>CSV</code> o <code>JSON</code>. </li>
</ol>

También puede ver el uso mensual y los cargos asociados al nivel de cuenta para sus ejecutables, apps y servicios sindicados desde
el {{site.data.keyword.Bluemix_notm}} público. Puede utilizar estos datos para identificar cuánto cargar a organizaciones específicas
según su uso. 

<ol>
<li>Pulse en el icono <strong>Cuenta y soporte</strong> ![Cuenta y soporte](../support/images/account_support.svg) &gt; <strong>Cuenta</strong> &gt; <strong>Detalles de uso</strong>. </li>
<li>Pulse <strong>Público</strong>.</li>
<li>Seleccione la organización para la que quiere ver los datos, o seleccione <strong>Todas las organizaciones</strong> para ver los datos de
todas las organizaciones a la vez. </li>
<li>Puede ver los detalles de uso de las categorías siguientes:
<ul>
<li>Apps de tiempo de ejecución que tienen uso</li>
<li>Uso total de apps de tiempo de ejecución en GB-horas</li>
<li>Instancias de servicio que tienen uso</li>
<li>Un resumen de cargo para todos los ejecutables sindicados, servicios y apps</li>
</ul>
</li>
<li>Opcional: ver sus datos para un mes específico, seleccionando el mes que quiera del gráfico de barras. Los datos del mes actual
se muestran de forma predeterminada. </li>
<li>Opcional: pulse <strong>EXPORT DATA</strong>, y seleccione <strong>CSV</strong> o <strong>JSON</strong> para exportar sus datos para el
mes seleccionado a un archivo <code>CSV</code> o <code>JSON</code>. </li>
</ol>


### Uso de la organización
{: #orgusage}

Para ver el uso por organización, pulse **ADMINISTRACIÓN &gt; ADMINISTRACIÓN DE ORGANIZACIÓN**, y luego seleccione una
organización de la **Lista de organizaciones**. En la página **Gestionar organizaciones** para la
organización que ha seleccionado, puede ver la información de uso siguiente: 

- Número de servicios que hay actualmente en uso. 
- Número de rutas que hay actualmente en uso. 
- Gráfico de cuota de memoria que muestra qué parte de la cuota está en uso y qué parte no se usa actualmente. 
- Gráfico de asignación de aplicaciones que muestra qué aplicaciones se incluyen en la cuota de memoria utilizada. 
- Gráfico de uso de aplicaciones medidas que muestra un informe de tres meses de los GB-horas usados por app desplegada. Puede
seleccionar la **Vista de lista** para ver los datos de todas las aplicaciones, incluyendo la asignación de memoria por app y
el uso de GB-hora medido para los últimos tres meses. 

Para obtener más información sobre la visualización del uso por organización, el ajuste de planes de cuota y la gestión de sus
organizaciones, consulte [Administración de organizaciones](../admin/index.html#oc_organizations). 

## Visualización de informes
{: #oc_report}

Puede ver informes de seguridad y registros, como por ejemplo DataPower&trade;, el cortafuegos y la auditoría de inicio de sesión, para
la instancia de {{site.data.keyword.Bluemix_notm}}.

Para visualizar informes y registros, pulse **ADMINISTRACIÓN &gt; INFORMES Y REGISTROS**.

Seleccione una de las opciones siguientes:

- Puede seleccionar fechas de inicio y finalización en los campos para filtrar los informes y registros que se muestran.
- Puede expandir y visualizar distintos informes desde el panel de navegación.
- Puede buscar dentro del conjunto de informes y registros. La búsqueda se aplica a los nombres de informes y al contenido de texto que se incluye en los informes y los registros. También puede optar por filtrar
la búsqueda por **Sucesos de administración**, **Informes de DataPower**, **Cortafuegos** y **Auditoría
de inicio de sesión**.
- Cuando visualice un informe o un registro, puede pulsar el icono ![Descargar](images/icon_download.png)
para descargar el informe.

La tabla siguiente muestra la lista de los informes de seguridad generados para {{site.data.keyword.Bluemix_notm}} local y {{site.data.keyword.Bluemix_notm}} dedicado.

| **Categoría** | **Informe** | **Descripción** |      
|-----------------|-------------------|---------------------|
| Cortafuegos | Inicios de sesión de cortafuegos | Sucesos relacionados con el inicio de sesión del administrador en los dispositivos de cortafuegos Vyatta. |
| Cortafuegos | Denegaciones de cortafuegos | Sucesos generados por los dispositivos cortafuegos Vyatta cuando se deniega una solicitud de acceso acuerdo con las reglas vigentes del cortafuegos. |
| Sucesos de inicio de sesión del administrador de {{site.data.keyword.Bluemix_notm}} | Inicio de sesión de los administradores de {{site.data.keyword.Bluemix_notm}} | Sucesos generados por el sistema operativo cuando un administrador inicia una sesión SSH en cada sistema {{site.data.keyword.Bluemix_notm}}. |
| Sucesos de inicio de sesión de desarrollador de apps de {{site.data.keyword.Bluemix_notm}} | Inicio de sesión de desarrolladores de apps de {{site.data.keyword.Bluemix_notm}} | Sucesos generados por el componente de inicio de sesión de la plataforma {{site.data.keyword.Bluemix_notm}} cuando un usuario de la plataforma {{site.data.keyword.Bluemix_notm}} inicia sesión mediante la línea de mandatos, las API REST o la interfaz de usuario de {{site.data.keyword.Bluemix_notm}}. |
| Sucesos administrativos del administrador de {{site.data.keyword.Bluemix_notm}} | Sucesos administrativos del sistema operativo de los administradores de {{site.data.keyword.Bluemix_notm}} | Sucesos generados por el sistema operativo cuando un administrador realiza una acción durante una sesión de trabajo actual. |
| Sucesos administrativos de desarrollador de apps de {{site.data.keyword.Bluemix_notm}} | Sucesos administrativos de {{site.data.keyword.Bluemix_notm}} (Cloud Foundry) | Sucesos relacionados con operaciones realizadas por el usuario de la plataforma {{site.data.keyword.Bluemix_notm}} utilizando la línea de mandatos, las API REST o la interfaz de usuario de {{site.data.keyword.Bluemix_notm}}. |
| Sucesos administrativos de la base de datos del administrador de {{site.data.keyword.Bluemix_notm}} | Sucesos administrativos de la base de datos | Sucesos relacionados con las operaciones realizadas por un administrador de bases de datos en las bases de datos internas de {{site.data.keyword.Bluemix_notm}}. |
| Sucesos de administración | Sucesos de gestión de usuarios | Sucesos relacionados con acciones de gestión de usuarios realizadas en la página Administración. |
| Sucesos de administración | Catálogo | Sucesos relacionados con cambios en el catálogo de servicios. |
| Sucesos de administración | Sucesos de gestión de informes de seguridad | Sucesos relacionados con acciones de gestión de informes de seguridad realizadas en la página Administración. |
| Revisiones de acceso | Informe de revisiones de acceso | Revisiones para accesos privilegiados. |
| Gestión de cambios | Gestión de cambios de software | Actividad de gestión de cambios. |
| Gestión de claves | Gestión de certificados SSL personalizados | Certificados SSL personalizados cargados y almacenados. |
| Cifrado | Cifrado data-in-transit (datos en tránsito) | Cifrado data-in-transit (datos en tránsito) configurado. |
| Antivirus | Informe de exploración de antivirus | Software antivirus vigente. |
| Gestión de arreglos de software | Informe de app de parches | Arreglos de software aplicados. |
| Gestión de incidentes de seguridad | Informe de solución de incidentes de seguridad | Pruebas de incidentes de seguridad para la gestión de incidentes de seguridad. |

*Tabla 4. Lista de informe de seguridad*

## Visualización del estado
{: #oc_status}

Puede supervisar el estado de la instancia de {{site.data.keyword.Bluemix_notm}} mediante la página de Estado de {{site.data.keyword.Bluemix_notm}}. Pulse el icono **Cuenta y soporte** ![Cuenta y soporte](../support/images/account_support.svg), y seleccione **Estado**. 

La página Estado es el recurso central para buscar notificaciones y anuncios sobre sucesos clave que afectan a la plataforma {{site.data.keyword.Bluemix_notm}} y a los servicios principales de {{site.data.keyword.Bluemix_notm}}.

Puede suscribirse a un hilo RSS para recibir notificaciones de forma que no tenga que comprobar si se han publicado. Para obtener más información sobre la página Estado y la configuración del hilo RSS, consulte [Visualización de {{site.data.keyword.Bluemix_notm}}](../support/index.html#viewing-bluemix-status).

## Gestión del catálogo
{: #oc_catalog}

Puede gestionar qué servicios e iniciadores de {{site.data.keyword.Bluemix_notm}} podrán ver los usuarios en el Catálogo de {{site.data.keyword.Bluemix_notm}}. Pulse **ADMINISTRACIÓN &gt; GESTIÓN DE CATÁLOGOS**.

Seleccione un mosaico de servicios o iniciadores para editar la visibilidad del plan de servicios o iniciadores. Para editar la visibilidad, seleccione una de las siguientes opciones:

- Para mostrar el servicio o iniciador oculto para que esté visible para los usuarios en el
Catálogo, seleccione **HABILITAR TODOS LOS PLANES**.
- Para ocultar el servicio o el iniciador de los usuarios en el Catálogo de {{site.data.keyword.Bluemix_notm}},
seleccione **INHABILITAR TODOS LOS PLANES**.
- Para controlar la visibilidad de un plan individual, seleccione el nombre del plan y utilice el menú desplegable para seleccionar **Habilitar para todas las organizaciones**, **Inhabilitar para todas las organizaciones** o **Habilitar plan para organizaciones específicas**.

<!-- staging only start -->

### Registro de un intermediario de servicio
{: #servicebrokerui}

Si tiene un servicio que quiere mostrar en su catálogo de {{site.data.keyword.Bluemix_notm}}, debe implementar y registrar un
intermediario de servicio. Tras registrar su intermediario, puede elegir las organizaciones que pueden tener acceso al
servicio en su instancia dedicada o local. 

Los métodos para trabajar con su intermediario de servicio varía según la cantidad de servicios que gestiona, o si ya se ha registrado con
{{site.data.keyword.Bluemix_notm}}. 

- Si su intermediario de servicio gestiona un servicio, puede utilizar la interfaz de usuario para registrarlo tras haber implementado
la [API de intermediario de servicio](http://docs.cloudfoundry.org/services/api.html){: new_window}. Consulte [Registro de un intermediario de servicio que gestiona un servicio](index.html#registerbrokerui). 
- Si su intermediario de servicio gestiona varios servicios, en este momento no puede registrarlo tras haber implementado la API de intermediario de servicio. En su lugar, utilice la CLI cf con el plugin [CLI admin de {{site.data.keyword.Bluemix_notm}}](../cli/plugins/bluemix_admin/index.html) (submandato `ba`) o use la [API de servicio personalizado](index.html#servicebrokerapi). 
- Si su intermediario de servicio ya está registrado y quiere actualizarlo o suprimirlo, utilice la CLI cf con el plugin [CLI admin de {{site.data.keyword.Bluemix_notm}}](../cli/plugins/bluemix_admin/index.html) (submandato `ba`) o use la [API de servicio personalizado](index.html#servicebrokerapi). 

#### Registro de un intermediario de servicio que gestiona un servicio
{: #registerbrokerui}

Realice los pasos siguientes para registrar su intermediario de servicio: 

1\. [Implemente la API del intermediario de servicio de Cloud Foundry
](http://docs.cloudfoundry.org/services/api.html){: new_window} para habilitar la comunicación entre su servicio y {{site.data.keyword.Bluemix_notm}}. La API del intermediario de servicio es un conjunto de puntos finales de REST que {{site.data.keyword.Bluemix_notm}} consume. 

Cuando implementa el intermediario de servicio, en la respuesta JSON de `GET /v2/catalog`, debe proporcionar
las definiciones para su servicio y planes de servicio, incluyendo la información de servicio que quiere visualizar. Por ejemplo, revise
el JSON de ejemplo siguiente de la respuesta del catálogo (GET): 

```
"services": [
   {
      "bindable":true,
      "description":"Cool Service is a data warehousing and analytics solution.",
      "id":"cool-service-id",
      "name":"coolservice",
      "tags":[
         "customer_dedicated"
      ],
      "metadata":{
         "displayName":"Cool Service",
         "serviceMonitorApi":"https://myservicesstatus.mybluemix.net/healthcheck/",
         "providerDisplayName":"Cool company",
         "longDescription":"Cool Service is a data warehousing and analytics solution. You can quickly move your data into a next-generation columnar in-memory database and start running complex analytical queries.",
         "bullets":[
            {
               "title":"Fast and Simple",
               "description":"Cool Service uses dynamic in-memory columnar technology and innovations, such as parallel vector processing and actionable compression to rapidly scan and return relevant data."
            },
            {
               "title":"Connectivity",
               "description":"Cool Service is built to let you connect easily and to all of your services and applications. You can start analyzing your data right away with familiar tools."
            }
         ],
         "featuredImageUrl":"http://path/to/icon_64x64.png",
         "imageUrl":"http://path/to/icon_50x50.png",
         "mediumImageUrl":"http://path/to/icon_32x32.png",
         "smallImageUrl":"http://path/to/icon_24x24.png",
         "documentationUrl":"http://path/to/documentation.html",
         "instructionsUrl":"http://path/to/servicesample.md",
         "termsUrl":"http://path/to/terms_of_agreement.pdf",
         "media":[
            {
               "type":"youtube",
               "thumbnailUrl":"http://path/to/thumbnail.png",
               "url":"http://path/to/youtube/video",
               "caption":"Using Cool Service in 60 Seconds"
            },
            {
               "type":"image",
               "thumbnailUrl":"http://path/to/thumbnail.png",
               "url":"http://path/to/image_file.png",
               "caption":"Cool Service connects applications"
            },
            {
               "type":"video",
               "thumbnailUrl":"http://path/to/thumb.png",
               "caption":"Cool Service works with tables",
               "source":[
                  {
                     "type":"video/mp4",
                     "url":"http://path/to/video_file.mp4"
                  },
                  {
                     "type":"video/ogg",
                     "url":"http://path/to/video_file.ogg"
                  }
               ]
            }
         ]
      },
      "plans":[
         {
            "name":"smallplan",
            "description":"Dedicated schema and tablespace per service instance on a shared server. 1GB and 10GB of compressed database storage can hold up to 5GB and 50GB of uncompressed data respectively based on typical compression ratios.",
            "free":false,
            "id":"cool-service-plan-id",
            "metadata":{
               "bullets":[
                  "1 GB Min per instance. 10 GB Max per instance."
               ],
               "costs":[
                  {
                     "unitId":"INSTANCES_PER_MONTH",
                     "unit":"MONTHLY",
                     "partNumber":"D15UTLL"
                  }
               ],
               "displayName":"Small"
            }
         }
      ]
   }
]
}
```
{: codeblock}

**Nota**: cuando crea un intermediario de servicio para un entorno local o dedicado, debe especificar
`customer_dedicated` en el campo "tags" de su archivo JSON de definición de servicio. 

2\. Tras implementar la API del intermediario de servicio, acceda a **ADMINISTRACIÓN &gt; GESTIÓN DEL CATÁLOGO**.

3\. pULSE **REGISTRAR UN INTERMEDIARIO DE SERVICIO**.

4\. Complete el formulario especificando los valores en los campos siguientes: 

- Nombre de intermediario de servicio
- URL de intermediario de servicio
- Nombre de usuario del intermediario de servicio
- Contraseña del intermediario de servicio

5\. Pulse **CONECTAR**.

6\. Revise la información de su servicio, incluyendo los planes disponibles, el icono y la descripción del servicio. 

**Nota**: si necesita cambiar la información del catálogo para el servicio, actualice su intermediario de servicio e
inicie el proceso de registro otra vez rellenado el formulario. 

7\. Pulse **REGISTRAR**. 

8\. Elija para habilitar todos los planes o solo los planes específicos para su servicio. De forma predeterminada se inhabilitan
todos los planes. 

9\. Habilite la instancia de servicio para todas las organizaciones o para organizaciones específicas. 

Ahora puede ver su servicio en la categoría Servicios personalizados en su catálogo de {{site.data.keyword.Bluemix_notm}}. Acceda a
**ADMINISTRACIÓN &gt; GESTIÓN DEL CATÁLOGO**, y seleccione el icono en el catálogo. Puede habilitar distintos planes y editar la visibilidad del plan para sus organizaciones en cualquier momento. 

## Administración de organizaciones
{: #oc_organizations}

Puede gestionar sus organizaciones creando y suprimiendo organizaciones, añadiendo o eliminando gestores para organizaciones y
supervisando el uso de la cuota para tomar las mejores decisiones en su negocio. 

Pulse **ADMINISTRACIÓN &gt; ADMINISTRACIÓN DE LA ORGANIZACIÓN**.

Puede expandir y visualizar diversas secciones. También puede revisar y gestionar los planes de cuotas de sus organizaciones.

### Creación de organizaciones

Para crear una nueva organización y añadir gestores, realice los pasos siguientes: 

1. Pulse <strong>CREAR ORGANIZACIÓN</strong>. 
2. Especifique un nombre para la organización
3. Especifique el nombre o correo electrónico de la persona que quiera añadir como gestor. Puede añadir más de un gestor especificando y seleccionando varios nombres.
4. Pulse <strong>CREAR ORGANIZACIÓN</strong> para guardar los cambios y crear la organización.

### Supervisión de cuota

En la sección Supervisión de cuotas puede expandir la sección y ver la siguiente información:

- Uso de memoria del entorno. En esta sección se proporcionan detalles sobre el uso de memoria del entorno del sistema completo.
	En el diagrama se proporciona información que incluye la memoria del sistema utilizada, la memoria total del sistema, la cuota utilizada y la cuota total asignada. En la siguiente lista de términos se definen los tipos de uso de memoria que se visualizan en el diagrama.

	<dl>
	<dt><strong>Memoria del sistema utilizada</strong></dt>
	<dd>Memoria física utilizada por el entorno.</dd>
	<dt><strong>Memoria total del sistema</strong></dt>
	<dd>Memoria física total disponible en el entorno.</dd>
	<dt><strong>Cuota desplegada</strong></dt>
	<dd>La suma de la memoria asignada para todas las apps desplegadas en todas las organizaciones. La suma de
	la cuota desplegada puede superar la memoria física total del sistema de su entorno. Por ejemplo, si tiene una memoria total del sistema de 16 GB y asigna 4 GB de memoria para cinco organizaciones distintas, la cuota total excede la memoria total del sistema que se ha asignado a todas las organizaciones. Sin embargo, en muchos casos las organizaciones no utilizan la cuota total que se ha asignado a cada una de ellas. Además, es posible que las organizaciones no utilicen su asignación de memoria de cuota total al mismo tiempo. </dd>
	<dt><strong>Cuota total</strong></dt>
	<dd>La memoria total asignada en todas las organizaciones.</dd>
	</dl>

- Uso de memoria de la organización. En esta sección se proporcionan detalles del uso de memoria a nivel de organización. Puede ver la concesión de cuota total y la cuota desplegada para cada organización. En el gráfico se proporciona información que aparece ordenada por el uso de memoria más alto por organización; la organización que utiliza la cantidad de memoria más elevada aparece en primer lugar de forma predeterminada. Puede ordenar por **Uso de memoria más alto** y **Asignación de memoria excesiva**.

	<dl>
	<dt><strong>Uso de memoria máximo</strong></dt>
	<dd>Utilice esta opción para identificar la organización que utiliza la mayor cantidad de memoria. Ordene por uso de memoria más alto
	para identificar las organizaciones que utilizan la mayor cantidad de memoria. La lista está ordenada por cuota desplegada. </dd>
	<dt><strong>Asignación de memoria excesiva</strong></dt>
	<dd>Utilice esta opción para identificar las organizaciones que tienen un plan de cuotas superior al necesario:
	ordene por uso de memoria excesivo para identificar las organizaciones que utilizan la cantidad de memoria más pequeña para la cuota que se les ha asignado. </dd>
	</dl>

### Ajuste de planes de cuota

Para cambiar el plan de cuota para una organización, realice los pasos siguientes: 

<ol>
<li>Pulse la barra del gráfico de la organización que desea editar en la sección Uso de memoria de la organización, o bien seleccione el nombre de la organización en la sección Lista de organizaciones. </li>
<li>En la página Gestionar organización puede cambiar el plan de cuotas, cambiar el nombre de la organización y añadir o eliminar gestores. <br />
<p><strong>Nota</strong>: Si selecciona un plan de cuotas insuficiente para el uso actual de la organización, recibirá un mensaje. </p>
</li>
<li>Para guardar los cambios que haya efectuado en la página Gestionar
organización, pulse <strong>GUARDAR</strong>.</li>
</ol>

### Gestión de sus organizaciones desde la lista de organizaciones

En la sección Lista de organizaciones, puede ver todas las organizaciones del entorno
de {{site.data.keyword.Bluemix_notm}}, y puede realizar acciones para organizaciones individuales pulsando en el nombre de la organización. 

- Para suprimir la organización, pulse el icono **Suprimir** ![Suprimir](images/icon_trash.svg) en la columna Acciones. 
- Para ver el plan de cuotas y uso de una organización, pulse el nombre de la organización en la lista. En la página **Gestionar organizaciones** para la
organización que ha seleccionado, puede ver la información de uso siguiente: 

  - Número de servicios que hay actualmente en uso. 
  - Número de rutas que hay actualmente en uso. 
  - Gráfico de cuota de memoria que muestra qué parte de la cuota está en uso y qué parte no se usa actualmente. 
  - Gráfico de asignación de aplicaciones que muestra qué aplicaciones se incluyen en la cuota de memoria utilizada. 
  - Gráfico de uso de aplicaciones medidas que muestra un informe de tres meses de los GB-horas usados por app desplegada. Puede
seleccionar la **Vista de lista** para ver los datos de todas las aplicaciones, incluyendo la asignación de memoria por app y
el uso de GB-hora medido para los últimos tres meses. 

- Para editar el nombre de la organización y añadir o eliminar gestores, pulse el nombre de la organización en la lista y siga las indicaciones en pantalla. 

## Gestión de usuarios y permisos
{: #oc_useradmin}

Puede añadir usuarios a la instancia de {{site.data.keyword.Bluemix_notm}} del registro de usuarios de la empresa mediante LDAP. Puede añadir usuarios individualmente o en grupos, y ver los permisos de usuario. Si tiene asignado el permiso `admin`, también puede establecer y gestionar permisos de otros usuarios. Pulse **ADMINISTRACIÓN &gt; ADMINISTRACIÓN DE USUARIOS**.

La página Administración de usuarios muestra todos los usuarios para la instancia local o dedicada.
Se muestran los permisos para cada usuario. Los permisos pueden ser los siguientes: Ninguno, `Admin`, `Catalog`, `Login`,
`Reports` y `Users`. Los permisos se pueden habilitar o bien se puede asignar al usuario acceso para `view` o `write` para dicho permiso, representado mediante iconos. Consulte [Permisos](#permissions) para ver las descripciones
de cada tipo y las explicaciones de los iconos.

Elija una de las opciones siguientes:

* Localizar usuarios. Puede localizar usuarios en la tabla mediante el campo **Buscar**.
* Añadir usuarios. Si tiene el permiso `admin` o el permiso `users` con la acceso `write`, puede añadir usuarios. Para añadir un usuario o un grupo de usuarios, pulse **AÑADIR UN SOLO USUARIO** o **AÑADIR GRUPO DE USUARIOS**. En el campo **Buscar**, escriba el nombre de usuario o nombre de grupo que desea buscar y seleccione la organización a la que desea añadir el usuario o el grupo de usuarios en la lista **Org**. Cuando encuentre el usuario o grupo que desea añadir, pulse el nombre de usuario y luego pulse **AÑADIR USUARIO** o **AÑADIR USUARIOS** para añadirlos.
Los grupos de más de 50 usuarios se añaden mediante un trabajo por lotes en segundo plano. Cuando la operación de añadir finaliza correctamente, el usuario o grupo se añade a la tabla para que lo pueda ver y buscar. Cuando se añaden usuarios, no tienen ningún permiso asignado.
* Editar permisos y organizaciones. Si tiene el permiso `admin`, puede editar permisos y organizaciones de otros usuarios. Para editar permisos, localice el usuario y pulse el nombre de usuario. Para habilitar o inhabilitar permisos, seleccione una de las opciones siguientes en la ventana que se abre:
	* Seleccione **Activado** en la lista para habilitar un permiso.
	* Seleccione **Leer** en la lista para que el usuario tenga el acceso
`view` (solo lectura) sobre dicho permiso, o seleccione **Escribir** para asignar el
acceso `write` (editar o añadir y eliminar) para dicho permiso.
	* Seleccione **Desactivado** para inhabilitar el permiso.
Para editar organizaciones, seleccione una de las siguientes opciones:
	* Para añadir el usuario a una organización, utilice el campo de búsqueda para localizar una organización, pulse para seleccionar una de las opciones y pulse **AÑADIR**.
	* Para eliminar un usuario de una organización, pulse el icono ![Eliminar, representado mediante un signo menos](images/icon_remove.svg).
Cuando termine, pulse **GUARDAR**.
* Eliminar usuarios. Si tiene el permiso `admin` o el permiso `users` con el acceso `write`, puede eliminar usuarios. Para eliminar un usuario, localice el usuario y pulse el icono ![Suprimir](images/icon_trash.svg) y, a continuación, **Eliminar**.

### Permisos
{: #permissions}

Se pueden asignar los siguientes permisos a los usuarios:

| **Permiso de usuario** | **Descripción** |       
|-----------------|-------------------|
| Admin | Los usuarios con el permiso `admin` pueden editar los permisos de otros usuarios. |
| Catálogo | A los usuarios con el permiso `catalaog` se les puede asignar el acceso para `view` o `write` (modificar) los servicios que están disponibles en la instancia local o dedicada.  |  
| Login | Los usuarios con el permiso `login` pueden ver la página Administración. Sin este permiso, los usuarios no pueden ver la opción de menú Administración. |
| Reports | A los usuarios con el permiso `reports` se les puede asignar acceso `view` o `write` (modificar) sobre los informes de seguridad. |
| Users | A los usuarios con el permiso `users` se les puede asignar el acceso `view` sobre la lista de usuarios o `write` (añadir o eliminar) sobre los usuarios. Este permiso no le permite definir permisos para otros usuarios.|

*Tabla 5. Permisos*

Los permisos se pueden habilitar o bien se puede asignar al usuario acceso `view` o `write` para dicho permiso, representado mediante los siguientes iconos: 

* El icono ![Habilitado, representado mediante una marca de selección](images/icon_enabled.svg) junto a un permiso significa que está habilitado.
* El icono ![Ver, representado mediante un ojo](images/icon_read.svg) significa que el usuario tiene el acceso `view` (solo lectura) sobre dicho permiso. 
* El icono ![Grabar, representado por un lápiz](images/icon_write.svg) significa que el usuario tiene
acceso `write` (editar, añadir o eliminar) para dicho permiso. 

## Gestión de usuarios con la API REST de administración
{: #usingadminapi}

Puede utilizar la API REST `Admin` para añadir y eliminar usuarios de la instancia de
{{site.data.keyword.Bluemix_notm}}.
Se proporcionan puntos finales de la API REST `Admin` y respuestas JSON a modo experimental para habilitar operaciones básicas desde una línea de mandatos. Los puntos finales y URL de los ejemplos de esta información pueden cambiar o pueden ser retirados previo aviso.

Las herramientas siguientes constituyen requisitos previos para utilizar los ejemplos siguientes. También puede utilizar otras herramientas.
* cURL, para especificar solicitudes de la API REST como mandatos. cURL es un programa de utilidad gratuito que puede utilizar para enviar solicitudes HTTP a un servidor y recibir las respuestas del servidor a través de una interfaz de línea de mandatos. Puede descargar
cURL del [Sitio de descargas de cURL](http://curl.haxx.se/download.html){: new_window}.
* Python, para utilizar la herramienta JSON pretty-print de Python. Esta herramienta opcional toma texto JSON como entrada y genera información de salida de fácil lectura. Puede descargar Python del [Sitio de descargas de Python](https://www.python.org/downloads){: new_window}.

### Inicio de sesión en la consola de administración

Para poder ejecutar cualquier solicitud de la API `Admin`, debe iniciar una sesión en la consola de administración. Si tiene el permiso `admin` o el permiso `users` con el acceso `write`, puede añadir o eliminar usuarios. Debe tener el permiso `admin` para poder editar los permisos de otros usuarios.

Para iniciar la sesión en la Consola de administración, puede utilizar la autenticación de acceso básica en el punto final
`https://<su_host>.ibm.com/login`. El servidor devuelve una cookie con la sesión. Utilice dicha cookie para todas las operaciones con la consola de administración.

**Nota:** La sesión deja de ser válida si no se utiliza durante unas cuantas horas.

Para iniciar una sesión en la consola de administración, ejecute el mandato siguiente:

`curl --user <id_usuario>:<contraseña> -c ./cookies.txt --header "Accept: application/json" https://<su_host>.ibm.com/login | python -m json.tool`
{: codeblock}

<dl class="parml">

<dt class="pt dlterm">--user <em>id_usuario</em>:<em>contraseña</em></dt>
<dd class="pd">Acepta el ID de usuario y la contraseña y envía una cabecera de autorización básica.</dd>


<dt class="pt dlterm">-c <em>nombre_archivo</em></dt>
<dd class="pd">Almacena el ID de usuario y la contraseña especificados como una cookie en el archivo especificado.</dd>


<dt class="pt dlterm">--header</dt>
<dd class="pd">Envía una cabecera de aceptación.</dd>

</dl>

El siguiente ejemplo muestra la salida de este mandato:
```
{
    "message": "Logged in",
    "name": {
        "familyName": "*apellido*",
        "givenName": "*nombre*"
    }
}
```
{: screen}

### Listado de organizaciones
{: #listingorg}

Cuando añada un usuario, debe especificar una organización. Puede utilizar la API REST `Admin` para obtener una lista de todas las organizaciones. Debe tener el permiso
`users` con acceso `read` para poder listar
organizaciones. Para listar todas las organizaciones, ejecute el mandato siguiente: 

`curl -b ./cookies.txt https://<su_host>.ibm.com/codi/v1/organizations | python -m json.tool`
{: codeblock}

<dl class="parml">

<dt class="pt dlterm">-b <em>nombre_archivo</em></dt>
<dd class="pd">Pasa el ID de usuario y la contraseña que se han almacenado anteriormente con la opción <samp class="ph codeph">-c</samp> en el archivo al servidor HTTP como una cookie.</dd>

</dl>

Para cada organización, los resultados incluyen la siguiente información:
* `"guid"`, GUID de la organización
* `"name"`, nombre de la organización

El siguiente ejemplo muestra la salida de este mandato:
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

### Listado de usuarios
{: #listingusr}

Puede determinar si un usuario ya se ha añadido al entorno de
{{site.data.keyword.Bluemix_notm}} mediante
la API REST de `Admin` para obtener una lista de los usuarios registrados. Debe tener
el permiso `users` con acceso `read` para poder listar usuarios registrados.
Para listar todos los usuarios, ejecute el mandato siguiente: 

`curl -b ./cookies.txt https://<su_host>.ibm.com/codi/v1/users | python -m json.tool`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-b <em>nombre_archivo</em></dt>
<dd class="pd">Pasa el ID de usuario y la contraseña que se han almacenado anteriormente con la opción <samp class="ph codeph">-c</samp> en el archivo al servidor HTTP como una cookie.</dd>
</dl>

Para cada usuario registrado, los resultados incluyen la siguiente información:
* `"first_name"` (nombre) y
                                `"last_name"` (apellido)
* `"user_id"`, ID de usuario y dirección de correo electrónico
* `"guid"`, GUID de la organización.
* `"permissions"` asignados al usuario para la consola de administración.

El siguiente ejemplo muestra la salida de este mandato:

```
{
    "next_url": "/codi/v1/users?results_per_page=100&amp;page=2",
    "prev_url": "",
    "resources": [
        {
            "active": true,
            "created_at": "2015-04-08T17:38:51.788Z",
            "created_by": "",
            "first_name": "some first name",
            "guid": "5d5268cf-39c0-48d3-96ae-7afe928e5dd7",
            "last_name": "some last name",
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
            "user_id": "someid@us.ibm.com"
        },
		 		 ...


     }
    ],
    "total_pages": 395,
    "total_results": 39421
}

```
{: screen}

### Adición de un usuario

Puede utilizar la API REST `Admin` para añadir usuarios a la instancia de
{{site.data.keyword.Bluemix_notm}}. Debe tener el permiso `users` con acceso `write` para poder añadir usuarios. 

Puede añadir un usuario o una lista de usuarios. Puede añadir usuarios a una única
organización, o a varias organizaciones. Para añadir un usuario, debe proporcionar la información siguiente: 

* Nombre y apellido del usuario. Especifique
`"nombre"` y `"apellido"` de [Listado de usuarios](index.html#listingusr).
* Dirección de correo electrónico e ID de usuario: especifique el `"id_usuario"` del [Listado de usuarios](index.html#listingusr) tanto para la dirección de correo electrónico como para el ID de usuario.
* `"guid"`. Especifique el GUID de la organización de [Listado de organizaciones](index.html#listingorg).

Debe proporcionar la información en un archivo JSON.

`curl -b ./cookies.txt https://<su_host>.ibm.com/codi/v1/users | python -m json.tool`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-b <em>nombre_archivo</em></dt>
<dd class="pd">Pasa el ID de usuario y la contraseña que se han almacenado anteriormente con la opción <samp class="ph codeph">-c</samp> en el archivo al servidor HTTP como una cookie.</dd>
</dl>

<ol>
<li>Cree un archivo JSON que contenga la información en un formato JSON adecuado.
<p>Por ejemplo, cree un archivo llamado `user.json` con el siguiente contenido:</p>
<pre>
{
    "members": [
        {
            "emails": [
                "some_user_id@domain.com"
            ],
            "first_name": "Some_first_name",
            "last_name": "Some_last_name",
            "user_id": "some_user_id@domain.com"
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
<li>Publique el contenido del archivo JSON en el punto final del usuario mediante la ejecución del mandato
siguiente:<br/><br/>
<code>
curl -v -b ./cookies.txt -X POST -H "Content-Type: application/json" -d @./user.json https://<su_host>.ibm.com/codi/v1/users
</code>
</li>
</ol>

<dl class="parml">

<dt class="pt dlterm">-v </dt>
<dd class="pd">Especifica salida detallada.</dd>


<dt class="pt dlterm">-X POST</dt>
<dd class="pd">Especifica una solicitud POST, alterando temporalmente la solicitud GET predeterminada.</dd>


<dt class="pt dlterm">-H "Content-Type: application/json"</dt>
<dd class="pd">Especifica la cabecera content-type, que en este caso es JSON.</dd>


<dt class="pt dlterm">-d *datos*</dt>
<dd class="pd">Especifica los datos, en este caso el archivo `user.json`, que se van a enviar en la solicitud POST al servidor HTTP.</dd>

</dl>



El siguiente ejemplo muestra la salida de este mandato:

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

### Eliminación de un usuario

Puede utilizar la API REST `Admin` para eliminar usuarios de la instancia de
{{site.data.keyword.Bluemix_notm}}. Debe tener el permiso `users` con acceso `write` para poder eliminar usuarios. 

Para eliminar un usuario, debe especificar el ID del usuario. Ejecute el mandato siguiente:

`curl -v -b ./cookies.txt -X DELETE https://<su_host>.ibm.com/codi/v1/users?user_id=<some_user_id@domain.com>`
{: codeblock}

<dl class="parml">
<dt class="pt dlterm">-X DELETE</dt>
<dd class="pd">Especifica una solicitud DELETE.</dd>
</dl>

El siguiente ejemplo muestra la salida de este mandato:

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


## API de servicio personalizado
{: #servicebrokerapi}

Hay tres API que puede utilizar para registrar o crear un nuevo servicio, actualizar un servicio y suprimir un servicio.

Todas las API son relativas a <code>https://console.&lt;subdomain&gt;.bluemix.net/</code>. 

<dl>
<dt><strong>&lt;subdominio&gt;</strong></dt>
<dd>Este valor es el nombre de la instancia local o dedicada. El nombre del subdominio de la instancia {{site.data.keyword.Bluemix}} se ha asignado
durante la incorporación.</dd>
</dl>

## Registro de un nuevo servicio

Utilice la siguiente API y ejemplos de código para registrar un nuevo servicio.

### Ruta
{: #registerroute}

```
POST /codi/v1/serviceBrokers
```
{: screen}

### Solicitud
{: #registerrequest}

| **Nombre** | **Descripción** |
|-----------------|-------------------|
| name | Nombre del intermediario de servicio. |
| auth_username | Nombre de usuario utilizado para conectarse con el intermediario de servicio. |
| auth_password | Contraseña utilizada para conectarse con el intermediario de servicio. |
| broker_url | URL utilizada para conectarse al intermediario de servicio. |
| owningOrganization | Organización inicial con la que incluir en la lista blanca el servicio. |

*Tabla 6. Campos*

#### Cuerpo
{: #registerbody}

```
{
  "name" : "Service broker's name",
  "auth_username" : "username",
  "auth_password" : "password",
  "broker_url" : "https://broker.comp.com",
  "owningOrganization" : "ORG"
}
```
{: screen}

#### Cabeceras
{: #registerheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### Respuesta
{: #registerresponse}

#### Estado
{: #registerstatus}

```
201 Created
```
{: screen}

#### Cuerpo
{: #registerbody2}

```
{
  "entity": {
    "name": "Service broker's name",
    "broker_url": "https://provision-broker.comp.bluemix.net/bmx/provisioning/brokers/2063580064-8f23230c-7f36-4ce5-a298-2ab4108f1120",
    "auth_username": "username",
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

## Actualización de un servicio

Utilice la siguiente API y ejemplos de código para actualizar un servicio.

### Ruta
{: #updateroute}

`PUT /codi/v1/serviceBrokers`
{: screen}

### Solicitud
{: #updaterequest}

| **Nombre** | **Descripción** |
|-----------------|-------------------|
| name | Nombre del intermediario de servicio. Este nombre no puede modificarse a partir del nombre con el que se ha creado el servicio. |
| auth_username | Nombre de usuario utilizado para conectarse con el intermediario de servicio. |
| auth_password | Contraseña utilizada para conectarse con el intermediario de servicio. |
| broker_url | URL utilizada para conectarse al intermediario de servicio. |
| owningOrganization | Organización inicial con la que incluir en la lista blanca el servicio. |

*Tabla 7. Campos*

#### Cuerpo
{: #updatebody}

```
{
  "name" : "Service Broker's name",
  "auth_username" : "username",
  "auth_password" : "newPassword",
  "broker_url" : "https://broker.comp.com",
  "owningOrganization" : "ORG"
}
```
{: screen}

#### Cabeceras
{: #updateheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### Respuesta
{: #updateresponse}

#### Estado
{: #updatestatus}

```
201 Created
```
{: screen}

#### Cuerpo
{: #updatebody2}

```
{
  "entity": {
    "name": "Service Broker's name",
    "broker_url": "https://provision-broker.dys0.bluemix.net/bmx/provisioning/brokers/2063580064-d11bdd84-7556-469f-858d-2098b531f7f2",
    "auth_username": "username",
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

## Supresión de un servicio

Utilice la siguiente API y ejemplos de código para suprimir un servicio.

| **Nombre** | **Descripción** |
|-----------------|-------------------|
| name | Nombre del intermediario de servicio. Este nombre no puede modificarse a partir del nombre con el que se ha creado el servicio. |

*Tabla 8. Parámetro*

### Ruta

```
DELETE /codi/v1/serviceBrokers?name=name of service broker
```
{: screen}

### Solicitud
{: #deleterequest}

#### Cabeceras
{: #deleteheaders}

```
Authorization: bearer eyJ0eXAiOiJKV1QiLCJhbG ... ciOiJIUzI1
Host: console.comp.bluemix.net
Content-Type: application/json
```
{: screen}

### Respuesta
{: #deleteresponse}

#### Estado
{: #deletestatus}

```
204 No Content
```
{: screen}

## Gestión de usuarios con la CLI cf
{: #usingadmincli}

Puede gestionar usuarios del entorno de
{{site.data.keyword.Bluemix_notm}} mediante la interfaz
de línea de mandatos de Cloud Foundry con el plug-in CLI de
administración de {{site.data.keyword.Bluemix_notm}}. Por ejemplo, puede añadir usuarios de un registro
de LDAP.

Antes de empezar, instale la interfaz de línea de mandatos cf. El plug-in CLI de administración de {{site.data.keyword.Bluemix_notm}} necesita
cf versión 6.11.2 o posterior. [Descargue la interfaz de línea de mandatos
de Cloud Foundry](https://github.com/cloudfoundry/cli/releases){: new_window}

**Restricción:** Cygwin no admite la interfaz de línea de mandatos de Cloud Foundry. Utilice esta interfaz en una ventana de línea de mandatos que no sea la ventana de Cygwin.

### Adición del plug-in CLI de administración de {{site.data.keyword.Bluemix_notm}}

Una vez instalada la interfaz de línea de mandatos cf, puede añadir el plug-in CLI de administración de {{site.data.keyword.Bluemix_notm}}.

**Nota**: si ha instalado previamente el plugin Admin de {{site.data.keyword.Bluemix_notm}}, es posible que
tenga que desinstalarlo, suprimir el repositorio y luego volver a instalarlo para obtener las actualizaciones más recientes. 

Siga estos pasos para añadir el repositorio e instalar el plug-in:

<ol>
<li>Para añadir el repositorio de plugin de administración de {{site.data.keyword.Bluemix_notm}}, ejecute el mandato siguiente:<br/><br/> <code>
cf add-plugin-repo BluemixAdmin https://console.&lt;subdominio&gt;.bluemix.net/cli
</code><br/><br/>
<dl class="parml">
<dt class="pt dlterm">&lt;subdominio&gt;</dt>
<dd class="pd">Subdominio del URL correspondiente a la instancia de {{site.data.keyword.Bluemix_notm}}.</dd>
</dl>
</li>
<li>Para instalar el plug-in de CLI de administración de {{site.data.keyword.Bluemix_notm}}, ejecute el siguiente mandato:<br/><br/> <code>
cf install-plugin bluemix-admin-cli -r BluemixAdmin
</code>
</li>
</ol>

Para ver una lista de mandatos, ejecute el mandato siguiente:

`cf plugins`
{: codeblock}

Para obtener más ayuda sobre un mandato, utilice la opción `-help`.

Para obtener más información sobre cómo trabajar con el plug-in CLI de administración de {{site.data.keyword.Bluemix_notm}}, consulte Administración de [{{site.data.keyword.Bluemix_notm}}](../cli/plugins/bluemix_admin/index.html).
