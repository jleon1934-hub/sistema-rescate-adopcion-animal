
# Documentación del Sistema de Control de Rescate y Adopción Animal

## 1. Información general

**Nombre del proyecto:** Sistema de Control de Rescate y Adopción Animal.

**Objetivo:** facilitar el registro, seguimiento y gestión de animales rescatados, desde el reporte inicial hasta su atención veterinaria y posible adopción.

## 2. Organización del repositorio

El proyecto utiliza GitHub para almacenar los archivos, organizar el trabajo y mantener un historial de cambios.

La estructura de ramas es la siguiente:

- `master`: contiene la versión estable del proyecto.
- `develop`: integra los cambios de las diferentes funcionalidades.
- `feature/diagramas`: contiene los diagramas UML.
- `feature/requisitos`: contiene los requerimientos funcionales y no funcionales.
- `feature/arquitectura`: contiene la propuesta arquitectónica y los patrones de diseño.
- `feature/documentacion`: contiene la documentación general del proyecto.

## 3. Estrategia de trabajo Gitflow

Se utiliza Gitflow como estrategia de control de versiones.

El procedimiento de trabajo es:

1. Crear las ramas de funcionalidad a partir de `develop`.
2. Realizar los cambios correspondientes en cada rama.
3. Guardar los cambios mediante commits.
4. Crear un Pull Request desde cada rama `feature` hacia `develop`.
5. Revisar los cambios antes de integrarlos.
6. Integrar `develop` en `master` cuando la versión esté revisada y estable.

## 4. Descripción de los módulos del sistema

### 4.1 Gestión de usuarios

Permite organizar los usuarios según sus roles: ciudadanos, voluntarios, veterinarios y administradores.

### 4.2 Gestión de rescates

Permite registrar reportes, identificar animales y consultar el estado de los casos.

### 4.3 Asignación de responsables

Permite asociar voluntarios y veterinarios con los casos de rescate.

### 4.4 Atención veterinaria

Permite registrar diagnósticos, tratamientos y observaciones médicas.

### 4.5 Gestión de adopciones

Permite administrar la disponibilidad de animales y el seguimiento de los procesos de adopción.

### 4.6 Notificaciones

Permite informar a los usuarios interesados sobre cambios relevantes en los casos.

## 5. Diagramas del proyecto

El diseño del sistema contempla los siguientes diagramas:

- Diagrama de casos de uso.
- Diagrama de clases.
- Diagrama de arquitectura lógica MVC.
- Diagrama de secuencia para registrar un rescate.
- Diagrama de secuencia para actualizar el estado de un caso.

Los diagramas editables se encuentran en el archivo `Diagramas_Rescate_Adopcion_Animal.drawio`, dentro de la rama correspondiente, cuando haya sido incorporado al repositorio.

## 6. Control de cambios

Cada modificación del proyecto deberá registrarse mediante un commit con un mensaje claro que describa el cambio realizado.

Los Pull Requests permitirán revisar e integrar los cambios de las ramas de funcionalidad en `develop`.

## 7. Consideraciones de seguridad y mantenimiento

- Restringir las operaciones administrativas a usuarios autorizados.
- Validar la información ingresada en los formularios.
- Mantener un historial de cambios.
- Evitar almacenar contraseñas en texto plano.
- Realizar revisiones antes de integrar cambios en la rama estable.

## 8. Conclusión

La documentación permite comprender la organización del proyecto, sus módulos principales y la estrategia utilizada para controlar las versiones. Su mantenimiento facilitará la comprensión, revisión y evolución del Sistema de Control de Rescate y Adopción Animal.
