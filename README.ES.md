<div align="center" style="padding: 10px; border: 1px solid #ccc; background-color: #f9f9f9; border-radius: 10px; margin-bottom: 20px;">
    <h2 style="margin: 0; font-size: 24px; color: #333;">¡Langflow 1.0 está DISPONIBLE! 🎉</h2>
    <p style="margin: 5px 0 0 0; font-size: 16px; color: #666;">Lee todo sobre ello <a href="https://medium.com/p/73d3bdce8440" style="text-decoration: underline; color: #1a73e8;">aquí</a>!</p>
</div>

<!-- markdownlint-disable MD030 -->

# [![Langflow](./docs/static/img/hero.png)](https://www.langflow.org)

<p align="center"><strong>
    Un marco visual para construir aplicaciones multi-agente y RAG
</strong></p>
<p align="center" style="font-size: 12px;">
    De código abierto, impulsado por Python, totalmente personalizable, agnóstico a LLM y almacén de vectores
</p>

<p align="center" style="font-size: 12px;">
    <a href="https://docs.langflow.org" style="text-decoration: underline;">Documentación</a> -
    <a href="https://discord.com/invite/EqksyE2EX9" style="text-decoration: underline;">Únete a nuestro Discord</a> -
    <a href="https://twitter.com/langflow_ai" style="text-decoration: underline;">Síguenos en X</a> -
    <a href="https://huggingface.co/spaces/Langflow/Langflow" style="text-decoration: underline;">Demo en vivo</a>
</p>

<p align="center">
    <a href="https://github.com/langflow-ai/langflow">
        <img src="https://img.shields.io/github/stars/langflow-ai/langflow">
    </a>
    <a href="https://discord.com/invite/EqksyE2EX9">
        <img src="https://img.shields.io/discord/1116803230643527710?label=Discord">
    </a>
</p>

<div align="center">
  <a href="./README.md"><img alt="README en inglés" src="https://img.shields.io/badge/English-d9d9d9"></a>
    <a href="./README.ES.md"><img alt="README en español" src="https://img.shields.io/badge/Spanish-d9d9d9"></a>
  <a href="./README.PT.md"><img alt="README en portugués" src="https://img.shields.io/badge/Portuguese-d9d9d9"></a>
  <a href="./README.zh_CN.md"><img alt="README en chino simplificado" src="https://img.shields.io/badge/简体中文-d9d9d9"></a>
  <a href="./README.ja.md"><img alt="README en japonés" src="https://img.shields.io/badge/日本語-d9d9d9"></a>
  <a href="./README.KR.md"><img alt="README en coreano" src="https://img.shields.io/badge/한국어-d9d9d9"></a>
</div>

<p align="center">
  <img src="./docs/static/img/langflow_basic_howto.gif" alt="Tu GIF" style="border: 3px solid #211C43;">
</p>

# 📝 Contenido

- [📝 Contenido](#-contenido)
- [📦 Empezar](#-empezar)
- [🎨 Crear Flujos](#-crear-flujos)
- [Desplegar](#desplegar)
  - [DataStax Langflow](#datastax-langflow)
  - [Desplegar Langflow en Hugging Face Spaces](#desplegar-langflow-en-hugging-face-spaces)
  - [Desplegar Langflow en Google Cloud Platform](#desplegar-langflow-en-google-cloud-platform)
  - [Desplegar en Railway](#desplegar-en-railway)
  - [Desplegar en Render](#desplegar-en-render)
  - [Desplegar en Kubernetes](#desplegar-en-kubernetes)
- [🖥️ Interfaz de Línea de Comandos (CLI)](#️-interfaz-de-línea-de-comandos-cli)
  - [Uso](#uso)
    - [Variables de Entorno](#variables-de-entorno)
- [👋 Contribuir](#-contribuir)
- [🌟 Colaboradores](#-colaboradores)
- [📄 Licencia](#-licencia)

# 📦 Empezar

Puedes instalar Langflow con pip:

```shell
# Asegúrate de tener Python 3.10 o superior instalado en tu sistema.
python -m pip install langflow -U
```
O

Si deseas instalar desde tu repositorio clonado, puedes construir e instalar el frontend y backend de Langflow con:

```shell
make install_frontend && make build_frontend && make install_backend
```

Luego, ejecuta Langflow con:

```shell
python -m langflow run
```

# 🎨 Crear Flujos

Crear flujos con Langflow es fácil. Simplemente arrastra componentes desde la barra lateral al espacio de trabajo y conéctalos para empezar a construir tu aplicación.

Explora editando parámetros de prompt, agrupando componentes en un único componente de alto nivel y construyendo tus propios Componentes Personalizados.

Una vez que hayas terminado, puedes exportar tu flujo como un archivo JSON.

Carga el flujo con:

```python
from langflow.load import run_flow_from_json

results = run_flow_from_json("ruta/al/flujo.json", input_value="¡Hola, Mundo!")
```

# Desplegar

## DataStax Langflow

DataStax Langflow es una versión alojada de Langflow integrada con [AstraDB](https://www.datastax.com/products/datastax-astra). Puedes estar en funcionamiento en minutos sin instalación ni configuración requerida. [Regístrate gratis](https://langflow.datastax.com).

## Desplegar Langflow en Hugging Face Spaces

También puedes previsualizar Langflow en [HuggingFace Spaces](https://huggingface.co/spaces/Langflow/Langflow). [Clona el espacio usando este enlace](https://huggingface.co/spaces/Langflow/Langflow?duplicate=true) para crear tu propio espacio de trabajo Langflow en minutos.

## Desplegar Langflow en Google Cloud Platform

Sigue nuestra guía paso a paso para desplegar Langflow en Google Cloud Platform (GCP) usando Google Cloud Shell. La guía está disponible en el documento [**Langflow en Google Cloud Platform**](./docs/docs/Deployment/deployment-gcp.md).

Alternativamente, haz clic en el botón **"Abrir en Cloud Shell"** a continuación para lanzar Google Cloud Shell, clonar el repositorio Langflow y comenzar un **tutorial interactivo** que te guiará a través del proceso de configuración de los recursos necesarios y el despliegue de Langflow en tu proyecto GCP.

[![Abrir en Cloud Shell](https://gstatic.com/cloudssh/images/open-btn.svg)](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/langflow-ai/langflow&working_dir=scripts/gcp&shellonly=true&tutorial=walkthroughtutorial_spot.md)

## Desplegar en Railway

Usa esta plantilla para desplegar Langflow 1.0 en Railway:

[![Desplegar en Railway](https://railway.app/button.svg)](https://railway.app/template/JMXEWp?referralCode=MnPSdg)

## Desplegar en Render

<a href="https://render.com/deploy?repo=https://github.com/langflow-ai/langflow/tree/main">
<img src="https://render.com/images/deploy-to-render-button.svg" alt="Desplegar en Render" />
</a>

## Desplegar en Kubernetes

Sigue nuestra guía paso a paso para desplegar [Langflow en Kubernetes](./docs/docs/Deployment/deployment-kubernetes.md).

# 🖥️ Interfaz de Línea de Comandos (CLI)

Langflow proporciona una interfaz de línea de comandos (CLI) para una fácil gestión y configuración.

## Uso

Puedes ejecutar Langflow usando el siguiente comando:

```shell
langflow run [OPCIONES]
```

Cada opción se detalla a continuación:

- `--help`: Muestra todas las opciones disponibles.
- `--host`: Define el host al que se enlazará el servidor. Se puede configurar usando la variable de entorno `LANGFLOW_HOST`. El valor predeterminado es `127.0.0.1`.
- `--workers`: Establece el número de procesos de trabajo. Se puede configurar usando la variable de entorno `LANGFLOW_WORKERS`. El valor predeterminado es `1`.
- `--timeout`: Establece el tiempo de espera del trabajador en segundos. El valor predeterminado es `60`.
- `--port`: Establece el puerto en el que escuchar. Se puede configurar usando la variable de entorno `LANGFLOW_PORT`. El valor predeterminado es `7860`.
- `--env-file`: Especifica la ruta al archivo .env que contiene las variables de entorno. El valor predeterminado es `.env`.
- `--log-level`: Define el nivel de registro. Se puede configurar usando la variable de entorno `LANGFLOW_LOG_LEVEL`. El valor predeterminado es `critical`.
- `--components-path`: Especifica la ruta al directorio que contiene los componentes personalizados. Se puede configurar usando la variable de entorno `LANGFLOW_COMPONENTS_PATH`. El valor predeterminado es `langflow/components`.
- `--log-file`: Especifica la ruta al archivo de registro. Se puede configurar usando la variable de entorno `LANGFLOW_LOG_FILE`. El valor predeterminado es `logs/langflow.log`.
- `--cache`: Selecciona el tipo de caché a utilizar. Las opciones son `InMemoryCache` y `SQLiteCache`. Se puede configurar usando la variable de entorno `LANGFLOW_LANGCHAIN_CACHE`. El valor predeterminado es `SQLiteCache`.
- `--dev/--no-dev`: Activa o desactiva el modo de desarrollo. El valor predeterminado es `no-dev`.
- `--path`: Especifica la ruta al directorio frontend que contiene los archivos de construcción. Esta opción es solo para fines de desarrollo. Se puede configurar usando la variable de entorno `LANGFLOW_FRONTEND_PATH`.
- `--open-browser/--no-open-browser`: Activa o desactiva la opción de abrir el navegador después de iniciar el servidor. Se puede configurar usando la variable de entorno `LANGFLOW_OPEN_BROWSER`. El valor predeterminado es `open-browser`.
- `--remove-api-keys/--no-remove-api-keys`: Activa o desactiva la opción de eliminar las claves API de los proyectos guardados en la base de datos. Se puede configurar usando la variable de entorno `LANGFLOW_REMOVE_API_KEYS`. El valor predeterminado es `no-remove-api-keys`.
- `--install-completion [bash|zsh|fish|powershell|pwsh]`: Instala la finalización para el shell especificado.
- `--show-completion [bash|zsh|fish|powershell|pwsh]`: Muestra la finalización para el shell especificado, permitiéndote copiarla o personalizar la instalación.
- `--backend-only`: Este parámetro, con un valor predeterminado de `False`, permite ejecutar solo el servidor backend sin el frontend. También se puede configurar usando la variable de entorno `LANGFLOW_BACKEND_ONLY`.
- `--store`: Este parámetro, con un valor predeterminado de `True`, habilita las características de la tienda, usa `--no-store` para desactivarlo. Se puede configurar usando la variable de entorno `LANGFLOW_STORE`.

Estos parámetros son importantes para los usuarios que necesitan personalizar el comportamiento de Langflow, especialmente en escenarios de desarrollo o despliegue especializado.

### Variables de Entorno

Puedes configurar muchas de las opciones de CLI usando variables de entorno. Estas pueden exportarse en tu sistema operativo o añadirse a un archivo `.env` y cargarse usando la opción `--env-file`.

Se incluye un archivo `.env` de ejemplo llamado `.env.example` con el proyecto. Copia este archivo a un nuevo archivo llamado `.env` y reemplaza los valores de ejemplo con tus configuraciones reales. Si estás configurando valores tanto en tu SO como en el archivo `.env`, las configuraciones del `.env` tendrán prioridad.

# 👋 Contribuir

Damos la bienvenida a las contribuciones de desarrolladores de todos los niveles a nuestro proyecto de código abierto en GitHub. Si deseas contribuir, por favor revisa nuestras [directrices de contribución](./CONTRIBUTING.md) y ayuda a hacer Langflow más accesible.

---

[![Gráfico del Historial de Estrellas](https://api.star-history.com/svg?repos=langflow-ai/langflow&type=Timeline)](https://star-history.com/#langflow-ai/langflow&Date)

# 🌟 Colaboradores

[![colaboradores de langflow](https://contrib.rocks/image?repo=langflow-ai/langflow)](https://github.com/langflow-ai/langflow/graphs/contributors)

# 📄 Licencia

Langflow se publica bajo la Licencia MIT. Consulta el archivo [LICENSE](LICENSE) para más detalles.
