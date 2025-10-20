# Prompts del proyecto


> Dime las etapas para un proyecto de una startup 

| Etapa | Objetivo | Herramienta o entregable típico |
|--------|-----------|--------------------------------|
| **1. Descubrimiento** | Comprender el problema, el mercado y el cliente. | 🧩 **Lean Canvas**, entrevistas, mapa de empatía, análisis de mercado. |
| **2. Definición** | Clarificar la propuesta de valor y el alcance inicial. | ✍️ **Value Proposition Canvas**, definición del MVP, user personas. |
| **3. Diseño del producto** | Traducir el modelo de negocio a funcionalidades concretas. | ⚙️ Lista de **requisitos**, **casos de uso**, **user stories**. |
| **4. Modelado del sistema** | Estructurar los datos y arquitectura. | 🧱 **Modelo de datos**, **diagramas UML/C4**. |
| **5. Implementación y validación** | Construir el MVP y probarlo con usuarios reales. | 🚀 MVP funcional, pruebas, retroalimentación. |




## Investigación y análisis de requisitos


A. Entendiendo que es un ATS.

> Dime es que un ATS?.   


B. Para conocer las funcionalidades y los mejores ATS del mercado.

> Eres un experto en producto, con experiencia en ATS (Applicant-Tracking System).
Somos una startup llamada LTI y queremos crear un ATS (Applicant-Tracking System) del futuro.
Haz un análisis de los mejores ATS del mercado y con ellos haz una matriz de “brechas de funcionalidad” (qué ofrecen / qué no ofrecen) que nos sirva para definir mejor nuestro diferencial. Necesitamos encontrar el valor añadido y nuestras ventajas competitivas. Queremos: 
- Aumentar la eficiencia para los departamentos de HR
- Mejorar la colaboración en tiempo real entre reclutadores y managers
- Automatizaciones
- Asistencia de IA en diversas tareas
- Y algunas otras innovaciones que nos hagan diferenciar de las actuales ATS.

> Generame un documento en markdown descargable con la información que obtengas.


> Podrias realizar el diagrama Lean Canvas para entender el modelo de negocio.
> En que sección del documento "Análisis Competitivo de Sistemas ATS (Applicant Tracking System)" integrariamos lo de Lean Canvas ?
> Pasemos a la Diseño del producto


## C. Diseño del Producto

Opción 1 

> Etapa 3: Diseño del producto, cuyo objetivo es traducir el modelo de negocio a funcionalidades concretas del sistema, es decir: convertir las ideas en requisitos claros, casos de uso y user stories.

> Podrias generarme un diagrama general de casos de uso
> 
> podrias darme la descripcion o prompt para generar el diagrama en plantUML
> 
> genera una tabla de trazabilidad completa (funcionalidades → requisitos → casos → user stories) como documento descargable en Markdown o Excel para tu proyecto LTI


> Dame el diagrama para el caso de uso "UC01 – Publicar una vacante"
> Ahora pasemos a el UC02 – Gestionar candidatos en pipeline
> Pasemos ahora al UC03 – Asistente de IA (recomendador)
> Pasemos ahora UC04 – Portal del candidato

-----
Opción 2:

> Eres un analista de software experto. Enumera y describe brevemente los casos de uso más importantes a implementar para lograr una funcionalidad básica

> Representa estos casos de uso en el tipo de diagrama más adecuado usando el formato plantUML. Acorde a la sintaxis y buenas prácticas UML, define y describe lo que sea necesario. 




### Modelado de Datos


> Eres un arquitecto de software experto. Cuales son las entidades de modelo de datos del  LTI ATS (Applicant Tracking System). Dame los campos de cada una y cómo se relacionan


> Eres un brillante arquitecto de software. Eres capaz de diseñar, explicar y diagramar los diferentes aspectos de un sistema de software. 
> Estoy construyendo el sistema LTI ATS (Applicant Tracking System). He definido las entidades con sus campos y relaciones, lo adjunto. 
> Qué otras entidades del modelo de datos son importantes para el sistema LTI ATS (Applicant Tracking System)? Dame los campos más importantes de cada una y cómo se relacionan entre entidades.



### Arquitectura de Alto Nivel

> Eres un arquitecto/a de software senior con experiencia en el diseño de sistemas distribuidos, SaaS y arquitecturas basadas en microservicios.

> Tu tarea es **diseñar la arquitectura de alto nivel del sistema LTI ATS (Applicant Tracking System)**, una plataforma de reclutamiento moderna impulsada por IA.
#### Contexto del sistema
LTI ATS busca revolucionar el proceso de reclutamiento, ofreciendo:
- Eficiencia para departamentos de RRHH mediante automatización.
- Colaboración en tiempo real entre reclutadores y managers.
- Asistencia con IA para filtrado, scoring y recomendación de candidatos.
- Analítica predictiva de contratación.
- Experiencia de usuario fluida para candidatos y equipos.
#### Requisitos de diseño
1. **Patrón arquitectónico principal:** Microservicios.
2. Cada microservicio debe tener su **propia base de datos** (evitar acoplamiento).
3. El sistema debe incluir:
   - Un **frontend** web (React, Angular o similar) que se comunique con una **API Gateway**.
   - **Servicios backend** independientes (vacantes, candidatos, IA, notificaciones, analítica, etc.).
   - **Mensajería asíncrona** para eventos (Kafka, RabbitMQ o AWS SNS/SQS).
   - **Autenticación centralizada** (OAuth2, JWT, o AWS Cognito).
   - **Mecanismos de cacheo y búsqueda** (Redis, Elasticsearch).
   - **Observabilidad completa:** logging, métricas y monitoreo.
4. **Proveedor de nube:** AWS. Usa servicios adecuados (ECS, API Gateway, DynamoDB, CloudFront, ELB, etc.).
5. Incluye **balanceo de carga, CDN y seguridad** a nivel de arquitectura.
6. La arquitectura debe ser **escalable, resiliente y fácil de mantener**.
7. Muestra las **interacciones entre componentes** (cómo el frontend consume la API Gateway, cómo los microservicios se comunican, cómo fluyen los eventos).

>#### Entregables esperados
- Descripción textual de la arquitectura (componentes, responsabilidades y comunicación).
- Diagrama de arquitectura a alto nivel (puede ser en **Mermaid**, **PlantUML** o **Diagrams as Code**).
- Tabla con microservicios propuestos, su propósito y base de datos asociada.
- Explicación de por qué la arquitectura elegida garantiza escalabilidad, seguridad y mantenibilidad.

> #### Ejemplo de salida esperada
- Diagrama que muestre:
  - Frontend → API Gateway → microservicios → bases de datos.
  - Event Bus para comunicación asíncrona.
  - Integraciones externas (correo, IA, firma electrónica, etc.).
  - Balanceo de carga, CDN y monitoreo.
- Breve explicación técnica de las decisiones de diseño.

> **Genera una salida detallada, profesional y documentada en formato Markdown.**



## Diagrama C4 que llegue en profundidad a uno de los componentes del sistema, el que prefieras.

> Eres un arquitecto de software experto en C4. Vamos a realizar una visión integral de la arquitectura de software, mostrando distintos niveles de abstracción (desde la interacción global del sistema con su entorno hasta los detalles de implementación a nivel de código. Veremos primero el nivel 1, y después me preguntarás cuál de ellos queremos expandir en el resto de los niveles.
