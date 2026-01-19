# Decisiones de Workflow - SCV Empresarial

## Sección 1: ¿Cuándo usamos rebase en este proyecto?
- **Limpieza local:** Lo usamos para organizar nuestro historial local antes de compartir el código (ej. unir varios commits de "WIP" o correcciones pequeñas en uno solo significativo).
- **Actualización de ramas:** Para traer los cambios más recientes de `main` a nuestra rama de `feature` sin crear un "merge commit" innecesario, manteniendo un historial lineal y limpio.
- **Regla de oro:** Nunca hacemos rebase en ramas públicas compartidas con otros desarrolladores.

## Sección 2: ¿Cuándo usamos merge en este proyecto?
- **Integración final:** Lo usamos para unir una rama de `feature` completada hacia la rama `main` o `develop`.
- **Preservar historia:** Cuando queremos que quede constancia explícita de cuándo y cómo se unió una funcionalidad al proyecto (Merge Commit), lo cual facilita revertir el grupo de cambios si algo sale mal.

## Sección 3: ¿Cuándo usamos cherry-pick?
- **Deploy selectivo:** Cuando necesitamos pasar una funcionalidad específica (como una función lista para producción) desde una rama experimental a `main`, sin traer el resto de código incompleto o inestable.
- **Hotfixes:** Para aplicar una corrección urgente que ya se hizo en otra rama, sin tener que fusionar toda la rama.

## Sección 4: Lecciones aprendidas en la Fase 2
- **Dependencias en Cherry-pick:** Aprendimos que `cherry-pick` traslada cambios, no archivos completos. Si el commit modifica un archivo que no existe en la rama destino, Git generará un conflicto.
- **Resolución manual:** En casos de archivos inexistentes, es necesario recrear el archivo o aceptar el conflicto manualmente (`git add`) para que Git tenga una base donde aplicar el cambio.
- **Conflictos lógicos:** Mover código fuera de orden (el paso B antes que el A) requiere atención manual para asegurar que el código resultante tenga sentido.
