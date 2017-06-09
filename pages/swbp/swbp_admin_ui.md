---
title: Elementos de la interfaz del sitio de administración
tags: [getting_started]
summary: "Descripción de la interfaz del sitio de administración y ubicación de los componentes principales"
sidebar: swbp_sidebar
permalink: swbp_admin_ui.html
folder: swbp
---

Para acceder al sitio Web de administración, deberá utilizar la URL correspondiente y proporcionar los datos de acceso necesarios. Para más información puede consultar la información en la sección [sitio web de administración](http://localhost:4000/swbp_app_components.html#sitio-web-de-administarcin)

## Estructura general
El sitio Web de administración proporciona a los usuarios los elementos mostrados en la siguiente figura. Cada elemento se describe en la sección correspondiente.

![Interfaz de administración](images/screenshots/admin_ui.png)

### Barra de menús
Delimitada en el recuadro rojo, contiene las opciones generales de la administración de SWBProcess y provee los accesos a todas las acciones administrativas. La siguiente tabla describe el primer nivel de los menus provistos.

|Menú|Opciones presentadas|
|---|---|
|Archivo|Opciones para la creación de sitios Web, importación y exportación de información|
|Herramientas|Opciones para indexado del buscador, búsqueda de elementos de los sitios y acceso al explorador de archivos|
|Reportes|Opciones para generación de reportes de acceso, usuarios, sesiones, etcétera|
|Ver|Opciones para gestión de flujos de publicación de contenidos|
|Usuarios|Gestión de usuarios, asignación de roles y filtros de acceso|
|Sistema|Opciones para el monitoreo y configuración del desempeño de la instancia de SWBProcess|
|Ayuda|Enlaces a la ayuda de SemanticWebBuilder|

### Acordeones de estructura
Delimitados en color verde, muestran diversos elementos de configuración de la estructura de los sitios generados, así como herramientas y funciones de operación general. Los acordeones presentados se describen en la siguiente tabla.

|Acordeón|Descripción|
|---|---|
|Sitios|Presenta el árbol de estructura de los sitios existentes|
|Repositorios de usuarios|Provee acceso directo a los repositorios de usuarios de los sitios existentes|
|Favoritos|Provee accesos directos a los elementos marcados como favoritos|
|Propiedades|Muestra la información asociada a los elementos seleccionados en otros acordeones|

### Zona de trabajo
Delimitada en color azul, despliega el detalle de la información, pestañas de configuración y formularios de administración de los elementos que componen un sitio Web de procesos, en función de la selección actual en los acordeones.

### Pestañas de configuración
Cada elemento de un sitio de procesos cuenta con distintas pestañas de configuración asociadas. Dichas pestañas se muestran en la zona de trabajo al momento de seleccionar un elemento en los acordeones (ver figura).

![Pestañas de configuración](images/screenshots/admin_tabs.png)

Aunque existen pestañas específicas para los elementos, también existen algunas compartidas por la mayoría, cuya descripción se muestra a continuación.

|Pestaña|Descripción|
|---|---|
|Información|Presenta un formulario con la información general del elemento para su modificación|
|Relacionados|Muestra elementos relacionados conforme al modelo de datos general de SWBProcess|
|Bitácora|Muestra un log de cambios realizados al elemento|

{% include links.html %}
