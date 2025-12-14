---
applyTo: '**'
---
Provide project context and coding guidelines that AI should follow when generating code, answering questions, or reviewing changes.

## Creación de Ramas en Git y GitHub

Al trabajar en este proyecto, siempre se deben crear ramas de Git para nuevas funcionalidades o correcciones. 

### Proceso de creación de rama:
1. El usuario proporciona solo el **nombre base de la rama** (ej: `Alta-Usuario`, `Corregir-Validacion`)
2. El AI debe **analizar el contexto** para determinar el prefijo apropiado
3. El AI **construye el nombre completo** combinando prefijo + nombre base
4. El AI **crea la rama** con el nombre completo

### Convención de nombres y prefijos:

| Prefijo | Caso de uso | Ejemplo |
|---------|-------------|---------|
| `feature/` | Nuevas funcionalidades / Desarrollo | `feature/alta-usuario` |
| `release/` | Cambios para producción | `release/v1.2.0` |
| `bugfix/` | Corrección de errores | `bugfix/corregir-validacion` |
| `docs/` | Cambios en documentación | `docs/actualizar-readme` |
| `refactor/` | Mejoras de código existente | `refactor/optimizar-renders` |

### Reglas de nombrado:
- Nombres descriptivos y en minúsculas
- Usar guiones para separar palabras
- Basarse en la rama `develop` antes de empezar trabajo nuevo
- Ser eliminadas después de hacer merge en `develop`

### Lógica de selección de prefijo (AI):
- **Si es trabajo de desarrollo o nuevas funcionalidades ? usar `feature/`** (prefijo por defecto)
- **Si es para cambios de producción ? `release/`**
- **Si es arreglo de error ? `bugfix/`**
- **Si es cambio de documentación ? `docs/`**
- **Si es mejora de código existente ? `refactor/`**

## Estándares de Commits

Los mensajes de commit deben ser claros y descriptivos:
- Usar tiempo verbal presente ("Agrega" en lugar de "Agregó")
- Ser conciso pero informativo (máximo 50 caracteres para el título)
- Incluir descripción detallada si es necesario, separada por una línea en blanco

## Proceso de Pull Requests

Todos los cambios deben ser revisados antes de hacer merge a `main` o `master`. El proceso incluye:
- Crear un PR descriptivo con contexto del cambio
- Esperar revisión y aprobación
- Asegurar que todos los tests pasen
- Borrar la rama después del merge

## Estructura del Proyecto

El proyecto contiene información sobre héroes, villanos, ciudades y misiones con archivos markdown organizados en directorios específicos. Mantener esta estructura coherente es fundamental.

## Documentación

Todos los cambios significativos deben estar documentados en los archivos README correspondientes. La documentación debe ser clara y accesible para nuevos colaboradores.