🛠️ DroidAdopt — Plataforma de adopción de droides (MERN) DroidAdopt es una aplicación MERN donde los usuarios pueden explorar droides de Star Wars, solicitar su adopción mediante un workflow con estados, dejar reseñas, marcar favoritos y gestionar su perfil. Incluye autenticación JWT, subida de imágenes a Cloudinary y emails transaccionales con Nodemailer.

🚀 Tecnologías Backend: Node, Express, MongoDB/Mongoose, JWT, Nodemailer, Cloudinary Frontend: React, React Router, Axios Otros: Validación, middleware de errores, rutas protegidas

📦 Modelos principales User: datos, avatar, rol, verificación email

Droid: recurso principal (imagen, estado, categorías)

AdoptionRequest: solicitud con workflow (pending, approved, rejected, completed, cancelled)

Review: reseñas ligadas a adopciones completadas

Favorite: relación N‑N usuario ↔ droide

Message: mensajería entre usuario y admin

Notification: avisos de estado

Category: clasificación de droides

Relaciones: ✔ 1‑N (User→AdoptionRequest, Droid→Review…) ✔ N‑N (User ↔ Droid mediante Favorite)

🔐 Autenticación Registro + login con JWT

Verificación de email

Reset de contraseña

Roles: user y admin

Protección de recursos según rol y propiedad

📧 Emails Verificación de email

Recuperación de contraseña

Notificación de cambio de estado en adopciones

🖼️ Imágenes (Cloudinary) Subida desde React

Guardado de URL + cloudinaryId

Reemplazo de imagen al editar

🧠 Lógica de negocio Workflow de adopción multi‑paso

Un droide solo puede tener una adopción activa

Solo usuarios verificados pueden adoptar

Solo se puede reseñar una adopción completada

Favoritos únicos por usuario/droide

📡 API (resumen) Auth /auth/register, /auth/login, /auth/verify-email, /auth/forgot-password, /auth/reset-password

Droids CRUD + filtros, paginación y ordenación

Adoption Requests Crear, listar, cambiar estado, cancelar

Reviews Crear, listar por droide, borrar

Favorites Añadir, quitar, listar

🖥️ Frontend (React) Home con filtros y paginación

Detalle de droide

Registro/Login

Dashboard (user): adopciones, favoritos, reviews

Dashboard (admin): gestión de droides y adopciones

Formularios con subida de imagen

Rutas protegidas
