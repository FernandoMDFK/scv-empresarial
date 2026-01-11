cat <<EOF > docs/architecture/git-architecture.md
# Arquitectura de Control de Versiones

Este documento define los estándares y la estrategia de Git para el proyecto **scv-empresarial**.

## 1. Estrategia de Branching
Se utiliza una adaptación de **GitHub Flow**:
- **main**: Rama de producción. Solo contiene código estable y verificado.
- **feature/**: Ramas temporales para el desarrollo de nuevas funcionalidades (ej. \`feature/login-system\`).
- **fix/**: Ramas para corrección de errores (ej. \`fix/header-bugs\`).

## 2. Convención de Commits
Seguimos el estándar de **Conventional Commits**:
- \`feat:\` para nuevas funcionalidades.
- \`fix:\` para corrección de errores.
- \`docs:\` para cambios en documentación.
- \`chore:\` para tareas de mantenimiento o estructura.

## 3. Políticas de Seguridad
- **Firmas GPG**: Todos los commits en la rama \`main\` deben estar firmados criptográficamente para garantizar la autoría.
- **Protección de Ramas**: No se permite el push directo a \`main\` (requiere Pull Request).

## 4. Estructura del Repositorio
- \`/src\`: Código fuente del sistema.
- \`/tests\`: Pruebas unitarias e integrales.
- \`/docs\`: Documentación técnica y de usuario.
EOF