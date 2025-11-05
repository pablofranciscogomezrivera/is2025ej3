# Ingeniería de Software
## Ejercicio para Clase de Teoría N° 3
### Control de Versiones

### Objetivos
- Aplicar estrategia de ramificación
- Actualización de rama mediante pull request
- Simular liberación con rama release
- Reflexionar sobre los beneficios de aplicar una buena estrategia de ramas

## Descargar el proyecto
1. Realizar una bifurcación (fork) del repositorio
2. Clonar el repositorio bifurcado

## Trabajar en la rama de funcionalidad
1. Crear una rama nueva, basada en `master`, llamada `feature/modificar-producto`
2. Agregar a la clase `Product` los atributos `Tax` (double) y `FinalPrice` (double)
3. `FinalPrice`es de solo lectura y debe realizar la operación: `Price` * `Tax`
4. Realizar commits con los cambios (no olvidar comentarios)
5. Subir los cambios al repositorio y abrir un pull request (PR) hacia `master`
6. Aprobar el PR y mezclar a `master`

## Crear rama de release
1. Desde `master`crear una rama `release/v1.0`
2. Actualizar el archivo `version`con v1.0.0
3. Realizar commit y subir los cambios a la rama remota
4. Crear regla para que las ramas `release` solo puedan ser actualizadas mediante un PR

## Corregir bug
1. Crear la rama `bugfix/v1.0.1` desde `release/v1.0`
2. Reemplazar la operación en el atributo `FinalPrice`por `Price` * `1 + Tax`
3. Realizar commit
4. Actualizar el archivo `version` con v1.0.1
5. Realizar commit y subir los cambios a la rama remota
6. Abri un PR a `release/v1.0`
7. Aprobar el PR y mezclar

## Actualizar rama principal
1. Crear, desde `master`, la rama `bugfix/calculo-impuesto`
2. Identificar el commit con los cambios en `FinalPrice`
3. Realizar un cherry-pick del commit a la nueva rama
4. Abrir un PR a `master`
5. Aprobar el PR y mezclar
