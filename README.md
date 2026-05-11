Laboratorio de Nivelación Intensiva
CASAS PUCLLA, Arvin Roberto  (80%)
HUAMAN RAMOS, Bryan Jefferson
HUAMANI ARONI, Josuey

Fase 1:
Modelo de negocio: B2C (Business to Consumer) — tienda electrónica directa al consumidor final especializada en productos de electrónica y tecnología.

Tecnología: Desarrollo a medida con Laravel (backend/API REST) + React (frontend SPA). Esta combinación es ideal porque ofrece control total del código, escalabilidad, separación de responsabilidades, y permite un catálogo de productos tecnológicos con filtros avanzados, comparadores y ficha técnica detallada que un CMS no facilita de forma nativa.

Repositorio: https://github.com/Audaxeff/Lab_ecommerce

Fase 2: Modelado del Negocio Digital

Requisitos funcionales — derivados del BMC
RF-01
Registro y autenticación de usuarios
Email, Google OAuth, recuperación de contraseña
Laravel Sanctum

RF-02
Catálogo de productos con filtros avanzados
Marca, precio, categoría, valoración, disponibilidad
React + Zustand

RF-03
Ficha técnica detallada de producto
Especificaciones, imágenes, reseñas
React Component

RF-04
Comparador de productos
Hasta 3 productos en paralelo con tabla de specs
React

RF-05
Carrito de compras y checkout
Persistente en sesión, cupones de descuento, resumen
Laravel API

RF-06
Pasarela de pagos integrada
Laravel Webhook

RF-07
Gestión de pedidos y seguimiento
Estados: pendiente → confirmado → enviado → entregado
SQL server

RF-08
Panel de administración (backoffice)
CRUD productos, categorías, usuarios, pedidos e inventario
Laravel Nova / Filament

RF-09
Sistema de reseñas y valoraciones
Rating 1–5 estrellas, comentarios verificados por compra
SQL server

RF-10
Notificaciones por email y sistema
Confirmación de orden, cambio de estado, ofertas
Laravel Mail / Queue

RF-11
Lista de deseos (wishlist)
Guardar productos, alerta de baja de precio
React + API

RF-12
Buscador con autocompletado
Búsqueda por nombre, modelo, SKU con sugerencias en tiempo real
Laravel Scout

Fase 3: Arquitectura de Información y Patrones

Sitemap

Nivel 1 — Público (morado): Home, Catálogo con filtros, Detalle de producto, Comparador, Nosotros/Contacto. Son accesibles sin autenticación.
Nivel 2 — Transaccional (verde): Carrito → Checkout → Confirmación de orden. Es el flujo de compra completo, requiere sesión activa para finalizar.
Nivel 3 — Área privada (coral): Login/Registro como puerta de entrada, luego Mi perfil, Mis pedidos e historial, y Direcciones guardadas.


Fase 4: Prototipado y validación
https://stitch.withgoogle.com/projects/966039075652087871
