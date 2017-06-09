---
title: Configuración de las herramientas de proceso
summary: "Esta sección describe las acciones asociadas con la configuración de los elementos reutilizables en un proceso de negocio"
sidebar: swbp_sidebar
permalink: swbp_processmanagement_tools.html
folder: swbp
---

## Herramientas de Proceso
Las herramientas de proceso, descritas en las siguientes secciones, son elementos reutilizables que se organizan en catálogos. Dichas herramientas se ubican en el nodo _Herramientas de Proceso_ {% include inline_image.html class="icon" file="screenshots/icon_processtools.png" %} del árbol de estructura del sitio, como se muestra en la siguiente figura.

{% include image.html class="centered x-small shadow adjusted" file="screenshots/swbp_processtools.png" alt="BPM" %}

## Certificados X509
X509 es un estándar que define, entre otras cosas, el manejo de certificados digitales y comunicación segura en la web y por e-mail. SWBProcess utiliza certificados bajo este estándar para proporcionar firmado electrónico al cierre de las tareas.

{{site.data.alerts.callout_success}}
SWBProcess no utiliza una entidad validadora para procesar los certificados. En su lugar, utiliza los datos en el certificado en asociación con el perfil del usuario para validar la identidad.
{{site.data.alerts.end}}

### Creación de certificados
Para crear un certificado necesitará un archivo de certificado creado en este estándar (archivo .cer). Puede conseguir este archivo con alguna entidad generadora de certificados.

Deberá hacer click con el botón derecho en el nodo _Certificados X509_ {% include inline_image.html file="screenshots/icon_X509.png" class="icon" %} y seleccionar la opción **Agregar Certificado X509** como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_addx509_menu.gif" alt="Opción para agregar certificado" %}

Se presentará el diálogo _Agregar Certificado X509_ como se muestra en la siguiente figura. En el diálogo deberá presionar el botón **Select File** del campo **Archivo**.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_newx509_dialog.png" alt="Diálogo crear certificado" %}

Se mostrará una pantalla de selección donde deberá ubicar su archivo de certificado.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_newx509_selectdialog.png" alt="Diálogo seleccionar certificado" %}

Una vez seleccionado el archivo, se mostrará un mensaje de confirmación de la carga y podrá presionar el botón **Guardar**.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_newx509_confirmdialog.png" alt="Confirmación de carga de certificado" %}

Finalmente, se mostrará en la zona de trabajo el nuevo certificado con la pestaña _Información_ seleccionada por defecto. En el campo **Sujeto** del formulario se presentará la información contenida en el certificado y en el campo **Serie** se mostrará el valor utilizado para asociar el certificado con un perfil de usuario.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_x509_tabs.png" alt="Pestañas del certificado" %}

### Asociación de un certificado con un perfil de usuario
La asociación de un perfil de usuario con un certificado X509 se realiza mediante el valor del campo **Serie** del certificado. Para ello, deberá primero ubicar ese valor en la pestaña de _Información_ del certificado, como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_x509_serial.png" alt="Serie del certificado" %}

Posteriormente, deberá acceder a la configuración de los datos del usuario al que desea asociar el certificado. Para ello, puede consultar el procedimiento en la sección [Edición de las propiedades de un usuario](http://localhost:4000/swbp_users.html#edicin-de-las-propiedades-de-un-usuario). Una vez en la pestaña de configuración del usuario, ubique el campo **ID externo** y capture el valor del campo **Serie** del certificado.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_externalID.png" alt="ID externo del usuario" %}

Finalmente, presione el botón **Guardar** para actualizar la información del usuario. Desde ese momento, la identidad del usuario será relacionada con el certificado referido.

### Modificación de la configuración de un certificado
Para modificar las propiedades de un certificado deberá acceder a la pestaña de información del mismo. Se presentará un formulario donde podrá modificar la información de acuerdo con la siguiente tabla.

|Propiedad|Descripción|
|---|---|
|Archivo|Muestra una ventana de selección para ubicar un archivo .cer|
|Eliminar|Si marca esta casilla, el archivo .cer asociado al certificado será eliminado.|
|Fecha de expiración|Muestra un calendario para establecer una fecha de expiración del certificado.|

### Eliminación de certificados
Podrá eliminar un certificado presionando el botón **Eliminar** en el formulario de la pestaña de información del mismo.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_x509_removebutton.png" alt="Botón de eliminación" %}

También puede realizar la acción desde el árbol de estructura del sitio, haciendo click con el botón derecho sobre el nombre del certificado y seleccionando la opción **Eliminar**, como se muestra en la siguiente figura.

{% include image.html class="centered small shadow adjusted" file="screenshots/swbp_x509_removeoption.gif" alt="Opción de eliminación del certificado" %}

En cualquier caso, se solicitará confirmación de la acción. Si acepta, el certificado será eliminado y desaparecerá del árbol del sitio.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_x509_deleteconfirm.png" alt="Confirmación de eliminación del certificado" %}

## Plantillas de notificaciones
El motor de SWBProcess permite el envío de correos para notificar asignaciones de tareas o condiciones de retraso según la configuración de un proceso de negocio. Para este fin, SWBProcess hace uso de plantillas de notificaciones, que incorporan la información del mensaje de correo que se enviará.

### Creación de plantillas de notificaciones
Para crear una plantilla de notificaciones deberá hacer click con el botón derecho en el nodo _Plantillas de Notificaciones_ {% include inline_image.html file="screenshots/icon_notificationtemplates.png" class="icon" %} y seleccionar la opción **Agregar Plantilla de Notificaciones** como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_addnotificationtemplate_menu.gif" alt="Opción para agregar plantilla de notificación" %}

Se presentará el diálogo _Agregar Plantilla de Notificaciones_, deberá capturar un título para la plantilla y presionar el botón **Guardar**.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_newnotificationtemplate_dialog.png" alt="Diálogo crear plantilla de notificación" %}

Finalmente, se mostrará en la zona de trabajo la nueva plantilla de notificaciones con la pestaña _Información_ seleccionada por defecto.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_notificationtemplate_tabs.png" alt="Pestañas de la plantilla" %}

### Edición de las propiedades de una plantilla de notificaciones
Para modificar las propiedades de una plantilla de notificaciones deberá acceder a la pestaña de información de la misma. Se presentará un formulario donde podrá modificar la información de acuerdo con la siguiente tabla.

|Propiedad|Descripción|
|---|---|
|Título|Nombre visible de la plantilla en toda la administración, este nombre es usado como campo de búsqueda.|
|Descripción|Descripción del propósito de la plantilla.|
|Asunto|Asunto que aparecerá en el correo electrónico enviado.|
|Cuerpo del mensaje|Contenido del mensaje de correo electrónico que será enviado.|

### Eliminación de plantillas de notificaciones
Podrá eliminar una plantilla de notificaciones presionando el botón **Eliminar** en el formulario de la pestaña de información de la misma.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_notificationtemplate_removebutton.png" alt="Botón de eliminación" %}

También puede realizar la acción desde el árbol de estructura del sitio, haciendo click con el botón derecho sobre el nombre de la plantilla y seleccionando la opción **Eliminar**, como se muestra en la siguiente figura.

{% include image.html class="centered small shadow adjusted" file="screenshots/swbp_notificationtemplate_removeoption.gif" alt="Opción de eliminación de la plantilla" %}

En cualquier caso, se solicitará confirmación de la acción. Si acepta, la plantilla será eliminada y desaparecerá del árbol del sitio.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_notificationtemplate_deleteconfirm.png" alt="Confirmación de eliminación de la plantilla" %}

## Plantillas de archivos
El motor de SWBProcess permite el llenado de documentos MSWord con información de las variables del proceso como resultado de actividades de servicio. Para este fin, SWBProcess hace uso de plantillas de archivos, que definen campos de mezcla de correo para insertar la información proveniente del proceso.

### Creación de plantillas de archivos
{{site.data.alerts.callout_success}}
Para crear una plantilla de archivos deberá contar previamente con un archivo MSWord con campos de mezcla de correo referenciando variables del proceso. Puede consultar la documentación asociada con la inserción de campos de mezcla de correo en el <a href="https://answers.microsoft.com/en-us/msoffice/forum/msoffice_word-mso_other/mail-merge-in-word/7636c3c6-e5bf-403d-a2f7-31c2867828dd">foro de ayuda</a> de Microsoft. También puede consultar la información sobre el <a href="http://localhost:4000/swbp_processmanagement_processconfig.html#variables-de-procesos-en-la-configuracin-de-los-elementos">uso de variables de procesos</a> en la configuración de SWBProcess.
{{site.data.alerts.end}}

Para crear una nueva plantilla de archivos deberá hacer click con el botón derecho en el nodo _Plantillas de Archivos_ {% include inline_image.html file="screenshots/icon_filetemplates.png" class="icon" %} y seleccionar la opción **Agregar Plantilla de Archivo de Proceso** como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_addfiletemplate_menu.gif" alt="Opción para agregar plantilla de archivos" %}

Se presentará el diálogo _Agregar Plantilla de Archivo de Proceso_, deberá capturar un título para la plantilla y presionar el botón **Guardar**.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_newfiletemplate_dialog.png" alt="Diálogo crear plantilla de archivo" %}

Finalmente, se mostrará en la zona de trabajo la nueva plantilla de archivo con la pestaña _Información_ seleccionada por defecto.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_filetemplate_tabs.png" alt="Pestañas de la plantilla" %}

En el formulario presentado, deberá presionar el botón **Select File** del campo **Archivo**.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_filetemplate_filebutton.png" alt="Botón para seleccionar archivo" %}

Se mostrará una pantalla de selección donde deberá ubicar el archivo MSWord deseado.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_filetemplate_selectdialog.png" alt="Diálogo seleccionar archivo" %}

Una vez seleccionado el archivo, se mostrará un mensaje de confirmación de la carga y podrá presionar el botón **Guardar**.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_filetemplate_confirmmesage.png" alt="Confirmación de carga de archivo" %}

Se mostrará el archivo en el campo **Archivo** del formulario.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_filetemplate_fileloaded.png" alt="Información del archivo asociado" %}

### Edición de las propiedades de una plantilla de archivos
Para modificar las propiedades de una plantilla de archivos deberá acceder a la pestaña de información de la misma. Se presentará un formulario donde podrá modificar la información de acuerdo con la siguiente tabla.

|Propiedad|Descripción|
|---|---|
|Título|Nombre visible de la plantilla en toda la administración, este nombre es usado como campo de búsqueda.|
|Descripción|Descripción del propósito de la plantilla.|
|Archivo|Muestra una ventana de selección para ubicar un archivo MSWord.|
|Eliminar|Si marca esta casilla, el archivo asociado a la plantilla será eliminado.|

### Eliminación de plantillas de archivos
Podrá eliminar una plantilla de archivos presionando el botón **Eliminar** en el formulario de la pestaña de información de la misma.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_filetemplate_removebutton.png" alt="Botón de eliminación" %}

También puede realizar la acción desde el árbol de estructura del sitio, haciendo click con el botón derecho sobre el nombre de la plantilla y seleccionando la opción **Eliminar**, como se muestra en la siguiente figura.

{% include image.html class="centered small shadow adjusted" file="screenshots/swbp_filetemplate_removeoption.gif" alt="Opción de eliminación de la plantilla" %}

En cualquier caso, se solicitará confirmación de la acción. Si acepta, la plantilla será eliminada y desaparecerá del árbol del sitio.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_filetemplate_deleteconfirm.png" alt="Confirmación de eliminación de la plantilla" %}

## Intervalos de ejecución
Los intervalos de ejecución permiten definir condiciones asociadas a eventos temporales, por ejemplo, una calendarización para una fecha y hora determinada o un evento recurrente cada cierto periodo de tiempo. El motor de SWBProcess utiliza los intervalos de ejecución para configurar los eventos temporizadores en el flujo de un proceso.

### Creación de intervalos de ejecución
Para crear un intervalo de ejecución deberá hacer click con el botón derecho en el nodo _Intervalos de ejecución_ {% include inline_image.html file="screenshots/icon_interval.png" class="icon" %} y seleccionar la opción **Agregar Intervalo de Ejecución** como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_addinterval_menu.gif" alt="Opción para agregar intervalo de ejecución" %}

Se presentará el diálogo _Agregar Intervalo de Ejecución_, deberá capturar un título para el intervalo y presionar el botón **Guardar**.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_newninterval_dialog.png" alt="Diálogo crear intervalo de ejecución" %}

Finalmente, se mostrará en la zona de trabajo el nuevo intervalo con la pestaña _Información_ seleccionada por defecto.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_interval_tabs.png" alt="Pestañas del intervalo de ejecución" %}

### Edición de las propiedades generales de un intervalo de ejecución
Para modificar las propiedades de un intervalo de ejecución deberá acceder a la pestaña de información del mismo. Se presentará un formulario donde podrá modificar la información de acuerdo con la siguiente tabla.

|Propiedad|Descripción|
|---|---|
|Título|Nombre visible del intervalo en toda la administración, este nombre es usado como campo de búsqueda.|
|Descripción|Descripción del propósito del intervalo.|
|Activo|Permite activar/desactivar el elemento.|

### Configuración de un intervalo de ejecución
Para configurar un intervalo, deberá acceder a su pestaña _Editar Periodo_, como se muestra en la siguiente figura. Si desea configurar el intervalo como un evento calendarizado, deberá presionar el botón **Temporizador** (seleccionado por defecto). Se mostrará un formulario donde podrá definir la fecha y hora de inicio y fin o un tiempo de espera en minutos.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_interval_timer.png" alt="Intervalo como temporizador" %}

{{site.data.alerts.callout_success}}
Al configurar un intervalo como temporizador, las opciones <i>Termina</i> y <i>No termina</i> de la sección <i>Inicio y fin</i> se desactivan. Si selecciona la casilla <i>Tiempo de espera</i>, las opciones de la sección <i>Inicio y fin</i> se desactivan.
{{site.data.alerts.end}}

Si desea configurar el intervalo como un evento recurrente, deberá presionar el botón **Intervalo**. Se mostrará un formulario donde podrá definir con detalle la información del evento.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_interval_interval.png" alt="Intervalo como temporizador" %}




### Eliminación de intervalos de ejecución
Podrá eliminar un intervalo de ejecución presionando el botón **Eliminar** en el formulario de la pestaña de información del mismo.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_interval_removebutton.png" alt="Botón de eliminación" %}

También puede realizar la acción desde el árbol de estructura del sitio, haciendo click con el botón derecho sobre el nombre del intervalo y seleccionando la opción **Eliminar**, como se muestra en la siguiente figura.

{% include image.html class="centered small shadow adjusted" file="screenshots/swbp_interval_removeoption.gif" alt="Opción de eliminación del intervalo" %}

En cualquier caso, se solicitará confirmación de la acción. Si acepta, el intervalo será eliminado y desaparecerá del árbol del sitio.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_interval_deleteconfirm.png" alt="Confirmación de eliminación del intervalo" %}

{{site.data.alerts.callout_warning}}
Al eliminar un intervalo de ejecución se eliminan las asociaciones del mismo con los eventos temporizadores de los procesos, por lo que la configuración de los flujos se verá afectada.
{{site.data.alerts.end}}


## Reglas de negocio

## Conexiones a BD

## Servicios web

## Propiedades de asignación

{% include links.html %}
