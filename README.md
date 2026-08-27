# Console TVFix Pro v3

**Console TVFix Pro v3** es una aplicación profesional multiplataforma diseñada para el diagnóstico avanzado, comunicación serial y reparación de Smart TVs. Impulsada por un motor gráfico de alto rendimiento y una interfaz moderna "Hi-Tech", proporciona un entorno de terminal robusto, librerías de comandos extensas para las principales tecnologías del mercado, telemetría en tiempo real y herramientas de seguridad de grado comercial.

> **Nota:** Este repositorio funciona como portal de releases, documentación y hoja de ruta. El código fuente es propietario y no está disponible públicamente.
> 🌐 **Sitio Web Oficial:** [https://yoelcode-ui.github.io/YoelCode/](https://yoelcode-ui.github.io/YoelCode/)

[![Versión](https://img.shields.io/badge/Versión-v3.1.7-00E5FF?style=flat-square)]()
[![Plataforma](https://img.shields.io/badge/Plataforma-Windows%20x64%20%7C%20Android-1A1D27?style=flat-square)]()
[![Licencia](https://img.shields.io/badge/Licencia-Comercial%20(RSA--3072)-FF3D00?style=flat-square)]()

<!-- Placeholder para video o imagen de demostración -->
<!-- [▶️ Haz clic aquí para ver el video de demostración en YouTube](https://www.youtube.com/@yoelcode) -->

---

## ✨ Características Principales

### 🔌 Conectividad y Comunicación Serial
* **Multiplataforma:** Soporte nativo y optimizado para **Windows (x64)** y **Android (ARMv7/ARM64)**.
* **Conexión Física y OTG:** Conéctate a TVs mediante puertos COM físicos en Windows o a través de cables USB-OTG en Android.
* **Terminal Bluetooth:** Soporte integrado para conexiones de diagnóstico inalámbrico vía Bluetooth (exclusivo en Android).
* **Configuración Avanzada:** Control total sobre baudios (1200 a 230400 bps), bits de datos, bits de parada y paridad.
* **Manejo seguro de desconexiones:** Notificaciones inteligentes (tipo Toast) que alertan inmediatamente si el hardware se desconecta de forma inesperada.

### 🖥️ Motor de Terminal (VT420 + Extensiones xterm)
* **Más allá de VT100:** Soporte completo para **TrueColor (24-bit)**, paletas de 256 colores, operaciones rectangulares (VT420) y modo legado VT52.
* **Telemetría en tiempo real (Live Meter):** Indicadores visuales dinámicos (TX/RX) que monitorean la actividad serial al instante.
* **Búsqueda integrada:** Busca en el historial del log en tiempo real para encontrar errores o cadenas de texto específicas rápidamente.
* **Exportación a HTML:** Exporta las sesiones de diagnóstico completas a archivos HTML con formato y colores para compartir reportes.
* **Envío Continuo (Macro Injection):** Repite comandos o pulsaciones de teclas (como `ENTER` o `CTRL+C`) de forma automatizada para forzar el acceso a modos DEBUG durante el arranque de la TV.

### 📚 Gestión Inteligente de Comandos
* **Librerías Predefinidas:** Comandos de un solo clic organizados por familia de chipsets y nivel de soporte.
* **Editor de Comandos Custom:** Interfaz dedicada para crear, editar y organizar tus propias secuencias de comandos (macros) con tokenización visual de escapes (`\r`, `\n`, `\xHH`).
* **Modo Recovery:** Pestaña dedicada con rutinas de recuperación de sistema para diferentes plataformas.

### 🎨 Interfaz Adaptable y Rendimiento
* **Diseño Responsivo:** La interfaz se adapta dinámicamente si estás en un monitor de escritorio o en un dispositivo móvil, ajustando paneles y áreas táctiles.
* **Panel de Control de Rendimiento:** Ajuste fino que permite al usuario equilibrar el impacto visual y el uso de recursos. Incluye 5 perfiles (desde *Máximo Rendimiento* hasta *Máxima Calidad*) para activar/desactivar animaciones, sombras, brillos (glow) y parpadeos.
* **Actualizaciones OTA:** El software verifica automáticamente si hay nuevas versiones en los Releases de GitHub y permite la descarga directa desde la app (Windows).

---

## 🛡️ Nuevo Sistema de Licencias y Seguridad

El sistema de licencias ha sido completamente rediseñado para ofrecer un modelo comercial seguro, offline y a prueba de manipulaciones.

* **Criptografía RSA-3072:** Cada licencia está firmada digitalmente.
* **Vinculación a Hardware (Hardware-Bound):** La licencia se ancla a la huella única de tu dispositivo (En Windows: Serial HDD, CPU ID, MAC, SMBIOS UUID. En Android: Widevine Device ID / Android ID).
* **Activación Offline:** No requiere conexión permanente a internet. Generas una solicitud, la envías, y recibes tu licencia firmada.
* **Lista de Revocación:** Verificación periódica contra una lista de revocación online para proteger el software ante uso no autorizado.
* **Protección Anti-Debug y Anti-Tamper (Windows):** Sistema de puntuación con decaimiento que detecta depuradores (PEB, NtQueryInformationProcess, Hardware Breakpoints, Timing) y protege la integridad del ejecutable en memoria.

---

## 📱 Hardware y Chipsets Soportados

### Chipsets de Smart TVs (Librerías de Comandos)
* ✅ **Soporte Completo:** MSTAR, REALTEK, MEDIATEK (DTV y MT58XX), SONY DTV / MT58XX, NUGGUET, PANASONIC, HISILICON, AMLOGIC.
* 🟡 **Soporte Parcial:** NOVATEK, SAMSUNG.
* *(Nota: MstarTool 3, disponible en nuestra web, cubre la edición profunda de dumps para Mstar).*

### Conversores USB-Serial Soportados (Android OTG)
La aplicación incluye drivers nativos compatibles con los chips más comunes del mercado:
* **FTDI:** FT232R, FT232H, FT2232H, FT4232H, FT230X, FT231X
* **Prolific:** PL2303
* **Silicon Labs:** CP2102, CP210*
* **WCH:** CH340, CH341A, CH9102
* **CDC/ACM:** Arduino, Digispark, Microchip MCP2221

---

## 🖥️ Requisitos del Sistema

**Windows:**
* Windows 10 (versión 1809 o superior) / Windows 11 - **Solo 64 bits**.
* Puerto serial físico o adaptador USB-to-Serial.

**Android:**
* Android 9 (API 28) o superior.
* Cable o adaptador USB-OTG.
* *Permisos:* Bluetooth, Ubicación (necesario en Android 12+ para escaneo BT) y Almacenamiento (para logs y licencias).

---

## 🚀 Guía Rápida de Uso

1. **Inicia la aplicación** y abre el panel de **Ajustes** (⚙️).
2. Configura el tipo de conexión (Serial, Bluetooth u OTG) y ajusta el BaudRate (usualmente `115200`) según la placa de la TV.
3. Selecciona la **Tecnología** de la TV en el menú lateral (ej. MSTAR, REALTEK) o elige *Recovery*.
4. Usa el panel derecho para acceder a:
   * **Predefinidos:** Comandos probados para la tecnología seleccionada.
   * **Personalizados:** Tus propios scripts guardados.
   * **Recovery:** Rutinas de rescate y bootloader.
5. Haz clic en cualquier comando para enviarlo, o escribe manualmente en la barra inferior.
6. Monitorea los medidores **RX/TX** en la barra superior y usa el buscador para analizar el log.

---

## 🔒 Proceso de Activación (Licencia Comercial)

Console TVFix Pro es una aplicación comercial. Se requiere un archivo de licencia válido para desbloquear todas las capacidades. **(Se ofrece licencia de prueba gratuita por tiempo limitado solicitándola al soporte).**

1. **Genera tu Solicitud:** Al abrir la app por primera vez, el sistema generará un texto con la huella única de tu hardware.
2. **Envía la Solicitud:** Copia ese texto y envíalo al desarrollador por WhatsApp o Telegram.
3. **Recibe tu Licencia:** Recibirás de vuelta un texto/archivo de licencia firmado criptográficamente.
4. **Activa:** Importa la licencia en la aplicación (o pégala en la ventana de activación en Android) para desbloquear el software permanentemente en ese dispositivo.

*¿Cambias de equipo? El sistema incluye una opción para generar un "Ticket de Desactivación" y transferir tu licencia.*

---

## 📞 Soporte y Contacto

Para licencias, soporte técnico, reportar bugs o solicitar una **Licencia de Prueba Gratuita**, contacta directamente al desarrollador:

* 👤 **Arquitecto del Sistema:** Yoel Romero H.
* 📱 **WhatsApp / Telegram:** [+53 56113984](https://api.whatsapp.com/send?phone=5356113984&text=Hola%2C%20quiero%20información%20sobre%20Console%20TVFix%20Pro%20v3)
* 🌐 **Sitio Web:** [yoelcode-ui.github.io/YoelCode](https://yoelcode-ui.github.io/YoelCode/)
* 📺 **YouTube:** [@yoelcode](https://www.youtube.com/@yoelcode) (Tutoriales y demos)
* 💬 **Comunidad de Telegram:** [Smart TV Mods Community](https://t.me/+jhrpO99SAy4wZDlh)

---

## ⚙️ Notas de Desarrollo

* Este repositorio sirve únicamente como hoja de ruta y portal de releases.
* No se requiere hardware propietario ni cajas de flasheo externas; un simple adaptador USB-to-TTL/Serial es suficiente.
* Toda la comunicación utiliza protocolos serial estándar.

## ⚖️ Copyright

© 2026 **YoelCode** / Console TVFix Pro – Todos los derechos reservados.
*La redistribución, ingeniería inversa, modificación, elusión de licencias o uso no autorizado de este software está estrictamente prohibido y perseguido por las leyes de propiedad intelectual.*
