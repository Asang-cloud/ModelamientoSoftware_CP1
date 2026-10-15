# ModelamientoSoftware_CP1
## Nombre del Estudiante
Asang Veloz Edson Andrés
## Caso de Estudio
Plataforma de reservas y check-in de la cadena hotelera TravelNow Área: turismo y servicios de alojamiento.
## Descripción Breve del Sistema
TravelNow necesita una plataforma para que los huéspedes reserven alojamiento y gestionen su estadía antes de llegar. El cliente consulta la disponibilidad por ciudad y fechas, elige una alternativa y realiza la reserva. El sistema registra sus datos, vuelve a comprobar la disponibilidad, calcula el valor total y procesa el pago mediante una pasarela de pagos externa. Cuando el pago se aprueba, la reserva se confirma y se notifica al cliente con un servicio externo de correo electrónico.
Antes de la estadía, el cliente puede modificar o cancelar la reserva y realizar el pre check-in, con la opción de pedir servicios adicionales (desayuno, traslado al aeropuerto). Los empleados consultan las reservas y actualizan su estado, y el supervisor además autoriza las modificaciones que exceden las condiciones normales.
### Reglas de negocio principales
* La reserva solo se confirma cuando el pago es aprobado.
* La disponibilidad se comprueba otra vez al confirmar; si la última habitación ya fue asignada, se pide una nueva selección.
* Modificar o cancelar solo procede antes de la estadía y dentro de las condiciones definidas.
* Las modificaciones excepcionales requieren autorización del supervisor.

| N° | Diagrama | Trabajo | Representa |
| --- | --- | --- | --- |
| 1 | Casos de uso | TPE1 – Modelado de comportamiento mediante casos de uso | 5 actores (3 primarios y 2 secundarios externos) y 14 casos de uso, con 5 <<include>>, 2 <<extend>> y la generalización Supervisor -> Empleado |
| 2 | Comunicación | TPE2 – Diagrama de comunicación y diagrama de secuencia | Colaboración entre Cliente, :SistemaTravelNow, :PasarelaPagos y :ServicioCorreoElectronico en el CU-02 Realizar reserva, con mensajes numerados |
| 3 | Secuencia | TPE2 – Diagrama de comunicación y diagrama de secuencia | El mismo escenario del CU-02 ordenado en el tiempo, de solicitarReserva() a reservaConfirmada.|

**Cómo se relacionan:** el diagrama de casos de uso (TPE1) define qué hace el sistema. En el TPE2 se tomó su caso principal, CU-02 Realizar reserva, y se modeló cómo se ejecuta. Los casos incluidos del TPE1 (registrar datos, comprobar disponibilidad, calcular valor total, procesar pago y enviar notificación) aparecen como mensajes en los dos diagramas de interacción. Ambos describen el mismo comportamiento: el de secuencia muestra el cuándo y el de comunicación el quién con quién.  
### Organización del repositorio
ModelamientoSoftware_CP1/  
├── TPE1/  
│   ├── Diagrama de caso de uso.png  
│   └── Archivo editable de los diagramas.md  
├── TPE2/  
│   ├── Diagrama de Comunicacion.png  
│   ├── Diagrama de Secuencia.png  
│   └── Archivo editable de los diagramas.md  
└── README.md  
