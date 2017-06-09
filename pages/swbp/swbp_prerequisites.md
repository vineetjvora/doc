---
title: Prerequisitos
tags: [setup]
keywords: release notes, announcements, what's new, new features
sidebar: swbp_sidebar
permalink: swbp_prerequisites.html
folder: swbp
---

## Java Development Kit 1.7 o superior

SWB Process es una aplicación Web Java, por lo que es requerido contar con el Java Development Kit (JDK). Aunque SWB Process puede desplegarse utilizando [OpenJDK](http://openjdk.java.net/), se recomienda el uso de la versión del [JDK de Oracle](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

## Servidor de Base de Datos

Para almacenar la información generada por SWB Process, es necesario contar con un servidor de base de datos. SWB Process solo se podrá instalar en Bases de Datos que se encuentren soportadas en los conectores SDB y TDB, por  ejemplo  MySQL, Oracle 10gR2, SQL Server 2005, etc. Puede consultar más información sobre  dichos  conectores  en la  [documentación  del  proyecto  jena](http://jena.apache.org/documentation/sdb/databases_supported.html).

Por defecto, SWB Process está configurado para utilizar una base de datos [HyperSQL](http://hsqldb.org/).

## Servidor de aplicaciones Java

SWB Process es una aplicación Web Java, por lo que su despliegue se realiza a través de un servidor de aplicaciones, por  ejemplo: [Jetty](https://eclipse.org/jetty/),  [Apache Tomcat](http://tomcat.apache.org/),  [GlassFish](https://glassfish.java.net/),  [JBoss](http://www.jboss.org/) o [WebLogic](http://www.oracle.com/technetwork/middleware/weblogic/overview/index-085209.html).

Puede consultar la compatibilidad de los servidores de aplicaciones con las versiones del JDK en la [página de compatibilidad de Oracle](http://www.oracle.com/technetwork/java/javaee/overview/compatibility-jsp-136984.html)

## Archivo WAR de la aplicación

Puede descargar la última versión de SWBProcess en la sección de descargas de la página de [SemanticWebBuilder](http://semanticwebbuilder.org.mx/es_mx/swb/SWB_Process).

## Requerimientos de Hardware

Se recomienda como mínimo contar con el poder de cómputo equivalente a un procesador Xeon 2007 a 1Ghz (1vCore) y 600MB de RAM. Para un rendimiento estándar se recomiendan 2vCore y 1.7GB de RAM.

{% include links.html %}
