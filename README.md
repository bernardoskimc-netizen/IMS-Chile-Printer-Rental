# 🖨️ IMS Chile - Plataforma de Arriendo de Impresoras

![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![Node](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen.svg)

Plataforma profesional y moderna para la gestión integral del arriendo de impresoras Xerox & Kyocera. Incluye cotizador inteligente, panel administrativo, integración de ventas y más.

## ✨ Características Principales

### 🎯 Frontend
- ✅ Interfaz moderna y responsiva con React 18 + TypeScript
- ✅ Sistema de componentes reutilizables
- ✅ Cotizador inteligente con IA
- ✅ Carrito de cotización persistente
- ✅ Historial de cotizaciones
- ✅ Búsqueda y filtrado avanzado
- ✅ Generación de PDFs
- ✅ Modo claro/oscuro

### 🔧 Backend
- ✅ API REST con autenticación JWT
- ✅ Gestión completa de inventario
- ✅ Sistema de cotizaciones con seguimiento
- ✅ Integración Nodemailer (envío de PDFs)
- ✅ Webhooks WhatsApp Business API
- ✅ Dashboard analítico
- ✅ Validación y seguridad robusta

### 💾 Base de Datos
- ✅ MongoDB con Mongoose ODM
- ✅ Modelos documentales optimizados
- ✅ Indexación inteligente
- ✅ Auditoría de cambios

### 🛠️ DevOps
- ✅ Docker + Docker Compose
- ✅ GitHub Actions CI/CD
- ✅ Variables de entorno seguros
- ✅ Documentación Swagger API

## 📁 Estructura del Proyecto

```
.
├── packages/
│   ├── frontend/          # React + TypeScript
│   │   ├── src/
│   │   │   ├── components/
│   │   │   ├── pages/
│   │   │   ├── services/
│   │   │   ├── store/
│   │   │   ├── styles/
│   │   │   └── App.tsx
│   │   └── package.json
│   └── backend/           # Node.js + Express
│       ├── src/
│       │   ├── api/
│       │   ├── models/
│       │   ├── middleware/
│       │   ├── services/
│       │   ├── utils/
│       │   └── server.ts
│       └── package.json
├── docker-compose.yml
├── .github/
│   └── workflows/
│       ├── ci.yml
│       └── deploy.yml
└── README.md
```

## 🚀 Instalación Rápida

### Prerequisitos
- Node.js >= 18.0.0
- Docker & Docker Compose
- MongoDB Atlas o instancia local

### Setup Local

```bash
# Clonar repositorio
git clone https://github.com/tu-usuario/IMS-Chile-Printer-Rental.git
cd IMS-Chile-Printer-Rental

# Instalar dependencias
npm install

# Configurar variables de entorno
cp packages/frontend/.env.example packages/frontend/.env.local
cp packages/backend/.env.example packages/backend/.env

# Iniciar con Docker
docker-compose up -d

# O desarrollo local
npm run dev
```

## 🐳 Docker

```bash
# Construir imágenes
docker-compose build

# Iniciar servicios
docker-compose up -d

# Logs
docker-compose logs -f

# Detener
docker-compose down
```

## 📚 API Documentation

La documentación interactiva está disponible en `/api/docs` después de iniciar el servidor.

### Endpoints Principales

```
POST   /api/auth/register        - Registrar usuario
POST   /api/auth/login           - Iniciar sesión
GET    /api/printers             - Listar impresoras
GET    /api/printers/:id         - Obtener detalles
POST   /api/quotations           - Crear cotización
GET    /api/quotations/:id       - Obtener cotización
POST   /api/quotations/:id/pdf   - Descargar PDF
```

## 🔐 Seguridad

- ✅ Autenticación JWT con refresh tokens
- ✅ Validación de entrada con Joi
- ✅ Rate limiting en endpoints públicos
- ✅ CORS configurado
- ✅ Helmet.js para headers de seguridad
- ✅ Variables de entorno seguros
- ✅ Hash de contraseñas con bcrypt

## 📊 Funcionalidades Avanzadas

### Calculadora Inteligente
- Recomendación automática basada en volumen
- Cálculo de precio con descuentos
- Estimación de ROI

### Generación de Documentos
- Cotizaciones en PDF profesionales
- Propuestas personalizadas
- Contratos automáticos

### Integraciones
- WhatsApp Business API
- Nodemailer para emails
- Stripe/PayPal (ready)
- Zapier (ready)

## 🧪 Testing

```bash
# Tests unitarios
npm run test:unit

# Tests de integración
npm run test:integration

# Cobertura
npm run test:coverage
```

## 📈 Monitoreo

- Dashboard en `/admin/dashboard`
- Métricas de conversión
- Reporte de impresoras
- Analytics de usuarios

## 🤝 Contribuir

1. Fork el proyecto
2. Crear rama feature (`git checkout -b feature/AmazingFeature`)
3. Commit cambios (`git commit -m 'Add AmazingFeature'`)
4. Push a rama (`git push origin feature/AmazingFeature`)
5. Abrir Pull Request

## 📝 Licencia

Este proyecto está bajo licencia MIT - ver archivo [LICENSE](LICENSE) para detalles.

## 👨‍💼 Soporte

- Email: desarrollo@imschile.cl
- WhatsApp: +56 9 1234 5678
- Issues: GitHub Issues

## 🙏 Agradecimientos

Desarrollado con ❤️ para IMS Chile SpA
