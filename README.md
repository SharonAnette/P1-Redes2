# Comunicación Cliente-Servidor con Sockets en Python y C

Este repositorio contiene dos prácticas desarrolladas para la asignatura **Aplicaciones para Comunicaciones en Red** (6CV2) en la **Escuela Superior de Cómputo (ESCOM)** del **Instituto Politécnico Nacional (IPN)**.  
Ambas prácticas exploran el uso de **sockets TCP** en el modelo **cliente-servidor**, mostrando la diferencia entre **comunicaciones bloqueantes** y **no bloqueantes** en distintos lenguajes de programación.

---

## Práctica 1 — Sockets Orientados a Conexiones Bloqueantes (Python)

###  Descripción
Implementación de un sistema cliente-servidor utilizando **sockets bloqueantes** en Python.  
El servidor escucha en el puerto 8080, acepta conexiones y recibe mensajes de un cliente, garantizando una comunicación **fiable y secuencial** mediante el protocolo **TCP**.

### Objetivo
Comprender el funcionamiento de los **sockets bloqueantes** y su uso en aplicaciones que requieren **integridad y orden en los datos** transmitidos.

### Archivos principales
- `servidor_bloqueante.py` — Implementación del servidor TCP.
- `cliente_bloqueante.py` — Implementación del cliente TCP.

### Análisis
Mediante **Wireshark**, se verificó el intercambio correcto de paquetes y la fiabilidad del protocolo TCP, confirmando la transmisión ordenada entre cliente y servidor:contentReference[oaicite:0]{index=0}.

### Lenguaje y herramientas
- **Python 3**
- **Librería:** `socket`
- **Analizador de red:** Wireshark

---

## Práctica 2 — Sockets No Bloqueantes en C

### Descripción
Desarrollo de un servidor no bloqueante en **C** que gestiona múltiples clientes simultáneamente utilizando la función `select()` y configurando los sockets con `fcntl()` para **operar sin detener el flujo de ejecución**.

### Objetivo
Aprender a manejar **conexiones concurrentes** de forma eficiente mediante **sockets no bloqueantes**, aplicando técnicas de multiplexación de entrada/salida para mejorar el rendimiento en sistemas de red:contentReference[oaicite:1]{index=1}.

### Archivos principales
- `servidor_no_bloqueante.c` — Servidor TCP con multiplexación y sockets no bloqueantes.
- `cliente_no_bloqueante.c` — Cliente TCP que envía y recibe mensajes del servidor.

### Análisis
Se comprobó, mediante Wireshark, la transmisión bidireccional de datos bajo el protocolo TCP, observando cómo el servidor atiende varias conexiones sin bloquearse durante la lectura o escritura:contentReference[oaicite:2]{index=2}.

### Lenguaje y herramientas
- **C (GCC)**
- **Bibliotecas:** `<sys/socket.h>`, `<fcntl.h>`, `<sys/select.h>`
- **Analizador de red:** Wireshark
