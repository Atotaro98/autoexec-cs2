# alwj0 AutoExec - Configuración CS2 (Español)

Una configuración completa y optimizada para Counter-Strike 2 con scripts útiles, comandos documentados y configuraciones profesionales.

## 📥 Instalación

### Pasos para Descargar e Instalar:

1. **Descarga la última versión** del config desde el repositorio.

2. **Extrae el contenido:**

   - Abre el archivo comprimido y extrae el contenido de la carpeta `cfg`
   - Copia todos los archivos a la siguiente ruta:
     ```
     \...\Steam\steamapps\common\Counter-Strike Global Offensive\game\csgo\cfg\
     ```

3. **Inicia el juego** y escribe en la consola:

   ```
   exec autoexec.cfg
   ```

4. **Si el autoexec no se ejecuta automáticamente**, intenta usar la opción de lanzamiento:

   ```
   +exec autoexec.cfg
   ```

5. **Para un nuevo escritorio o sistema operativo** (ej. Linux):
   - Asegúrate de colocar (nuevamente) todos los archivos en su lugar
   - No dejes que Steam Cloud los transfiera automáticamente

## ⚠️ Importante

- **El sistema de binds ha cambiado.** En lugar de usar el nombre de la tecla, ahora hay **scancodes asignados por tecla**. Esto asegura compatibilidad entre diferentes distribuciones de teclado e idiomas.

- **La mira está diseñada para una resolución de 1920x1080;** en otros casos, la experiencia puede variar.

## 🔄 Actualización

Cuando salga una nueva versión, tienes dos métodos para actualizar:

### Método 1: Has editado el config según tus preferencias

- Revisa los nuevos commits y actualiza el config manualmente basándote en los commits.
- Esto preserva tus personalizaciones.

### Método 2: No has editado el config (o al menos no mucho)

- Elimina todo (o reemplaza los archivos cuando te lo pida).
- Vuelve a realizar los pasos de instalación.
- Después de la configuración, vuelve a cambiar tus preferencias (si es el caso).

## ⌨️ Binds

![Keyboard Layout](keyboard-layout.png)

La configuración usa **scancodes** en lugar de nombres de teclas para mejor compatibilidad entre diferentes distribuciones de teclado. Cada tecla está vinculada usando su posición física en el teclado.

### Leyenda de Colores:

- 🔵 **Azul**: Binds por defecto
- 🟠 **Naranja**: Binds secundarios (mantén presionado ALT o MOUSE5)
- 🟢 **Verde**: Compra rápida
- ⚪ **Blanco**: Sin binds configurados
- 🩷 **Rosa**: Scripts
- 🔴 **Rojo**: Binds no permitidos
- 🟡 **Amarillo**: Nuevas ubicaciones y comandos infrecuentes

### Características Clave:

- **Binds secundarios**: Mantén presionado ALT o MOUSE5 para acceder a funciones secundarias
- **Scripts**: Funcionalidad personalizada para varios escenarios del juego
- **Compra rápida**: Vinculaciones de compra rápida
- **Categorías organizadas**: Los binds están categorizados por función

Para información detallada sobre los binds, consulta la página del wiki [alwj0 AutoExec Binds](https://github.com/alwj0-AutoExec/wiki/Binds).

## 📁 Archivos de Configuración

El config está organizado en múltiples archivos para facilitar la personalización:

- **autoexec.cfg**: Archivo principal que ejecuta todas las demás configuraciones
- **alwj0/audio.cfg**: Configuración de audio y optimización de sonido
- **alwj0/bind.cfg**: Todas las vinculaciones de teclas usando scancodes
- **alwj0/crosshair.cfg**: Configuración de la mira
- **alwj0/hud.cfg**: Elementos y diseño del HUD
- **alwj0/mouse.cfg**: Sensibilidad y configuración del mouse
- **alwj0/network.cfg**: Configuración de optimización de red
- **alwj0/script.cfg**: Scripts personalizados y automatización
- **alwj0/video.cfg**: Configuración de video y gráficos
