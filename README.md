# Reverse Tethering Launcher (para Windows)
### Basado en: https://github.com/Genymobile/gnirehtet

Conexión de internet de Windows a Android con un solo clic (Lo opuesto a Android USB Tethering).

## ¿Qué hace esto?

Te ayuda en una situación en la que:
1.  Tu teléfono necesita conexión a internet.
2.  Tu PC tiene conexión a internet (por cable o Wi-Fi) pero no puede crear un Hotspot.
3.  Tienes un cable USB para conectar el teléfono a la PC.
4.  Quieres usar el internet de tu PC en tu teléfono.

## ⚠️ Información MUY Importante

Estos ejecutables **NO** son virus. Son *scripts* compilados con "Bat-to-Exe" para ser más fáciles de usar. Puedes ver el código fuente [aquí](TU_ENLACE_AL_CODIGO_SI_LO_SUBES).

### Requisito Previo CRÍTICO
Para que estos lanzadores funcionen, **primero debes haber instalado la versión oficial de `gnirehtet` para Windows**.

1.  Ve a la página oficial de lanzamientos:
    [**https://github.com/Genymobile/gnirehtet/releases**](https://github.com/Genymobile/gnirehtet/releases)
2.  Descarga el **instalador** más reciente (ej: `gnirehtet-v2.6.1-windows-x64-installer.exe`).
3.  Instálalo. Esto es crucial, ya que este instalador pone `gnirehtet.exe` en la carpeta `%APPDATA%`, que es donde nuestros lanzadores lo buscan.

## 📦 Los Dos Lanzadores

Este proyecto te ofrece dos formas de iniciar el programa, cada una con su propio ícono:

<img width="272" height="175" alt="image" src="https://github.com/user-attachments/assets/5be63dae-2087-48d6-8f14-1d869cc59205" />

### 1. `Reverse-Tethering-Visible.exe`

* **¿Qué hace?** Inicia el script mostrando la ventana de la consola (la terminal negra).
* **¿Cuándo usarlo?** Es la **opción recomendada para la primera vez** o si algo parece no funcionar. En esta ventana podrás ver el registro de conexión en tiempo real, confirmar que tu teléfono se conectó y diagnosticar cualquier error.

### 2. `Reverse-Tethering.exe` (Invisible)
* **¿Qué hace?** Inicia el script de forma **totalmente silenciosa en segundo plano**. No verás ninguna ventana emergente; simplemente funcionará.
* **¿Cuándo usarlo?** Esta es la **opción para el uso diario**. Una vez que ya sabes que tu conexión funciona, no necesitas ver la consola. Simplemente haz doble clic y tu teléfono tendrá internet.

## ⚡ Cómo Usar (Paso a Paso)

Una vez hayas instalado el requisito previo:

1.  **Ejecuta el lanzador** que prefieras (se recomienda `Reverse-Tethering-Visible.exe` la primera vez).
    ![Ventana de la consola al iniciar](help/onstart.png)

2.  **Acepta los permisos de administrador** cuando Windows te lo pida. Son necesarios para gestionar la conexión.

3.  **Conecta tu teléfono Android** a tu PC con el cable USB.

4.  En tu teléfono, cambia el modo de conexión de "Solo carga" a **"Transferencia de archivos"**.
    ![Cambiar modo de "Solo Carga" a "Transferencia de archivos"](help/charge_only_to_transfer_files.jpg)

5.  **Habilita la "Depuración USB"** en tu teléfono.
    *(Si no sabes cómo, busca en Google "Cómo habilitar opciones de desarrollador en [tu modelo de móvil]")*.
    ![Opciones de desarrollador con Depuración USB habilitada](help/enable_usb_debugging_developer_options.png)

6.  Aparecerá un **aviso en tu teléfono** pidiendo permiso para la depuración. Marca "Permitir siempre" y pulsa **OK**.
    ![Aviso de depuración USB "Permitir..."](help/usb_debugging_prompt.png)

7.  El script instalará automáticamente la aplicación cliente de `gnirehtet` en tu teléfono.
    ![Instalación automática de la app cliente](help/client_app_install_and_start_app_with_broadcast.png)

8.  Aparecerá una **solicitud de conexión VPN** en tu teléfono. Es necesario para que el internet funcione. Acepta la solicitud.
    ![Solicitud de conexión VPN en Android](help/vpn_request.jpg)

9.  **¡Y listo!** Verás un ícono de una **llave (VPN)** en la barra de estado de tu teléfono. Esto significa que ya estás conectado y usando el internet de tu PC.
    ![Barra de estado de Android con el ícono de VPN (llave)](help/vpn_started_internet_connected_indication.png)

---

### Notas Adicionales

* Si usas la versión **visible**, verás una consola con el registro de todas las conexiones que está haciendo tu teléfono.
* Para desconectar, simplemente **cierra la ventana de la consola** (si usaste la versión visible) o **desconecta el cable USB**.
* Si dejas la ventana visible abierta, el proceso se reiniciará automáticamente cada vez que desconectes y reconectes el móvil.
    ![Registro de conexión y desconexión](help/connection_starts_successfully_and_device_disconnect_after_use.png)

---
🧑‍💻 Hecho por **elmendezz** y **Gemini**.
*(Guía de usuario adaptada del excelente README de [omkar-tenkale](https://github.com/omkar-tenkale/Reverse-tethering-setup-Windows)).*
