# elbuensabor
Integrador Desarrollo de Software

Participantes del grupo:
- Sebastian Pineda
- Franco Suarez
- Juan Ingacio Sola


Sistema:
El delivery de comidas de la ciudad “El Buen Sabor” ofrece a sus clientes una amplia variedad de bebidas y de
comidas de fabricación propia. Posee un horario de atención de lunes a domingos de 20:00 a 12:00, y de sábados y
domingos de 11:00 a 15:00. Los clientes tienen a disposición un menú que describe cada una de las comidas, el
nombre, los ingredientes y el precio. Los clientes realizan sus pedidos en el mostrador del local mediante una PC o
pueden hacerlo en forma remota desde su casa o su celular personal (la aplicación debe ser responsive).
El cliente debe proceder a registrarse en la aplicación como paso inicial para realizar el pedido o ejecutar el login en
la misma si ya se encuentra registrado, el identificador único y nombre de usuario para el cliente será su email.
El pedido debe contener el número y la fecha del pedido, el nombre del Cliente, teléfono, su domicilio y el detalle de
las comidas y bebidas deseadas. Además, el cliente deberá indicar si retira el pedido en el local (en este caso se le
otorga un 10% de descuento en la compra) o desea que se lo envíen a su domicilio. El local admite 2 formas de pago,
efectivo únicamente si el pago se realiza en el local de forma presencial, si el pedido se entrega a domicilio solo se
acepta pago mediante mercado pago.
El sistema debe validar que el stock de artículos insumos que se posee sea suficiente para llevar a cabo el pedido, por
ejemplo, si el cliente pide una pizza de jamón crudo y rúcula, pero el stock de rúcula es 0, el sistema deberá emitir un
mensaje indicando la situación e impidiendo la carga de dicho artículo manufacturado al pedido.
Finalizada la carga del pedido el sistema le informará al cliente cuánto es el tiempo estimado para el retiro o entrega
de su pedido, este tiempo surgirá de la siguiente formula:
∑ Sumatoria del tiempo estimado de los artículos manufacturados solicitados por el cliente en el pedido actual
+
∑ Sumatoria del tiempo estimado de los artículos manufacturados que se encuentran en la cocina / cantidad
cocineros
+
10 Minutos de entrega por delivery (solo si corresponde).
El pedido realizado por el cliente ingresa a la bandeja de entrada de pedidos pendientes del cajero, este usuario
(cajero) revisa el pedido y si está correcto, lo aprueba, dicha acción envía el pedido a la cocina. El usuario cocinero
consulta los pedidos aprobados que debe preparar y cuando el pedido está listo lo marca con estado terminado, esta
acción envía el pedido nuevamente al usuario cajero pero a la bandeja de pedidos listos para entregar, ahora el
pedido puede seguir 2 caminos, el primero es que sea entregado al cliente directamente en el local lo cual originara
la factura correspondiente, con la forma de pago que corresponda y será entregada al cliente, dejando el pedido con
el estado final FACTURADO, o segundo el pedido es enviado mediante delivery al domicilio del cliente asignando al
pedido el estado “En delivery” hasta que el empleado que realizo el envío retorna al local e indica que la entrega fue
exitosa con lo cual el estado del pedido pasa a su estado final FACTURADO. La factura generada es enviada mediante
email al cliente, y puede ser accedida por él mediante la aplicación web en la sección Historial de Pedidos.
∙ El cliente además de poder cargar el pedido deberá poder consultar el historial de todos los pedidos realizados y
acceder a las correspondientes facturas asociadas, las cuales podrá descargar (Formato PDF).
∙ El cajero cumple un rol central de gestión ya que procesa todos los pedidos e interactúa con el resto de los actores
del sistema.
∙ El cocinero recepciona los pedidos y los elabora y además tiene el control de los artículos manufacturados pudiendo
variar la composición de los mismos.
∙ Finalmente, el usuario Administrador tiene acceso a todas las funcionalidades del sistema pero se ocupa
principalmente de los artículos insumo controlando que los mismos no se agoten.
