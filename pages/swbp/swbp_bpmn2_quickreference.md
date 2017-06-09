---
title: Referencia rápida de la notación BPMN 2.0
tags: [getting_started]
sidebar: swbp_sidebar
permalink: swbp_bpmn2_quickreference.html
folder: swbp
---

La presente sección constituye un glosario con los conceptos asociados a los diagramas de procesos de negocio bajo la especificación BPMN 2.0. La información proporcionada es para fines únicamente de referencia. Si desea un mayor detalle sobre el funcionamiento, restricciones y propiedades de cada uno de los elementos puede consultar el documento del Estándar BPMN 2.0 en la página del [Object Management Group](http://www.omg.org/spec/BPMN/2.0/).

## Actividades
Una actividad es un paso del proceso, un trabajo divisible o indivisible con un objetivo en el flujo del mismo. A continuación se describen las actividades existentes en BPMN 2.0.

### Subprocesos
La siguiente tabla describe los distintos tipos de subprocesos, que son actividades divisibles.

{% include bpmnref.html block="subprocesses" %}

### Tareas

La siguiente tabla describe los distintos tipos de tareas, que son actividades indivisibles.

{% include bpmnref.html block="tasks" %}

### Tareas llamadas

La siguiente tabla describe los distintos tipos de tareas llamadas, que son actividades definidas como globales y pueden reutilizarse en distintos procesos.

{% include bpmnref.html block="calltasks" %}

## Eventos
Un evento es algo que acontece durante el flujo del proceso, influyendo en el curso del mismo.

### Eventos de inicio
Un evento inicial es un tipo de evento que crea una nueva instancia de un proceso. La siguiente tabla describe los distintos tipos de eventos de inicio.

{% include bpmnref.html block="startevents" %}

### Eventos intermedios
Un evento intermedio es un acontecimiento que sucede durante el curso del proceso indicando que algo ha ocurrido. Hay dos tipos de eventos intermedios: los eventos disparadores (inician una acción) y los receptores (esperan a que ocurra una acción). Adicionalmente, algunos de los eventos pueden comportarse como eventos interruptores (cancelan una actividad) o no interruptores. Un evento no interruptor se caracteriza por tener el borde punteado. La siguiente tabla describe los distintos tipos de eventos intermedios.

{% include bpmnref.html block="intermediateevents" %}

### Eventos finales
Los eventos finales indican que el proceso ha terminado y por tanto, cierran la instancia activa del mismo. Este tipo de eventos, mostrados en la tabla siguiente, puede además disparar una acción al momento del cierre.

{% include bpmnref.html block="endevents" %}

## Compuertas
Las compuertas son mecanismos de bifurcación o unión de flujos en procesos. Dicha bifurcación puede darse por condiciones en las variables del proceso (basadas en datos) o eventos que ocurren (basadas en eventos). La unión de flujos mediante compuertas siempre tiene un criterio fijo. La siguiente tabla describe los distintos tipos de compuertas.

{% include bpmnref.html block="gateways" %}

## Objetos de conexión
Los objetos de conexión son elementos que permiten indicar el flujo del proceso y el orden en que se realizan las distintas actividades. La siguiente tabla describe los distintos tipos de objetos de conexión.

{% include bpmnref.html block="flows" %}

## Artefactos
Los artefactos son elementos documentales que permiten agregar información adicional a los diagramas para hacer más entendible su lectura. La siguiente tabla describe los distintos tipos de artefactos.

{% include bpmnref.html block="artifacts" %}

## Objetos de Datos
Los objetos de datos representan la información que es transformada a lo largo del flujo del proceso. Se les puede ver como variables de un tipo establecido que pueden ser manipuladas durante el proceso. La siguiente tabla describe los distintos tipos de objetos de datos.

{% include bpmnref.html block="dataobjects" %}

## Carriles
Los carriles son mecanismos de organización de las actividades de un proceso. La siguiente tabla describe los distintos tipos de objetos de carriles.

{% include bpmnref.html block="swimlanes" %}

{% include links.html %}
