# Tarea 0 - CNA

## Instrucciones

1. Hacer un fork de este repo
2. En el fork crear un archivo llamado `RESPUESTA.MD` con las respuestas al ejercicio, además debe dejar el diagrama solicitado en formato PDF, PNG, o JPG. El archivo `RESPUESTA.MD` debe contener el nombre de los miembros del grupo que contestaron el ejercicio.

## Ejercicio: Modelar Micro Servicios

### Contexto 

“CraftStore” es un sitio web que permite la compra y venta de artesanía en línea. 

Funciona del siguiente modo:

-	Los artesanos interesados en vender sus productos en CraftStore se registran en un sitio especial (CraftStore/BackStore). Para esto llenan un formulario con sus antecedentes, el tipo de artesanía que venden y otros datos comerciales. Esta información es validada por un equipo de CraftStore que después de chequear los antecedentes procede a darles de alta.
-	Un artesano validado puede gestionar su catálogo de productos, asignando datos de sus productos, como la descripción, fotografías, precio y stock.
-	El sitio web tiene un punto de entrada donde el público masivo puede realizar las compras de los diferentes productos provistos por los artesanos. El portal permite que el cliente arme un carro de compra con productos de diferentes artesanos y genere una sola compra. La estructura de este sitio público es la típica de cualquier tienda online. Esta se integra con diversas plataformas de pago, como PayPal, Stripe, etc. 
-	El comprador puede registrarse y de este modo puede revisar sus pasadas compras, recibir ofertas por correo electrónico, y participar de eventos y promociones en el sitio.
-	Internamente el sistema se encarga de dividir la compra en diversas órdenes a cada artesano involucrado. Por ejemplo, si un usuario compra en el portal 2 artículos del artesano A, y 3 artículos del artesano B, el sistema crea una orden para el artesano A por los 2 productos, y la respectiva orden para el artesano B.
-	Los artesanos reciben notificaciones con las órdenes de compra que deben completar. Cuando tienen listo el pedido informan en la plataforma Backstore que el pedido está listo para ser despachado al cliente.
-	La plataforma se encarga de coordinar el despacho de los productos desde el artesano al comprador a través de una empresa de Courier (con quienes tienen un convenio y se integran usando una API).
-	Además de la compra y venta de artesanías, el sitio web tiene un canal con videos en que entrevistan a los artesanos. Un blog con sugerencias de decoración usando los productos expuestos, y además tienen una mini tienda propia donde vende merchandising propio (poleras, stickers, posa vasos, etc).
-	Craftstore se encarga de consolidar todas las ventas y administra el dinero recaudado, generando liquidaciones mensuales, enviando un único pago a fin de mes a cada artesano. Los artesanos deben subir una factura electrónica a la plataforma, para recibir el pago. Para aquellos artesanos que no cuentan con la tecnología, CraftStore les proporciona un módulo de gestión de facturas electrónicas.
-	Craftstore cuenta además con una app para Android y otra para iOS, ambas se integran con un backend que proporciona todos los servicios necesarios para vender productos.
-	También se está desarrollando una app para los artesanos, pues no todos cuentan con PC para conectarse, o prefieren usar el celular.

### Actividades y Preguntas

Usted ha sido contratado como arquitecto para diseñar una nueva plataforma para CraftStore usando micro servicios.

1. Haga una descomposición por dominios o por capacidades del negocio y de acuerdo a esta proponga la arquitectura de micro servicios inicial. Dibuje un diagrama con los micro servicios involucrados, dibujando interconexiones entre estos, si es que son necesarias. Deje este dibujo como un archivo PDF, PNG o JPG, junto con su respuesta. Considere micro servicios genéricos y las integraciones con terceras partes.
2. Cree un archivo `RESPUESTA.MD` y responda allí lo siguiente:
   - Liste los micro servicios necesarios y por cada uno describa su función principal.
   - Indique cuantos equipos necesitaría para soportar este desarrollo.
   - ¿Que patrón usaría para gestionar el tràfico entrante: API Gateway o Backends x Frontends? Justifique su respuesta
3. Recuerde colocar su nombre y el de sus compañeros en el archivo de respuesta.
