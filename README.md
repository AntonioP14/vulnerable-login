# Vulnerable Login Application

## Descripción
Esta es una aplicación web simple de inicio de sesión con varias vulnerabilidades de seguridad comunes. Este repositorio contiene las correcciones a estas vulnerabilidades siguiendo las mejores prácticas de seguridad de OWASP Top Ten.

## Rama Principal (`main`)
La rama principal contiene el código original antes de aplicar las correcciones.

## Rama de Desarrollo (`develop`)
La rama de desarrollo (`develop`) se creó para gestionar el flujo de trabajo de desarrollo y la integración de las correcciones de seguridad.

## Ramas de Características
Cada vulnerabilidad se aborda en su propia rama de características:
- `feature/fix-xss` para la corrección de XSS.
- `feature/fix-sql-injection` para la corrección de inyección SQL.
- `feature/fix-authentication` para la corrección de problemas de autenticación.
- `feature/fix-localstorage` para la corrección de almacenamiento inseguro en localStorage.

Cada rama de características se fusiona en `develop` y luego en `main` una vez que se validan las correcciones.

## Cómo Corregimos las Vulnerabilidades
Las explicaciones de cada corrección se detallan a continuación:

### 1. XSS (Cross-Site Scripting)
- **Problema**: El código original permitía la inyección de scripts en la salida HTML.
- **Solución**: Usamos funciones de escape de caracteres y sanitización de entradas para evitar la inyección de scripts.

### 2. SQL Injection
- **Problema**: El código original tenía vulnerabilidades de inyección SQL.
- **Solución**: Utilizamos consultas parametrizadas para prevenir inyección SQL.

### 3. Autenticación
- **Problema**: Las credenciales se almacenaban en localStorage de manera insegura.
- **Solución**: Implementamos almacenamiento seguro y métodos de autenticación adecuados.

### 4. Almacenamiento Inseguro
- **Problema**: Las credenciales de usuario se almacenaban en localStorage.
- **Solución**: Eliminamos el uso de localStorage para almacenar credenciales y utilizamos cookies seguras o tokens de sesión.

## Cómo Ejecutar el Proyecto
1. Clona el repositorio.
2. Instala las dependencias necesarias.
3. Ejecuta la aplicación en un servidor local.

## Contribuciones
Las contribuciones son bienvenidas. Por favor, abre un `issue` o un `pull request` para cualquier mejora o corrección adicional.