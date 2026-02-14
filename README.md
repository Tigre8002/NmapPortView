# NmapPortView 🛡️

![Python](https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python)
![Bash](https://img.shields.io/badge/Script-Bash-green?style=for-the-badge&logo=gnu-bash)

**NmapPortView** es una herramienta escrita en Python diseñada para agilizar el flujo de trabajo en pruebas de penetración y CTFs. Permite extraer y copiar puertos rápidamente desde escaneos de Nmap, así como visualizar reportes XML de forma automática en el navegador.

## 🚀 Características

* **Extracción de Puertos (`-c`)**: Analiza la salida *grepable* de Nmap, muestra el estado de los puertos (TCP/UDP) en la terminal y **copia automáticamente al portapapeles** la lista de puertos abiertos separados por comas (ej: `22,80,443`).
* **Conversión XML a HTML (`-xF`)**: Transforma archivos XML de Nmap en reportes HTML legibles utilizando `xsltproc`. Genera un enlace temporal y lo copia al portapapeles listo para pegar en el navegador.
* **Compatibilidad**: Script de instalación automático para múltiples distribuciones (Debian/Kali, Arch, Fedora, Alpine, macOS).

## 📋 Requisitos

* Python 3
* `xsltproc` (El instalador intentará instalarlo automáticamente si no existe).
* Librería `pyperclip` de Python (necesaria para las funciones de portapapeles).

## 🛠️ Instalación

1.  **Clona el repositorio:**
    ```bash
    git clone [https://github.com/Tigre8002/nmapPortView.git](https://github.com/Tigre8002/nmapPortView.git)
    cd nmapPortView
    ```

2.  **Instala la dependencia de Python:**
    ```bash
    pip3 install pyperclip
    ```

3.  **Ejecuta el instalador:**
    Da permisos de ejecución e instala la herramienta (requiere `sudo` para mover el binario a `/usr/local/bin` e instalar dependencias del sistema).
    ```bash
    chmod +x install.sh
    ./install.sh
    ```

## 📖 Uso

Una vez instalado, puedes ejecutar la herramienta desde cualquier lugar en tu terminal:

```bash
nmapPortView [opción] <archivo>
