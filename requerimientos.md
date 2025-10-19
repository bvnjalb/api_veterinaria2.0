# Toma de Requerimientos

## 1. Problema
Una veterinaria en una zona rural tiene dificultades para registrar atenciones médicas y controles, ademas no existe una documentación de los animales que son atendidos,lo que complica el seguimiento de tratamientos y diagnósticos.

## 2. Objetivo
Diseñar un sistema que permita agendar, registrar y consultar información médica de mascotas y animales, incluyendo horarios, atenciones, fichas clínicas y roles de usuario diferenciados.

## 3. Alcance

### El sistema debe permitir:
- Registro y gestión de clientes, mascotas, fichas médicas y citas.
- Acceso diferenciado según el rol del usuario.
- Visualización y modificación de disponibilidad de atención.
- Envío de notificaciones

### Datos a tomar:
- Clientes: Nombres / apellidos / Fono / Email/ 
- Mascota: Nombre / Especie / Proxima Atencion/ 
- Ficha Medica: Tipo Atención / Fecha / ID-Mascota / MedicoAcargo.

## 4. Requerimientos Funcionales

### Gestion de Usuarios:
- Registro e inicio de sesión para tres tipos de usuario: clientes, veterinarios y administradores.
- Acceso diferenciado según el rol asignado.
- Los clientes pueden registrar mascotas.
- Los veterinarios pueden gestionar fichas clínicas y atender consultas.
- Los administradores tienen acceso total al sistema.

    ### Registro y gestión de mascotas y animales:
- Los veterinarios pueden registrar mascotas y animales, ingresando nombre, especie, raza y peso.
- Cada mascota queda asociada a su dueño en el sistema.
- La información registrada permite realizar diagnósticos y aplicar tratamientos adecuados.

    ### Gestión de citas:
- Visualización de disponibilidad por parte del cliente.
- Confirmación, modificación y cancelación de citas.
- Envío de notificaciones por correo electrónico o dentro del sistema.

    ### Fichas clínicas:
- Registro de síntomas, diagnóstico médico y tratamiento.
- Acceso a fichas clínicas según el rol del usuario.
- Edición y seguimiento de fichas por parte del veterinario



## 5. Requerimientos No Funcionales
- Seguridad: Autenticación segura, encriptación de datos sensibles.

- Rendimiento: El sistema debe responder en menos de 2 segundos por operación.

- Escalabilidad: Capacidad de agregar más usuarios y funcionalidades en el futuro.

- Usabilidad: Interfaz intuitiva y accesible para usuarios no técnicos.

- Compatibilidad: Funcional en navegadores modernos y dispositivos móviles.


## 6. Supuestos
- Se cuenta con conexión a internet en la veterinaria.
- Los usuarios tienen conocimientos básicos de informática.
- El sistema será utilizado principalmente en horario laboral.
- Los datos ingresados por los usuarios son verídicos y actualizados.

## 7. Criterios de Aceptación
- El sistema permite registrar y consultar fichas médicas por mascota.
- Los usuarios pueden iniciar sesión y acceder solo a sus funcionalidades.
- Las citas pueden ser agendadas, modificadas y canceladas correctamente.
- Las notificaciones se envían al menos 24 horas antes de la cita.
- El historial médico está disponible para cada mascota.

## 8. Notas Adicionales
- Se sugiere implementar copias de seguridad automáticas.
- El sistema debe permitir exportar fichas médicas en formato PDF.
- Se recomienda incluir un módulo de estadísticas básicas (atenciones por mes, especies más atendidas, etc.).


## 9. Usuarios-Roles

### SuperAdministrador: 
Acceso total: gestión de usuarios, roles, fichas médicas, horarios, bloqueo de cuentas.

### Administrador Menor:
Ver y editar fichas médicas, gestionar horarios y disponibilidad de veterinarios.

### Veterinario:
Registrar, editar y eliminar fichas médicas, diagnósticos, tratamientos y vacunas. Consultar agenda.

### Cliente (Dueño):
Ver historial médico de sus mascotas, consultar próximas citas y vacunas, solicitar nuevas citas, recibir notificaciones.

### Restricciones por rol:
Indica qué no puede hacer cada rol. Ejemplo:
- El cliente no puede ver fichas médicas de otras mascotas.
- El veterinario no puede modificar roles ni eliminar usuarios.
- El administrador menor no puede asignar roles ni bloquear cuentas.

### Validaciones de acceso:
- Cada usuario debe iniciar sesión con credenciales válidas.
- El sistema debe validar el rol antes de permitir acceso a funciones específicas.
- Las acciones sensibles (como eliminar fichas o usuarios) deben requerir permisos elevados.

### Asignación y modificación de roles:
- Solo el SuperAdministrador puede asignar o cambiar roles.
- El sistema debe registrar quién hizo el cambio y cuándo.

## 10. Accesibilidad y Soporte

- El sistema debe ser usable por personas con visión reducida (uso de contraste y tamaño de fuente ajustable).  
- Se incluirá una sección de ayuda o preguntas frecuentes.  
- El sistema debe mostrar mensajes claros ante errores o validaciones fallidas.

## 11. Validaciones

 ### Usuarios:
- El correo electrónico debe tener formato válido (ej: usuario@dominio.com).
- La contraseña debe tener al menos 8 caracteres, incluyendo una mayúscula y un número.
- No se permite registrar dos usuarios con el mismo correo.
- Validación de credenciales en el inicio de sesión.

### Mascotas:
- El nombre no puede estar vacío.
- La especie debe seleccionarse de una lista predefinida.
- El peso debe ser un número positivo.
- No se permite registrar una mascota sin dueño asignado.

### Citas:
- La fecha seleccionada debe estar disponible y dentro del horario laboral.
- No se permite agendar citas en horarios ocupados.
- Validación de que el veterinario esté disponible en ese horario.
- Confirmación obligatoria antes de modificar o cancelar una cita.

### Fichas clínicas:
- Todos los campos deben estar completos antes de guardar.
- Diagnóstico y tratamiento deben tener mínimo 10 caracteres.
- No se permite editar fichas médicas cerradas o archivadas.
- Solo usuarios con rol autorizado pueden acceder o modificar fichas.

### General:
- Todos los formularios deben tener validación en tiempo real.
- Los campos obligatorios deben estar marcados visualmente.
- El sistema debe mostrar mensajes claros ante errores o datos inválidos.

