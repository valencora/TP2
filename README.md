# Proyecto TP2 - Procesamiento de Imágenes 

## Descripción

Este proyecto es una aplicación distribuida que incluye:
- Un **servidor asincrónico** que recibe imágenes, las convierte a escala de grises y las envía a un segundo servidor para ser escaladas.
- Un **servidor de escalado** que redimensiona las imágenes recibidas y las devuelve al servidor asincrónico.
- Un **cliente** que envía imágenes al servidor asincrónico para procesarlas.

La aplicación está diseñada para manejar múltiples conexiones de manera eficiente utilizando `asyncio` para la concurrencia asíncrona y `multiprocessing` para ejecutar cada servidor en un proceso separado.

## Estructura del Proyecto

```plaintext
TP2/
├── async_server/
│   ├── __init__.py
│   └── server.py               # Código del servidor asincrónico
├── scaling_server/
│   ├── __init__.py
│   └── server.py               # Código del servidor de escalado
├── client.py                   # Cliente que envía imágenes al servidor asincrónico
├── tp2.py                      # Script principal que inicia ambos servidores
├── prueba.jpeg                 # Imagen de prueba
└── tests/
    ├── __init__.py
    ├── test_async_server.py    # Pruebas unitarias para el servidor asincrónico
    └── test_scaling_server.py  # Pruebas unitarias para el servidor de escalado
