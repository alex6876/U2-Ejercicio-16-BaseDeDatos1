# Base de Datos de Gestión Inmobiliaria (Alquiler de Propiedades)



Proyecto enfocado en la modelación Entidad-Relación (DER / MER) e implementación de base de datos relacional para un sistema de gestión inmobiliaria, administrando propietarios, inquilinos, propiedades, contratos de alquiler, pagos periódicos y empleados/agentes intervinientes.

---

## Descripción

El sistema modela una estructura de datos relacional para la administración integral de alquileres en bienes raíces. Permite registrar la información de los propietarios y las propiedades del catálogo, administrar la información de los inquilinos, formalizar los contratos de alquiler gestionados por los empleados de la inmobiliaria, y controlar el historial de pagos efectuados por cada contrato.

---

## Funcionalidades e Implementación

### Entidades y Atributos

* Propietario:


* id_CUIT_DNI: Clave primaria única identificadora del propietario.


* nombre: Nombre del propietario.


* apellido: Apellido del propietario.


* teléfono: Número telefónico de contacto.


* correo electronico: Dirección de correo electrónico de contacto.




* Inquilino:


* id_CUIT_DNI1: Clave primaria única identificadora del inquilino.


* nombre: Nombre del inquilino.


* apellido: Apellido del inquilino.


* teléfono: Número telefónico de contacto.


* correo electronico: Dirección de correo electrónico.




* Empleado:


* id_ampliado: Clave primaria única identificadora del empleado/agente inmobiliario.


* nombre: Nombre del empleado.


* apellido: Apellido del empleado.


* teléfono: Número de contacto del empleado.


* correo electronico: Dirección de correo institucional o de contacto.




* Propiedad:


* id_codigo catastral: Clave primaria única identificadora de la propiedad.


* dirección: Ubicación o domicilio del inmueble.


* ciudad: Ciudad donde se localiza el inmueble.


* tipo de propiedad: Clasificación del inmueble (ej. departamento, casa, local commercial).


* superficie: Superficie total o cubierta del inmueble.


* cantidad de ambientes: Número de ambientes del inmueble.


* precio de tasa: Valor o monto de impuestos/tasas asociadas.


* precio alquiler: Valor de alquiler publicado o base.




* Contrato:


* id_Contrato: Clave primaria única del contrato de alquiler.


* fecha inicio: Fecha de comienzo de vigencia del contrato.


* fecha finalización: Fecha de término del contrato.


* monto mensual: Canon locativo o alquiler pactado mensualmente.


* deposito garantia: Monto entregado en concepto de depósito en garantía.


* modalidad alquiler: Términos o condiciones específicas del acuerdo.




* Pago:


* id_pago: Clave primaria única del registro de pago.


* periodo abonado: Período correspondiente al pago (ej. mes/año).


* fecha efectiva: Fecha en que se concretó la transacción.


* monto abonado: Importe abonado.


* medio de pago: Forma o canal de pago utilizado (ej. transferencia, efectivo).


* recargo por demora: Monto cobrado por penalización de mora o retraso.





---

## Relaciones del Modelo

1. Propietario ↔ Propiedad (Relación 1:N):


* Un propietario puede poseer una o más propiedades registradas en el catálogo, pero cada propiedad pertenece a un único propietario titular.




2. Inquilino ↔ Contrato (Relación 1:N):


* Un inquilino puede firmar uno o varios contratos de alquiler a lo largo del tiempo, pero cada contrato individual se celebra con un inquilino titular.




3. Propiedad ↔ Contrato (Relación 1:N):


* Una propiedad puede ser objeto de múltiples contratos de alquiler en distintos periodos de tiempo, pero cada contrato corresponde a una única propiedad.




4. Empleado ↔ Contrato (Relación 1:N):


* Un empleado/agente inmobiliario puede gestionar o intermediar en múltiples contratos de alquiler.




5. Contrato ↔ Pago (Relación 1:N):


* Un contrato de alquiler genera una serie de pagos periódicos (cuotas/mensualidades), pero cada pago queda imputado a un único contrato.
