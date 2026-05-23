# [nombre-del-proyecto]

[Descripción en una línea del proyecto y su stack principal.]

## Comandos

[Completá los comandos principales para correr, buildear, testear y deployar el proyecto.]

```bash
# ejemplo
npm run dev     # Servidor de desarrollo
npm run build   # Build de producción
npm test        # Correr tests
```

## Arquitectura

[Describí la estructura de carpetas y los entry points. Breve — enfocate en lo que no es obvio.]

```
src/
├── [entry-point]    # [qué hace]
└── [carpeta clave]/ # [qué contiene]
```

## Modelo de datos

[Listá las entidades principales y sus relaciones. Solo lo que Claude necesita para entender el dominio.]

## Entorno

[Listá las variables de entorno requeridas y dónde van.]

```
VARIABLE=valor   # para qué sirve
```

## Prioridades

1. **Orden** — branches limpios, un PR por bloque, issues linkeados
2. **Seguridad** — auth, validación de inputs, secrets
3. **Todo lo demás**

## Reglas de flujo

- **Nunca commitear** sin que el usuario confirme explícitamente que la feature funciona end-to-end
- **Diagnóstico completo antes de cualquier fix** — identificar TODAS las causas raíz, enunciarlas, pedir confirmación, recién después escribir código
- **Sin mejoras especulativas** — solo cambiar lo que se pidió

## Reglas (auto-cargadas por Claude)

| Archivo | Cuándo está activo |
|---------|-------------------|
| `.claude/rules/git-workflow.md` | Siempre |
| `.claude/rules/security.md` | Siempre |
| `.claude/rules/[stack].md` | Al editar `src/**` — agregá las tuyas |

## Agentes disponibles

- `explorer` — mapea la estructura del codebase, nunca edita código
