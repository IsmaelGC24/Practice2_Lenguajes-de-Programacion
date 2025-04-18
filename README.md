Solution for Programming Languages ​​Practice 2. Created by: Ismael García Ceballos and Kevin Eduardo Hernández Durango.

Video link:

# Prolog Vehicle Catalog System

## Descripción del Proyecto

Este proyecto implementa un sistema en Prolog para la gestión y consulta del inventario de vehículos de un concesionario. Permite consultar vehículos por tipo, marca, presupuesto y generar reportes estructurados usando técnicas de recolección como `findall/3` y `bagof/3`.

El sistema aplica restricciones de presupuesto y asegura que el valor total del inventario mostrado no exceda ciertos límites predefinidos. También permite filtrar por marcas específicas y agrupar resultados por atributos como tipo o año.

## Características

- Definición de un catálogo de vehículos con marca, referencia, tipo, precio y año.
- Filtros por tipo de vehículo y presupuesto.
- Agrupación de vehículos por marca usando `findall/3`.
- Generación de reportes con valor total usando `generate_report/4`.
- Casos de prueba para validar el correcto funcionamiento.

## Medios utilizados

- SWISH (https://swish.swi-prolog.org/) para correr el código en línea.
