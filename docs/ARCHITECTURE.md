# Arquitectura conceptual

Este documento resume la arquitectura observada sin copiar implementación propietaria.

## Flujo principal

1. El navegador carga la interfaz web.
2. El frontend solicita datos a la API local.
3. Express valida la sesión de desarrollo y ejecuta operaciones sobre SQLite.
4. Comunicación, Agenda Interior y notificaciones simuladas actualizan la interfaz con datos persistentes.
5. Capacitor reutiliza el frontend en Android y adapta la URL del backend según el entorno.

## Límites deliberados

- El backend es local en el prototipo.
- Las notificaciones son registros internos, no push reales.
- El asistente virtual usa conocimiento local y no llama a servicios de IA externos.
- Firebase, despliegue público, tiendas y firma release quedan fuera del alcance validado.

