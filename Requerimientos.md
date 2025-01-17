# Tienda la 40
## Requerimientos funcionales y no funcionales

- [Tienda la 40](#tienda-la-40)
  - [Requerimientos funcionales y no funcionales](#requerimientos-funcionales-y-no-funcionales)
  - [Propósito](#propósito)
  - [Alcance del software](#alcance-del-software)
  - [Funcionalidades del producto](#funcionalidades-del-producto)
  - [Clases y características de usuarios](#clases-y-características-de-usuarios)
  - [Requerimientos funcionales](#requerimientos-funcionales)
    - [Gestionar ventas](#gestionar-ventas)
      - [Descripción](#descripción)
      - [Acciones iniciadoras y comportamiento esperado](#acciones-iniciadoras-y-comportamiento-esperado)
      - [Requerimientos funcionales](#requerimientos-funcionales-1)
    - [Gestionar Inventario](#gestionar-inventario)
      - [Descripción](#descripción-1)
      - [Acciones y comportamiento esperado](#acciones-y-comportamiento-esperado)
      - [Requerimientos funcionales](#requerimientos-funcionales-2)
    - [Gestionar pedidos](#gestionar-pedidos)
      - [Descripción](#descripción-2)
      - [Acciones iniciadoras y comportamiento esperado](#acciones-iniciadoras-y-comportamiento-esperado-1)
      - [Requerimientos funcionales](#requerimientos-funcionales-3)
    - [Gestionar Pago o Transacción](#gestionar-pago-o-transacción)
      - [Descripción](#descripción-3)
      - [Acciones iniciadoras y comportamiento esperado](#acciones-iniciadoras-y-comportamiento-esperado-2)
      - [Requerimientos funcionales](#requerimientos-funcionales-4)
    - [Gestionar Envíos](#gestionar-envíos)
      - [Descripción](#descripción-4)
      - [Acciones iniciadoras y comportamiento esperado](#acciones-iniciadoras-y-comportamiento-esperado-3)
      - [Requerimientos funcionales](#requerimientos-funcionales-5)
    - [Gestionar Usuarios](#gestionar-usuarios)
      - [Definición](#definición)
      - [__Caso 1__](#caso-1)
        - [Acciones iniciadas, comportamiento esperado](#acciones-iniciadas-comportamiento-esperado)
        - [Requerimientos](#requerimientos)
      - [Caso 2](#caso-2)
        - [Acciones iniciadoras, comportamiento esperado](#acciones-iniciadoras-comportamiento-esperado)
        - [Requerimientos](#requerimientos-1)
  - [Requerimientos no funcionales](#requerimientos-no-funcionales)
    - [Tiempo de espera](#tiempo-de-espera)

## Propósito 

Sistema de gestión de ventas La 40.

La 40 es un punto de abastecimiento local cuyo objeto social es la comercialización de productos en el sector en el cual se encuentra ubicado.  Sus administradores solicitan el diseño e implementación de un sistema de información que le permita administrar la operación de venta de sus productos. 

El objetivo consiste en construir un sistema de información que permita gestionar las ventas de los productos de la organización, que abarque desde las solicitudes de pedido hasta el despacho de los productos. Para ello, se busca desarrollar una herramienta que permita el registro de las ventas, la gestión de productos, la gestión de pagos y la gestión de envíos de la mercancía, los cuales son los componentes principales que se consideran en el primer avance del sistema. 

## Alcance del software

En el sistema de información se busca desarrollar las actividades relacionadas con la gestión de las ventas de la tienda de La 40, incluyendo la gestión de pedidos, pagos y envío de productos.

Por lo anterior, el sistema de información no realizará operaciones de reembolso o devolución de pedidos, modificaciones a las ventas, buzón, quejas o reclamos y/o sugerencias respecto a los pedidos o relacionados, entre otros.

Se espera que el producto software beneficie a la tienda en su organización como punto de abastecimiento local de productos de la canasta familiar, así como en la posibilidad de la reactivación económica a través de nuevos canales digitales que se acoplen a los contenidos emergentes de las tecnologías de la información y las comunicaciones a nivel local, regional o nacional.

## Funcionalidades del producto

Lista de las funcionalidades del software que se están especificando en el documento de requerimientos. Cada funcionalidad puede estar compuesta por uno o varios requerimientos funcionales de software.

Aquí solo se incluye una lista numerada de las principales funcionalidades, la información detallada de requerimientos funcionales se documenta en las secciones posteriores.

| Funcionalidad                                          | Requerimiento funcional                                  |
|--------------------------------------------------------|----------------------------------------------------------|
| Gestionar ventas                                       | Orquestador                                              |
| Gestionar inventario                                   | Registrar ingreso y salida de mercancía                  |
| Gestionar pedidos                                      | Visualizar el estado actual de los pedidos               |
|                                                        | Validar el estado actual de los pedidos                  |
| Gestionar pago o transacción                           | Elegir la forma de pago (Efectivo o Tarjeta de crédito)  |
|                                                        | Calcular el valor a pagar (Aplicar impuesto)             |
|                                                        | Registrar pago del pedido.                               |
| Gestionar envíos                                       | Registrar envío                                          |  
|                                                        | Seguir estado del envío                                  |   
|                                                        | Actualizar estado del envío                              |
| Gestionar usuarios                                     | Validar tipo de usuario                                  | 
|                                                        | Registrar usuarios                                       |
|                                                        | Iniciar sesión de usuarios                               |

## Clases y características de usuarios

| Usuario                                          | Característica                                |
|--------------------------------------------------|-----------------------------------------------|
| Vendedor                                         | Este usuario es el encargado de realizar el registro de nuevas ventas. Además, puede visualizar el valor vendido hasta el momento. Por otro lado, también puede registrar nuevos productos que llegan a la tienda. |
| Cliente                                          | Usuario quien puede acceder a la plataforma y realizar su registro dentro de la página y así como efectuar compras. |
| Domiciliario                                     | Usuario quien recibe las órdenes de compra para despachar los pedidos a los clientes. |

## Requerimientos funcionales

### Gestionar ventas

#### Descripción 

esta funcionalidad permite la consulta, visualización y redireccionamiento a los componentes en cualquiera de las fases en la que se encuentre el proceso (vista del inventario, carrito de compras, pago, envío, pedido). 

> __Prioridad__ alto

#### Acciones iniciadoras y comportamiento esperado

- Se espera que el sistema tenga la capacidad de redireccionar hacía el componente solicitado por el usuario.
- Se espera que el sistema muestre la información hasta el momento registrada según la fase de compra.
- El usuario debe seguir el flujo de compra, esto es, iniciarlo y dirigirse a un componente en particular. 

#### Requerimientos funcionales

__REQ-1-F1__: Direccionar a componentes
- El sistema debe permitir al usuario seleccionar la opción del proceso de compra que desea visualizar.
- El sistema debe mostrar la información del componente que el usuario selecciona o que continua en el flujo.
- El sistema debe responder a la solicitud de direccionamiento que realiza el usuario sobre algún componente u opción en particular.
- El sistema debe direccionar correctamente al componente y cargar la información pertinente relacionada a la acción o proceso de ejecución.
- El sistema debe capturar la información asociada a la acción solicitada por el cliente para su consulta.

### Gestionar Inventario

#### Descripción 

Con esta funcionalidad el vendedor podrá hacer gestión de la entrada y salida de productos del inventario, esta gestión de inventario puede ser automática en el proceso de generar el pedido o también de manera manual en el proceso en el que se genere un pedido manual como por ejemplo cuando llega alguien que no tiene contacto con la plataforma virtual sino que es un usuario promedio de la tienda.

> __Prioridad__: alto

#### Acciones y comportamiento esperado
- Usuario(Cliente): Al generar el pedido se envía para verificarse con el sistema.
- Sistema:El sistema deberá descontar del inventario el producto, en caso de que si exista. Para el otro caso deberá existir o aparecer una advertencia de que el producto deseado no existe o no se encuentra en la cantidad deseada.
- Usuario(Vendedor): El vendedor deberá ser el encargado de ingresar o retirar elementos del inventario. Solo se podrá retirar en los casos que se genere un pedido físico.

#### Requerimientos funcionales

__REQ-1-F2__: Añadir productos al inventario

- El sistema muestra un formulario para añadir el producto
- El sistema deberá mostrar si el producto ya está creado, en dado caso que si solo se aceptará añadir una cantidad del producto.
- El sistema deberá mostrar la lista de productos, su cantidad, su descripción y su precio.
- El sistema deberá mostrar los cambios realizados.

__REQ-2-F2__: Retirar productos al inventario

- El sistema dejará retirar productos del inventario si se genera un pedido de venta y posteriormente una factura.
- El sistema dejará retirar productos solo si existe en el inventario la cantidad deseada.
- El sistema descontará el producto del inventario cuando se desee retirar.
- El sistema deberá mostrar los cambios realizados.

__REQ-3-F2__: Verificar productos existentes en el inventario
- El sistema deberá verificar si el producto existe o no - en el inventario
- El sistema deberá verificar que el producto existe en la cantidad deseada.


### Gestionar pedidos

#### Descripción 

con esta funcionalidad el vendedor podrá visualizar los pedidos hechos por los clientes, el domiciliario podrá visualizar los pedidos a su nombre y el cliente podrá visualizar y/o validar el estado de su pedido (Recibido, en preparación, pago fallido, enviado, entregado, cancelado, no entregado).

> __Prioridad__: medio

#### Acciones iniciadoras y comportamiento esperado
- Usuario (cliente): Puede visualizar el estado actual de los pedidos realizados.
- Sistema: Muestra el estado de los pedidos al cliente.
- Usuario (vendedor): Logra visualizar los estados de los pedidos.
- Usuario (domiciliario): Logra visualizar los estados de los pedidos asignados para entrega o el histórico de pedidos entregados a su nombre.

#### Requerimientos funcionales

__REQ-1-F3__: Visualizar estado actual de los pedidos
- El sistema muestra el listado de los pedidos para cada uno de los actores.

__REQ-2-F3__: Validar el estado de los pedidos
- El sistema da la opción de cancelación a cada uno de los actores, para el caso del domiciliario da la opción de aceptar o rechazar la oferta.
- El sistema de forma automática asigna a la persona domiciliaria.
Según el estado del pedido da la opción al cliente de modificar su pedido.

### Gestionar Pago o Transacción

#### Descripción 

Permite realizar el pago correspondiente a la compra, de acuerdo al valor de pago calculado, que varía dependiendo de la forma de pago y los impuestos que se apliquen. También se contemplan diferentes acciones dependiendo de la forma de pago (en efectivo o con tarjeta de crédito) elegida.  

> __Prioridad__: medio

#### Acciones iniciadoras y comportamiento esperado
- Sistema: genera factura preliminar de venta desde el módulo “gestionar carrito”.
- Usuario (cliente): elige forma de pago (en efectivo o con tarjeta de crédito).
- Sistema:  genera factura de venta final con el pago total a realizar.
- Caso 1 (Pago en efectivo):
  - Usuario (Domiciliario): realiza la gestión del envío.
  - Usuario (cliente): realiza pago contra entrega del pedido.
  - Usuario (Vendedor): actualiza estado de pago de la factura de venta a: pagado.
- Caso 2 (pago con tarjeta de crédito):
  - Sistema: Presenta interfaz de pago electrónico.
  - Usuario (cliente): Realiza pago electrónico.
  - Sistema: actualiza estado de pago de la factura de venta a: pagado.
  - Usuario (Domiciliario): realiza la gestión del envío.


#### Requerimientos funcionales

__REQ-1-F4__: Elegir forma de pago del pedido (Efectivo o Tarjeta de crédito). 

- El software debe mostrar las opciones de pago posterior a la generación preliminar de la factura de venta.
- En caso de no seleccionar forma de pago, el sistema no permite continuar con la transacción.

__REQ-2-F4__: Calcular el valor a pagar.

- De acuerdo a la forma de pago seleccionada, el sistema debe calcular nuevamente el valor a pagar, agregando cargos adicionales como impuestos y costes de envío, obteniendo la factura de venta final.

__REQ-3-F4__: Registrar pago del pedido.

- Una vez se haya realizado el pago del pedido, el sistema debe registrar y efectuar el cambio de estado de pago de la factura de venta a: pagado. En caso de ser pago contra entrega, se debe realizar el cambio de forma manual por parte del vendedor.
- Si el pago no se realiza, la factura de venta no cambia de estado.

### Gestionar Envíos

#### Descripción 

Permite al cliente conocer el estado de envío en que se encuentra su pedido (Recibido, Alistamiento, Enviado, Entregado, Cancelado, No entregado), el cual es actualizado por el vendedor o Domiciliario.

> __Prioridad__: medio

#### Acciones iniciadoras y comportamiento esperado 

- El registro del envío se registra con estado inicial de: Recibido, cuando se confirma el pedido.
- Los usuarios cliente, vendedor y domiciliario, pueden consultar en cualquier momento el estado de los envíos asociados a pedidos.
- Los usuarios vendedor y domiciliario pueden actualizar el estado del envío y el sistema debe realizar el cambio y el registro de la hora actual.

#### Requerimientos funcionales

__REQ-1-F5__: Registro del envío

- El sistema registrará el estado del envío como: recibido, cuando el pedido esté confirmado.
- El sistema almacenará la hora del registro del envío.
- Al ingresar el envío, todo envío estará asociado a un pedido de venta.
- A cada envío se le asignará un identificador único, que será utilizado para identificarlo en todos los procesos subsecuentes que se realicen sobre este.

__REQ-2-F5__: Seguimiento del estado del envío

- Se permitirá el seguimiento de los envíos asociados a pedidos de compra, desde la interfaz del cliente, del vendedor y de domiciliario.

__REQ-3-F5__: Actualización del estado del envío
- Se permitirá el cambio de estado de un envío por parte del vendedor o domiciliario.
- El sistema permitirá cambiar o actualizar el estado del envío.
- El sistema almacenará la hora del cambio del estado del envío.

### Gestionar Usuarios

#### Definición

Permite al dueño de la tienda conocer la información del cliente (nombre, dirección, teléfono de contacto, información de compra) que ha solicitado el pedido.

> __Prioridad__: alto

#### __Caso 1__
     
    El usuario debe registrarse y tener una cuenta para realizar los pedidos.

##### Acciones iniciadas, comportamiento esperado

- El cliente debe poder generar un nuevo usuario
- El cliente  debe entrar con su usuario registrado para hacer la compra.
- El usuario puede ingresar cuando quiera y ver su información, el estado de su pedido (si aplica) y demás opciones que este tenga.
- El usuario debe poder cambiar las credenciales y su información cuando lo desee siempre y cuando ya esté dentro de su perfil.
- El usuario puede gestionar sus compras, o pedir nuevas desde su perfil.
  
##### Requerimientos

__Req 1-F6__: Creación de usuario

- Debe permitir crear un perfil nuevo al llenar un formulario. Esto para generar un usuario.

__Req 2-F6__: Acceso de usuario

- Debe permitir al usuario entrar a una interfaz donde pueda realizar los pedidos, ver el seguimiento de estos y actualizar sus datos.
 
__Req 3-F6__: Interfaz de usuario.

- La interfaz de usuario permite acceder a diferentes herramientas únicas del tipo de usuario, el vendedor o administrador podrá acceder a la información de todos los usuarios, pero un usuario, puede acceder únicamente a su propia información.
 
 
#### Caso 2
    
    El usuario debe llenar un formulario con información básica para el envío del pedido, pero no tendrá una cuenta en la aplicación.

##### Acciones iniciadoras, comportamiento esperado

- El cliente debe poder llenar los datos de envío tras seleccionar los productos que desea llevar.
- El cliente puede elegir el medio de pago que más le favorezca dentro del formulario.
- El usuario puede hacer seguimiento a su pedido con el número de compra.

##### Requerimientos

__Req 1-F6.2__: El usuario no necesita un perfil:

- Para que el usuario solicite un producto solo debe diligenciar un formulario con nombre, teléfono, dirección y forma de pago de los productos solicitados.
- El formulario no se puede enviar sin rellenar los datos Nombre, teléfono, dirección y de medio de pago. 
- El formulario debe generar y mostrar un número de compra, para que el cliente pueda hacer un seguimiento del estado del producto.


## Requerimientos no funcionales

__REQNF-1__:
### Tiempo de espera

Para el funcionamiento de la aplicación se espera que el tiempo de respuesta sea imperceptible por el usuario final. Con este propósito, la aplicación considerada debe poseer un tiempo de respuesta menor o igual a 5 segundos.

- Criterios de aceptación:

La aplicación debe tener un tiempo de respuesta como máximo de 5 segundos en todas las tareas que tenga. De lo contrario, se considera que la aplicación no tiene el tiempo de respuesta esperado.

__REQNF-2__:
### Concurrencia

Para el funcionamiento de la aplicación se espera que diferentes usuarios puedan estar en el sitio web sin percibir fallas. Por lo tanto, el sistema debe ser capaz de operar adecuadamente con hasta 20 sesiones concurrentes.

- Criterios de aceptación:

La aplicación debe estar en capacidad de responder las peticiones de hasta 20 sesiones de manera concurrente. De lo contrario, se considera que la aplicación no cumple con el nivel de concurrencia esperado.

__REQNF-3__:
### Pruebas

Las pruebas de software se gestionarán con una herramienta de gestión de software testing.

- Criterios de aceptación:

Las pruebas de la aplicación deben ser realizadas por medio de una herramienta de gestión de gestión de software testing. De lo contrario, se considera que la aplicación no cumple con el nivel de confiabilidad y robustez esperado.

__REQNF-4__:
### Seguridad

La aplicación debe manejar criterios mínimos de seguridad y patrones de programación que permitan garantizar la integridad de la información en el manejo de datos. 

- Criterios de aceptación:
  - No presentar antipatrones de diseño que comprometan la integridad del aplicativo.
  - No incluir Hard-code en el código fuente del aplicativo (incrustar datos directamente en el código).
  - Utilizar protocolos de autenticación y autorización que garanticen la integridad de datos de usuario en el intercambio de información de extremo a extremo.
  - Creación y asignación de roles según el tipo de usuario.

__REQNF-4__:
### Persistencia

Toda la información relacionada al sistema, que está involucrada en las operaciones de los diferentes componentes, debe ser manejada y almacenada mediante el sistema de base de datos NoSQL orientado a documentos MongoDB.

- Criterios de aceptación:
  - La información debe ser almacenada en las colecciones definidas en el modelo de datos del sistema.
  - La información debe ser manipulable a través de las diferentes operaciones del sistema de base de datos.
