# Prompts utilizados – LTI ATS Design (MBC)

Este documento recoge los prompts empleados con el asistente Claude para generar los artefactos del documento `LTI-MBC.md`.

---

## 1. Prompt inicial – Descripción del producto y ventajas competitivas

```
Eres un experto en producto y estrategia de software B2B SaaS.
Necesito que diseñes el producto LTI, una startup que quiere crear el ATS
(Applicant Tracking System) del futuro.

Define:
- Una descripción breve y atractiva del software
- El valor añadido y las ventajas competitivas frente a ATS tradicionales
  (como Workday, Greenhouse, Lever)
- Las funciones principales que lo harán destacar, incluyendo:
  eficiencia para RRHH, colaboración en tiempo real, automatizaciones
  e inteligencia artificial

Sé específico sobre las capacidades de IA y colaboración.
Usa un tono profesional pero dinámico.
```

---

## 2. Prompt – Lean Canvas

```
Crea un Lean Canvas completo para LTI, el ATS con IA descrito anteriormente.
Incluye los 9 bloques estándar del modelo:
1. Problema
2. Solución
3. Propuesta de valor única
4. Ventaja injusta
5. Segmentos de clientes
6. Métricas clave
7. Canales
8. Estructura de costes
9. Fuentes de ingresos

Represéntalo primero como tabla ASCII/texto estructurado y luego como
diagrama Mermaid con subgrafos o nodos descriptivos.
```

---

## 3. Prompt – Casos de uso principales

```
Define los 3 casos de uso más importantes del ATS LTI. Para cada uno:
- Nombre descriptivo del caso de uso
- Descripción del flujo
- Actores involucrados
- Flujo principal paso a paso
- Diagrama Mermaid que lo represente (usa flowchart, sequenceDiagram
  o el tipo más adecuado para cada caso)

Los casos de uso deben cubrir las funcionalidades más diferenciadoras:
cribado con IA, colaboración reclutador-manager y gestión de entrevistas.
```

---

## 4. Prompt – Modelo de datos

```
Diseña el modelo de datos completo para el ATS LTI. Incluye:
- Todas las entidades principales del sistema
- Para cada entidad: nombre, atributos con nombre y tipo de dato
- Las relaciones entre entidades (cardinalidad)

Las entidades deben cubrir: organizaciones, usuarios, ofertas de trabajo,
candidatos, aplicaciones, entrevistas, evaluaciones, scorecards,
notificaciones, automatizaciones y análisis de IA.

Represéntalo como diagrama Mermaid erDiagram.
```

---

## 5. Prompt – Diseño de alto nivel

```
Diseña la arquitectura de alto nivel del sistema LTI siguiendo principios
de microservicios cloud-native. Incluye:

- Descripción de las capas: presentación, API Gateway, microservicios,
  mensajería, datos e IA
- Lista de microservicios por dominio de negocio con su responsabilidad
- Stack tecnológico sugerido (AWS, Kafka, PostgreSQL, Redis, Elasticsearch, etc.)
- Servicios externos integrados (LinkedIn, calendarios, proveedores LLM)

Representa la arquitectura como diagrama Mermaid graph TB con subgrafos
por capa. Usa emojis para mejorar la legibilidad visual.
```

---

## 6. Prompt – Diagrama C4 del AI Service

```
Crea un diagrama C4 completo para el componente "AI Service" del ATS LTI,
que es el más diferenciador del sistema.

Genera los 4 niveles:
1. Nivel 1 - Contexto: posición del sistema LTI en su entorno
2. Nivel 2 - Contenedores: todos los contenedores dentro del AI Service
   (APIs, workers, servicios de embedding, bases de datos propias)
3. Nivel 3 - Componentes: detalle del componente más complejo del AI Service,
   el CV Analyser Worker, con todos sus componentes internos y relaciones
4. (Nivel 4 queda implícito en el código)

Usa la sintaxis C4 de Mermaid (C4Context, C4Container, C4Component).
Muestra flujos de datos y dependencias entre componentes.
```

---

## 7. Prompt de integración y estructura del documento

```
Genera un documento Markdown completo y bien estructurado llamado LTI-MBC.md
que integre todos los artefactos anteriores en el siguiente orden:

1. Descripción del producto (con tabla comparativa ATS tradicional vs LTI)
2. Lean Canvas (ASCII + Mermaid)
3. Los 3 casos de uso con sus diagramas Mermaid
4. Modelo de datos completo erDiagram
5. Diseño de alto nivel con descripción y diagrama
6. Diagrama C4 con los 3 niveles (Contexto, Contenedores, Componentes)

Añade un índice al inicio, usa encabezados claros (H2/H3) y termina
con un resumen ejecutivo. El tono debe ser profesional y orientado
a un equipo de desarrollo que va a implementar el sistema.
```

---
