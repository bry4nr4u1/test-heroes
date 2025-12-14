---
agent: agent
---

# Creación de Ramas en Git

## Objetivo
Automatizar el proceso de creación de ramas locales y remotas con validación y sincronización.

## Requisitos

### 0. Actualizar la rama develop
- Actualizar la rama `develop` respecto a su versión en la nube
- Ejecutar `git fetch origin`
- Ejecutar `git pull origin develop` en la rama develop

### 1. Entrada del usuario
- Nombre de repositorio
- Ambiente donde se realizará cambios
- Nombre de rama a crear

### 2. Validación de repositorio actual
- Se debe validar la existencia de un repositorio actual
- Verificar que `.git` exista en el directorio actual
- Validar que hay conexión con el repositorio remoto
- Confirmar que es el repositorio correcto solicitado por el usuario

### 3. Creación sincronizada de ramas
- Crear la rama primero de manera local: `git branch <nombre-rama>`
- Crear la rama de manera remota: `git push -u origin <nombre-rama>`
- **Configurar el tracking (seguimiento)**: La rama local debe tener seguimiento de la rama remota
  - El parámetro `-u` establece automáticamente la rama remota como upstream
  - La rama local debe sincronizar con `origin/<nombre-rama>`
  - Verificar con `git branch -vv` que muestra el upstream de cada rama
- Validar que ambas ramas estén sincronizadas
- Verificar con `git branch -a` que aparezcan en local y remoto

### 4. Resultado informativo
- Mostrar el resultado de la creación de ambas ramas en un cuadro informativo dentro del chat
- Incluir:
  - ? Estado de creación de rama local
  - ? Estado de creación de rama remota
  - ? Confirmación de sincronización
  - ? Rama actual después de la operación
  - Errores (si los hay)

## Criterios de Éxito
- La rama existe localmente y en el repositorio remoto
- Ambas ramas están sincronizadas
- El usuario recibe confirmación clara del estado final
- No hay conflictos pendientes