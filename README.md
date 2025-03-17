# Desafio1
Repositorio para el Desafio #1 EducacionIT-DevOps

## Objetivo:
Este desafío tiene como objetivo desarrollar un pipeline declarativo en Jenkins que nos permite
crear usuarios dentro de un sistema linux.

Escenario:
El área de seguridad cuenta con un equipo que tiene la responsabilidad de gestionar la
creación de usuarios y baja de usuarios en los sistemas de la empresa.
Debido a que en el último tiempo hubo muchos ingresos y algunos operadores cometieron
errores al dar de alta usuarios, nos encomendaron generar un job en jenkins que permita
generar estos usuarios.
Requisitos:
1. El operador de seguridad desea que el al momento de crear el usuario se tomen estos
datos de entrada:
Dato Descripción
Login Es un identificador único que se
compone del nombre y el
apellido
Nombre y Apellido Nombre y Apellido del usuario
Departamento Este es el grupo que
corresponde al área del usuario.
Estos grupos son contabilidad,
finanzas, tecnología.
2. Requiere que la automatización generé un password temporal que sea asignado al
usuario, que luego el usuario final deberá cambiar en el primer inicio de sesión.
3. El operador requiere que pueda obtener la password temporal para copiarla y enviarla
por email al usuario final.
Entregables:
Los entregables establecidos para este proyecto con:
1. Código fuente del pipeline de Jenkins publicado en un repositorio de Github.
2. Guía detallada de cómo utilizar el job publicada en el archivo README.md del
repositorio.
3. Evidencia de las pruebas con resultado exitoso.

### Guia detallada

Pre-requisitos
- Se debe tener instalado OpenSSL. Para instalar utilizar: sudo apt install openssl
- Se debe tener habilitado el usuario de Jenkins para realizar cambios. Para esto:
        - Vamos a editar el archivo sudoers: sudo visudo
        - Con nano o vi, vamos a agregar al final: jenkins ALL=(ALL) NOPASSWD: ALL
        - Guardar los cambios y salir.
- Los grupos seran previamente creados por el script.     
