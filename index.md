---
title: SemanticWeBuilder Process
tags: [getting_started]
sidebar: swbp_sidebar
permalink: index.html
summary: Esta sección brinda una introducción a SemanticWeBuilder Process y sus características.
---

## Acerca del producto

SemanticWebBuilder Process (abreviado SWBProcess) es el sistema de gestión de procesos de negocio (BPMS) de la Suite de productos SemanticWebBuilder (SWB) que tiene el objetivo de agilizar la automatización de la gestión de procesos de negocio y su seguimiento en las organizaciones. En este sentido, SWB Process permite el modelado, documentación, configuración, ejecución y monitoreo de los procesos de una organización con base en la metodología de administración de procesos de negocio (BPM).

SWB Process está dirigido a PyMES, el gobierno y las organizaciones públicas o privadas que cuenten con proyectos de descubrimiento, estandarización y automatización de sus procesos de negocio.

## Tecnología

SWB Process hace uso de las tecnologías de la Web Semántica (mediante su construcción con SWB Platform) para dotar de significado a los elementos de un proceso de negocio y a los artefactos de negocio asociados, permitiendo una mejor gestión de la información generada y manipulada en las actividades operacionales de las organizaciones. Esto proporciona un mecanismo para explicitar el conocimiento organizacional y crear una base de interoperabilidad entre las aplicaciones de la organización mediante el uso de ontologías y los estándares RDF y OWL.

Para el modelado de procesos de negocio, SWB Process hace uso de la notación del estándar BPMN 2.0 y para el intercambio de diagramas de procesos, el estándar XPDL 2.0.

{{site.data.alerts.callout_success}}
Usted verá los términos <i>ontología</i> y <i>modelo ontológico</i> a lo largo de toda la documentación. En términos simples, se les puede considerar un modelo de datos basado en conceptos y sus relaciones. Si desea conocer más acerca de las ontologías y los estándares asociados puede consultar la página de la <a href="https://www.w3.org/standards/semanticweb/ontology">W3C</a>.
{{site.data.alerts.end}}

## Características

SemanticWebBuilder Process provee los siguientes componentes:

### SWBProcess Modeler
Diagramador de modelos de procesos con el estándar BPMN 2.0 que integra las mejores prácticas del modelado con esta notación y permite la exportación de los modelos a distintos formatos.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_modeler.png" alt="SWBProcess Modeler" %}

### SWBProcess Documenter
Permite generar un manual de procesos navegable con la información de los procesos y la documentación capturada en SWB Process Configurator. Este componente es especialmente útil para realizar la documentación de los procesos en la fase de descubrimiento y para proporcionar a los usuarios finales una documentación amigable.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_documenter.png" alt="SWBProcess Documenter" %}

### SWB Process Configurator
Permite definir en detalle las propiedades de ejecución de los elementos en un modelo de procesos, así como relacionar elementos semánticos con los artefactos del proceso. Ofrece la opción de documentar cada proceso para tener contexto sobre las actividades que los usuarios finales deben desarrollar.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_configurator.png" alt="SWBProcess Configurator" %}

### SWB Process Forms Builder
Permite definir formularios para captura o visualización de información en las actividades de los usuarios de una manera rápida y dinámica. Hace uso de las definiciones de los elementos semánticos relacionados con los artefactos del proceso.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_forms.png" alt="SWBProcess Forms" %}

### SWB Process Engine / Task Inbox
Es el motor semántico que permite ejecutar el despliegue de los procesos de negocio, las aplicaciones compuestas y la orquestación de servicios, esto se hace mediante bandejas de trabajo para organizar la participación de los ejecutores del proceso.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_taskinbox.png" alt="SWBProcess Task Inbox" %}

### SWBProcess Monitor
Facilita la supervisión del rendimiento de los procesos, ya sea global o individual, de acuerdo a medidas de tiempos de respuesta y atención de los procesos mediante el despliegue de información gráfica y tabular.

{% include image.html class="centered shadow adjusted" file="screenshots/swbp_monitor.png" alt="SWBProcess Monitor" %}

## SemanticWebBuilder como Open Source
SWB Process ha sido liberado bajo un esquema de código abierto, es decir, sin restricciones para su distribución y desarrollo libremente. Lo anterior para cumplir con los siguientes objetivos: a) apoyar al crecimiento de la industria de TI en el país; b) abrir una oportunidad de negocio a la iniciativa privada; c) buscar el apoyo de la comunidad para crecer y potenciar la evolución de la herramienta.

Usted podrá consultar la [licencia de SemanticWebBuilder Process](http://svn.semanticwebbuilder.org.mx/SemWB4/SWB4/swb/web/WEB-INF/license/LICENCIA-SWB.txt), así como descargar el código fuente de mediante los enlaces en la sección de [Información para Desarrolladores](swbp_developers.html).

{% include links.html %}
