# EcclesiaRed — portfolio case study

> Proyecto realizado en un contexto de prácticas. Este snapshot es una ficha técnica de portfolio y **no incluye el código fuente ni materiales internos** mientras no exista una autorización expresa de publicación.

Proyecto mostrado exclusivamente con fines de portfolio. El código fuente y los materiales propietarios de EcclesiaRed/Clixade no se distribuyen. No se concede permiso para reutilizar, redistribuir o explotar materiales de terceros.

## Resumen

EcclesiaRed fue un prototipo de aplicación para gestión interna de una organización, evolucionado desde una interfaz web hasta una arquitectura local con API, persistencia y una envoltura móvil Android. El trabajo demuestra cómo convertir una maqueta en un flujo funcional verificable sin confundir una demo local con un sistema de producción.

## Qué problema aborda

Centraliza comunicación, agenda y avisos operativos en una interfaz sencilla, manteniendo los datos persistentes y una base preparada para ampliar el producto con autenticación, notificaciones y despliegue controlado.

## Arquitectura conceptual

```text
Web HTML/CSS/JavaScript
          ↓
API local Node.js + Express
          ↓
SQLite local
          ↓
Capacitor → Android
```

La aplicación móvil reutiliza el frontend mediante Capacitor. En desarrollo, el emulador Android accede al backend del equipo a través de la dirección especial `10.0.2.2`; no se incluyen endpoints públicos ni credenciales.

## Stack trabajado

- HTML, CSS y JavaScript.
- Node.js y Express para la API REST local.
- SQLite para persistencia de prototipo.
- JWT para las rutas privadas del entorno local.
- Capacitor y Android/Gradle para la envoltura móvil.
- JDK Eclipse Temurin 21 LTS para la validación Android.

## Funcionalidades desarrolladas

- Comunicación: bandeja, enviados, lectura y persistencia.
- Agenda Interior: eventos, edición, navegación y persistencia.
- Notificaciones simuladas dentro de la aplicación.
- Login de desarrollo y API REST local.
- Asistente virtual en modo `local_demo`, sin API externa ni coste.
- Sincronización del frontend con Capacitor y compilación Android debug.

## Qué demuestra técnicamente

- Separación frontend/API/persistencia.
- Diseño de contratos REST y manejo de estados de error.
- Persistencia local verificable tras recarga.
- Adaptación de una aplicación web a Android con Capacitor.
- Validación incremental: tests, sincronización Capacitor y `assembleDebug`.
- Prudencia al mantener fuera de la demo las integraciones de producción no verificadas.

## Estado de validación

La evidencia local existente registra saneado de PII y secretos, tests correctos, sincronización de Capacitor y compilación `gradlew assembleDebug` correcta con JDK 21. Este documento no sustituye una autorización de publicación ni una revisión legal de la propiedad intelectual.

## Alcance de este snapshot

Este directorio contiene únicamente documentación conceptual redactada para portfolio. No contiene:

- código fuente;
- SQLite, APK/AAB ni builds;
- manuales o PDFs internos;
- datos reales, PII o credenciales;
- configuración local o secretos;
- historial Git.

## Licencia

No se añade licencia. La licencia y cualquier publicación de código deberán decidirse después de confirmar por escrito los derechos de publicación con la empresa o responsable de las prácticas.

