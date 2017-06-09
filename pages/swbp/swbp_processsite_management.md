---
title: Gestión de sitios de procesos
tags: [getting_started]
summary: "Descripción de las herramientas y acciones asociadas con la gestión de sitios de procesos"
sidebar: swbp_sidebar
permalink: swbp_processsite_management.html
folder: swbp
---

## Creación de sitios Web de procesos

### Creación de un sitio vacío
{{site.data.alerts.callout_warning}}
No se recomienda la creación de sitios Web vacíos
{{site.data.alerts.end}}
Un sitio Web de procesos vacío contiene los elementos generales para la gestión de procesos desde el sitio de administración, sin embargo, no cuenta con la configuración de los componentes para la documentación y operación de los procesos (bandeja, monitor, herramientas de colaboración). Por lo anterior, este tipo de sitio sólo es útil para desarrolladores que necesiten un punto de partida para crear su propio sitio de procesos con componentes ad-hoc.

Para crear un sitio de procesos vacío, seleccione en la barra de menús la opción **Nuevo** en el menú **Archivo > Crear Sitios Web**, como se muestra en la siguiente figura.

{%include image.html class="centered medium shadow adjusted" file="screenshots/swbp_newsite_menu.gif" alt="Opción para crear sitio"%}

Se presentará el diálogo de creación de sitios como se muestra en la siguiente figura.

{%include image.html class="centered medium shadow adjusted" file="screenshots/swbp_newsite_dialog.png" alt="Diálogo crear sitio"%}

Deberá capturar en el diálogo los datos del formulario de acuerdo a la siguiente descripción de campos, seleccionando **Exclusivo** y **Sitio de Procesos** para los campos _Repositorio a utilizar_ y _Tipo de sitio_ respectivamente:

|Campo|Descripción|
|---|---|
|Título|Nombre visible del sitio en toda la administración, este nombre es usado como campo de búsqueda.|
|Identificador|Identificador único del sitio, usado en la URL de navegación. De existir el valor capturado se marcará el campo como erróneo.|
|Repositorio a utilizar|Combo de opciones para seleccionar el repositorio de usuarios a utilizar. Se mostrarán los repositorios existentes así como las opciones _Exclusive_, _Default UserRepository_ y _Admin UserRepository_ |
|Tipo de sitio|Combo de opciones para seleccionar el modelo de sitio a utilizar. Se mostrarán opciones como _Sitio Web_, _Sitio de Administración_ y _Sitio de Procesos_|

Finalmente, deberá presionar el botón **Guardar**. Se mostrará un mensaje de confirmación de la acción y en el acordeón de estructura de sitios se presentará el sitio recién creado.

{{site.data.alerts.callout_success}}
Si desea obtener más información sobre la creación de sitios Web y la descripción de los tipos de sitios y repositorios, puede consultar la <a href="http://semanticwebbuilder.org.mx/swb/swb/Manuales_Portal_Esoanol">página de documentación</a> de SemanticWebBuilder.
{{site.data.alerts.end}}

### Creación de un sitio desde la plantilla predeterminada
La opción recomendada para la creación de sitios de procesos es mediante el uso de la plantilla de sitio predeterminada. Esta plantilla de sitio tiene configurados los componentes necesarios para permitir la operación de procesos e incorpora la imagen de producto de SemanticWebBuilder Process. El sitio demo creado en la instalación de SWBProcess es creado mediante esta plantilla.

Para crear un sitio de procesos desde la plantilla predeterminada, seleccione en la barra de menús la opción **Predeterminado** en el menú **Archivo > Crear Sitios Web**, como se muestra en la siguiente figura.

{%include image.html class="centered medium shadow adjusted" file="screenshots/swbp_templatesite_menu.gif" alt="Opción para crear sitio plantilla"%}

En la zona de trabajo se mostrará la pestaña _Predeterminado_ con la lista de plantillas disponibles para la creación de sitios.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_template_list.png" alt="Lista de plantillas"%}

En la lista de plantillas presione el icono **instalar** de la plantilla llamada _demo_.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_template_install.png" alt="Instalar plantilla"%}

Se presentará un formulario para capturar los datos del nuevo sitio. Deberá proporcionar valores válidos conforme a los campos descritos en la sección [creación de un sitio vacío](http://localhost:4000/swbp_processsite_management.html#creacin-de-un-sitio-vaco)

{%include image.html class="centered medium shadow adjusted" file="screenshots/swbp_template_data.png" alt="Datos del nuevo sitio"%}

Cuando haya terminado deberá presionar el botón **Enviar**. Se le solicitará confirmación de la acción.

{% include image.html class="centered medium shadow adjusted" file="screenshots/swbp_template_confirm.png" alt="Confirmar nuevo sitio" %}

Tras aceptar, se mostrará información del progreso. El sitio será instalado cuando en la tabla de progreso se muestre la leyenda _COMPLETO_ en cada columna.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_template_progress.png" alt="Indicador de progreso" %}

Finalmente, se mostrará un mensaje de confirmación de la acción y en el acordeón de estructura de sitios se presentará el sitio recién creado.

{% include image.html class="centered x-small shadow adjusted" file="screenshots/swbp_process_created.png" alt="Sitio creado" %}

## Estructura de un sitio Web de procesos
{{site.data.alerts.callout_success}}
Aunque en esta sección se describen todos los elementos de un sitio Web de procesos, en el resto de la documentación sólo se hará uso de algunos de ellos, relevantes para la gestión de SWBProcess.
{{site.data.alerts.end}}

Al crear un nuevo sitio de procesos, ya sea vacío o desde la plantilla predeterminada, éste presentará en los acordeones de estructura, una organización similar a la de la figura.

{% include image.html class="centered small shadow adjusted" file="screenshots/swbp_site_structure.png" alt="Estructura de un sitio de procesos" %}

Cada elemento (nodo) en el árbol de estructura del sitio se describe a continuación.

|Elemento|Descripción|
|---|---|
|Plantillas|Contiene las plantillas (código HTML de despliegue) y grupos de plantillas existentes en el sitio. SWBProcess cuenta con una sola plantilla llamada _main_ en el grupo denominado _Process_. Puede obtener más información sobre la gestión de plantillas en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/426/_mto/3/_act/download/doc/Creacion_y_Administracion_de_Plantillas_para_Presentacion_de_Paginas_Web.pdf) correspondiente.|
|Reglas|Contiene las reglas definidas para el sitio, aplicables a los usuarios para el control de acceso. SWBProcess sólo cuenta con una regla llamada _Registrado_ que obliga a que los usuarios tengan un registro para acceder al sitio. Puede obtener más información sobre la gestión de reglas en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/435/_mto/3/_act/download/doc/Creacion_y_Administracion_de_Reglas_de_Personalizacion.pdf) correspondiente.|
|Calendarios|Contiene las calendarizaciones aplicables a los elementos del sitio. Puede obtener más información sobre la gestión de calendarios en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/425/_mto/3/_act/download/doc/Creacion_y_Uso_de_Calendarizacion.pdf) correspondiente.|
|Flujos de publicación|Contiene los flujos de publicación aplicables a los contenidos del sitio. Puede obtener más información sobre la gestión de flujos de publicación en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/424/_mto/3/_act/download/doc/Creacion_y_Administracion_de_Flujos_de_Publicacion.pdf) correspondiente.|
|Lenguajes|Contiene los idiomas aplicables a los elementos y contenidos del sitio. Puede obtener más información sobre la gestión de idiomas en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/437/_mto/3/_act/download/doc/Administracion_de_Catalogo_de_Lenguajes_y_Paises_de_Presentacion.pdf) correspondiente.|
|Países|Contiene los países asociados a los idiomas del sitio. Puede obtener más información sobre la gestión de países en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/437/_mto/3/_act/download/doc/Administracion_de_Catalogo_de_Lenguajes_y_Paises_de_Presentacion.pdf) correspondiente.|
|Dispositivos|Contiene una jerarquía de dispositivos utilizados para definir reglas de presentación específicas. Puede obtener más información sobre la gestión de dispositivos en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/436/_mto/3/_act/download/doc/Adminstracion_de_Catalogo_de_Dispositivos_de_Navegacion_de_Usuarios.pdf) correspondiente.|
|DNS|Contiene mapeos entre nombres de dominio y sitios, con la finalidad de proporcionar un mecanismo para presentar sitios distintos de acuerdo con los nombres de dominio. Puede obtener más información sobre la gestión de DNS en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/438/_mto/3/_act/download/doc/Adminstracion_de_Catalogo_de_DNS.pdf) correspondiente.|
|Colecciones|Permite crear agrupadores de elementos de un sitio con base en su definición ontológica.|
|Colección de recursos|Permite crear agrupadores de recursos de un sitio.|
|Componentes de estrategia|Contiene el catálogo de componentes de estrategia del sitio. Estos elementos son utilizados como bloques de construcción en las plantillas del sitio. Puede obtener más información sobre la gestión de componentes de estrategia en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/428/_mto/3/_act/download/doc/Administracion_y_Publicacion_de_Componentes_de_Estrategia.pdf) correspondiente.|
|Componentes de sistema|Contiene el catálogo de componentes de sistema del sitio. Estos elementos son utilizados como bloques de construcción en las plantillas del sitio o como componentes de contenido en las páginas. Puede obtener más información sobre la gestión de componentes de sistema en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/432/_mto/3/_act/download/doc/Administracion_y_Publicacion_de_Componentes_de_Sistema_v2.pdf) correspondiente.|
|Componentes de contenido|Contiene el catálogo de componentes de contenido del sitio. Estos elementos son utilizados como bloques de funcionalidad o información en las páginas del sitio. Puede obtener más información sobre la gestión de componentes de contenido en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/423/_mto/3/_act/download/doc/Administracion_y_Publicacion_de_Componentes_de_Contenido.pdf) correspondiente.|
|Herramientas de proceso|Contiene el catálogo de elementos utilizados en la configuración de uno o más procesos: _Certificados_, _Plantillas de notificaciones_, _Intervalos de ejecución_, _Reglas de negocio_, _Conexiones a bases de datos_, _Servicios Web_ y _Propiedades de asignación_.|
|Procesos|Contiene la definición de los procesos de negocio del sitio, sus modelos y sus grupos.|
|Repositorio de usuarios|Contiene el repositorio de usuarios asociado al sitio, los roles y grupos de usuarios.|
|Home(SWBProcess)|Contiene la estructura de páginas Web del sitio. SWBProcess tiene una estructura previamente definida, por lo que no debe editar el nodo llamado _Herramientas de SWBProcess_ en la estructura de páginas. Puede obtener más información sobre la gestión de páginas Web en el [manual](http://www.semanticwebbuilder.org.mx/en_mx/swb/Manuales_Portal_Esoanol/_rid/431/_mto/3/_act/download/doc/Creacion_y_Administracion_de_Paginas_Web.pdf) correspondiente.|

## Edición de la configuración de un sitio de procesos
Podrá editar la configuración de los sitios de procesos mediante sus pestañas de configuración o mediante las acciones disponibles en el árbol de estructura. Para acceder a las pestañas de configuración, deberá hacer doble click en el icono de sitio en el acordeón de estructura de sitios. Esto mostrará las pestañas en la zona de trabajo como se muestra en la siguiente figura.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_site_tabs.png" alt="Pestañas de configuración del sitio"%}

La siguiente tabla describe cada una de las pestañas presentadas.

|Pestaña|Descripción|
|---|---|
|Información|Muestra el formulario para la edición de la información principal del sitio.|
|Ontologías|Permite agregar modelos ontológicos al sitio.|
|Papelera de reciclaje|Permite gestionar y recuperar los elementos eliminados en el sitio.|
|Propiedades|Permite agregar propiedades extendidas al sitio.|
|Relacionados|Muestra los elementos relacionados con el sitio de acuerdo con la definición del modelo ontológico.|
|Bitácora|Muestra un log con los cambios realizados al sitio web.|

### Edición de las propiedades generales del sitio
Para modificar las propiedades generales del sitio deberá acceder a la pestaña de información, como se indica previamente. Se presentará un formulario donde podrá modificar la información de acuerdo con la siguiente tabla.

|Propiedad|Descripción|
|---|---|
|Título|Nombre del proceso como será mostrado en el sitio de administración. Puede agregar un título para los idiomas definidos en el sitio. Este campo es utilizado para búsquedas.|
|Descripción|Descripción del sitio de procesos. Puede agregar una descripción para los idiomas definidos en el sitio. Este campo es utilizado para búsquedas.|
|Activo|Indica si el sitio está activo o inactivo. |
|Indexable|Indica si el sitio será indexado por el motor de búsqueda.|
|Plantilla por omisión|Permite seleccionar la plantilla que será aplicada por defecto a las páginas Web del sitio.|
|Lenguaje|Permite seleccionar el idioma aplicado por defecto al sitio.|
|País|Permite seleccionar el país aplicado por defecto al sitio.|
|Página inicial|Permite seleccionar la página que se mostrará como inicio al acceder a la URL del sitio.|
|Repositorio de usuarios|Permite seleccionar el repositorio de usuarios asociado al sitio.|


### Activación/desactivación de elementos en un sitio de procesos
Muchos de los elementos de un sitio de procesos (por ejemplo páginas Web, reglas, plantillas, procesos, etcétera) pueden ser activados o desactivados en cualquier momento, incluyendo el mismo sitio. Las páginas Web desactivadas no son mostradas a los usuarios en la navegación y los elementos de configuración desactivados no son aplicados.

A continuación se describe el procedimiento para activar o desactivar un sitio de procesos, aunque dicho procedimiento aplica para los demás elementos. Podrá activar o desactivar un sitio marcando o desmarcando la casilla del campo **Activo** en el formulario de la pestaña de información del sitio.

{%include image.html class="centered medium shadow adjusted" file="screenshots/swbp_site_active.png" alt="Casilla de activación del sitio"%}

También puede realizar la acción desde el árbol de estructura, haciendo click con el botón derecho sobre el nombre del sitio y seleccionando la opción **Activar** o **Desactivar** según corresponda, como se muestra en la siguiente figura.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_site_activemenu.gif" alt="Opción de activación del sitio"%}

En cualquier caso, el icono del sitio cambiará de acuerdo con la configuración. Éste será azul {% include inline_image.html file="screenshots/icon_siteb.gif" %} cuando el sitio esté activo y rojo {% include inline_image.html file="screenshots/icon_sitein.png" %} cuando el sitio esté inactivo.

{{site.data.alerts.callout_warning}}
Debe tomar en cuenta que los elementos inactivos no son mostrados a los usuarios en la navegación. En el caso de los sitios, éstos no son accesibles mediante su URL, tampoco son considerados en los resultados de los buscadores de SemanticWebBuilder Process. Del mismo modo, si tiene configurados DNS que apuntan a un sitio inactivo, el sitio no será mostrado al acceder mediante el nombre de dominio.
{{site.data.alerts.end}}

### Uso de la papelera de reciclaje del sitio
Muchos de los elementos eliminados en un sitio de procesos son enviados a la papelera de reciclaje antes de ser eliminados definitivamente. Esto permite recuperar elementos eliminados de manera accidental.

Para acceder a la papelera de reciclaje del sitio de procesos, deberá acceder primero a las pestañas de configuración haciendo doble click en el icono de sitio en el acordeón de estructura de sitios. Posteriormente, deberá seleccionar la pestaña **Papelera de Reciclaje**, mostrada a continuación.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_trash.png" alt="Papelera de reciclaje del sitio"%}

Para eliminar un elemento de manera definitiva, haga click en el ícono _Eliminar de la papelera_ {% include inline_image.html file="screenshots/trash_vacio.gif" class="icon"%}. Se le pedirá confirmación de la acción. Si acepta, el elemento desaparecerá de la papelera y será eliminado de SWBProcess.

{%include image.html class="centered medium shadow adjusted" file="screenshots/swbp_trash_delete_confirm.png" alt="Confirmación de eliminación"%}

{{site.data.alerts.callout_warning}}
Al eliminar un elemento de la papelera se elimina no sólo la información asociada al elemento, sino también los archivos correspondientes que el elemento generó en el disco duro. Asegúrese de conocer todas las implicaciones antes de eliminar un elemento de la papelera.
{{site.data.alerts.end}}

Para recuperar un elemento de la papelera, haga click en el ícono _Recuperar de la papelera_ {% include inline_image.html file="screenshots/recover.gif" class="icon"%}. Se le pedirá confirmación de la acción. Si acepta, el elemento desaparecerá de la papelera y será restaurado a su ubicación en el árbol de estructura del sitio.

{%include image.html class="centered medium shadow adjusted" file="screenshots/swbp_trash_recover_confirm.png" alt="Confirmación de recuperación"%}

### Eliminación de sitios Web de procesos
{{site.data.alerts.callout_warning}}
Al eliminar un sitio de procesos se elimina no sólo la información asociada, sino también los archivos correspondientes generados en el disco duro. Asegúrese de conocer todas las implicaciones antes de eliminar un sitio de procesos.
{{site.data.alerts.end}}

Podrá eliminar un sitio de procesos presionando el botón **Eliminar** en el formulario de la pestaña de información del sitio.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_site_delete.png" alt="Botón de eliminación"%}

También puede realizar la acción desde el árbol de estructura, haciendo click con el botón derecho sobre el nombre del sitio y seleccionando la opción **Eliminar**, como se muestra en la siguiente figura.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_site_removeoption.gif" alt="Opción de eliminación del sitio"%}

En cualquier caso, se solicitará confirmación de la acción. Si acepta, el sitio será eliminado y desaparecerá del acordeón de estructura de sitios.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_site_confirmdelete.png" alt="Confirmación de eliminación del sitio"%}

{% include links.html %}
