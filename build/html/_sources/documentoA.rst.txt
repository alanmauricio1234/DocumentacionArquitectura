**Sistema Uacemita's Candy**
*****************************

**Introducción**
================
1. **Introducción**

  - **Contexto de negocio**
  
    - **Antecedentes**
    
      En la tienda “Uacemita’s Candy” se dedica a vender dulces, y las ventas e inventario de estos productos se realiza de manera manual. Esto representa un problema debido a que el proceso de ventas e inventario se realiza de una manera más tardada. Es por esta razón que los socios desean exponer su catálogo de productos en un sistema que exponga el gestionamiento (altas, bajas y cambios) de los mismos a través de un servicio web para que sea consumido por una o varias aplicaciones.
      
    - **Fase del problema**  
      
      Los socios de la dulcería sólo llevan el control manual del inventario de los dulces que venden y que tienen a través de un cuaderno, y esto hace que ocurran errores a la hora de cuadrar los insumos reales con los que tienen anotados en la libreta.
      
    - **Objetivos del negocio** 
      
+------------+-----------------------------------------------------------------------------------------------------------+
| ID         | Descripción del objetivo del negocio                                                                      |
+============+===========================================================================================================+
| ON-01      | Hacer que las ventas aumenten 10%                                                                         |
+------------+-----------------------------------------------------------------------------------------------------------+
| ON-02      | Localizar los productos más vendidos para abarrotar la tienda con dicho producto                          |
+------------+-----------------------------------------------------------------------------------------------------------+
| ON-03      | Tener un control automatizado de productos existentes                                                     |
+------------+-----------------------------------------------------------------------------------------------------------+
| ON-05      | Sacar a venta los productos con fecha próxima a caducar.                                                  |
+------------+-----------------------------------------------------------------------------------------------------------+
| ON-06      | Identificar los productos con menos demanda para crear ofertas donde se puedan vender con mayor facilidad |
+------------+-----------------------------------------------------------------------------------------------------------+
| ON-07      | Restringir el acceso a la gestión de productos solo a personas autorizadas                                |
+------------+-----------------------------------------------------------------------------------------------------------+

2. **Visión de la solución** 

  - **Fase de visión** 
   
   En esta aplicación tiene los siguientes propósitos:   
   
     1. En principio, subir las ventas de dulces con la ayuda de la aplicación. 
     2. Llevar el control de los productos de una manera automatizada.
     3. Localizar de una manera ágil los productos con mayor demanda.
     4. Localizar de manera ágil los productos con menos demanda para crear ofertas.
        
        
  - **Características del sistema** 

+------------+------------------------------------------+--------------+-----------------------+
| ID         | Descripción                              | Prioridad    | Objetivos del negocio |
+============+==========================================+==============+=======================+
|CAR-01      |El sistema debe permitir                  | Alta         | ON-03                 |
|            |dar de alta nuevos productos al catálogo. |              |                       |
+------------+------------------------------------------+--------------+-----------------------+
|CAR-02      |El sistema debe permitir dar de baja un   | Alta         | ON-03                 |
|            |producto del catálogo.                    |              |                       |
+------------+------------------------------------------+--------------+-----------------------+
|CAR-03      |El sistema debe permitir consultar el     | Alta         | ON-03                 |
|            |catálogo de productos.                    |              |                       |
+------------+------------------------------------------+--------------+-----------------------+
|CAR-04      |El sistema debe permitir gestionar la     | Alta         | ON-02, ON-05 y        |
|            |venta de los productos.                   |              | ON-06                 |
+------------+------------------------------------------+--------------+-----------------------+
|CAR-05      |El sistema debe permitir modificar las    | Alta         | ON-03                 |
|            |caracterísiticas de los productos         |              |                       |
|            |disponibles                               |              |                       |
+------------+------------------------------------------+--------------+-----------------------+
|CAR-06      |El sistema debe permitir exponer          | Alta         | ON-03                 |
|            |microservicos para su consumo.            |              |                       |
+------------+------------------------------------------+--------------+-----------------------+
|CAR-07      |El sistema debe permitir registrar y      | Media        | ON-07                 |
|            |autentificarse a usuarios que administren |              |                       |
|            |la gestión de productos.                  |              |                       |
+------------+------------------------------------------+--------------+-----------------------+

3. **Alcance**
  
  Este proyecto consiste en crear un sistema que sea capaz de administrar y exponer los servicios de altas, bajas y cambios de productos. Este proyecto se realizará por dos desarrolladores, se planea concluir con la estructura e implementación arquitectónica para el 29 de diciembre del 2020  así como tener el sistema y documentación por completo.
  Para cubrir con los requisitos del sistema será necesario crear una aplicación web.  La funcionalidad principal de la aplicación es la de poder presentar al cliente las diferentes funciones que se tienen disponibles sobre los productos.


+-------------------+-------------------------------+---------------------------+
| Número de Entrega | Tema Principal                | ID de las características |
+===================+===============================+===========================+
| 1.0               |El gestionamiento de productos |CAR-01, CAR-02, CAR-03,    |
|                   |                               |CAR-04 Y CAR-05            |
+-------------------+-------------------------------+---------------------------+
| 2.0               |El exponer los servicios       |CAR-06 Y CAR-07            |
+-------------------+-------------------------------+---------------------------+

4. **Contexto del Sistema**

  - **Interesados** 

+------------+-----------------------+-----------------------------------+
| Nombre     | Descripción           | Responsabilidad                   |
+============+=======================+===================================+
|Sergio Mena |El administrador de    |Revisar cada uno de los            |
|            |proyecto               |entregables desde el inicio hacia  |
|            |                       |el final                           |
+------------+-----------------------+-----------------------------------+
|Esperanza   |Arquitecta de software,|Realizar el especificación,        |
|Romero      |desarrolladora y       |análisis, diseño de la app, diseño |
|Lobato      |analista               |de la arquitecura e implementación |
+------------+-----------------------+-----------------------------------+
|Alan M.     |Arquitecto de software,|Realizar el especificación,        |
|Medrano     |desarrollador y        |análisis, diseño de la app, diseño |
|Hernández   |analista               |de la arquitecura e implementación |
+------------+-----------------------+-----------------------------------+

  - **Diagrama de Contexto**
  
  .. figure:: _static/diagrama_contexto.png
     :align: center
     
  - **Entorno de Operación**
    
    El Cliente tendrá la posibilidad y facilidad de acceder a la aplicación desde cualquier navegador de internet, así como también contará con una base de datos en PostgreSQL y se ejecutará en un servidor web.

5. **Información Adicional**

  - **Herramientas**
  
    Las herramientas que se utilizaron
    
    - Spring tool Suite 4
    - Spring Boot 2.0
    - StarUml
    - Enterprise Architect 
    - Java openjdk 11.0.7 
    - Bootstrap 5
    - PostgreSQL 11
    - GitLab
    - Git


**Requerimientos de la Arquitectura**
======================================

  1. **Drivers Funcionales**

    Se consideraron estos drivers funcionales debido a que son las funcionalidades principales del sistema, las cuales nos ayudarán a alcanzar los objetivos de negocio planteados y cumplen con las caracterísiticas esenciales del sistema.
    
+----------+------------------------------------------------------------------------------------------------+-----------------------------+
| ID       | DESCRIPCIÓN                                                                                    | CARACTERÍSTICA ASOCIADA     |
+==========+================================================================================================+=============================+
|CU-01     |**Gestión de Productos**. El propietario o gerente de la tienda puede realizar altas, bajas     | CAR-01, CAR-02 Y CAR-05     |
|          |y cambios de productos.                                                                         |                             |
+----------+------------------------------------------------------------------------------------------------+-----------------------------+
|CU-02     |**Venta de Productos**. El cliente puede agregar productos que se encuentren disponibles a un   | CAR-03 Y CAR-04             |
|          |carrito de compra para que, posteriormente, se realice la venta.                                |                             |
+----------+------------------------------------------------------------------------------------------------+-----------------------------+
|CU-03     |**Registro**. El propietario realiza el registro de un gerente al sistema para que tenga acceso | CAR-07                      |
|          |a la gestión de productos.                                                                      |                             |
+----------+------------------------------------------------------------------------------------------------+-----------------------------+

    - **Modelo de casos de uso**
    
    .. figure:: _static/caso_de_uso.jpg
     :align: center
     
    - **Elección de casos de uso primarios**
    
      La razón de la elección de estos casos de uso primarios es que cumplen con las principales funcionalidades del sistema tal cual se describió anteriormente, estos casos de uso nos ayudarán a alcanzar los objetivos de negocio planteados al inicio del proyecto.

+----------+---------------+---------------------------------------------------------------------------------+
| ID       |  PRIORIDAD    |  JUSTIFICACIÓN                                                                  |
+==========+===============+=================================================================================+
| CU-01    | ALTA          |Es de prioridad alta debido a que el proceso de gestión de productos es          |
|          |               |fundamental para poder tener el catálogo en linea y ser consumido por el sistema |
|          |               |de ventas para que se puedan concretar ganancias con la tienda de dulces.        |
+----------+---------------+---------------------------------------------------------------------------------+
| CU-02    |  ALTA         |Es de prioridad alta debido a que el sistema de ventas en linea es que dejará    |
|          |               |ganacias a la tienda de dulces.                                                  |
+----------+---------------+---------------------------------------------------------------------------------+
| CU-03    |  MEDIA        |Es de prioridad media debido a que al inicio sólo tendrá acceso el propietario   |
|          |               |de la tienda de dulces a la gestión de productos.                                |
+----------+---------------+---------------------------------------------------------------------------------+

  2. **Drivers de atributos de calidad**  
   
   Los atributos de calidad que se muestran a continuación se obtuvieron utilizando, principalmente, dos métodos:
   
     - Goal Question Metric
     
     - Lista de Supuestos

+-------+------------------+-------------------------------------------------------------------------+----------------+
| ID    | CATEGORÍA        | ESCENARIO                                                               |PRIORIDAD       |
+=======+==================+=========================================================================+================+
| EC1   | Seguridad        |El dueño de la tienda de dulces desea incorporar a su sistema en         | ALTA           |
|       |                  |desarrollo un módulo de autentificación para realizar la gestión de sus  |                |
|       |                  |productos a el personal autorizado.                                      |                |
|       |                  |                                                                         |                |
|       |                  | - **Fuente**. El Propietario                                            |                |
|       |                  | - **Artefacto**. El sistema                                             |                |
|       |                  | - **Ambiente**. Etapa de desarrollo                                     |                |
|       |                  | - **Estímulo**. El dueño desea gestionar sus productos                  |                |
|       |                  | - **Medida de Respuesta**. Inmediata                                    |                |
|       |                  | - **Respuesta**. Dar acceso al módulo de gestión de productos           |                |
+-------+------------------+-------------------------------------------------------------------------+----------------+
| EC2   | Usabilidad       |El cliente hace una compra exitosa de los productos a través del sistema | ALTA           |
|       |                  |de compras de la tienda Uacemita’s Candy sin que el sistema muestre a lo |                |
|       |                  |más cuatro pantallas.                                                    |                |
|       |                  |                                                                         |                |
|       |                  | - **Fuente**. El Cliente                                                |                |
|       |                  | - **Artefacto**. El sistema de ventas                                   |                |
|       |                  | - **Ambiente**. Bajo condiciones normales                               |                |
|       |                  | - **Estímulo**. Compra exitosa                                          |                |
|       |                  | - **Medida de Respuesta**. Muestra a lo más cuatro pantallas            |                |
|       |                  | - **Respuesta**. Muestra que la compra fue realizada de forma exitosa   |                |
+-------+------------------+-------------------------------------------------------------------------+----------------+
| EC3   | Performance      |Si hay 100 clientes simultáneamente queriendo realizar una compra, el    | ALTA           |
|       |                  |de respuesta debería ser menor que un segundo bajo condiciones normales  |                |
|       |                  |                                                                         |                |
|       |                  | - **Fuente**. Los Clientes                                              |                |
|       |                  | - **Artefacto**. El sistema de ventas                                   |                |
|       |                  | - **Ambiente**. Bajo condiciones normales                               |                |
|       |                  | - **Estímulo**. 100 clientes simultáneos                                |                |
|       |                  | - **Medida de Respuesta**. Un segundo                                   |                |
|       |                  | - **Respuesta**. Los clientes realizan la compra                        |                |
+-------+------------------+-------------------------------------------------------------------------+----------------+
| EC4   | Disponibilidad   |El propietario requiere que el sistema de ventas esté disponible 99%     | ALTA           |
|       |                  |del año.                                                                 |                |
|       |                  |                                                                         |                |
|       |                  | - **Fuente**. El Propietario                                            |                |
|       |                  | - **Artefacto**. El sistema de ventas                                   |                |
|       |                  | - **Ambiente**. Bajo condiciones normales                               |                |
|       |                  | - **Estímulo**. Intentar acceder al sistema de ventas                   |                |
|       |                  | - **Medida de Respuesta**. Que esté disponible el 99% del año           |                |
|       |                  | - **Respuesta**. Acceder al sistema de ventas                           |                |
+-------+------------------+-------------------------------------------------------------------------+----------------+

  3. **Anexos**
  
    - **CU-1: Gestión de Productos**
    
      - **Resumen y Objetivos**
      
         Se realiza la alta, bajas y cambios de productos del catálogo de  la dulcería “Uacemita’s Candy”.
     
     -**Diagrama**
     
       .. figure:: _static/gestion_productos.jpg
        
      - **Actor/es**
      
        Propietario o Gerente de la tienda de dulces.
        
      - **Caso de uso relacionado**
      
        Ninguno.
        
      - **Precondiciones**
      
        1. Se debe contener la información del producto que se desea dar de alta, modificar o dar de baja.
        

       - **Secuencia**
       
         **Curso Principal: Alta de Producto**

+------+---------------------------------+---------------------------------------------------------+
| #    | Evento desencadenate            | Respuesta del sistema                                   |
+======+=================================+=========================================================+
| A1   |El propietario desea registrar   |Muestra los campos a ingresar para registrar un producto |
|      |un producto                      |                                                         |
+------+---------------------------------+---------------------------------------------------------+
| A2   |El propietario ingresa los       |Muestra un mensaje en pantalla y actualiza el catálogo   |
|      |campos y registra el producto    |de productos                                             |
+------+---------------------------------+---------------------------------------------------------+

         - **Postcondiciones**
      
          1. El sistema mostrará la actualización en el catálogo de productos que observa el consumidor.
          2. El sistema mandará un mensaje de que el producto se registró.


         - **Flujos Alternos**
         
           1. Modificar un producto
           2. Eliminar un producto


    - **CU-2: Venta de Productos**
    
      - **Resumen y Objetivos**
      
        Se realiza una venta de algún producto de la tienda de dulces “Uacemita’s Candy”.

      - **Diagrama**
        
          .. figure:: _static/venta_productos.jpg
        
      - **Actor/es**
      
        Cliente
        
      - **Caso de uso relacionado**
      
        Ninguno.
        
      - **Precondiciones**
      
        1. El consumidor tiene en mente los productos a comprar.
        

       - **Secuencia**
       
         **Curso Principal: Alta de Producto**

+------+---------------------------------+---------------------------------------------------------+
| #    | Evento desencadenate            | Respuesta del sistema                                   |
+======+=================================+=========================================================+
| A1   |El cliente desea comprar un      |Muestra el catálogo de productos.                        |
|      |producto                         |                                                         |
+------+---------------------------------+---------------------------------------------------------+
| A2   |Mientras el cliente agregue      |Actualiza la lista de productos del carrito e incrementa |
|      |productos                        |el total de la venta.                                    |
+------+---------------------------------+---------------------------------------------------------+
| A3   |Realiza la compra                |Muestra el total de los productos del carrito de compras |
|      |                                 |                                                         |
+------+---------------------------------+---------------------------------------------------------+

         - **Postcondiciones**
      
          1. Se muestra el total de la compra.


         - **Flujos Alternos**
         
           1. Eliminar un producto

    - **CU-3: Registrar**
    
      - **Resumen y Objetivos**
      
        Agregar al sistema un Administrador que tenga permisos de gestionar los productos de la dulcería "Uacemita Candy's"

      - **Diagrama**
      
        .. figure:: _static/registrar.jpg  
        
      - **Actor/es**
      
        Propietario/Gerente
        
      - **Caso de uso relacionado**
      
        Ninguno.
        
      - **Precondiciones**
      
        1. Ser el propietario o gerente de la tienda.
        

       - **Secuencia**
       
         **Curso Principal: Alta de Producto**

+------+---------------------------------+---------------------------------------------------------+
| #    | Evento desencadenate            | Respuesta del sistema                                   |
+======+=================================+=========================================================+
| A1   |El propietario o gerente         |Muestra los campos para registrar al nuevo administrador |
|      |requiere agregar un nuevo        |                                                         |
|      |administrador de productos       |                                                         |
+------+---------------------------------+---------------------------------------------------------+
| A2   |El propietario agrega los campos |Muestra que se registró el administrador                 |
|      |y registra al administrador      |                                                         |
+------+---------------------------------+---------------------------------------------------------+

         - **Postcondiciones**
      
          1. Se muestra que se registró el usuario.


         - **Flujos Alternos**
         
           1. Eliminar un administrador.
           
**Diseño de la Arquitectura**
================================

  Para el diseño de la arquitectura de software se eligió el modelo arquitectónico 4+1
  
  1. **Vista Lógica**
  
    En la vista lógica se realizaron los diagramas de clases y los diagramas de secuencia respectivos de la funcionalidad del sistema.
    
      - **Diagrama de Módulos**
        
        Se realizo un diagrama de módulos divido en dos partes, la primera que es la parte del sistema que ofrece el servicio
        (se encuentra pintado de verde) y el segunda parte es del sistema que lo comsume, en este caso es el que utilizará el 
        dueño debido que le permitirá la gestión de productos.
        
        .. figure:: _static/dg_modulos.png
        
      
      - **Diagrama de Objetos**
      
        Se realizaron dos diagramas de objetos. El primero es el diagrama de objetos del sistema que provee el microservicio,
        el segundo es el diagrama de objetos que se utilizará en el sistema de ventas.
        
          Digrama de objetos del sistema que provee el microservicio.
          
          
        .. figure:: _static/dg_objetos_micro.png
        
          Diagrama de objetos del sistema de ventas.
          
          
        .. figure:: _static/dg_objetos_ventas.png
        
        
  2. **Vista de Desarrollo**
  
    En la vista de desarrollo se realizó el diagrama de componentes y el diagrama de paquetes.
    
      - **Diagrama de Paquetes**
        
        En esta parte se muestran tres diagramas: el primero representa a la parte de los microservicios,
        el segundo a la parte de la venta de productos y el último para la gestión de productos.
        
        .. figure:: _static/dg_paquetes.png  
             
     
      - **Diagrama de Componentes**
      
        Se muestra el diagrama de componentes general del sistema.
        
        .. figure:: _static/dg_componentes.png
    
        
  3. **Vista de Proceso**
  
    Se realizaron dos diagramas de actividad. Las actividades plasmadas en los diagramas son las siguientes:
    gestión de productos y venta de productos.
    
      - **Diagrama de Actividad**
      
      .. figure:: _static/DA_Gestion_Productos.jpg
    
    
    
      .. figure:: _static/DA_ventas.jpg
    
    
  4. **Vista Física**
  
    En esta vista se incluye el diagrama de despliegue de la aplicación.
    
      - **Diagrama de Despliegue**  
      
      .. figure:: _static/dg_despliegue.png    

