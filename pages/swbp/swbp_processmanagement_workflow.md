---
title: Flujo de trabajo
tags: [getting_started]
summary: "Esta sección presenta la descripción de BPM y su relación con el flujo de trabajo en SWBProcess"
sidebar: swbp_sidebar
permalink: swbp_processmanagement_workflow.html
folder: swbp
---

## Business Process Management
SemanticWebBuilder process fue diseñado para ayudar a los distintos actores involucrados en la gestión de los procesos de negocio de una organización. Con este objetivo, los componentes integrados en SWBProcess permiten cubrir por completo el ciclo de vida planteado por la metodología Business Process Management (BPM por sus siglas en inglés). De acuerdo con la definición de Wetzstein et. al.[^wetzstein1], el ciclo de vida de los procesos en BPMN contiene cuatro etapas: Modelado, implementación, ejecución y análisis. Las etapas se esquematizan en la figura siguiente.

{% include image.html class="centered shadow adjusted" file="BPM_flow.svg" alt="BPM" %}

La descripción de cada etapa y la manera en que SWBProcess contribuye a su realización se describe en los siguientes párrafos conforme a lo establecido en Pacheco et. al.[^Pacheco1].

* **Modelado:** en esta etapa los analistas del negocio crean un modelo de procesos de negocio con la ayuda de herramientas específicas, estableciendo el orden de las tareas en el modelo. Esta fase es cubierta por _SWBP Modeler_, que soporta el diseño de diagramas de procesos mediante el estándar BPMN 2.0 y los transforma en modelos semánticos de procesos. Adicionalmente, _SWBProcess Documenter_ permite capturar la información de negocio asociada a los procesos y generar un manual en línea.

* **Implementación:** en esta etapa, con la ayuda de los ingenieros en TI, el modelo del proceso es enriquecido con propiedades para convertirlo en un modelo de procesos ejecutable. Esta etapa es cubierta por _SWBProcess Configurator_, que permite la asociación de las propiedades necesarias para la ejecución y despliegue de los procesos en un sistema Web. Adicionalmente, mediante _SWBProcess Forms_, es posible definir las formas de captura y visualización de la información de los procesos conforme a la definición de su modelo semántico.

* **Ejecución:** en esta etapa un motor de procesos crea casos (instancias) a partir de las definiciones en los modelos de procesos ejecutables. El motor de procesos controla la activación de las actividades en el flujo y genera información específica para cada caso. Esta etapa es cubierta por _SWBProcess Engine_ y el componente _Bandeja de Tareas_ del sitio de procesos.

* **Análisis:** en esta etapa los analistas de procesos revisan los datos del desempeño en la ejecución de los distintos casos para identificar mejoras al proceso y tomar decisiones. Esta etapa está cubierta por _SWBProcess Monitor_ y _SWBProcess Reports_, que permiten visualizar la información básica sobre el desempeño de los procesos y generar reportes con información específica de cada caso.

[^wetzstein1]: B. Wetzstein, Z. Ma, A. Filipowska, M. Kaczmarek, S. Bhiri, S. Losada, J.-M. Lopez-Cob, L. Cicurel, "Semantic business process management: A lifecycle based requirements analysis", Workshop on Semantic Business Process and Product Lifecycle Management, 2007.

[^Pacheco1]: H. Pacheco, K. Najera, H. Estrada and J. Solis, "SWB process: A business process management system driven by semantic technologies," 2014 2nd International Conference on Model-Driven Engineering and Software Development (MODELSWARD), Lisbon, 2014, pp. 525-532.


## Flujo de trabajo en SWBProcess
De manera concreta, el flujo de trabajo en SWBProcess para cubrir el ciclo completo de BPM se describe a continuación. Para cada una de las actividades se especifica si ésta debe ser ejecutada en el sitio de procesos o en el sitio de administración.

{{site.data.alerts.callout_success}}
Dependiendo de los objetivos de los analistas del negocio, las actividades en el flujo de trabajo planteado pueden ser distintas, cambiar de orden o ser omitidas parcialmente.
{{site.data.alerts.end}}

### Modelado de datos
Un activo importante en los procesos de negocio es la información que se genera en la ejecución de los mismos, presentada y capturada por los usuarios ejecutores mediante interfaces o formularios específicos. Para la gestión de dicha información, SWBProcess hace uso de definiciones de datos en modelos ontológicos.

La realización de estos modelos ontológicos y su relación con los sitios Web de procesos queda fuera del alcance de la presente documentación, sin embargo, puede consultar más información en el sitio de [SemanticWebBuilder](http://www.semanticwebbuilder.org.mx/BMV/Espanol).

### Modelado del proceso
Un modelo de proceso generado bajo una notación estándar ayuda a transmitir la intención de los modelos reduciendo la ambigüedad. También ayuda a lograr una interoperabilidad entre distintas herramientas en torno a la gestión de procesos. Usted podrá definir las actividades realizadas en un modelo de procesos mediante SWBProcess Modeler en el sitio de administración, utilizando la semántica de la notación en el estándar BPMN 2.0. En esta actividad se definirán los participantes en el flujo, las decisiones y bifurcaciones, así como los eventos que ocurrirán durante la ejecución de los modelos.

### Documentación del proceso
Para ayudar en el descubrimiento, establecimiento y mejora continua de los procesos, debe generarse la documentación asociada a los mismos. Mediante SWBProcess Documenter en el sitio de procesos, usted podrá definir y capturar la documentación de los procesos para generar un manual en línea que describa, por ejemplo, los objetivos, reglas, formatos y métricas utilizadas. Ésta documentación en línea podrá ayudarle para integrar un manual de procedimientos en la institución, en procesos de auditoría o certificación de calidad.

### Configuración de herramientas
En los procesos existen elementos que pueden ser reutilizados por más de un modelo ejecutable, por ejemplo, conexiones a bases de datos, reglas de negocio, plantillas de archivos, certificados, etcétera. Estos elementos deben configurarse de manera previa a la configuración de los modelos de procesos para asegurar su existencia en el momento necesario y hacer más eficiente el flujo de trabajo. Usted podrá administrar el catálogo de herramientas de procesos en el sitio de administración.

### Configuración del proceso
Una vez que un modelo de procesos ha sido revisado y aprobado por los analistas para proseguir con su implementación, éste debe ser configurado para su ejecución y marcado como un proceso ejecutable. La configuración consiste en establecer los parámetros necesarios, relacionar los objetos de datos correspondientes y establecer los permisos y notificaciones adecuadas para que el flujo de procesos sea funcional como sistema de información. Usted podrá realizar esta configuración en el sitio de administración de SWBProcess.

### Ejecución del proceso
Mediante el componente de bandeja de tareas en el sitio Web de procesos, los usuarios ejecutores podrán crear instancias de los procesos marcados como ejecutables y atender las actividades correspondientes de acuerdo con la definición en el modelo de procesos y la configuración establecida. El motor de SWBProcess se encarga de despachar las actividades a los usuarios con los permisos adecuados, gestionar la información asociada en las interfaces de captura y generar la información de bitácora para cada ejecución.

### Monitoreo del proceso
Después de la ejecución de varias instancias de procesos, usted podrá visualizar la información básica sobre su desempeño mediante SWBProcess Monitor. Esta información puede ayudar a los especialistas en procesos para la realización del análisis y propuestas de mejora pertinentes.

<hr>

{% include links.html %}
