#  Documento de Requerimientos — API Veterinaria 2.0


## 1. Información General
- **Nombre del Proyecto:** API_Veterinaria2.0  
- **Cliente / Empresa:** Veterinaria  

---

## 2. Problemática Principal
Una veterinaria, ubicada en una zona rural, actualmente registra las atenciones de forma manual (en papel), lo que provoca pérdida y duplicación de datos.  
Además, las fichas médicas son responsabilidad de los clientes, por lo que no existe un respaldo en caso de extravío.

---

## 3. Objetivo / Descripción del Caso
Desarrollar un **Programa** que permita:
- Gestionar el **registro de animales atendidos**.  
- Visualizar la **ficha médica** con las atenciones realizadas.  
- Registrar **antecedentes, controles próximos y consultas**.  
- Restringir el acceso y las funciones según el **tipo de usuario**.  
- Registrar **clientes** y consultar el **estado de los animales**.

> **Nota:** Este sistema **no manejará facturas ni boletas**, se limita al **manejo de información médica y de clientes**.

---

## 4. Alcance y Tipos de Usuarios

###  Usuario Admin
- Dominio total del sistema.  
- Puede **agregar, actualizar y eliminar** información o registros de:
  - Veterinarios  
  - Fichas de animales  
  - Consultas
  - Dueños  

###  Usuario Veterinario
- Puede **agregar, actualizar y eliminar** registros de:
  - Fichas de animales  
  - Consultas
  - Dueños  

###  Usuario Cliente
- Solo puede **consultar** y **acceder** a la información de la ficha médica y consultas de sus animales.  

---

## 5. Reglas de Negocio Críticas

### A. Relación entre Animales y Dueños
- Cada animal debe estar **asociado a un único dueño registrado** en el sistema.  
- No se puede eliminar la ficha de un animal si tiene **consultas, vacunas o tratamientos asociados**.  
- Si el dueño cambia (por adopción o traspaso), el sistema debe permitir **reasignar al animal sin perder su historial**.  
- Un mismo dueño puede tener **varias mascotas** y debe poder consultarlas desde su perfil.  
- No se puede registrar un animal sin **un dueño o propietario**.  
- Es **obligatorio** que el cliente proporcione **dirección** y **número de contacto**. 
- Si el tratamiento termina, el sistema debe **permitir marcarlo como “finalizado”**, sin perder el registro histórico. 
- 

### B. Fichas Médicas y Consultas
- Cada paciente debe tener **una única ficha médica principal** con un **número de historia clínica único**.  
- No se puede registrar una nueva ficha médica para un paciente ya existente (**evitar duplicados**).  
- Toda ficha médica debe incluir **al menos una consulta inicial** antes de ser marcada como “activa”.  
- Las fichas deben registrar **fecha, hora de creación** y **profesional responsable**.  
- Las fichas médicas **no pueden eliminarse**, solo **marcarse como “inactivas”** por el veterinario.  

- Una consulta **no puede registrarse** si el paciente no tiene ficha médica activa.

- Toda consulta debe incluir **motivo, diagnóstico y tratamiento** antes de ser guardada.

### C. Seguridad y Control
- Cada usuario debe autenticarse con **usuario y contraseña únicos**.  
- Los tipos de usuario deben tener **distintos niveles de permisos** dentro del sistema.  


---

## 6. Funcionalidades Principales (MVP)

- **Ingresar, modificar y eliminar** datos de los animales:
  - ID.Chip | Nombre | Especie | Raza | Sexo | Edad |
Esterilización | Peso | Dueño

- **Ingresar, modificar y eliminar** fichas medicas o antecedentes:
  - Vacunas (Fecha / TipoVacuna) | 
Desparasitaciones (TipoDespa / NomProd / Fecha)
| Alergias | Cirugías | Enfermedades | Tratamientos | HistorialRepro

- **Ingresar, modificar y eliminar** consultas o atenciones:
  - MotivoConsulta | DetalleExamen | Diagnóstico |
Pruebas (radiografía / ecografía)
Tratamiento (medicación / dosis)
DatoRecomendación | FechaPróximoControl

- **Ingresar, modificar y eliminar** datos de los propietarios o dueños:
  - Nombre Completo | Dirección | Teléfono | Email | Animales


- **Visualizar y consultar** datos de fichas y mascotas.

---

## 7. Requisitos No Funcionales
- **Control de acceso** para todos los tipos de usuarios.  
- **Seguridad y protección de datos.**  
- **Rendimiento:** respuesta rápida ante consultas.  
- **Usabilidad:** interfaz intuitiva, clara y fácil de usar. 
>>>>>>> feature/requerimientos-FCheck
