---
description: Reglas base de seguridad — siempre activo
---

## General

- Nunca loguear secrets, tokens, contraseñas ni PII
- Nunca hardcodear credenciales — siempre usar variables de entorno
- Validar y sanitizar todo input del usuario en los límites del sistema
- Nunca confiar en IDs provistos por el cliente para autorización — verificar server-side

## Multi-tenancy (si aplica)

- Toda query DEBE estar scopeada al tenant/usuario autenticado
- Nunca consultar entre tenants, ni siquiera para operaciones admin salvo que esté diseñado explícitamente para eso

## Dependencias

- Nunca agregar una dependencia sin verificar que tiene mantenimiento reciente y sin CVEs críticos
- Preferir paquetes conocidos sobre desconocidos con funcionalidad similar
