## Endpoints

// 1. Listar productos por tag y precio
GET /api/products?tags=electronics&minPrice=50&maxPrice=500&sort=rating&page=1

// 2. Ver promociones activas hoy
GET /api/promotions/active

// 3. Historial de órdenes del usuario
GET /api/users/{userId}/orders?page=1&limit=10

// 4. Top productos por rating
GET /api/products/top?category=electronics&limit=10

// 5. Products de un merchant específico
GET /api/merchants/{merchantId}/products?status=active

// 6. Reviews de un producto
GET /api/products/{productId}/reviews?sort=helpful&page=1

// 7. Órdenes por estado para merchant
GET /api/merchants/{merchantId}/orders?status=processing

// 8. Búsqueda de productos
GET /api/products/search?q=laptop&category=electronics&merchantId=xxx

// 9. Dashboard del merchant
GET /api/merchants/{merchantId}/dashboard

// 10. Validar cupón
POST /api/promotions/validate
Body: { "code": "SUMMER20", "orderAmount": 150, "productIds": ["p1", "p2"] }
