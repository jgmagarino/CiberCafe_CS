# Proyecto: Simulación de Laboratorio de Computación

**Autor:** Jose Manuel Gomez Magariño

## Descripción del Proyecto

Este proyecto se propone desarrollar el backend de una problemática ficticia con el objetivo de mejorar mis conocimientos en C#. La problemática fue elaborada con la intención de utilizar Programación Orientada a Objetos (POO), bases de datos y servicios TCP o UDP, involucrando una conexión cliente-servidor para practicar la concurrencia y repasar los conocimientos adquiridos durante mis estudios de programación de sistemas.

## Problemática

En un laboratorio de computación se ofrecen diversos servicios a los usuarios, tales como Internet, Juego Offline, Juego Online e Impresión. Existen varios tipos de usuarios: el usuario común y los asociados.

### Tipos de Usuarios y Descuentos

- **Usuario común**
- **Usuarios asociados**: 
  - **Asociado Bronce**: Descuento del 5% en el costo de los servicios.
  - **Asociado Plata**: Descuento del 10% en el costo de los servicios.
  - **Asociado Oro**: Descuento del 30% en el costo de los servicios.

### Sistema de Puntos

Los usuarios asociados pueden ingresar dinero a cambio de puntos que se utilizarán para comprar más servicios. Los puntos de los asociados aumentan diariamente según la siguiente tasa de interés:
- **Bronce**: 0.15% por día
- **Plata**: 0.5% por día
- **Oro**: 0.6% por día

Cada dólar equivale a un punto. Los puntos pueden ser transferidos entre asociados con un descuento del 1% durante la transferencia. Además, por cada 200 puntos o dólares gastados en servicios, la tasa de interés aumenta un 0.01%.

### Servicios y Formas de Pago

Los usuarios pueden comprar distintos paquetes de tiempo determinado para acceder a los servicios:

- **Internet**:
  - 00:00:30 x $10 o 15 puntos
  - 00:01:00 x $15 o 22.5 puntos
  - 00:01:30 x $25 o 37.5 puntos
- **Juego Offline**:
  - 00:00:30 x $25 o 37.5 puntos
  - 00:01:00 x $40 o 60 puntos
  - 00:01:30 x $65 o 97.5 puntos
- **Juego Online**:
  - 00:00:30 x $35 o 52.5 puntos
  - 00:01:00 x $50 o 75 puntos
  - 00:01:30 x $75 o 112.5 puntos
- **Impresión**:
  - $10 o 15 puntos por hoja (200 palabras por hoja)
  - $0.5 o 0.75 puntos por palabra

### Registro de Usuarios

De todos los usuarios se registrará:
- Nombre de usuario: único para cada uno.
- Fecha de registro.
- Tiempo invertido en el laboratorio.
- Dinero invertido en el laboratorio.

De los usuarios asociados se registrará además:
- Categoría.
- Puntos.

### Requisitos para Ascender de Categoría

- **Bronce**:
  - Tiempo en laboratorio: 00:05:00
- **Plata**:
  - Tiempo en laboratorio: 00:10:00
- **Oro**:
  - Tiempo en laboratorio: 00:20:00
  - Dinero invertido: $1000 (los puntos también cuentan, dividiéndolos entre 1.5)

## Objetivo del Proyecto

El objetivo es crear un sistema que simule el laboratorio, con un servidor y varios clientes que representen las PC usadas por los usuarios. El servidor deberá comunicarse con las PC informando sobre el servicio que se brinda, el usuario que lo usa y por cuánto tiempo. Durante el uso de un servicio, el usuario podrá aumentar el tiempo comprando un paquete adicional del mismo servicio, y el servidor deberá enviar una señal al cliente para que aumente su tiempo.

Además, se deberá implementar un sistema para registrar a los usuarios y mantener un historial de los servicios usados y por quién.
