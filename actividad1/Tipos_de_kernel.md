Walter Gustavo Cotí Xalin
```201700522```
# Tipos de Nucleos

## Exonúcleos

Este tipo de kernel se denomina también sistema operativo verticalmente estructurado, simboliza un acercamiento nuevo y radical a la producción de sistemas operativos. La noción profunda es facilitar que el productor tome todas las decisiones vinculadas a la productividad del hardware.

Los exonúcleos son muy diminutos, debido a que su funcionalidad se vincula únicamente al resguardo y el multiplexado de los materiales. Se denominan de esta forma debido a que toda la funcionalidad deja de estar presente en la memoria y pasa a estar en el exterior, en librerías activas.

## Micro-núcleos
Consisten en núcleos de reducido tamaño que fueron generados sólo con los requerimientos más sencillos del sistema operativo. Las demás funciones son agregadas a través de la suma de módulos exteriores al núcleo, lo que les otorga flexibilidad y permite la extensión. Se consideran más seguros que el kernel monolítico.

## Kernel de Poisson
El kernel de Poisson es un núcleo completo que se emplea para poder solucionar en dos extensiones el problema de Dirchlet.  Este tipo de kernel tiene su nombre debido al físico Siméon Poisson, quien nació en Francia.

## Núcleos monolíticos
Estas estructuras poseen un núcleo enorme y complicado, que abarca todos los servicios del sistema. Está diseñado de manera no modular, y tiene un funcionamiento mayor que el micronúcleo.

Pero, cualquier modificación realizada en un servicio necesita un compendio del núcleo y el inicio del sistema para ejecutar las nuevas modificaciones.

El sistema operativo con un kernel monolítico agrupa todas las funcionalidades probables (sistema de archivos, gestión de almacenamiento, reguladores de dispositivos, entre otros) en el interior de una aplicación. El mismo puede tener una dimensión considerable, y deberá ser agrupado totalmente al agregar una funcionalidad nueva.

## Núcleos híbridos
Consiste en una estructura fundamentada en la unión de microkernel y el núcleo monolítico, dichos sistemas son empleados dentro de los ordenadores mediante los sistemas operativos.

Una cualidad esencial que tiene el núcleo híbrido es que insertan un código extra con el propósito de mejorar la productividad.

Al contrario de los núcleos monolíticos comunes, los controladores de ordenadores y las dimensiones al sistema operativo se pueden descargar o cargar de forma fácil como si fueran módulos, mientras la estructura sigue funcionando sin inconvenientes.

De igual forma, al contrario del kernel monolítico tradicional, es posible que los controladores sean prevolcados (retenidos de forma breve por ejercicios más esenciales) bajo diversas estipulaciones. Esta capacidad fue añadida para trabajar de forma apropiada las suspensiones de hardware, y para beneficiar la base de multiproceso proporcionado.

## Kernel panic
Consiste en una actividad realizada por un sistema operativo al descubrir una equivocación interna grave de la que no puede librarse.

El vocablo es usado en especial en los sistemas Unix. Sin embargo, es posible que se observen en los sistemas Mac OS X. Una de las causas del kernel panic, se manifiesta cuando un sistema operativo trata de leer una dirección de almacenamiento incorrecto.

| Tipo de Núcleo   | Ventajas                                                                                                                                                                                                                                                                                                                                                                 | Desventajas                                                                                                                                                                                                                                  |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Exonúcleos       | - Permite decisiones personalizadas de productividad del hardware.<br>- Bajo consumo de recursos de memoria.                                                                                                                                                                                                                                                            | - Restricción a la funcionalidad interna.<br>- Dependencia de librerías activas.<br>- Menos flexibilidad comparado con otros tipos de núcleo.                                                                                                                                                             |
| Micro-núcleos    | - Mayor seguridad debido a la modularidad.<br>- Flexibilidad y capacidad de extensión del sistema operativo.                                                                                                                                                                                                                                                          | - Rendimiento ligeramente inferior debido a la comunicación entre módulos.<br>- Mayor complejidad en la gestión de módulos.<br>- Posible sobrecarga de comunicación entre componentes.                                                                                                                   |
| Kernel de Poisson | - Soluciona el problema de Dirichlet en dos extensiones.<br>- Aplicable en problemas matemáticos específicos.                                                                                                                                                                                                                                                          | - Limitado a un problema matemático específico.<br>- No es un núcleo generalista para sistemas operativos.<br>- Poca relevancia en sistemas operativos modernos.                                                                                                                                         |
| Núcleos monolíticos | - Mayor rendimiento debido a la ausencia de comunicación entre módulos.<br>- Acceso directo a todas las funcionalidades del sistema.                                                                                                                                                                                                                                  | - Menor flexibilidad para agregar o modificar funcionalidades.<br>- Mayor dificultad en el mantenimiento y depuración.<br>- Mayor vulnerabilidad a errores que pueden afectar todo el sistema.                                                                                                             |
| Núcleos híbridos | - Mayor flexibilidad para agregar y quitar componentes.<br>- Mejor manejo de suspensiones de hardware y multiproceso.<br>- Equilibrio entre rendimiento y modularidad.                                                                                                                                                                                                | - Complejidad adicional en el diseño y gestión de módulos.<br>- Posibles conflictos entre componentes cargados dinámicamente.<br>- No alcanza el rendimiento puro de un núcleo monolítico en algunas situaciones.                                                                                            |
| Kernel panic     | - Evita que el sistema continúe funcionando con un error grave.<br>- Puede prevenir corrupción de datos o daños mayores.<br>- Facilita la identificación de problemas y su corrección.                                                                                                                                                                                 | - Interrumpe abruptamente la operación del sistema.<br>- No siempre proporciona información detallada sobre la causa del error.<br>- Puede provocar pérdida de trabajo no guardado.<br>- Requiere reiniciar el sistema para continuar la operación. |



# User vs Kernel Mode
| Criterio                  | Modo Kernel                     | Modo Usuario                                                   |
|-------------------------|--------------------------------|----------------------------------------------------------------|
| Acceso a recursos       | En el modo kernel, el programa tiene acceso directo e irrestricto a los recursos del sistema. | En el modo usuario, el programa de la aplicación no tiene acceso directo a los recursos del sistema. Para acceder a los recursos, se debe realizar una llamada al sistema (system call). |
| Interrupciones          | En el modo kernel, todo el sistema operativo podría colapsar si ocurre una interrupción. | En el modo usuario, un solo proceso falla si ocurre una interrupción. |
| Modos                   | El modo kernel también se conoce como modo maestro, modo privilegiado o modo sistema. | El modo usuario también se conoce como modo no privilegiado, modo restringido o modo esclavo. |
| Espacio de direcciones virtuales | En el modo kernel, todos los procesos comparten un único espacio de direcciones virtuales. | En el modo usuario, cada proceso tiene su propio espacio de direcciones virtuales separado. |
| Nivel de privilegio     | En el modo kernel, las aplicaciones tienen más privilegios en comparación con el modo usuario. | En el modo usuario, las aplicaciones tienen menos privilegios. |
| Restricciones           | En el modo kernel, al tener acceso tanto a los programas de usuario como a los programas del kernel, no hay restricciones. | En el modo usuario, se necesitan acceder a los programas del kernel a través de llamadas al sistema, ya que no puede acceder directamente a ellos. |
| Valor del bit de modo   | El bit de modo del modo kernel es 0. | Mientras que el bit de modo del modo usuario es 1. |
| Referencias de memoria  | El modo kernel es capaz de referenciar ambas áreas de memoria. | El modo usuario solo puede hacer referencias a la memoria asignada para el modo usuario. |
| Fallo del sistema       | Un fallo del sistema en el modo kernel es grave y complica las cosas. | En el modo usuario, un fallo del sistema se puede recuperar simplemente reanudando la sesión. |
| Acceso                  | Solo se permite la funcionalidad esencial para operar en este modo. | Los programas de usuario pueden acceder y ejecutar en este modo para un sistema determinado. |
| Funcionalidad           | El modo kernel puede referirse a cualquier bloque de memoria en el sistema y también puede dirigir la CPU para la ejecución de una instrucción, lo que lo convierte en un modo muy potente y significativo. | El modo usuario es un modo de visualización estándar y típico, lo que implica que la información no puede ejecutarse por sí sola ni hacer referencia a ningún bloque de memoria; necesita una Interfaz de Programación de Aplicaciones (API) para lograr estas cosas. |