# ⚖️🤖 Proyecto Final — Derecho e Inteligencia Artificial

**Pontificia Universidad Javeriana** · 2026-II · **Docente:** Pedro Ardila  
**Estudiante:** Beatriz Muñoz Prieto | **Nombre del proyecto:** TituloCheck 360 | **Fecha de inicio:** 2026-08-03  
**Repositorio:** [Beatrizmunozprieto/Estudio-de-T-tulos](https://github.com/Beatrizmunozprieto/Estudio-de-T-tulos)

---

## 📋 Parte 1 — Descripción del proyecto

### 1.1 El problema jurídico

En Colombia, la adquisición de bienes raíces representa una de las inversiones patrimoniales más trascendentales para las personas naturales y familias. No obstante, el análisis de los antecedentes registrales a través del **Certificado de Tradición y Libertad (CTL)** y las escrituras públicas notariales constituye un proceso complejo, técnico y opaco para el ciudadano no jurista.

El sistema registral colombiano (regulado por la Ley 1579 de 2012) se basa en un folio real dividido en seis columnas técnicas (tradición, gravámenes, medidas cautelares, limitaciones al dominio, cancelaciones y falsa tradición). Un ciudadano común que recibe un folio no logra determinar con facilidad si una hipoteca abierta anterior fue efectivamente cancelada, si una anotación de embargo saca el bien del comercio, si existe una afectación a vivienda familiar que exija la firma obligatoria del cónyuge, o si el predio está viciado por una "falsa tradición" que no transfiere el dominio pleno. 

Esta asimetría informativa propicia fraudes inmobiliarios, desembolso apresurado de arras en promesas de compraventa nulas de pleno derecho y una saturación de litigios civiles por saneamiento por evicción. **TituloCheck 360** busca cerrar esta brecha mediante un asistente analítico pedagógico que procesa y clasifica las anotaciones registrales en un semáforo de riesgo tricolor, una reconstrucción de la cadena de tradición (tracto sucesivo), un inventario de gravámenes vigentes vs. cancelados y un glosario notarial en lenguaje claro.

### 1.2 Usuarios

El usuario principal es cualquier ciudadano colombiano que se encuentre evaluando la compra o arriendo de un inmueble (casa, apartamento, lote o finca) y necesite entender los antecedentes de la matrícula inmobiliaria antes de firmar documentos o transferir dinero. Asimismo, la herramienta es de utilidad para estudiantes de derecho, consultorios jurídicos, asesores inmobiliarios independientes y pequeños inversionistas que requieren un pre-diagnóstico registral ágil.

El usuario ideal es:  
> *“Un ciudadano colombiano que está por comprar una vivienda usada, recibió el Certificado de Tradición y Libertad por parte del vendedor y necesita verificar en minutos si el predio está libre de embargos o hipotecas, quiénes son los dueños reales y qué condiciones legales debe exigir en la promesa de compraventa.”*

### 1.3 Qué hace y qué NO hace

| ✅ Sí hace | ❌ No hace |
| :--- | :--- |
| Analiza y clasifica anotaciones de Certificados de Tradición y Libertad (CTL) y títulos notariales. | No constituye asesoría jurídica formal ni reemplaza el estudio de títulos definitivo de un abogado o notario. |
| Determina un **Semáforo de Riesgo Jurídico** (Verde = Viable, Amarillo = Precaución saneable, Rojo = Alto Riesgo). | No valida físicamente el inmueble en terreno ni verifica linderos topográficos o licencias de construcción. |
| Discrimina con base en el principio de tracto sucesivo si un gravamen está **VIGENTE** o **CANCELADO**. | No gestiona trámites de registro ante las Oficinas de Registro de Instrumentos Públicos (ORIP) ni ante notarías. |
| Identifica limitaciones legales como Afectación a Vivienda Familiar, Patrimonio de Familia y Embargos. | No redacta promesas de compraventa vinculantes ni minutas de escrituras públicas definitivas. |
| Funciona tanto con modelos LLM en la nube (OpenRouter) como con un motor analítico local autónomo sin costo ni API Key. | No almacena ni procesa datos sensibles ni cédulas de ciudadanía (Ley 1581 de 2012). |
| Traduce conceptos notariales y procesales a un glosario pedagógico en lenguaje ciudadano claro. | No asume responsabilidad patrimonial por negociaciones o pagos realizados entre particulares. |

### 1.4 Marco jurídico y fuentes

El marco jurídico de **TituloCheck 360** descansa sobre la legislación civil, registral y notarial colombiana:

* **Ley 1579 de 2012 (Estatuto de Registro de Instrumentos Públicos):**
  * *Art. 2 y 3:* Principios de rogación, legalidad, prioridad o rango, y tracto sucesivo.
  * *Art. 8:* Clasificación sistemática del folio real en las 6 columnas registrales.
* **Código Civil Colombiano:**
  * *Art. 756:* Tradición del dominio de los bienes raíces mediante la inscripción en la ORIP.
  * *Art. 1521:* Objeto ilícito en la enajenación de bienes embargados por decreto judicial.
  * *Art. 1857 y 1893:* Solemnidad de la venta de bienes inmuebles y saneamiento por evicción.
* **Ley 258 de 1996 y Ley 854 de 2003:** Afectación a Vivienda Familiar y obligatoriedad de la doble firma conyugal para su gravamen o enajenación.
* **Ley 70 de 1931 y Ley 861 de 2003:** Constitución y trámite de desafectación de Patrimonio de Familia Inembargable con presencia de hijos menores de edad.
* **Ley 675 de 2001 (Régimen de Propiedad Horizontal):** Exigibilidad del paz y salvo de expensas comunes ordinarias y extraordinarias.
* **Decreto 960 de 1970 (Estatuto del Notariado):** Protocolización de escrituras públicas y comprobantes fiscales (paz y salvo predial y valorización).
* **Ley 1581 de 2012 (Habeas Data):** Anonimización y protección de datos personales.

### 1.5 Nombre y lema

**TituloCheck 360**  
*“Seguridad jurídica inmobiliaria al alcance de todos.”*

El nombre reúne el objeto central de la verificación del título registral (*TituloCheck*) con un análisis panorámico e integral (*360°*). El lema refleja el objetivo democratizador: brindar a cualquier comprador o propietario la claridad necesaria para proteger su patrimonio.

---

## 🗺️ Parte 2 — Plan de desarrollo

El proyecto se estructuró a lo largo de cinco semanas siguiendo los hitos metodológicos del curso:

### Hitos del proyecto

* **M0 — Descripción y plan:** Delimitación de las fallas del análisis empírico de certificados inmobiliarios, definición de usuarios y delimitación del alcance frente al Estatuto de Registro (Ley 1579 de 2012).
* **M1 — Asistente con instrucciones v1:** Diseño y calibración del prompt de sistema que obliga a estructurar la salida en un esquema JSON de 6 componentes analíticos y glosario.
* **M2 — Casos de prueba documentados:** Formulación de 5 casos representativos (hipoteca con afectación familiar, embargo y falsa tradición, propiedad horizontal limpia, patrimonio con menores, y caso libre) en `docs/casos-de-prueba.md`.
* **M3 — Corpus conectado (RAG):** Consolidación de la base de conocimiento normativo en `corpus/normatividad_inmobiliaria.md` y reglas lógicas de pareo para cancelaciones registrales.
* **M4 — Interfaz web desplegada:** Desarrollo de una aplicación web accesible con diseño institucional en HTML5, CSS3 y Vanilla JavaScript, desplegable en GitHub Pages.
* **M5 — Análisis crítico y demo:** Validación de campo con usuario real (`docs/evidencia-usuario.md`), límites del modelo y sustentación académica.

### Bitácora de avance semanal

| Semana | Qué hice | Enlace / Documento | Dudas para la clase |
| :---: | :--- | :--- | :--- |
| **1** | Delimitación del problema de la opacidad de los certificados de libertad; definición del alcance y fuentes notariales. | [README — Parte 1](#-parte-1--descripción-del-proyecto) | ¿Cómo diferenciar la asesoría jurídica de un pre-diagnóstico registral pedagógico? |
| **2** | Diseño del prompt de sistema v1 con esquema JSON estricto y semáforo de riesgo. | [prompts/prompt_sistema_v1.md](file:///Users/beatrizmunozprieto/.gemini/antigravity/scratch/Estudio-de-T-tulos/prompts/prompt_sistema_v1.md) | ¿Qué variables determinan automáticamente un semáforo rojo vs. amarillo? |
| **3** | Creación del corpus normativo registral e incorporación de reglas de tracto sucesivo y cancelaciones. | [corpus/normatividad_inmobiliaria.md](file:///Users/beatrizmunozprieto/.gemini/antigravity/scratch/Estudio-de-T-tulos/corpus/normatividad_inmobiliaria.md) | ¿Cómo procesar folios de tradición de más de 30 anotaciones sin saturar contexto? |
| **4** | Programación del frontend interactivo, integración de motor analítico local y despliegue web. | [index.html](file:///Users/beatrizmunozprieto/.gemini/antigravity/scratch/Estudio-de-T-tulos/index.html) | ¿Cómo asegurar el funcionamiento sin requerir obligatoriamente API Keys costosas? |
| **5** | Prueba de usabilidad con comprador real, documentación de casos de prueba y redacción del análisis ético. | [docs/evidencia-usuario.md](file:///Users/beatrizmunozprieto/.gemini/antigravity/scratch/Estudio-de-T-tulos/docs/evidencia-usuario.md) | ¿Qué salvaguardas legales blindan a la plataforma frente a reclamos de usuarios? |

---

## 🛠️ Parte 3 — Stack técnico

| Pieza | Herramienta | Función |
| :--- | :--- | :--- |
| **Interfaz web** | HTML5 + CSS3 (Diseño institucional Javeriana) | Formulario interactivo, selector de casos, semáforo visual y tarjetas de diagnóstico. |
| **Lógica y Orquestación** | JavaScript Vanilla | Procesamiento de texto, parseo de expresiones regulares notariales y renderizado dinámico. |
| **Modelo LLM en la Nube** | OpenRouter (LLaMA 3.3 70B / Gemini) | Motor de lenguaje avanzado opcional activable si el usuario suministra su API Key. |
| **Motor Analítico Local** | Motor determinista de reglas semánticas | Análisis instantáneo, 100% gratuito y privado sin necesidad de conexión externa ni consumo de tokens. |
| **Corpus Jurídico** | Markdown en `/corpus` y `/docs` | Base normativa con el Estatuto de Registro, Código Civil y causales de nulidad. |
| **Control de versiones** | Git + GitHub | Gestión de código y trazabilidad del repositorio. |
| **Despliegue** | GitHub Pages | Despliegue estático y público accesible desde móviles y computadores. |

### Arquitectura del sistema

```text
                    ┌─────────────────────────┐
                    │     CIUDADANO / USUARIO │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │    INTERFAZ WEB         │
                    │   (GitHub Pages / HTML) │
                    └────────────┬────────────┘
                                 │
                     ┌───────────┴───────────┐
                     ▼                       ▼
            [¿Tiene API Key?]       [Sin API Key (Gratis)]
                     │                       │
                     ▼                       ▼
         ┌───────────────────────┐ ┌───────────────────────────┐
         │      OPENROUTER       │ │   MOTOR ANALÍTICO LOCAL   │
         │  (LLaMA 3.3 / Gemini) │ │   - Reglas Ley 1579/12    │
         │   Prompt Estructurado │ │   - Pareo de cancelaciones│
         └───────────┬───────────┘ └─────────────┬─────────────┘
                     │                           │
                     └─────────────┬─────────────┘
                                   │
                                   ▼
                    ┌─────────────────────────┐
                    │ INFORME 360° PRELIMINAR │
                    │ 1. Semáforo de Riesgo   │
                    │ 2. Ficha del Inmueble   │
                    │ 3. Cadena de Tradición  │
                    │ 4. Gravámenes Vigentes  │
                    │ 5. Acciones Previas     │
                    │ 6. Glosario Ciudadano   │
                    └─────────────────────────┘
```

---

## 🚀 Parte 4 — Despliegue

La aplicación fue desarrollada para funcionar como una **Single Page Application (SPA)** nativa, sin dependencias pesadas ni servidores backend intermediarios, lo que garantiza máxima velocidad y compatibilidad en cualquier navegador.

### URL pública

🔗 **https://beatrizmunozprieto.github.io/Estudio-de-T-tulos/**

### Checklist de despliegue

- [x] Interfaz web estilizada y 100% responsiva (móviles y escritorio).
- [x] Compatibilidad total en Safari, Chrome, Edge y Firefox sin plugins.
- [x] Advertencia legal obligatoria destacada en la parte superior.
- [x] Motor analítico local integrado para funcionamiento offline inmediato.
- [x] Protección estricta de datos (no se recopilan datos personales ni se almacenan en bases de datos).
- [x] Sin exposición de API Keys en el código fuente.
- [x] Documentación y casos de prueba completos en el repositorio.

---

## 🧠 Parte 5 — Guía de prompting para vibe coding

El desarrollo se llevó a cabo utilizando inteligencia artificial para acelerar la programación orientada a resultados (**vibe coding**), bajo un estricto control conceptual jurídico:

* **M0 — Delimitación:** Se definió la taxonomía de riesgos registrales en Colombia, dividiendo los hallazgos en tres niveles (Verde: transferible; Amarillo: requiere saneamiento previo; Rojo: objeto ilícito o prohibición de enajenar).
* **M1 — Instrucciones del asistente:** Se diseñó el prompt de sistema obligando al modelo a responder estrictamente en un objeto JSON con claves para `inmueble`, `semaforoRiesgo`, `dictamen`, `cadenaTradicion`, `limitacionesYGravamenes`, `recomendaciones` y `glosario`.
* **M2 — Pruebas y Calibración:** Se calibró el prompt para evitar que confunda hipotecas canceladas con hipotecas activas, verificando que consulte la columna 5 de cancelaciones.
* **M3 — Base de conocimiento:** Se alimentó con las definiciones de los códigos notariales más comunes en Colombia (0101 compraventa, 0208 hipoteca, 0314 afectación vivienda familiar, 0401 embargo, 0501 cancelación, 0601 falsa tradición).
* **M4 — Interfaz UI:** Se construyeron los componentes visuales con estética institucional, contrastes de accesibilidad WCAG y un botón para imprimir o exportar a PDF el resumen ejecutivo.

---

## ⚖️ Parte 6 — Ética, datos y responsabilidad

* **Advertencia legal visible:** La interfaz advierte de forma explícita que el informe no reemplaza el concepto de un abogado especialista ni la labor de la notaría.
* **Protección de datos (Ley 1581 de 2012):** La herramienta no envía datos personales a bases de datos ni almacena registros. El análisis se procesa de forma efímera en la memoria local del navegador.
* **Prevención de alucinaciones:** El asistente tiene la instrucción expresa de calificar como "No especificado" cualquier dato que no se desprenda textualmente del extracto suministrado, absteniéndose de inventar fechas o actos jurídicos.

---

## 🔍 Parte 7 — Análisis crítico

### 7.1 ¿Dónde falla la herramienta?
1. **Falsas tradiciones con múltiples posesiones superpuestas:** En predios rurales con cadenas de cesión de derechos informales de vieja data, la IA puede identificar que existe falsa tradición, pero no puede inferir si se han cumplido los tiempos para una prescripción adquisitiva ordinaria o extraordinaria.
2. **Segregaciones y desenglobes en escrituras matrices extensas:** Cuando un folio matriz no detalla de forma clara el lote segregado o existen incongruencias de linderos en escrituras complejas, se requiere necesariamente cotejo topográfico y catastral físico.

### 7.2 ¿Qué datos procesa?
* **Entrada:** Texto copiado o transcrito de anotaciones de un Certificado de Tradición y Libertad.
* **Procesamiento:** Detección de entidades notariales, cotejo de códigos de especificación registral, validación de cancelaciones y clasificación de riesgo.
* **Salida:** Informe ejecutivo modular en 6 tarjetas pedagógicas.
* **Almacenamiento:** Cero almacenamiento permanente.

### 7.3 ¿Por qué no reemplaza al abogado?
El estudio de títulos no se agota en la lectura del certificado de matrícula. Un abogado especialista realiza una auditoría jurídica que incluye el estudio de las escrituras matrices de los últimos 10 a 20 años, la revisión de licencias urbanísticas, la verificación de capacidad y estado civil de los otorgantes al momento de la venta, la comprobación de poderes notariales y el análisis de posibles demandas de pertenencia o procesos de restitución de tierras no inscritos oportunamente. **TituloCheck 360** es un filtro preventivo y pedagógico para el comprador, pero la seguridad jurídica definitiva exige la intervención profesional.

---

## 📚 Parte 8 — Casos de prueba

Los 5 casos emblemáticos se encuentran detallados con sus textos originales y salidas esperadas en:  
📁 [docs/casos-de-prueba.md](file:///Users/beatrizmunozprieto/.gemini/antigravity/scratch/Estudio-de-T-tulos/docs/casos-de-prueba.md)

1. **Caso 1:** Inmueble con Hipoteca Bancaria Activa y Afectación a Vivienda Familiar (Riesgo: 🟡 AMARILLO).
2. **Caso 2:** Inmueble con Embargo Ejecutivo Vigente y Falsa Tradición (Riesgo: 🔴 ROJO).
3. **Caso 3:** Apartamento en Propiedad Horizontal con Hipoteca Cancelada (Riesgo: 🟢 VERDE).
4. **Caso 4:** Inmueble con Patrimonio de Familia e Hijos Menores de Edad (Riesgo: 🟡 AMARILLO).
5. **Caso 5:** Entrada Libre / Certificado Propio del Usuario.

---

## 👤 Parte 9 — Prueba con usuario real

La validación con una persona externa sin conocimientos jurídicos se encuentra documentada en:  
📁 [docs/evidencia-usuario.md](file:///Users/beatrizmunozprieto/.gemini/antigravity/scratch/Estudio-de-T-tulos/docs/evidencia-usuario.md)

La participante logró identificar en menos de 45 segundos que el inmueble consultado exigía la comparecencia obligatoria de la cónyuge del vendedor y la cancelación previa de la hipoteca bancaria, evitando la entrega de un anticipo irregular.

---

## ✅ Parte 10 — Estado final del proyecto

| Requisito | Estado |
| :--- | :---: |
| Problema jurídico definido y delimitado | ✅ |
| Usuario objetivo definido | ✅ |
| Alcance delimitado (Qué hace y qué NO hace) | ✅ |
| Marco jurídico registral y civil seleccionado | ✅ |
| Prompt de sistema calibrado en JSON | ✅ |
| Casos de prueba documentados (5 casos) | ✅ |
| Corpus normativo y glosario implementados | ✅ |
| Interfaz web desarrollada, accesible y estilizada | ✅ |
| Advertencia legal obligatoria destacada | ✅ |
| Protección de datos y privacidad contemplada | ✅ |
| Análisis crítico y limitaciones redactadas | ✅ |
| Prueba con usuario real externo realizada | ✅ |
| URL pública desplegada y funcional | 🔗 [Ver en vivo](https://beatrizmunozprieto.github.io/Estudio-de-T-tulos/) |
| Historial de desarrollo en GitHub | ✅ |

---

## 🎓 Conclusión

**TituloCheck 360** demuestra cómo la inteligencia artificial y el diseño de lenguaje claro pueden transformar un trámite históricamente árido e intimidante en una experiencia comprensible para la ciudadanía. Al desglosar el folio de matrícula en un semáforo de riesgo y clarificar el estado real de los gravámenes, la herramienta empodera a los ciudadanos en la defensa de su patrimonio y promueve una cultura de prevención en el mercado inmobiliario colombiano.

*Construido con asistencia de IA — Pontificia Universidad Javeriana 2026-II.*
