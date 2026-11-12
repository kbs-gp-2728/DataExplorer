# Data Explorer

Desarrollar una aplicación web para cargar conjuntos de datos en formato CSV o Excel y obtener un diagnóstico exploratorio inicial. La aplicación permitirá examinar la estructura del archivo, los tipos de variables, los valores faltantes, los registros duplicados, las estadísticas descriptivas y las visualizaciones. Está dirigida a investigadores y estudiantes que necesitan conocer rápidamente las características de un dataset sin programar cada análisis desde cero.

## Herramientas identificadas

Esta sección es para la especificación de las herramientas que se van a utilizar en el desarrollo del proyecto, en base a un full stack de Python y con ayuda de varias librerías del mismo entorno.

--- 
### Librerías utilizadas:

| Librería | Función principal | Capa del sistema |
|---|---|---|
| numpy | Cálculo numérico vectorizado sobre arreglos `ndarray` | Núcleo numérico |
| pandas | Manipulación y análisis de datos tabulares (`DataFrame`, `Series`) | Procesamiento |
| scipy | Estadística, optimización, álgebra lineal y procesamiento de señales | Cálculo científico |
| openpyxl | Lectura y escritura de archivos `.xlsx` (Office Open XML) | Entrada/salida |
| plotly | Gráficos interactivos basados en especificaciones JSON renderizadas con plotly.js | Visualización |
| streamlit | Construcción de aplicaciones web de datos en Python puro | Presentación |
| pytest | Framework de pruebas unitarias e integración | Verificación |
---

## Instalación y preparación del entorno: 
 > Sección generada por IA

#### Requisitos previos

- Python 3.11 o superior
- Git
- Una terminal (PowerShell en Windows, Terminal en macOS o Linux)

#### Instalación

Todos los comandos se ejecutan desde la carpeta del proyecto, `data-explorer/`.

##### 1. Abrir la terminal en la carpeta del proyecto

- **Windows:** abre la carpeta `data-explorer` en el Explorador de archivos, haz clic en la barra de direcciones, escribe `powershell` y presiona Enter.
- **macOS o Linux:** abre la Terminal y usa `cd ruta/a/data-explorer`.

##### 2. Crear el entorno virtual

Un entorno virtual es una carpeta (`.venv`) donde se instalan las librerías de este proyecto, separadas del resto de tu computadora.

```bash
python -m venv .venv
```

En macOS o Linux, si `python` no funciona, usa `python3`.

##### 3. Activar el entorno virtual

Activar el entorno significa decirle a la terminal que use las librerías de `.venv` en lugar de las globales. Hay que hacerlo cada vez que abras una terminal nueva para trabajar en el proyecto.

**Windows (PowerShell):**

```powershell
.venv\Scripts\Activate.ps1
```

**Windows (símbolo del sistema, cmd):**

```bat
.venv\Scripts\activate.bat
```

**macOS o Linux:**

```bash
source .venv/bin/activate
```

Sabrás que funcionó porque aparece `(.venv)` al inicio de la línea de comandos.

> **Sobre el archivo `Activate.ps1`:** es un script de PowerShell, el lenguaje de la terminal de Windows. Su única función es cambiar las rutas de la terminal para que use `.venv`. Contiene instrucciones internas que no necesitas revisar.
>
> **Si aparece un error como «la ejecución de scripts está deshabilitada en este sistema»**, Windows bloquea por seguridad los scripts descargados. Para permitir los scripts de tu propio usuario, ejecuta una sola vez en PowerShell:
>
> ```powershell
> Set-ExecutionPolicy -Scope CurrentUser RemoteSigned
> ```
>
> Responde `S` (sí) si te lo pregunta, y vuelve a ejecutar el paso de activación. Este cambio solo afecta a tu usuario y no requiere permisos de administrador.

##### 4. Instalar las librerías

Con el entorno activado (`(.venv)` visible), ejecuta:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

El archivo `requirements.txt` contiene la lista de librerías que usa el proyecto. Este paso puede tardar unos minutos.

##### 5. Verificar la instalación

```bash
python -c "import pandas, streamlit, plotly, openpyxl, scipy; print('Instalación correcta')"
```

Si ves `Instalación correcta`, todo está listo.

## Ejecutar la aplicación

Con el entorno activado:

```bash
streamlit run app.py
```

Se abrirá el navegador en `http://localhost:8501`. Para detener la aplicación, vuelve a la terminal y presiona `Ctrl + C`.

#### Desactivar el entorno

Cuando termines de trabajar:

```bash
deactivate
```

#### Problemas frecuentes

| Problema | Solución |
|---|---|
| `python` no se reconoce | Instala Python desde python.org y marca la opción «Add Python to PATH». |
| La activación en PowerShell falla por permisos | Ejecuta `Set-ExecutionPolicy -Scope CurrentUser RemoteSigned` (ver paso 3). |
| `pip install` falla por red | Revisa tu conexión o la configuración de red de tu equipo. |
| `(.venv)` no aparece tras activar | Vuelve a ejecutar el comando de activación desde la carpeta del proyecto. |
| `streamlit` no se reconoce | Asegúrate de que el entorno esté activado antes de ejecutar la aplicación. |
