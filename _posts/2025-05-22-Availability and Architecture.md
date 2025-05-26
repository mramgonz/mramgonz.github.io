---
title: "Availability and Architecture"
date: 2025-05-22 00:00:00 +0800
categories: [Desarrollo, Oracle Apex]
tags: [Oracle APEX, Low Code]
image: images/Desarrollo-Full-Stack/Oracle/APEX/availability-architecture.jpg
---

Si estás aprendiendo Oracle APEX con vistas a trabajar profesionalmente, uno de los temas clave que tenés que dominar es su disponibilidad y arquitectura. En esta entrada te explico exactamente eso: dónde puede ejecutarse APEX, cómo se conecta, qué componentes lo forman y cómo fluye todo internamente.

## 🌐 **Disponibilidad de Oracle APEX**

Oracle APEX está diseñado para ser extremadamente flexible y portable, lo que significa que podés ejecutarlo prácticamente en cualquier lugar donde exista una Oracle Database. Esa es la base de todo.

## 📍 **Lugares donde podés desplegar APEX**:

1. **Oracle Cloud (OCI)** – recomendado

- A través del servicio APEX Application Development Service.

- Totalmente gestionado por Oracle.

- Incluye plan gratuito (Always Free Tier).

- Ideal para desarrollo profesional, sin configurar nada.

2. **On-Premises**

- Podés instalar Oracle Database y APEX en tu propio servidor o VM.

- Usado en empresas con entornos cerrados o regulaciones específicas.

3. **Nubes de terceros (AWS, Azure, GCP)**

- Instalás Oracle DB + APEX manualmente.

- Requiere más configuración, pero funciona perfectamente.

4. **Dedicated Region**

- Oracle instala una región completa de su nube en tu datacenter.

- Pensado para bancos, gobiernos o empresas con requisitos extremos de seguridad.

🔸 **Conclusión**: APEX es portátil. No estás atado a un proveedor específico, pero Oracle Cloud es el camino más rápido y simple.

## 🧱 **Arquitectura de Oracle APEX (simplificada)**

Oracle APEX tiene una arquitectura muy eficiente y fácil de entender porque todo sucede dentro de la base de datos Oracle. Eso le da muchas ventajas: rendimiento, seguridad y simplicidad.

## 🔄 **Flujo de arquitectura**:

```plaintext
[ Navegador del usuario ]
        ↓ HTTPS
[ ORDS - Oracle REST Data Services ]
        ↓
[ Oracle Database con APEX ]
```

## 🧩 **Componentes clave**:

1. **Navegador**

- El usuario accede vía web (PC, móvil, tablet).

- No se necesita cliente ni instalación.

2. **ORDS (Oracle REST Data Services)**

- Middleware liviano que traduce las peticiones HTTP en llamadas SQL/PLSQL.

- Expone APIs REST, maneja sesiones, y entrega páginas APEX.

- Puede correr como servicio separado (Tomcat, Standalone, etc.).

3. **Oracle Database + APEX Engine**

- Aquí está toda la lógica de la aplicación.

- APEX vive como un componente PL/SQL dentro de Oracle DB.

- Procesa datos, ejecuta la lógica, genera HTML dinámico.

- Alta seguridad, integridad y rendimiento nativo.

## 🚀 **¿Por qué esta arquitectura es tan buena?**

- No hay capas intermedias innecesarias (como ORMs o servidores de aplicaciones).

- Todo se ejecuta en la base de datos → más rendimiento, menos latencia.

- Escalable y segura por diseño (usando roles, privilegios y cifrado nativo).

- Fácil de mantener, migrar o desplegar en múltiples entornos.

## 🎯 **Conclusión**

Si vas a trabajar con Oracle APEX, entender su disponibilidad y arquitectura es clave para tomar buenas decisiones de despliegue y mantenimiento. Saber que podés correrlo en OCI, localmente o incluso en nubes como AWS, y que todo fluye sin necesidad de frameworks pesados, es lo que hace que APEX sea tan poderoso.

Ahora ya tenés la base técnica clara. Desde acá podés seguir explorando cómo configurar ORDS, desplegar en producción, o trabajar con APIs REST sobre esta misma arquitectura.