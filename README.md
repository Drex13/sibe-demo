# SIBE: Sistema Integrado de Bienestar Estudiantil (demo)

> **Prototipo académico. Datos ficticios. No es un servicio real de atención.**
> Si tú o alguien que conoces necesita ayuda, en Colombia puedes llamar a la **Línea 106** (apoyo emocional) o a la **Línea 123** (emergencias).

## ¿Qué es SIBE?

SIBE es una propuesta desarrollada para el curso de Emprendimiento de la Universidad del Cauca. Plantea una plataforma de bienestar estudiantil que conecta a tres actores:

- **Estudiantes**, que tienen salas de chat anónimas por tema, una consejera virtual y un seguimiento de su estado de ánimo.
- **Profesionales de bienestar** (PermaneSer y Salud Integral), que reciben alertas cuando aparecen señales de riesgo y pueden contactar al estudiante y agendarle una cita.
- **Docentes**, que pueden remitir una preocupación sobre un estudiante sin ver su perfil.

Este repositorio contiene una **demo navegable**. Todo funciona en el navegador, con datos simulados. No hay servidor ni base de datos, y nada de lo que escribas se guarda ni se envía a ninguna parte.

## Qué muestra la demo

La versión actual es la **1.1** ([`index.html`](index.html)). Es una sola página con un estilo visual colorido y cercano, pensado para estudiantes, que permite recorrer los tres roles del sistema.

Enlace: https://drex13.github.io/sibe-demo/

## Cómo recorrerla

En la parte superior hay un selector **Vista de demo** para cambiar de rol en cualquier momento.

### 1. Estudiante

1. Acepta el consentimiento informado ("Acepto y quiero participar"). Si eliges "Solo ver recursos de ayuda", solo verás las líneas de atención.
2. **Inicio**: haz un chequeo rápido de ánimo y mira los accesos principales.
3. **Salas**: entra a una sala (por ejemplo, *Ansiedad*) y lee la conversación anónima.
4. **Consejera**: prueba frases como "tengo ansiedad" o "quiero agendar una cita" y sigue el flujo hasta solicitar la cita.
5. **Mi proceso**: revisa la gráfica de ánimo por semana y el resumen de las últimas semanas.

### 2. Profesional

1. **Panel**: revisa las alertas (crítica, alta y media) y selecciona una para ver el detalle: fragmento detectado, gráfica de ánimo y línea de tiempo.
2. Pulsa **Contactar y agendar cita**, elige dependencia y horario, o marca la alerta como revisada.
3. **Citas**: consulta las citas solicitadas y confirmadas.

### 3. Docente

1. **Remitir**: elige un estudiante, marca lo que has observado y envía el aviso al equipo de bienestar.
2. **Guía**: lee las recomendaciones para acercarte a un estudiante que parece estar pasándola mal.

### Flujo de alerta (el recorrido principal)

1. Como **Estudiante**, entra a una sala de chat.
2. Escribe una frase de riesgo, por ejemplo: *"me quiero hacer daño"*.
3. Aparece un recuadro de ayuda con las líneas de atención, visible solo para quien escribió.
4. Cambia al rol **Profesional**: en el **Panel** aparece una nueva alerta crítica con el mensaje, lista para gestionar.

Lo mismo ocurre si escribes una frase de riesgo en el chat con la **Consejera**.

## Nota importante sobre la "IA"

La demo menciona una inteligencia artificial, pero **no usa ningún modelo de IA real**. La detección de riesgo y las respuestas de la consejera se basan en **búsqueda de palabras clave** (expresiones regulares) y en respuestas escritas de antemano. Sirven para ilustrar la experiencia propuesta, no para evaluar el riesgo de nadie. Un sistema real necesitaría validación clínica, supervisión profesional y un tratamiento de datos acorde con la Ley 1581 de 2012.

## Detalles técnicos

- Cada página es un único archivo HTML con su CSS y JavaScript incluidos.
- Se publica con GitHub Pages desde la rama `main`, carpeta raíz.
- Las páginas incluyen `<meta name="robots" content="noindex">` para que no aparezcan en buscadores.
