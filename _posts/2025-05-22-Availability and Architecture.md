---
title: "Availability and Architecture"
date: 2025-05-22 00:00:00 +0800
categories: [Desarrollo, Oracle Apex]
tags: [Oracle APEX, Low Code]
image: images/Desarrollo-Full-Stack/Oracle/APEX/availability-architecture.jpg
---

En esta entrada quiero compartir un resumen claro y práctico sobre la disponibilidad, arquitectura y capacidades de despliegue de Oracle APEX, especialmente cuando se combina con Oracle Autonomous Database. Si estás empezando o quieres entender mejor cómo funciona todo esto, esta guía te va a venir genial.

📍 Disponibilidad de Oracle APEX
Una de las cosas que más me gusta de Oracle APEX es que está disponible donde sea que puedas ejecutar Oracle Database. Literalmente:

En la nube de Oracle (OCI), que es lo más recomendable.

En tus propios servidores on-premises.

En nubes de terceros como AWS, Azure o Google Cloud.

Incluso en una región dedicada (sí, Oracle instala su nube completa en tu centro de datos si lo necesitas).

Además, viene incluido sin coste adicional en la base de datos Oracle y puedes usarlo con el plan gratuito de Oracle Cloud. Ideal para aprender o hacer pruebas reales sin gastar nada.

🔥 APEX + Autonomous Database: Combinación ganadora
Cuando usas APEX junto a una Autonomous Database, te olvidas de muchas tareas aburridas: parches, seguridad, backups, optimización… todo se hace solo.

Esto te deja enfocarte 100% en construir tu aplicación.

Y lo mejor: puedes elegir entre varios tipos de base de datos, según lo que necesites:

Transaction Processing – Para apps tipo ERP o CRM.

Data Warehouse – Si vas por análisis de datos o dashboards.

JSON Database – Si trabajas con datos semiestructurados.

APEX Service – El más simple y directo para desarrollo web.

🧩 ¿Qué es el APEX Application Development Service?
Este servicio de Oracle es lo más directo que hay para empezar a desarrollar con APEX en la nube. Ya viene con todo:

Editor visual APEX

Base de datos autónoma

Infraestructura de alto rendimiento

Lo uso personalmente cuando quiero desarrollar rápido, sin complicarme con configuración ni mantenimiento.

Ventajas que destaco:
Sin pagar por usuarios o apps.

APIs REST listas con ORDS.

Seguridad, rendimiento y backups gestionados por Oracle.

Puedes empezar gratis con el plan Always Free.

⚙️ Arquitectura de Oracle APEX (súper simplificada)
Una de las razones por las que APEX funciona tan bien es su arquitectura directa:

```plaintext
[ Navegador del usuario ]
        ↓ HTTPS
[ ORDS (REST Data Services) ]
        ↓ llamadas SQL/PLSQL
[ Oracle Database + Motor APEX ]
```

Todo pasa en la base de datos. No necesitas middleware complicado, servidores intermedios ni capas innecesarias. Esto significa menos fallos, más seguridad y mejor rendimiento.

🛠 Opciones de despliegue
Una vez terminada tu app, puedes publicarla en varios entornos:

Oracle Cloud (OCI) – Mi recomendación: más simple, escalable y económica.

Dedicated Region – Para gobiernos o bancos que necesitan tener todo in-house.

Terceras nubes (AWS, Azure, GCP) – También es posible, aunque requiere más configuración.

On-Premises – Si tienes tus propios servidores y políticas internas.

Hay libertad total para elegir según tus necesidades y presupuesto.

⚡ Desarrollo rápido y sin dolor
Lo que realmente hace que APEX brille es la velocidad de desarrollo. Tiene todo listo:

Seguridad y autenticación integradas.

Formularios, reportes, validaciones ya preconstruidas.

Conexión directa a la base de datos.

Control de sesiones, APIs REST, y más.

El flujo típico que yo sigo es:
Desarrollar – Uso asistentes y plantillas para generar interfaces.

Personalizar – Ajusto reglas, diseño y lógica con PL/SQL o JS si hace falta.

Entregar – Publico la app y ya está lista para usarse.

🎯 Conclusión personal
Si buscas una plataforma low-code que te permita desarrollar rápido, con seguridad, sin costos escondidos y sin preocuparte por la infraestructura, Oracle APEX con Autonomous Database es una excelente opción. Y si eres desarrollador como yo, vas a agradecer la flexibilidad que te da.