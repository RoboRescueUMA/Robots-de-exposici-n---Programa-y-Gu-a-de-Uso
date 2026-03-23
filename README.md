# 🤖 Web Controller para Makeblock

Este proyecto permite controlar un robot basado en la placa Makeblock directamente desde el navegador web de un ordenador, utilizando un módulo Bluetooth Dual Mode y la **Web Serial API**.

## ⚠️ Notas Técnicas Importantes
* **Hardware:** Diseñado para módulos Bluetooth conectados al **Puerto 5** (Pines RX/TX de Hardware Serial 0 y 1).
* **Comunicación:** Utiliza Bluetooth Clásico (SPP) a 115200 baudios para garantizar una transmisión de datos sin pérdida ni latencia.
* **Compatibilidad Web:** Debido a restricciones de seguridad de la Web Serial API, esta App Web **solo funciona en navegadores de escritorio** (Windows, Mac, Linux, ChromeOS). No funciona en móviles/tablets.

---

## 🛠️ Requisitos Previos (Setup)

1. **Cargar el programa al microcontrolador:**
   * Abre el código `robot_brazo_V1.ino` disponible en la carpeta de este repositorio con el IDE de Arduino.
   * Utiliza como microcontrolador de destino Arduino UNO
2. **Descargar la Web App:**
   * Descarga el archivo `app_control_brazo.html` de este repositorio en tu ordenador. Guárdalo en una carpeta vacía destinada para ello.

---

## 🚀 Guía de Uso

Sigue estos pasos para arrancar el centro de control:

1. **Preparar el entorno:** Instala el editor de código [Visual Studio Code](https://code.visualstudio.com/).
2. **Instalar Live Server:** Dentro de VSCode, ve al apartado de Extensiones y descarga la extensión **Live Server**.
3. **Emparejar el Bluetooth:** Ve a la configuración de Bluetooth de tu sistema operativo (Windows/Mac) y empareja el módulo de Makeblock.
4. **Lanzar la App Web:** Abre la carpeta donde guardaste el `app_control.html` con VSCode. Haz clic derecho sobre el código y selecciona **"Open with Live Server"** (o pulsa "Go Live" en la barra inferior). Se abrirá en tu navegador predeterminado.
5. **Conectar el robot:** * Enciende el robot.
   * En la App Web, pulsa el botón **VINCULAR ROBOT**.
   * El navegador te pedirá elegir un puerto serie. Selecciona el puerto COM correspondiente a tu Bluetooth. (Puede ser que en vez de COM aparezca directamente en la lista "Makeblock")
   * **Recomendación**: para evitar errores intenta que no haya ningún otro módulo bluetooth de Makeblock encendido para no encontrar varios en la lista de dispositivos accesibles.
6. **Todo listo:** Usa los botones en pantalla para cambiar entre el modo Automático y Manual. En modo manual, puedes hacer clic en las flechas o usar las teclas **W, A, S, D, X** de tu teclado para mover el robot.

# 📱 Versión Móvil (Android)

## 🛠️ Requisitos Previos (Setup)

1. **Cargar el programa al microcontrolador:**
   * Abre el código `robot_brazo_V1.ino` disponible en la carpeta de este repositorio con el IDE de Arduino.
   * Utiliza como microcontrolador de destino Arduino UNO

## 📥 Cómo obtener la app

Tienes dos opciones:

1. **Instalación directa (.apk):**
   * Descarga el archivo `Robot_brazo.apk` desde este repositorio.
   * Ábrelo en tu dispositivo Android e instálalo.

2. **Editar y compilar (.aia):**
   * Descarga el archivo `Robot_brazo.aia`.
   * Súbelo a MIT App Inventor (https://appinventor.mit.edu/).
   * Modifica el proyecto si lo necesitas.
   * Pulsa **Build** para generar la app.
   * Escanea el QR que aparece para descargarla en tu móvil.

> ⚠️ Es normal que aparezcan advertencias de seguridad al instalar. Ocurren porque la app no proviene de la Play Store. Debes aceptar los permisos para continuar.

---

## 🔗 Conexión y uso

1. **Conectar por Bluetooth:**
   * Ve a los ajustes de tu móvil.
   * Conéctate al dispositivo `Makeblock`.
   * ⚠️ No seleccionar `Makeblock_LE`.

2. **Abrir la app:**
   * Inicia la aplicación instalada.
   * Pulsa el botón **Conectar**.
   * Selecciona el dispositivo de la lista.

   > Si no aparece ningún dispositivo:
   > * Cierra y vuelve a abrir la app.
   > * Asegúrate de que el Bluetooth está activado.

   > Si no conecta:
   > * Comprueba que nadie más está conectado.
   > * Si el módulo tiene un LED azul fijo, ya está en uso.

3. **Control del robot:**
   * Usa los botones para mover el robot.
   * Después de avanzar o girar, pulsa **X** para detenerlo.
   * Para mover el brazo, mantén pulsado el botón:
     * Al soltarlo, se detiene automáticamente.
   * Usa el switch para cambiar entre modo **Manual** y **Automático**.
