
# Requerimientos del Sistema de Control de Rescate y Adopción Animal

## 1. Descripción general

El sistema tiene como finalidad gestionar los procesos de rescate, atención veterinaria y adopción de animales, facilitando el seguimiento de cada caso y la coordinación entre ciudadanos, voluntarios, veterinarios y administradores del refugio.

## 2. Actores del sistema

- **Ciudadano o reportante:** registra reportes de animales que necesitan rescate y consulta el estado de sus casos.
- **Voluntario:** consulta los casos asignados y participa en las actividades de rescate.
- **Veterinario:** registra diagnósticos, tratamientos y atenciones médicas.
- **Administrador del refugio:** administra usuarios, asignaciones, animales y procesos de adopción.

## 3. Requerimientos funcionales

| Código | Requerimiento |
|---|---|
| RF01 | El sistema permitirá registrar reportes de rescate animal. |
| RF02 | El sistema permitirá registrar información del animal rescatado. |
| RF03 | El sistema permitirá clasificar animales por especie: perros, gatos y fauna silvestre. |
| RF04 | El administrador podrá asignar voluntarios y veterinarios a los casos. |
| RF05 | El sistema permitirá consultar los casos registrados. |
| RF06 | El sistema permitirá actualizar el estado de cada caso. |
| RF07 | El veterinario podrá registrar diagnósticos y tratamientos. |
| RF08 | El sistema permitirá gestionar los procesos de adopción. |
| RF09 | El sistema notificará los cambios importantes en los casos. |
| RF10 | El administrador podrá gestionar los usuarios del sistema. |

## 4. Requerimientos no funcionales

| Código | Requerimiento |
|---|---|
| RNF01 | El sistema deberá ser escalable para permitir incorporar nuevas funcionalidades. |
| RNF02 | El código deberá estar organizado para facilitar su mantenimiento. |
| RNF03 | El proyecto deberá mantener trazabilidad de cambios mediante Git y GitHub. |
| RNF04 | El acceso a las funcionalidades deberá depender del rol del usuario. |
| RNF05 | La información deberá almacenarse de forma organizada y consistente. |
| RNF06 | La interfaz deberá ser clara y fácil de utilizar. |

## 5. Estados de los casos de rescate

- **Rescatado:** el animal ha sido localizado y rescatado.
- **En tratamiento:** el animal recibe atención veterinaria.
- **En adopción:** el animal está disponible para iniciar un proceso de adopción.

## 6. Reglas de negocio

1. Cada reporte deberá tener un identificador único.
2. Todo caso deberá estar asociado a un animal.
3. Las asignaciones deberán ser realizadas por el administrador.
4. Los cambios de estado deberán quedar registrados.
5. La adopción deberá gestionarse cuando el animal esté en condiciones adecuadas.

## 7. Conclusión

La definición de los requerimientos funcionales y no funcionales permite establecer las capacidades y condiciones que deberá cumplir el sistema. Esta documentación servirá como base para el diseño de la arquitectura y el desarrollo del proyecto.
