# Hospital Sale Sano

* PRODUCTO DE UN ERROR NO DETECTADO AL 3/2/2025 LA PANTALLA SE MUESTRA EN BLANCO *

Es un sitio web de presentación de los servicios y personal médico de un hospital ficticio. Este proyecto utiliza: React y Vite para construir una aplicación web moderna, modular y eficiente. Está diseñado con una estructura escalable, utilizando estilos SCSS y enrutamiento manejado con React Router.

## Tecnologías utilizadas

- React
- Vite
- React Router
- SCSS
- Bootstrap

## Actualizaciones:

1. **Lectura de información de doctores desde una base de datos con una API simulada**:
   - La información de los doctores se encuentra en `db.json`.
   - Las peticiones de la API utilizan Fetch API en `MedicosList.jsx` con `fetchMedicos` y `fetchServices`. En `Equipo.jsx` se utiliza el contexto `DoctorContext`, implementando Fetch API para obtener la lista de doctores. En `App.jsx` se utiliza para obtener la lista de médicos. Se utilizó Fetch API en vez de Axios ya que el primero funciona de forma nativa en el navegador, sin necesidad de instalaciones adicionales. Además, Fetch API tiene una interfaz más simple y utiliza promesas, lo que facilita las operaciones asíncronas y manejo de errores.

2. **Capacidad de interacción con la base de datos**:
   - Se le entrega al usuario la capacidad de relacionarse con la base de datos a través de la API con las opciones de visualización de información del equipo como tarjetas, tabla y actualización de la información.

3. **Implementación de seguridad en el consumo de APIs utilizando una API Key y JWT**:
   - Los datos sensibles (como la información de pacientes o citas) son accesibles solo si el usuario ha iniciado sesión y tiene un JWT válido.
   - Se muestra un mensaje de error si el token no es válido o ha expirado, y se redirige al usuario a la página de inicio de sesión.

4. **Medidas de seguridad implementadas para prevenir ataques comunes**:
   - Clickjacking: La aplicación está protegida para que no pueda ser incrustada en iframes no autorizados.
   - XSS (Cross-Site Scripting): Se escapa o limpia cualquier entrada del usuario que pueda inyectar código malicioso.
   - SQL Injection: Las solicitudes a la API están protegidas contra inyecciones de SQL.
   - Ataque DoS: Se implementaron mecanismos para mitigar posibles ataques de denegación de servicio.

5. **Encriptación de datos en el front-end**:
   - Utiliza técnicas de encriptación de datos para proteger la información sensible en el front-end, como las contraseñas de los usuarios o los datos personales de los pacientes.
   - Asegúrate de que los datos se encripten antes de ser enviados a la API.

## Descripción de páginas y funcionalidades:

- **Inicio (index.jsx)**: Página de bienvenida, mostrando la misión, visión, servicios y testimonios con la intención de generar confianza en nuevos posibles pacientes.
- **Equipo médico (equipo.jsx)**: Sección para mostrar la información de los especialistas que trabajan en el hospital.
- **Contacto (contacto.jsx)**: Página de contacto para que el usuario envíe un mensaje a través de un formulario y vea en un mapa la ubicación del hospital.
- **Reserva de hora (Reservar.jsx)**: Formulario para reservar citas médicas.

## Créditos

Para los elementos gráficos no se utilizaron imágenes cargadas como archivos en la carpeta del proyecto, sino que están conectadas a links de internet.

- **Íconos**: Íconos de servicios y redes sociales fueron tomados de:
  - Iconfinder
  - DuckDuckGo
  - Vecteezy
- **Imágenes**: Las imágenes de perfil de los doctores y el logo fueron obtenidos de:
  - SonicSEO
  - Public Domain Pictures
  - Stockvault

## Estructura del Proyecto

```
📦hospital
 ┣ 📂public
 ┃ ┗ 📜vite.svg
 ┣ 📂src
 ┃ ┣ 📂assets
 ┃ ┃ ┗ 📜react.svg
 ┃ ┣ 📂components
 ┃ ┃ ┣ 📜AppointmentForm.jsx
 ┃ ┃ ┣ 📜Contacto.jsx
 ┃ ┃ ┣ 📜DoctorCard.jsx
 ┃ ┃ ┣ 📜Equipo.jsx
 ┃ ┃ ┣ 📜Footer.jsx
 ┃ ┃ ┣ 📜Header.jsx
 ┃ ┃ ┣ 📜Home.jsx
 ┃ ┃ ┣ 📜MedicosList.jsx
 ┃ ┃ ┣ 📜Reservar.jsx
 ┃ ┃ ┗ 📜ServiceList.jsx
 ┃ ┣ 📂styles
 ┃ ┃ ┣ 📂abstracts
 ┃ ┃ ┃ ┣ 📜_bootstrap-override.scss
 ┃ ┃ ┃ ┣ 📜_breakpoints.scss
 ┃ ┃ ┃ ┣ 📜_functions.scss
 ┃ ┃ ┃ ┣ 📜_mixins.scss
 ┃ ┃ ┃ ┗ 📜_variables.scss
 ┃ ┃ ┣ 📂base
 ┃ ┃ ┃ ┣ 📜_base.scss
 ┃ ┃ ┃ ┣ 📜_resets.scss
 ┃ ┃ ┃ ┗ 📜_typography.scss
 ┃ ┃ ┣ 📂components
 ┃ ┃ ┃ ┣ 📜_button.scss
 ┃ ┃ ┃ ┣ 📜_footer.scss
 ┃ ┃ ┃ ┗ 📜_header.scss
 ┃ ┃ ┣ 📂layout
 ┃ ┃ ┃ ┣ 📜_footer.scss
 ┃ ┃ ┃ ┣ 📜_grid.scss
 ┃ ┃ ┃ ┗ 📜_header.scss
 ┃ ┃ ┣ 📂pages
 ┃ ┃ ┃ ┣ 📜_contacto.scss
 ┃ ┃ ┃ ┣ 📜_equipo.scss
 ┃ ┃ ┃ ┗ 📜_home.scss
 ┃ ┃ ┣ 📂partials
 ┃ ┃ ┃ ┗ 📜_breakpoints.scss
 ┃ ┃ ┣ 📂vendors
 ┃ ┃ ┃ ┗ 📜_bootstrap.scss
 ┃ ┃ ┣ 📜main.css
 ┃ ┃ ┣ 📜main.css.map
 ┃ ┃ ┗ 📜main.scss
 ┃ ┣ 📜App.css
 ┃ ┣ 📜App.jsx
 ┃ ┣ 📜index.css
 ┃ ┗ 📜main.jsx
 ┣ 📂styles
 ┃ ┗ 📜main.css
 ┣ 📜.gitignore
 ┣ 📜eslint.config.js
 ┣ 📜index.html
 ┣ 📜package-lock.json
 ┣ 📜package.json
 ┗ 📜README.md
```

