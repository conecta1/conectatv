# ConectaTV+ Subscription Page

Este proyecto es una página de suscripción para ConectaTV+, un servicio que ofrece planes de suscripción a diversas plataformas de streaming.

## Características Principales

### 1. Asistente Virtual Inteligente
- Chatbot impulsado por OpenAI que proporciona respuestas naturales y contextuales
- Comprende consultas con errores ortográficos y lenguaje natural
- Proporciona información sobre planes, precios, métodos de pago y seguridad
- Opción para redirigir a WhatsApp para atención humana

### 2. Sistema de Reseñas Global
- Almacenamiento de reseñas en Firebase Firestore
- Persistencia de reseñas entre diferentes dispositivos y navegadores
- Funcionalidad para agregar, ver y eliminar reseñas
- Soporte para imágenes en las reseñas

## Tecnologías Utilizadas

- **Frontend**: Next.js, React, TailwindCSS
- **Backend**: Next.js API Routes
- **IA**: OpenAI API (GPT-3.5 Turbo)
- **Base de Datos**: Firebase Firestore
- **Almacenamiento**: Firebase Storage

## Configuración del Proyecto

### Requisitos Previos

- Node.js (versión 18 o superior)
- Cuenta de Firebase con Firestore habilitado
- Clave API de OpenAI

### Configuración de Variables de Entorno

Crea un archivo `.env.local` en la raíz del proyecto con las siguientes variables:

```
# OpenAI API Key
OPENAI_API_KEY=tu_clave_api_de_openai

# Firebase Config
NEXT_PUBLIC_FIREBASE_API_KEY=tu_api_key_de_firebase
NEXT_PUBLIC_FIREBASE_AUTH_DOMAIN=tu_auth_domain_de_firebase
NEXT_PUBLIC_FIREBASE_PROJECT_ID=tu_project_id_de_firebase
NEXT_PUBLIC_FIREBASE_STORAGE_BUCKET=tu_storage_bucket_de_firebase
NEXT_PUBLIC_FIREBASE_MESSAGING_SENDER_ID=tu_messaging_sender_id_de_firebase
NEXT_PUBLIC_FIREBASE_APP_ID=tu_app_id_de_firebase
```

### Instalación de Dependencias

```bash
npm install
```

### Ejecución en Modo Desarrollo

```bash
npm run dev
```

### Construcción para Producción

```bash
npm run build
npm start
```

## Estructura del Proyecto

- `/app`: Componentes y páginas principales de la aplicación
  - `/api`: Endpoints de API para el chatbot y las reseñas
- `/components`: Componentes reutilizables de UI
- `/lib`: Utilidades y configuraciones (Firebase, OpenAI)
- `/public`: Archivos estáticos

## Funcionalidades Implementadas

### Asistente Virtual
- Integración con OpenAI para respuestas naturales
- Contexto específico sobre ConectaTV+ para respuestas precisas
- Indicador de "escribiendo..." durante la generación de respuestas
- Manejo de errores con mensajes amigables

### Sistema de Reseñas
- Almacenamiento en Firebase Firestore para persistencia global
- API endpoints para agregar, obtener y eliminar reseñas
- Soporte para imágenes en las reseñas
- Validación de datos en el servidor