# Toma de Requerimientos

## 1. Problema
Una veterinaria en una zona rural tiene dificultades al momento de registrar atenciones medicas y controles, ademas no existe una documentacion de los animales que son atendidos.

## 2. Objetivo
Permitir agendar adecuadamente informacion medica de mascotas y animales, horarios y atenciones.

## 3. Alcance
- El programa debe poder responder adecuadamente a cada consulta.
Datos a tomar:
- Clientes: Nombres / appellidos / Fono / Email/ 
- Mascota: Nombre / Especie / Proxima Atencion/ 
- Ficha Medica: Tipo Atencion / Fecha / ID-Mascota / MedicoAcargo



## 4. Requerimientos Funcionales
Lista de funcionalidades que debe tener el sistema.

## 5. Requerimientos No Funcionales
Restricciones o características técnicas (rendimiento, seguridad, etc.).

## 6. Supuestos
Se asume que todos los usuarios tienes acceso a internet.
Los clientes pueden registrarse por si mismo o ser registrados por el personal.
se asume que la aplicacion sera utilizada solo por un solo usuario a la vez.
La aplicacion estara en español

## 7. Criterios de Aceptación
Condiciones mínimas para considerar que el requerimiento está completo.

## 8. Notas Adicionales
Cualquier otra información relevante.

## Usuarios-Roles
La aplicación tendra roles los cuales son: un SuperAdministrador, AdminMenor, Veterinario, y usuario(cliente dueño del animal). El SuperAdmin podra: Acceder a todos los permisos de la aplicacion;
Registrar nuevos pacientes(Mascotas) vinculados a sus respectivos dueños, ver y editar fichas, Gestionar horarios y disponibilidad de veterinarios, Bloquear y/o eliminar cuentas de usuarios. Tambien podra asignar o modificar roles a usuarios como por ejemplo quien podra acceder a las fichas medicas.

El AdminMenor podra: Ver y editar fichas medicas de medicas, Gestionar Horarios y disponibilidad de veterinarios, 

El Veterinario podra: Registrar, editar y eliminar fichas de pacientes, diagnosticos, tratamientos y vacunas. Consultar fichas medicas asignadas, ver su agenda 

El usuario(cliente) podra: Ver historial de sus mascotas(animales), Consultar proximas citas, vacunas e Informacion de sus mascotas(animales), solicitar nuevas citas, recibir notificaciones o recordatorios.