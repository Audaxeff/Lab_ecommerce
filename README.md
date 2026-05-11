# Projeto de laboratorio Final de Curso: 📚<br>
## FASE 1:<br>
Modelo de negocio: B2C (Business to Consumer) — tienda electrónica directa al consumidor final especializada en productos de electrónica y tecnología.<br>
Tecnología: Desarrollo a medida con Laravel (backend/API REST) + React (frontend SPA). Esta combinación es ideal porque ofrece control total del código, escalabilidad, separación de responsabilidades, y permite un catálogo de productos tecnológicos con filtros avanzados, comparadores y ficha técnica detallada que un CMS no facilita de forma nativa.

Repositorio: https://github.com/Audaxeff/Lab_ecommerce

## FASE 2: Modelado del Negocio Digital
<img width="1291" height="883" alt="2026-05-11-182345_hyprshot" src="https://github.com/user-attachments/assets/b8a52cc6-7ee9-4770-af44-690051b39df6" />

### Requisitos funcionales — derivados del BMC

- RF-01<br>
Registro y autenticación de usuarios
Email, Google OAuth, recuperación de contraseña<br>
_Laravel Sanctum_

- RF-02<br>
Catálogo de productos con filtros avanzados
Marca, precio, categoría, valoración, disponibilidad<br>
_React + Zustand_

- RF-03<br>
Ficha técnica detallada de producto
Especificaciones, imágenes, reseñas<br>
_React Component_

- RF-04<br>
Comparador de productos
Hasta 3 productos en paralelo con tabla de specs<br>
_React_

- RF-05<br>
Carrito de compras y checkout
Persistente en sesión, cupones de descuento, resumen<br>
_Laravel API_

- RF-06<br>
Pasarela de pagos integrada<br>
_Laravel Webhook_

- RF-07<br>
Gestión de pedidos y seguimiento
Estados: pendiente → confirmado → enviado → entregado<br>
_SQL server_

- RF-08<br>
Panel de administración (backoffice)
CRUD productos, categorías, usuarios, pedidos e inventario<br>
_Laravel Nova / Filament_

- RF-09<br>
Sistema de reseñas y valoraciones
Rating 1–5 estrellas, comentarios verificados por compra<br>
_SQL server_

- RF-10<br>
Notificaciones por email y sistema
Confirmación de orden, cambio de estado, ofertas<br>
_Laravel Mail / Queue_

- RF-11<br>
Lista de deseos (wishlist)
Guardar productos, alerta de baja de precio<br>
_React + API_

- RF-12<br>
Buscador con autocompletado
Búsqueda por nombre, modelo, SKU con sugerencias en tiempo real<br>
_Laravel Scout_

## FASE 3: Arquitectura de Información y Patrones

### Sitemap
<img width="1127" height="936" alt="2026-05-11-182405_hyprshot" src="https://github.com/user-attachments/assets/c62a8243-2ed3-408c-93bf-653d1682e933" />

Nivel 1 — Público (morado): Home, Catálogo con filtros, Detalle de producto, Comparador, Nosotros/Contacto. Son accesibles sin autenticación.

Nivel 2 — Transaccional (verde): Carrito → Checkout → Confirmación de orden. Es el flujo de compra completo, requiere sesión activa para finalizar.

Nivel 3 — Área privada (coral): Login/Registro como puerta de entrada, luego Mi perfil, Mis pedidos e historial, y Direcciones guardadas.

### lujograma de venta
<img width="689" height="981" alt="2026-05-11-182517_hyprshot" src="https://github.com/user-attachments/assets/b0d312a5-ac58-4f28-af65-b9fb8ccac610" />


## FASE 4: Prototipado y validación<br>
https://stitch.withgoogle.com/projects/966039075652087871
