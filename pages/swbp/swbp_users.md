---
title: Gestión de usuarios y permisos
tags: [getting_started, troubleshooting, support]
summary: "Descripción de las herramientas y acciones asociadas con la gestión de usuarios y permisos en sitios Web de procesos"
sidebar: swbp_sidebar
permalink: swbp_users.html
folder: swbp
---

## Repositorios de usuarios
El manejo de usuarios en SemanticWebBuilder Process se realiza por medio de repositorios de usuarios, que son catálogos que almacenan tanto los perfiles individuales de cada persona como los grupos de usuarios y roles correspondientes.

{{site.data.alerts.callout_success}}
Un repositorio de usuarios puede ser compartido entre varios sitios, aunque no es una práctica común.
{{site.data.alerts.end}}

SWBProcess cuenta con un repositorio denominado _Admin_. Este repositorio está asociado al sitio de administración de SWBProcess y contiene el registro de los usuarios con facultades para administrar los distintos sitios de procesos. Por otro lado, el sitio de demostración instalado con SWBProcess contiene un repositorio de usuarios con los siguientes perfiles para realizar pruebas:

|Usuario|Password|Rol asociado|Descripción|
|---|---|---|---|
|admin|webbuilder|Administrador|Usuario con rol de administrador|
|empleado|empleado|Empleado|Usuario con rol de empleado|
|director|director|Director|Usuario con rol de director|
|humanos|humanos|RH|Usuario con rol de RH|

{{site.data.alerts.callout_success}}
A los usuarios del repositorio <i>Admin</i> se les denomina usuarios administradores. Es importante no asignar el repositorio <i>Admin</i> a los sitios de procesos.
{{site.data.alerts.end}}

Podrá acceder a los repositorios de usuario haciendo click en el acordeón **Repositorios de usuarios**.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_repaccordeon.png" alt="Acordeón de repositorios de usuarios" %}

Al expandirse el acordeón se mostrará la lista de los repositorios existentes, sus roles y grupos relacionados como se muestra en la siguiente figura.

{% include image.html class="centered x-small shadow adjusted" file="screenshots/swbp_userrep_list.png" alt="Lista de repositorios de usuarios" %}

### Creación de un repositorio de usuarios
Un repositorio de usuarios es creado de manera automática cada vez que se crea un sitio de procesos nuevo y se selecciona la opción _Exclusivo_ en el tipo de repositorio a utilizar (consultar sección [crear un sitio vacío](http://localhost:4000/swbp_processsite_management.html#creacin-de-un-sitio-vaco)). Sin embargo, usted puede crear un repositorio de usuarios mediante la barra de menús.

Para crear un nuevo repositorio seleccione la opción **Nuevo** en el menú **Archivo** > **Crear Repositorio de Usuarios**.

{% include image.html class="centered small shadow adjusted" file="screenshots/swbp_newrepo_menu.gif" alt="Opción para crear repositorio" %}

Se presentará el diálogo de creación de repositorios como se muestra en la siguiente figura.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_newrepo_dialog.png" alt="Diálogo crear repositorio"%}

Deberá capturar en el diálogo los datos del formulario de acuerdo a la siguiente descripción de campos.

|Campo|Descripción|
|---|---|
|Título|Nombre visible del repositorio en toda la administración, este nombre es usado como campo de búsqueda.|
|Identificador|Identificador único del repositorio. Éste es sensible a mayúsculas y minúsculas. De existir el valor capturado se marcará el campo como erróneo.|

Finalmente, deberá presionar el botón **Guardar**. El repositorio se presentará en el acordeón correspondiente.

### Creación de roles
En SemanticWebBuilder Process un rol representa de manera conceptual, una función, puesto o papel que un usuario desempeña dentro de la organización. A través de los roles se delimita el acceso a secciones, procesos, actividades y contenidos en el sitio de procesos o el sitio de administración.

Asignar un rol a un usuario significa que se le está concediendo un perfil nuevo dentro de los sitios y que en consecuencia podrá acceder a la información que esté filtrada para ese rol en particular.

{{site.data.alerts.callout_success}}
Los permisos asociados a los roles son acumulativos, es decir, un usuario con varios roles asignados tendrá acceso a las secciones y contenidos establecidas en cada uno de esos roles.
{{site.data.alerts.end}}

Para crear un rol, deberá primero ubicar el repositorio de usuarios deseado en el acordeón de **repositorios de usuarios** y deberá expandir su estructura usando el ícono _Expandir_ {% include inline_image.html file="screenshots/spriteTree.gif" %} a la izquierda del nombre del repositorio.

Posteriormente, deberá hacer click con el botón derecho en el nodo _Roles_ {% include inline_image.html file="screenshots/icon_role.png" class="icon" %} y seleccionar la opción **Agregar Rol** como se muestra en la siguiente figura.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_addrole_menu.gif" alt="Opción para agregar rol"%}

Se presentará el diálogo _Agregar Rol_ como se muestra en la siguiente figura.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_newrole_dialog.png" alt="Diálogo crear rol"%}

Deberá capturar en el diálogo los datos del formulario de acuerdo a la siguiente descripción de campos.

|Campo|Descripción|
|---|---|
|Título|Nombre visible del rol en toda la administración, este nombre es usado como campo de búsqueda.|
|Identificador|Identificador único del rol. Éste es sensible a mayúsculas y minúsculas. De existir el valor capturado se marcará el campo como erróneo.|

Finalmente, deberá presionar el botón **Guardar**. El nuevo rol se presentará en el árbol del repositorio correspondiente.

{%include image.html class="centered x-small shadow adjusted" file="screenshots/swbp_newrole_tree.png" alt="Nuevo rol en el repositorio"%}

Al mismo tiempo, se mostrarán las pestañas de edición del rol en la zona de trabajo, con la pestaña _Información_ seleccionada, como se muestra en la siguiente figura.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_role_tabs.png" alt="Pestañas de configuración del rol"%}

### Eliminación de roles
Podrá eliminar un rol de un repositorio presionando el botón **Eliminar** en el formulario de la pestaña de información del rol.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_role_removebutton.png" alt="Botón de eliminación"%}

También puede realizar la acción desde el árbol del repositorio, haciendo click con el botón derecho sobre el nombre del rol y seleccionando la opción **Eliminar**, como se muestra en la siguiente figura.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_role_removeoption.gif" alt="Opción de eliminación del rol"%}

En cualquier caso, se solicitará confirmación de la acción. Si acepta, el rol será eliminado y desaparecerá del árbol del repositorio de usuarios.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_role_deleteconfirm.png" alt="Opción de eliminación del rol"%}

{{site.data.alerts.callout_warning}}
Al eliminar un rol, se eliminan las asociaciones del mismo con los usuarios y los elementos del sitio, por lo que las restricciones de acceso cambiarán en consecuencia.
{{site.data.alerts.end}}

### Creación de grupos de usuarios
En SemanticWebBuilder Process un grupo de usuarios representa de manera conceptual un área o departamento de una organización y su función es categorizar a los usuarios de manera independiente a los roles que desempeñen dentro de un área. A través de los grupos se delimita el acceso a secciones, procesos, actividades y contenidos en el sitio de procesos o el sitio de administración.

Asignar un grupo a un usuario significa que se le está concediendo un perfil nuevo dentro de los sitios y que en consecuencia podrá acceder a la información que esté filtrada para ese grupo en particular.

Para crear un grupo de usuarios, deberá primero ubicar el repositorio de usuarios deseado en el acordeón de **repositorios de usuarios** y deberá expandir su estructura usando el ícono _Expandir_ {% include inline_image.html file="screenshots/spriteTree.gif" %} a la izquierda del nombre del repositorio.

Posteriormente, deberá hacer click con el botón derecho en el nodo _Grupos de usuarios_ {% include inline_image.html file="screenshots/icon_usergroup.png" class="icon" %} y seleccionar la opción **Agregar Grupo de Usuarios** como se muestra en la siguiente figura.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_addgroup_menu.gif" alt="Opción para agregar rol"%}

Se presentará el diálogo _Agregar Grupo de Usuarios_ como se muestra en la siguiente figura.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_newgroup_dialog.png" alt="Diálogo crear grupo"%}

Deberá capturar en el diálogo los datos del formulario de acuerdo a la siguiente descripción de campos.

|Campo|Descripción|
|---|---|
|Título|Nombre visible del grupo en toda la administración, este nombre es usado como campo de búsqueda.|
|Identificador|Identificador único del grupo. Éste es sensible a mayúsculas y minúsculas. De existir el valor capturado se marcará el campo como erróneo.|

Finalmente, deberá presionar el botón **Guardar**. El nuevo grupo se presentará en el árbol del repositorio correspondiente.

{%include image.html class="centered x-small shadow adjusted" file="screenshots/swbp_newgroup_tree.png" alt="Nuevo grupo en el repositorio"%}

Al mismo tiempo, se mostrarán las pestañas de edición del grupo en la zona de trabajo, con la pestaña _Información_ seleccionada, como se muestra en la siguiente figura.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_group_tabs.png" alt="Pestañas de configuración del grupo"%}

### Eliminación de grupos de usuarios
Podrá eliminar un grupo de usuarios de un repositorio presionando el botón **Eliminar** en el formulario de la pestaña de información del grupo.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_group_removebutton.png" alt="Botón de eliminación"%}

También puede realizar la acción desde el árbol del repositorio, haciendo click con el botón derecho sobre el nombre del grupo y seleccionando la opción **Eliminar**, como se muestra en la siguiente figura.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_group_removeoption.gif" alt="Opción de eliminación del grupo"%}

En cualquier caso, se solicitará confirmación de la acción. Si acepta, el grupo será eliminado y desaparecerá del árbol del repositorio de usuarios.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_group_deleteconfirm.png" alt="Opción de eliminación del grupo"%}

{{site.data.alerts.callout_warning}}
Al eliminar un grupo de usuarios, se eliminan las asociaciones del mismo con los usuarios y los elementos del sitio, por lo que las restricciones de acceso cambiarán en consecuencia.
{{site.data.alerts.end}}

## Gestión de usuarios
Los perfiles de usuarios en SemanticWebBuilder Process proveen una cuenta de acceso a las personas relacionadas con los sitios de procesos o el sitio de administración y son asociados siempre a un repositorio de usuarios en particular.

### Creación de usuarios
Para crear un nuevo usuario seleccione la opción **Agregar usuario** en el menú **Usuarios** de la barra de menús.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_newuser_menu.gif" alt="Opción para crear usuario" %}

Se presentará el diálogo de creación de repositorios como se muestra en la siguiente figura.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_newuser_dialog.png" alt="Diálogo crear usuario"%}

Deberá capturar en el diálogo los datos del formulario de acuerdo a la siguiente descripción de campos.

|Campo|Descripción|
|---|---|
|Repositorio de usuarios|Combo desplegable que muestra la lista de repositorios existentes y permite seleccionar el repositorio al cual será asociado el nuevo usuario.|
|Usuario|Identificador único que será usado para los formularios de acceso de los sitios. Éste es sensible a mayúsculas y minúsculas. De existir el valor capturado se marcará el campo como erróneo.|
|Contraseña|Contraseña asignada al nuevo usuario.|

Finalmente, deberá presionar el botón **Guardar**. Se mostrarán las pestañas de edición del usuario en la zona de trabajo, con la pestaña _Información_ seleccionada, como se muestra en la siguiente figura.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_user_tabs.png" alt="Pestañas de configuración del usuario"%}

Existen varias pestañas asociadas con los usuarios, que permiten configurar con mucho detalle cada perfil. Las pestañas presentadas se describen en la siguiente tabla.

|Pestaña|Descripción|
|---|---|
|Información|Muestra el formulario para la edición de la información principal del usuario.|
|Roles|Permite gestionar los roles asignados al usuario.|
|Grupos de Usuarios|Permite gestionar los grupos asociados al usuario.|
|Calendarización|Permite asociar calendarizaciones para controlar el acceso de los usuarios.|
|Filtros de Administración|Permite gestionar los filtros de administración asociados al usuario.|
|Relacionados|Muestra los elementos relacionados con el usuario de acuerdo con la definición del modelo ontológico.|
|Filtro de Secciones|Permite gestionar los filtros de secciones asociados al usuario.|
|Bitácora|Muestra un log con los cambios realizados al usuario.|

### Búsqueda de usuarios
Los usuarios creados no son desplegados como nodos en el árbol del repositorio asociado por cuestiones de espacio. En consecuencia, existe un mecanismo particular para acceder a la configuración de los usuarios mediante una búsqueda. Para ubicar un usuario particular, deberá seleccionar la opción **Buscador** del menú **Usuarios** en la barra de menús.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_searchuser_menu.gif" alt="Opción para buscar usuarios" %}

Se presentará el componente de búsqueda de usuarios como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_searchuser_component.png" alt="Componente de búsqueda" %}

En los campos de búsqueda podrá establecer los criterios de acuerdo con la siguiente tabla.

|Campo|Descripción|
|---|---|
|Repositorio de usuarios|Nombre del proceso como será mostrado en el sitio de administración. Puede agregar un título para los idiomas definidos en el sitio. Este campo es utilizado para búsquedas.|
|Correo electrónico|Descripción del sitio de procesos. Puede agregar una descripción para los idiomas definidos en el sitio. Este campo es utilizado para búsquedas.|
|Nombre(s)|Indica si el sitio está activo o inactivo. |
|Primer Apellido|Indica si el sitio será indexado por el motor de búsqueda.|
|Segundo Apellido|Permite seleccionar la plantilla que será aplicada por defecto a las páginas Web del sitio.|
|Activo|Permite seleccionar el idioma aplicado por defecto al sitio.|
|Roles|Permite seleccionar el país aplicado por defecto al sitio.|
|Grupos de usuarios|Permite seleccionar la página que se mostrará como inicio al acceder a la URL del sitio.|

Finalmente, deberá presionar el botón **Buscar** del formulario. Se presentará una tabla con los resultados de la búsqueda como se muestra a continuación.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_searchuser_results.png" alt="Resultados de búsqueda de usuarios" %}

Para acceder a las propiedades de configuración de un usuario deberá hacer doble click sobre la fila deseada en la tabla de resultados de búsqueda. Se abrirán las pestañas de configuración del usuario en la zona de trabajo con la pestaña _Información_ seleccionada, como se muestra en la siguiente figura.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_user_tabs.png" alt="Pestañas de configuración del usuario"%}

### Edición de las propiedades de un usuario
Para modificar las propiedades generales de un usuario deberá acceder a la pestaña de información del mismo mediante la búsqueda, como se indica previamente. Se presentará un formulario donde podrá modificar la información de acuerdo con la siguiente tabla.

|Propiedad|Descripción|
|---|---|
|Id de Usuario|Nombre del usuario utilizado como entrada en los diálogos de acceso de un sitio Web.|
|Contraseña|Contraseña del usuario como entrada en los diálogos de acceso de un sitio Web.|
|Solicitar cambio de contraseña|Indica si se solicitará al usuario el cambio de su contraseña al iniciar sesión. |
|Correo electrónico|Correo electrónico del usuario.|
|Nombre(s)|Nombres del usuario.|
|Primer Apellido|Primer apellido del usuario.|
|Segundo Apellido|Segundo apellido del usuario.|
|Respuesta de seguridad|Respuesta utilizada en el formulario de recuperación de contraseña.|
|Región|Permite indicar la región asociada a un usuario.|
|Área|Permite indicar el área asociada a un usuario.|
|Activo|Indica si el usuario está activo o inactivo.|
|Fecha de expiración|Permite indicar una fecha de expiración para la activación del usuario.|
|Idioma|Permite definir el idioma del usuario.|
|ID externo|Permite establecer un identificador para relacionar al usuario con aplicaciones externas.|

### Activación/desactivación de usuarios
{{site.data.alerts.callout_warning}}
Los usuarios inactivos no cuentan con acceso a las páginas Web de los sitios de procesos.
{{site.data.alerts.end}}
Podrá activar o desactivar un usuario marcando o desmarcando la casilla del campo **Activo** en el formulario de su pestaña de información.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_user_active.png" alt="Pestañas de configuración del usuario"%}

El icono del usuario cambiará de acuerdo con la configuración. Éste será azul {% include inline_image.html file="screenshots/icon_user_active.png" class="icon" %} cuando el usuario esté activo y rojo  {% include inline_image.html file="screenshots/icon_user_inactive.png" class="icon" %} cuando el usuario esté inactivo.

### Eliminación de usuarios
Podrá eliminar un usuario de un repositorio presionando el botón **Eliminar** en el formulario de su pestaña de información.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_user_removebutton.png" alt="Botón de eliminación"%}

Se solicitará confirmación de la acción. Si acepta, el usuario será eliminado definitivamente.

{%include image.html class="centered small shadow adjusted" file="screenshots/swbp_user_deleteconfirm.png" alt="Opción de eliminación del usuario"%}

### Asignación de roles a usuarios
Acceda a la pestaña de configuración _Roles_ del usuario de su interés. Se mostrará la lista de roles asociados al usuario. Para asignar uno o más roles, presione el botón **Agregar de lista** como se muestra en la siguiente imagen.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_user_addrolesbutton.png" alt="Botón Agregar de lista"%}

Se mostrará la lista de roles existentes en el repositorio de usuarios del sitio.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_rolelist.png" alt="Roles existentes" %}

Podrá asignar un rol al usuario haciendo click en el enlace con su nombre en la columna _Selecciona_ de la tabla.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_rolelist_link.png" alt="Selección de rol" %}

Del mismo modo, podrá asignar varios roles al usuario a la vez, seleccionando las casillas correspondientes de la columna _Marca_ en la tabla y presionando el botón **Agregar seleccionados** como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_rolelist_selection.png" alt="Selección múltiple de roles" %}

Podrá marcar o desmarcar todas las casillas de la columna _Marca_ en la tabla presionando los botones **Seleccionar todos** y **Deseleccionar todos** respectivamente. Presionando el botón **Regresar** volverá a la lista de roles asociados al usuario.

Cuando asigna uno o varios roles al usuario, se muestra la vista de roles asociados con los roles correspondientes.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_rolelist_assigned.png" alt="Roles asignados al usuario" %}

### Desasignación de roles a usuarios
{{site.data.alerts.callout_warning}}
Al desasignar un rol de un usuario las restricciones de acceso cambiarán en consecuencia.
{{site.data.alerts.end}}

Para eliminar la asignación de un rol con un usuario, en la pestaña de configuración _Roles_ deberá presionar el icono **Eliminar** {% include inline_image.html file="screenshots/delete.gif" %} en la columna _Acción_ dela tabla. Si desea eliminar todos los roles asociados, deberá presionar el botón **Eliminar todos** del formulario.

En cualquier caso, se le pedirá confirmación de la acción. Si acepta, los roles serán desasociados del usuario y desaparecerán de la lista.

{% include image.html class="centered small shadow adjusted" file="screenshots/swbp_user_role_removeconfirm.png" alt="Confirmación de eliminación" %}

### Asignación de grupos a usuarios
Acceda a la pestaña de configuración _Grupos de Usuarios_ del usuario de su interés. Se mostrará la lista de grupos asociados al usuario. Para asignar uno o más grupos, presione el botón **Agregar de lista** como se muestra en la siguiente imagen.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_user_addgroupsbutton.png" alt="Botón Agregar de lista"%}

Se mostrará la lista de grupos existentes en el repositorio de usuarios del sitio.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_grouplist.png" alt="Grupos existentes" %}

Podrá asignar un grupo al usuario haciendo click en el enlace con su nombre en la columna _Selecciona_ de la tabla.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_grouplist_link.png" alt="Selección de grupo" %}

Del mismo modo, podrá asignar varios grupos al usuario a la vez, seleccionando las casillas correspondientes de la columna _Marca_ en la tabla y presionando el botón **Agregar seleccionados** como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_grouplist_selection.png" alt="Selección múltiple de grupos" %}

Podrá marcar o desmarcar todas las casillas de la columna _Marca_ en la tabla presionando los botones **Seleccionar todos** y **Deseleccionar todos** respectivamente. Presionando el botón **Regresar** volverá a la lista de grupos asociados al usuario.

Cuando asigna uno o varios grupos al usuario, se muestra la vista de grupos asociados con los grupos correspondientes.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_user_grouplist_assigned.png" alt="Grupos asignados al usuario" %}

### Desasignación de grupos a usuarios
{{site.data.alerts.callout_warning}}
Al desasignar un grupo de un usuario las restricciones de acceso cambiarán en consecuencia.
{{site.data.alerts.end}}

Para eliminar la asignación de un grupo con un usuario, en la pestaña de configuración _Grupos de Usuarios_ deberá presionar el icono **Eliminar** {% include inline_image.html file="screenshots/delete.gif" %} en la columna _Acción_ dela tabla. Si desea eliminar todos los grupos asociados, deberá presionar el botón **Eliminar todos** del formulario.

En cualquier caso, se le pedirá confirmación de la acción. Si acepta, los grupos serán desasociados del usuario y desaparecerán de la lista.

{% include image.html class="centered small shadow adjusted" file="screenshots/swbp_user_group_removeconfirm.png" alt="Confirmación de eliminación" %}

## Control de acceso
SemanticWebBuilder Process permite limitar el acceso a sitios, procesos, actividades o contenidos utilizando entre otros mecanismos, los roles y grupos de usuarios. Los elementos de un sitio de procesos que permiten la restricción de acceso mediante roles y grupos presentarán una pestaña para cada configuración, denominada _Roles_ y _Grupos_ respectivamente. La siguiente figura muestra estas pestañas en la configuración de una tarea de usuario.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_tabs.png" alt="Pestaña de roles y grupos" %}

{{site.data.alerts.callout_warning}}
El sitio plantilla de SWBProcess cuenta con un catálogo predefinido de roles y grupos de usuarios asociados a los componentes del sitio, deberá tener cuidado al editar las configuraciones para evitar un funcionamiento inadecuado.
{{site.data.alerts.end}}

### Filtrado de elementos por roles
{{site.data.alerts.callout_success}}
La asignación de roles definida para un elemento es heredada a sus descendientes en la estructura del sitio de procesos.
{{site.data.alerts.end}}

Acceda a la pestaña de configuración _Roles_ del elemento de su interés. Se mostrará la lista de roles asociados. Para asignar uno o más roles, presione el botón **Agregar de lista** como se muestra en la siguiente imagen.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_addrolesbutton.png" alt="Botón Agregar de lista"%}

Se mostrará la lista de roles existentes en el repositorio de usuarios del sitio.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_rolelist.png" alt="Roles existentes" %}

Podrá asignar un rol al elemento haciendo click en el enlace con su nombre en la columna _Selecciona_ de la tabla.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_rolelist_link.png" alt="Selección de rol" %}

Del mismo modo, podrá asignar varios roles a la vez, seleccionando las casillas correspondientes de la columna _Marca_ en la tabla y presionando el botón **Agregar seleccionados** como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_rolelist_selection.png" alt="Selección múltiple de roles" %}

Podrá marcar o desmarcar todas las casillas de la columna _Marca_ en la tabla presionando los botones **Seleccionar todos** y **Deseleccionar todos** respectivamente. Presionando el botón **Regresar** volverá a la lista de roles asociados al elemento. Cuando asigna uno o varios roles al elemento, se muestra nuevamente la vista de roles asociados.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_rolelist_assigned.png" alt="Roles asignados al elemento" %}

{{site.data.alerts.callout_success}}
Por defecto, los roles asignados son evaluados de manera exclusiva, es decir, mediante una condicional <i>O</i>, donde al cumplirse la validación con uno de los roles, el usuario tendrá acceso al elemento.  
{{site.data.alerts.end}}

Podrá marcar la casilla **Evaluar como Y** si desea que sea mandatorio la evaluación de todos los roles para conceder acceso al elemento. También podrá marcar la casilla **No heredar** si desea que la configuración del elemento no se aplique a sus descendientes.

### Filtrado de elementos por grupos de usuarios
{{site.data.alerts.callout_success}}
La asignación de grupos definida para un elemento es heredada a sus descendientes en la estructura del sitio de procesos.
{{site.data.alerts.end}}

Acceda a la pestaña de configuración _Grupos_ del elemento de su interés. Se mostrará la lista de grupos asociados. Para asignar uno o más grupos, presione el botón **Agregar de lista** como se muestra en la siguiente imagen.

{%include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_addgroupsbutton.png" alt="Botón Agregar de lista"%}

Se mostrará la lista de grupos existentes en el repositorio de usuarios del sitio.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_grouplist.png" alt="Grupos existentes" %}

Podrá asignar un grupo al elemento haciendo click en el enlace con su nombre en la columna _Selecciona_ de la tabla.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_grouplist_link.png" alt="Selección de grupo" %}

Del mismo modo, podrá asignar varios grupos a la vez, seleccionando las casillas correspondientes de la columna _Marca_ en la tabla y presionando el botón **Agregar seleccionados** como se muestra en la siguiente figura.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_grouplist_selection.png" alt="Selección múltiple de grupos" %}

Podrá marcar o desmarcar todas las casillas de la columna _Marca_ en la tabla presionando los botones **Seleccionar todos** y **Deseleccionar todos** respectivamente. Presionando el botón **Regresar** volverá a la lista de grupos asociados al elemento. Cuando asigna uno o varios grupos al elemento, se muestra nuevamente la vista de grupos asociados.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_usertask_grouplist_assigned.png" alt="Grupos asignados al elemento" %}

{{site.data.alerts.callout_success}}
Por defecto, los grupos asignados son evaluados de manera exclusiva, es decir, mediante una condicional <i>O</i>, donde al cumplirse la validación con uno de los grupos, el usuario tendrá acceso al elemento.  
{{site.data.alerts.end}}

Podrá marcar la casilla **Evaluar como Y** si desea que sea mandatorio la evaluación de todos los grupos para conceder acceso al elemento. También podrá marcar la casilla **No heredar** si desea que la configuración del elemento no se aplique a sus descendientes.

{% include links.html %}
