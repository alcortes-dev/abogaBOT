# Abogabot

## Cliente

Despacho de abogados Hernández y Asociados, dedicados a los casos del ámbito civil, ubicado en la ciudad de México y con 20 años de experiencia, busca reducir los costos de tiempo y personal relacionados a la creación y seguimiento de las demandas, por lo que  automatizará estos procesos.

## Requerimientos

* Formulario de captura de demandas
* Formulario de pago
* Gestión de cuentas de usuario
* Seguimiento de demandas por usuario
* Creación de documento Word con información de demanda
* Gestión de notificaciones
* Seguimiento de pagos
* Actualización de demanda
* Diseño responsivo
* Paleta de colores azul marino, blanco



## Buyer persona

María es una mujer mexicana, profesionista de 28 años que reside en la ciudad de México, labora en una empresa con más de 100 empleados, y tiene un equipo a su cargo. Ella consume información de manera constante desde su equipo portátil y su Smartphone, donde también gestiona la mayoría de sus actividades.

María necesita del acompañamiento de profesionales en el ámbito de las leyes de carácter civil, para llevar temas legales, sin embargo es una persona con muchas responsabilidades, por lo que busca el el seguimiento de estos temas se pueda realizar de una manera sencilla y ágil.

## Público Objetivo

Nuestro público objetivo se encuentra determinado por los siguientes factores

### Demografía

* Hombres y mujeres mayores de 25 años
* Con educación media concluida
* Profesionistas

### Geografía

* Residentes en la ciudad de México y área metropolitana 

### Características

* Cuenta con acceso a equipo de computo
* Cuenta con Smartphone
* Tiene facilidad para consumir y crear información en dispositivos electrónicos.



## Especificación de requerimientos

### Formulario de captura de demandas

Se requiere de un formulario para la captura de la información inicial de la demanda, dentro de esta ventana se mostrarán los siguientes campos 

* Nombre del demandande - Caja de texto
* Domicilio del demandante - Caja de texto
* Documento de identidad del demandante - Selector con opciones válidas para la identificación del demandante
* Archivo de identidad del demandante - Selector de archivo para que el demandante ingrese su documento de identidad digitalizado.
* Nombre del demandano - Caja de texto
* Motivo de la demanda - Selector con opciones determinadas por Hernández y Asociados, del que se deberá seleccionar un valor.
* Descripción de Motivi - Cuadro de texto multilínea donde se  tallada del motivo por el que se realiza la demanda
* Botón de envío 

Todos los campos listados son requeridos para poder realizar la solicitud y continuar al siguiente paso.

Al enviar la información se verificará que esta sea completa, se almacenará y se le asignará un número de caso para su seguimiento.

Si todos los pasos anteriores se completan sin inconvenientes, se muestra una pantalla informando del éxito de la operación, así como el número de caso asignado. Finalmente se les muestra un botón para acceder al pago del servicio.

### Formulario de pago

Una vez realizada la solicitud, se realizará un cobro inicial con base en un tabulador que depende del Motivo de la demanda, en este formulario se mostrarán las siguientes opciones:

* Pago con tarjeta
  * Se deberá capturar la información de la tarjeta donde se realizará el cargo 
    * Número de tarjeta - Texto con un tamaño máximo de 16 dígitos
    * Fecha de vencimiento - Cuadro de texto con el formato MM/AA
    * CCV - Código en el reverso de la tarjeta limitado a 4 dígitos
    * Nombre impreso en la tarjeta
  * Después de la captura de los campos, se intentará realizar el cargo a la tarjeta indicada
  * Si el cargo se realiza de forma exitosa, se informará al usuario y se generará un comprobante de pago
  * Si no se concreta el cargo, se le dará al usuario la opción de intentarlo nuevamente, o utilizar el método de pago por referencia.
* Pago por referencia.
  * En esta opción se generará una referencia de pago que se podrá realizar en las Tiendas Oxxo a nivel nacional, con una vigencia de 48 horas para concretarla.
  * La referencia quedará ligada al número de caso
  * En la información mostrada en la referencia se encuentra la siguiente:
    * Número de referencia
    * Número de caso
    * Número de serie para cobro
    * Vigencia de la referencia

### Gestión de cuentas de usuario

Para poder realizar cualquier proceso dentro de la aplicación, se requiere la generación de una cuenta de usuario, para generar la misma se solicitará la siguiente información:

* Nombre de usuario - Texto 
* Correo electrónico - Texto de tipo email
* Password - Texto de tipo password con longitud mínima de 8 caracteres, y son el uso de mayúsculas, minúsculas, números y caracteres especiales.
* Confirmar Password - Texto de tipo password donde se deberá ingresar nuevamente el password para validad la captura correcta.

Para los usuarios clientes, se capturará esta información por ellos en un formulario dentro de la aplicación, para los usuarios abogados, se solicitará su creación al administrador de la aplicación.

### Seguimiento de demandas por usuario

Para dar seguimiento a las demandas, el sistema generará notificaciones a los usuarios clientes para informar sobre avances en el proceso, o requerimiento de información necesaria para continuación del proceso.

El usuario cliente podrá acceder a la aplicación con su cuenta, y podrá verificar el avance del proceso, o capturar la información que se le solicite para continuar con el mismo.

### Creación de documento Word con información de demanda

El sistema verificará de manera periódica las solicitudes de demanda en la que se ha realizado el pago, pero no se ha generado el documento inicial, para estos casos se generará una notificación para los usuarios abogados, y se generará un documento Worb basádo en plantillas definidas a partir del Motivo de la demanda especificado en el formulario de captura, y en secciones específicas de dicho documento se insertará la información capturada en el formulario.

### Gestión de notificaciones

La aplicación generará notificaciones por cada evento que genere un cambio en el estado, entre estos eventos se encuentran:

* Creación de nueva demanda - Se notificará a usuario abogado
* Registro de pago - Se notificará a usuario abogado
* Generación de documento de demanda - Se notificará a usuario  - Se notificará a usuario abogado
* Modificación en estado de demanda - Se notificará a usuario cliente
* Solicitud de carga de información extra - Se notificará a usuario cliente
* carga de información extra - Se notificará a usuario abogado

Estas notificaciones se realizarán vía correo electrónico

### Seguimiento de pagos

Se visualizará la información de los pagos realizados mostrando la siguiente información:

* ID de pago
* Caso relacionado
* Fecha de pago
* Tipo de pago (tarjeta o referencia)
* Nombre de usuario cliente
* Monto del pago

Esta información deberá contar con algún mecanismo para filtrar y/o agrupar por periodo de tiempo, cliente o tipo de pago.

### Actualización de demanda

Los usuarios abogado podrán realizar los siguientes procesos:

* Solicitud de carga de información complementaria para dar seguimiento al proceso
* Modificar el estado del proceso, mismo que se notificará al usuario cliente
* Solicitud de pago para seguimientos (honorarios, copias, procesos externos, etc)

### Diseño responsivo

El diseño de la aplicación se realizará con la metodología mobile first, para garantizar la usabilidad de la misma para todos los usuarios.

### Paleta de colores azul marino, blanco

La paleta de colores básica sera con los colores solicitados por el clientes, pero en la etapa de UI se definirán colores extra para resaltar elementos dentro de la aplicación.

