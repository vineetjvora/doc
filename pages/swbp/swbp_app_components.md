---
title: Organización de la aplicación
tags: [getting_started]
summary: "Organización de SemanticWebBuilder Process"
sidebar: swbp_sidebar
permalink: swbp_app_components.html
folder: swbp
---

## Arquitectura del producto
SWBProcess fue concebido para establecer una clara separación entre los roles involucrados en el ciclo de vida de los procesos. Lo anterior con la finalidad de permitir que cada actor enfoque sus capacidades en alguna etapa del desarrollo y automatización de los procesos.

Por este motivo, existen dos puntos de acceso a herramientas específicas que proveen acciones concretas para grupos de perfiles. Estos puntos de acceso son el **sitio de administración de SWBProcess** y el **sitio Web de procesos**.

## Sitio Web de administración
Es un punto de acceso con herramientas administrativas que permite, entre otras acciones, la gestión de sitios de procesos, usuarios y permisos, monitoreo general de la aplicación y generación de reportes de rendimiento. Podrá acceder a este sitio mediante el prefijo **/swbadmin** en la URL de la aplicación (por ejemplo: http://localhost:8080/swbadmin).

{{site.data.alerts.callout_success}}
El sitio Web de administración cuenta con un repositorio de usuarios distinto al de los sitios web de procesos. Esto implica que no podrá iniciar sesión con un usuario de administración en el sitio de procesos y viceversa
{{site.data.alerts.end}}

### Perfiles asociados
Los perfiles asociados con el uso de las herramientas del sitio de administración son los siguientes:

|Perfil|Acciones relacionadas|
|----|-------|
|Administrador de SWBProcess|Es el nivel más alto de gestión, con facultades para la gestión completa de la instancia de SWBProcess|
|Administrador de procesos|Control total de los sitios de procesos, incluyendo la creación de procesos, su modelado y organización en grupos, gestión de usuarios y permisos|
|Dueño de procesos|Creación de procesos, su modelado y organización en grupos, gestión de usuarios y permisos, configuración de procesos para su ejecución|

## Sitio Web de procesos
Un sitio Web de procesos es un punto de acceso con herramientas que permiten realizar la operación de los procesos de negocio definidos mediante la documentación de los mismos, la generación de casos y reportes, así como la colaboración en el contexto de su ejecución. Debido a que puede existir más de un sitio de procesos en una instancia de SWBProcess, podrá acceder a este sitio mediante el prefijo **/swb/XXX** en la URL de la aplicación, donde XXX es el identificador del sitio de procesos (por ejemplo: http://localhost:8080/swb/demo).

### Perfiles asociados
Los perfiles asociados con el uso de las herramientas del sitio de procesos son los siguientes:

|Perfil|Acciones relacionadas|
|----|-------|
|Operador de procesos|Ejecución de las actividades establecidas en los procesos y generación nuevos casos de los procesos a los que tienen acceso|
|Documentador de procesos|Definir las plantillas de documentación para procesos, capturar la documentación asociada|
|Usuario registrado|Visualización de la documentación de los procesos y de la interacción en las herramientas de colaboración|


{% include links.html %}
