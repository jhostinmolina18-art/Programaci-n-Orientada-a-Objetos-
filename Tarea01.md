## Caso de uso: Gestionar proceso de crédito venta de electrodomésticos

| Elemento | Descripción |
|----------|-------------|
| ID | CU01 |
| Caso de uso | Gestionar proceso de crédito venta de electrodomésticos |
| Actores | Cliente, Vendedor, Representante de crédito, Sistema de pago automático |
| Propósito | Solicitud de crédito por el cliente hasta el pago automático de las cuotas |
| Descripción | 1. El Cliente solicita crédito al Vendedor al momento de la compra.<br>2. El Vendedor registra la solicitud de crédito.<br>3. El Representante de Crédito autoriza o rechaza la solicitud.<br>4. Si el crédito es aprobado, el Vendedor entrega el producto al Cliente.<br>5. El Sistema de Pago Automático cobra mensualmente las cuotas del crédito al Cliente. |
| Precondiciones | El cliente desea comprar un electrodoméstico.<br>El sistema de registro de ventas y créditos está operativo.<br>El representante de créditos tiene acceso al sistema de autorización.<br>El cliente tiene una tarjeta de crédito válida para débito automático. |
| Postcondiciones | El cliente ha recibido el electrodoméstico.<br>El crédito ha sido otorgado y registrado.<br>El proceso de pago automático mensual está configurado. |
| Extensiones síncronas | Si el crédito es rechazado<br>Si el cliente no está registrado<br>Si la solicitud de crédito es cancelada por el vendedor o cliente<br>Si el Sistema de Pago Automático falla en el cobro mensual |

![Caso de uso 1](./Credito.png.png)

## Caso de uso: Registrar renta de película

| Elemento | Descripción |
|----------|-------------|
| ID | BB-02 |
| Caso de uso | Registrar renta de película |
| Actores | Empleado |
| Propósito | Permitir registrar el préstamo de una película a un cliente |
| Descripción | 1. El sistema solicita al empleado ingresar el identificador del cliente.<br>2. El empleado ingresa los datos del cliente.<br>3. El sistema verifica si el cliente está registrado.<br>4. Si el cliente no existe, el sistema solicita los datos para su registro.<br>5. El empleado ingresa los datos del nuevo cliente.<br>6. El sistema registra al cliente en la base de datos.<br>7. El sistema muestra el catálogo de películas disponibles.<br>8. El empleado selecciona la película que el cliente desea rentar.<br>9. El sistema verifica la disponibilidad de la película.<br>10. El sistema muestra la información de la película seleccionada.<br>11. El empleado confirma la renta.<br>12. El sistema registra la renta asociando cliente, película y fecha.<br>13. El sistema actualiza el estado de disponibilidad de la película.<br>14. El sistema muestra un mensaje de confirmación de la renta realizada.<br>15. El sistema detecta la hora (9:00 a.m.).<br>16. Consulta clientes con devoluciones atrasadas.<br>17. Genera el listado. |
| Precondiciones | El sistema debe estar operativo<br>El catálogo de películas debe existir<br>El empleado debe haber iniciado sesión |
| Postcondiciones | La renta queda registrada en el sistema<br>La película queda marcada como no disponible |
| Extensiones síncronas | En paso 3: si el cliente no está registrado → se ejecuta el registro de cliente<br>En paso 9: si la película no está disponible → el sistema muestra mensaje de error y finaliza el proceso<br>En paso 11: si el empleado cancela la operación |

![Caso de uso 2](./pelicula.png.png)

## Caso de uso: Reponer artículos

| Elemento | Descripción |
|----------|-------------|
| ID | CU02 |
| Caso de uso | Reponer artículos |
| Actores | Encargado de reposición |
| Propósito | Permitir al encargado reponer el stock de productos y actualizar el sistema |
| Descripción | 1. El Encargado de Reposición accede a la pantalla de gestión con su contraseña.<br>2. El sistema autentica al encargado.<br>3. El sistema muestra la pantalla de reposición, indicando productos faltantes o bajos en stock.<br>4. El Encargado selecciona el producto a reponer.<br>5. El Encargado indica la cantidad repuesta.<br>6. El Encargado confirma la reposición.<br>7. El sistema actualiza el stock del producto inmediatamente.<br>8. El sistema emite un resumen de faltante en dos copias (constancia y factura). |
| Precondiciones | La máquina expendedora está operativa.<br>El Encargado de Reposición tiene una contraseña válida.<br>El sistema de gestión de stock está operativo. |
| Postcondiciones | El stock del producto repuesto se actualiza en el sistema.<br>Se emiten dos copias del resumen de reposición. |
| Extensiones síncronas | Contraseña incorrecta → acceso denegado<br>Error en ingreso de datos → solicitar nuevamente |

![Caso de uso 3](./bebida.png.png)
