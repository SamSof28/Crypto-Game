# Crypto Ley: El Desafío del Abogado Digital ⚖️

---

## 1. Introducción al Proyecto

Este proyecto es un **videojuego educativo** desarrollado como parte de las actividades del **Curso de Metodologías Activas para la Comprensión de Problemas** de la Universidad de Medellín. Su principal objetivo es utilizar la **gamificación** como una metodología activa para facilitar la **comprensión, asimilación y discusión** de conceptos clave y desafíos jurídicos relacionados con los **criptoactivos** y la **tecnología _blockchain_**.

El juego se presenta en un estilo _plataformas 2D_ con estética _pixel-art_ para maximizar la inmersión y el compromiso lúdico del estudiante.

---

## 2. Fundamento Académico y Objetivo de Aprendizaje

El diseño de "Crypto Ley" se fundamenta en la teoría del **Aprendizaje Basado en Juegos (ABJ)**, buscando transformar un contenido denso y especializado (la regulación de criptoactivos) en una experiencia interactiva y memorable.

### 🎯 Objetivo Principal

**Evaluar y reforzar la comprensión** de los participantes sobre las clasificaciones, riesgos y vacíos legales asociados a los criptoactivos en el contexto del derecho colombiano e internacional, particularmente en materia de **protección al consumidor**.

### 💡 Conceptos Clave Abordados (Módulos de Conocimiento)

Durante el juego, el jugador debe recolectar 'monedas' que representan la adquisición de conocimiento jurídico. Cada moneda desbloquea un módulo de información específico:

* **Clasificación Regulatoria Internacional:** Tipologías de tokens (e-money, referenciados a activos, utilidad) según marcos como el reglamento MICA de la Unión Europea.
* **Desafíos Jurisdiccionales:** Problemas de territorialidad para la aplicación de leyes como el Estatuto del Consumidor en Colombia.
* **Principios de Regulación:** La máxima de "misma actividad, mismo riesgo, misma regulación".
* **Clasificación en EE.UU.:** Criptoactivos como _commodities_ (CFTC) vs. _valores_ (SEC - Test de Howey).
* **Riesgos de Estructuras Descentralizadas (DAO):** Vacío legal en la determinación de responsabilidad societaria.
* **Fundamentos Técnicos:** Definición de _blockchain_ como libro digital descentralizado.
* **Aplicación de la Ley Colombiana:** Alcance de la Ley 1480 de 2011 (Estatuto del Consumidor) a transacciones con criptoactivos.
* **Naturaleza Irreversible de Transacciones:** Dificultad para la reversión de pagos en redes descentralizadas.
* **Contratos Inteligentes (_Smart Contracts_):** Su papel en la eliminación de intermediarios.

---

## 3. Mecánica de Juego y Dinámica

### 🕹️ Controles

* **Flecha Izquierda (◀️) / Derecha (▶️):** Movimiento horizontal del personaje.
* **Flecha Arriba (▲):** Salto.

### 🚧 Elementos del Nivel

1.  **Personaje Jugable (Abogado/a Digital):** El jugador puede elegir entre dos avatares para representarse en la misión de obtener conocimiento.
2.  **Plataformas:** Representan los **cimientos legales** o los **sistemas regulados** que proveen una base firme para la acción.
3.  **Monedas (Criptoactivos de Conocimiento):** Al ser recolectadas, incrementan el puntaje de "Conocimiento" y activan un *modal* (ventana emergente) que presenta un dato clave sobre la regulación de criptoactivos (ver Sección 2). El juego requiere recolectar **todas las 10 monedas** para poder completar la meta final.
4.  **Enemigos (Riesgos y Amenazas):** Contactar con estos obstáculos provoca el reinicio inmediato del nivel, ilustrando el peligro de la ignorancia o la falta de precaución legal:
    * **Volatilidad (Picos):** Riesgo de pérdida económica por fluctuaciones rápidas de precio.
    * **Estafa (_Scam_ - Pirámide):** Riesgo de caer en esquemas Ponzi o fraudes.
    * **Vacío Legal (Signo ?):** Riesgo de operar en áreas sin normativa clara o protección.
    * **Anonimato Ilícito (Fantasma):** Riesgo de involucrarse en lavado de activos o actividades delictivas facilitadas por la privacidad de algunas redes.
5.  **Meta (Balanza de la Justicia):** El punto final del nivel. Solo puede ser alcanzado con éxito si el jugador ha adquirido todo el **Conocimiento (10/10)**, simbolizando que solo a través de la formación jurídica completa se puede alcanzar la equidad y la resolución del problema.

---

## 4. Estructura Técnica (Código Base HTML/JavaScript)

El juego es una aplicación web simple que requiere únicamente un navegador moderno.

### 🌐 Tecnologías Utilizadas

* **HTML5:** Estructura de la página y elementos de _interfaz de usuario_ (HUD, Pantalla de inicio, Modal).
* **CSS / Tailwind CSS:** Estilización y diseño _responsive_ y estética _pixel-art_ (mediante la fuente 'Press Start 2P').
* **JavaScript (Vainilla):** Toda la lógica del juego (motor, físicas, detección de colisiones, renderizado y manejo de datos académicos) se implementa directamente con JavaScript en el _frontend_.
* **Canvas API:** Utilizada para el renderizado de gráficos del juego (personaje, plataformas, enemigos, meta).

### 🛠️ Configuración y Componentes Clave

| Componente | Descripción Técnica |
| :--- | :--- |
| **`COIN_FACTS`** | Arreglo de objetos JavaScript que almacena los **10 puntos de conocimiento** extraídos del contenido académico, que se muestran al recolectar cada moneda. |
| **`ENEMY_RISKS`** | Objeto que define los **títulos y descripciones de los riesgos** que actúan como "enemigos", provocando el reinicio del juego. |
| **Bucle Principal (`gameLoop`)** | Función de alta frecuencia que gestiona la **lógica del juego (`update()`)** y el **dibujo (`draw()`)** utilizando `requestAnimationFrame` para un rendimiento óptimo. |
| **Colisiones** | Implementación de lógica de colisión para el _plataformas_ que maneja la interacción del jugador con plataformas, monedas y enemigos, además de la lógica de cámara (`ctx.translate`). |
| **Modales (`showModal`)** | Función crucial para la **entrega de contenido académico**. Pausa el juego y presenta la información de manera didáctica y obligatoria para el avance. |

---

## 5. Integrantes del Equipo

Este proyecto fue desarrollado por el equipo de estudiantes del curso:

* [**Belinda Carillo**] - [Rol/Función en el proyecto (Diseño de Contenido Jurídico)]
* [**Daniela Ospina**] - [Rol/Función en el proyecto (Desarrollo de la Lógica de Juego)]
* [**Sofía Manco Jaramillo**] - [Rol/Función en el proyecto (Diseño Gráfico/UI)]
* [**Kady**] - [Rol/Función en el proyecto (Documentación)]

---

## 6. Ejecución y Despliegue

Dado que es una aplicación puramente _frontend_ (HTML, CSS, JS), su ejecución es extremadamente simple:

1.  **Descargar el archivo** `index.html` (o el código completo).
2.  **Abrir el archivo** `index.html` directamente en cualquier navegador web moderno (Chrome, Firefox, Edge).

No se requiere ningún servidor web (como Node.js o Python HTTP Server) para su funcionamiento.