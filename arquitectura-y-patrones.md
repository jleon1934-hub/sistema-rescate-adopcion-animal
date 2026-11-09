
# Arquitectura y patrones de diseño

## 1. Arquitectura lógica del sistema

El Sistema de Control de Rescate y Adopción Animal utilizará una arquitectura basada en el patrón MVC (Modelo-Vista-Controlador), que permite separar la interfaz de usuario, la lógica de control y la gestión de los datos.

La arquitectura estará organizada en tres componentes principales:

### 1.1 Modelo (Model)

Representa los datos y las reglas de negocio del sistema.

Sus principales entidades serán:
- Usuario
- Ciudadano
- Voluntario
- Veterinario
- Animal
- CasoRescate
- Asignacion
- AtencionVeterinaria
- Adopcion
- Notificacion

### 1.2 Vista (View)

Representa la interfaz con la que interactúan los usuarios.

Permitirá:
- Registrar reportes de rescate.
- Consultar información de animales.
- Visualizar estados de los casos.
- Gestionar información de adopciones.

### 1.3 Controlador (Controller)

Recibe las solicitudes de la vista, coordina las operaciones y comunica los resultados.

Se proponen los siguientes controladores:
- RescateController
- AnimalController
- AsignacionController
- AdopcionController
- UsuarioController

## 2. Patrones de diseño

Se proponen los siguientes patrones de diseño para mejorar la organización, reutilización y mantenimiento del sistema.

### 2.1 Patrón Singleton

**Propósito:** garantizar una única instancia de una clase que centraliza una determinada responsabilidad.

**Aplicación:** se propone utilizarlo en un componente GestorCasos, encargado de centralizar determinadas operaciones de gestión de los casos de rescate.

**Justificación:** permite controlar el acceso a un gestor compartido y evitar la creación de múltiples instancias innecesarias. Su uso deberá limitarse para no introducir dependencias globales.

### 2.2 Patrón Observer

**Propósito:** establecer una relación de suscripción para notificar automáticamente a los interesados cuando ocurre un cambio.

**Aplicación:** cuando un caso cambie de estado, el sistema podrá generar una notificación para los usuarios o responsables suscritos.

**Justificación:** facilita la comunicación entre componentes y evita que la lógica principal del caso dependa directamente de cada mecanismo de notificación.

### 2.3 Patrón Factory Method

**Propósito:** definir un mecanismo para crear objetos sin depender directamente de la clase concreta que se instancia.

**Aplicación:** se propone utilizar una fábrica para crear registros especializados de animales según su especie, como perros, gatos y fauna silvestre.

**Justificación:** facilita la incorporación de nuevas categorías de animales y reduce la dependencia del código respecto a las clases concretas.

### 2.4 Patrón MVC

**Propósito:** separar la presentación, el control de solicitudes y la lógica de datos.

**Aplicación:** la interfaz se encargará de mostrar la información, los controladores procesarán las solicitudes y el modelo contendrá las entidades y reglas de negocio.

**Justificación:** mejora la organización, facilita el mantenimiento y permite modificar la interfaz sin alterar directamente las reglas de negocio.

## 3. Relación entre los patrones y el sistema

| Patrón | Aplicación | Beneficio |
|---|---|---|
| Singleton | GestorCasos | Centralización de una instancia compartida |
| Observer | Notificaciones | Avisos automáticos ante cambios |
| Factory Method | Creación de animales | Flexibilidad para nuevas especies |
| MVC | Organización general | Separación de responsabilidades |

## 4. Principios de diseño SOLID

Se consideran los siguientes principios para orientar el diseño:

- **Responsabilidad única:** cada clase debe tener una responsabilidad principal.
- **Abierto/cerrado:** permitir extender funcionalidades sin modificar innecesariamente el código existente.
- **Sustitución de Liskov:** las clases derivadas deben poder utilizarse respetando el comportamiento esperado de sus clases base.
- **Segregación de interfaces:** evitar interfaces demasiado grandes con operaciones que algunas clases no necesitan.
- **Inversión de dependencias:** procurar que los componentes dependan de abstracciones y no de implementaciones concretas.

## 5. Conclusión

La arquitectura MVC y los patrones Singleton, Observer y Factory Method proporcionan una propuesta organizada para el Sistema de Control de Rescate y Adopción Animal. Su aplicación busca facilitar el mantenimiento, la extensibilidad y la separación de responsabilidades durante el desarrollo del sistema.
