# 🤖 ChatBot Municipal - Cuponeras Digitales

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.shadow&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Express.js](https://img.shields.io/badge/express.js-%23404d59.svg?style=for-the-badge&logo=express&logoColor=61DAFB)
![MySQL](https://img.shields.io/badge/mysql-%2300f.svg?style=for-the-badge&logo=mysql&logoColor=white)

Asistente virtual inteligente diseñado para municipalidades locales que automatiza la distribución y consulta de cuponeras de tributos de manera interactiva a través de **WhatsApp**. Facilita la comunicación con el vecino, reduce la presencialidad en ventanilla y agiliza el flujo de recaudación tributaria.

## 🌟 Funcionalidades Clave

- 🎟️ **Descarga de Cuponeras PDF:** Generación y envío automatizado de documentos tributarios oficiales directamente al chat del vecino.
- 💬 **Flujos de Conversación Inteligentes:** Respuestas en tiempo real para preguntas frecuentes sobre arbitrios, prediales y cronogramas de pago.
- 🔑 **Autenticación Ciudadana Segura:** Validación de identidad a través de DNI, RUC o Código de Contribuyente en la base de datos municipal.
- 📈 **Panel de Administración:** API e interfaz gráfica interna para que los administradores municipales monitoreen el volumen de consultas y envíos.

## ⚙️ Arquitectura del Sistema

```
                   ┌─────────────────┐
                   │   Vecino (WA)   │
                   └────────┬────────┘
                            │ (Mensaje de texto/PDF)
                            ▼
                   ┌─────────────────┐
                   │  WhatsApp API   │
                   └────────┬────────┘
                            │
                            ▼
 ┌─────────────┐   ┌─────────────────┐   ┌─────────────┐
 │ Base Datos  │◀──│   NodeJS App    │──▶│ Generador   │
 │    MySQL    │   │ (Express / WA)  │   │  de PDFs    │
 └─────────────┘   └─────────────────┘   └─────────────┘
```

## 🛠️ Stack Tecnológico

- **Backend:** Node.js, Express
- **API Wrapper:** WhatsApp Web.js / Twilio API
- **Base de Datos:** MySQL (con soporte de Sequelize ORM)
- **Servicios:** Docker (para empaquetado de servicios)

## 🚀 Despliegue Rápido

1. Configura tus variables de entorno en un archivo `.env`:
   ```env
   PORT=3000
   DB_HOST=localhost
   DB_USER=root
   DB_PASS=tu_contraseña
   DB_NAME=municipalidad_db
   ```
2. Instala las dependencias:
   ```bash
   npm install
   ```
3. Inicia el servidor:
   ```bash
   npm start
   ```
4. Escanea el código QR que se imprimirá en la consola con tu dispositivo WhatsApp para sincronizar el bot.

---
Desarrollado por **[Jhony E. Ramos Ticse](https://github.com/Clun0x)**.
