# Voice Agent — Idea del proyecto

**Estado:** idea documentada. Sin código y sin decisiones técnicas.
**Fecha:** 8 de noviembre de 2026.
**Autor:** Emiliano Montanari.
**Nombre provisorio:** Voice Agent. El naming definitivo queda abierto.

---

## 1. Qué es

Un agente de voz en tiempo real que conversa con una persona, entiende lo que necesita, consulta información del negocio y ejecuta acciones: agendar un turno, responder una consulta, practicar un idioma o derivar a alguien.

Se ofrece de dos formas sobre la misma idea:

- **Web:** el usuario habla desde el navegador.
- **Teléfono:** el usuario llama a un número real.

La misma base sirve para distintos rubros. Cambia la persona del agente, el conocimiento del negocio y las acciones que puede ejecutar.

---

## 2. El problema

### Del usuario final

- **Alumno de idiomas:** quiere practicar speaking, pero depende de un profesor, de un horario y de animarse a hablar con otra persona.
- **Paciente o cliente:** llama a un negocio, cae en un menú telefónico, espera o no lo atienden.
- **Lead inmobiliario:** consulta y nadie responde rápido; se enfría y compra en otro lado.
- **Dueño de un servicio:** pierde urgencias nocturnas porque no hay quien conteste.

### Del comprador

- **Costo de atención:** cada conversación consume tiempo humano.
- **Cobertura limitada:** no hay atención fuera de horario ni en picos.
- **Pérdida invisible:** llamadas abandonadas, turnos no agendados, leads sin seguimiento.
- **Herramientas rígidas:** los menús telefónicos no entienden lenguaje natural y los chatbots de texto no se usan.

### Por qué ahora

- Hablar con un asistente de voz ya es cotidiano: el usuario final no necesita aprender nada nuevo.
- La conversación por voz se volvió natural y aceptable en la vida diaria.
- El costo por minuto de una conversación automatizada es competitivo frente a una persona.
- La voz en tiempo real todavía no es un commodity, a diferencia del chatbot de texto.

---

## 3. La propuesta

Un agente que escucha, entiende, responde y **actúa por voz en tiempo real**, con:

- Respuesta rápida y natural.
- Interrupciones: el usuario habla y el agente se detiene.
- Una persona configurable: nombre, rol, voz, idioma y objetivo.
- Acciones sobre información real del negocio.
- Derivación a una persona cuando hace falta.
- Registro de la conversación, resumen y métricas.

**La tesis del producto:** la latencia es la feature. Un agente que responde en menos de 800 ms y permite interrumpir se siente humano; uno que tarda dos segundos se abandona.

---

## 4. Evidencia

En el análisis de ~380 avisos de Workana (7–8 de noviembre de 2026) apareció este pedido:

> **Prototipo de teacher virtual de inglés con interacción por voz en tiempo real.**
> Escuela con más de 17 años de experiencia. Avatar masculino realista, voz americana neutral, conversación bidireccional por micrófono, sincronización labial, interrupciones, niveles A1–A2 e interfaz web.
> **Presupuesto:** USD 500–1.000. **Propuestas:** 16.

Es el mejor ratio demanda/competencia de la muestra: presupuesto medio-alto con muy poca competencia.

Evidencia adyacente:

- Un centro médico de Buenos Aires pidió autogestionar turnos por WhatsApp (USD 250–500, 76 propuestas). Valida la demanda de agendamiento, no el canal de voz.
- Un pedido de "soluciones digitales con IA" incluía agentes recepcionistas que agendan llamadas y hacen seguimiento (USD 100–250, 28 propuestas).
- 9 de 21 avisos de la primera página eran bots de atención; la mayoría, commoditizados.

---

## 5. Para quién

| Rol | Quién es | Qué quiere | Qué le preocupa |
|---|---|---|---|
| **Comprador** | Director de escuela, gerente de clínica, dueño de inmobiliaria o de servicios | Atender más, gastar menos, no perder oportunidades | Que el agente diga algo incorrecto o ahuyente al cliente |
| **Usuario final** | Alumno, paciente, lead, cliente | Ser atendido rápido y con naturalidad | Sentirse ignorado o hablar con una máquina torpe |
| **Operador** | Recepcionista, profesor, asesor | Que el agente le quite lo repetitivo | Perder control o tener que corregir todo |
| **Administrador** | Dueño del negocio o responsable de sistemas | Configurar persona, acciones y conocimiento | Dependencia externa y privacidad |

**Job to be done:**

> "Cuando alguien me habla por voz, quiero entenderlo, responderle bien y resolver su necesidad —agendar, informar, practicar o derivar— sin hacerlo esperar y sin inventar nada."

---

## 6. Casos de uso

**Primarios**

- **Tutor de inglés (web):** el alumno practica conversación por niveles, recibe correcciones suaves y al final obtiene un reporte con errores, vocabulario y puntaje.
- **Recepcionista de negocio (teléfono o web):** el usuario pregunta por horarios, servicios o disponibilidad; el agente consulta la agenda, reserva, reprograma o deriva.

**Secundarios**

- **Calificación de leads (inmobiliaria):** pregunta presupuesto, zona y plazo; agenda una visita si el lead califica.
- **Atención nivel 1 (soporte):** responde preguntas frecuentes con conocimiento del negocio y deriva lo complejo.
- **Reservas (restaurantes, gimnasios):** consulta disponibilidad, reserva y confirma.
- **Recuperación de clientes:** contacta a un cliente inactivo, ofrece una promo y agenda.
- **Práctica de entrevistas:** simula una entrevista y da feedback estructurado.

---

## 7. Sectores y prioridad

| Sector | Dolor | Qué hace el agente | Métrica de valor |
|---|---|---|---|
| **Escuelas de idiomas** | Práctica limitada a horarios y profesores | Práctica 24/7, corrección y reporte | Minutos de práctica, retención |
| **Clínicas y consultorios** | Llamadas perdidas, agenda manual, ausentismo | Atiende, agenda, valida y recuerda | Turnos agendados, no-shows |
| **Inmobiliarias** | Respuesta lenta a leads | Responde, califica y agenda visita | Leads calificados, visitas |
| **Servicios para el hogar** | Urgencias nocturnas sin atención | Toma pedido, prioriza urgencia, agenda | Trabajos capturados |
| **Gimnasios** | Consultas repetitivas y churn | Informa, reserva clase, recupera socio | Retención, reservas |
| **Restaurantes** | Reservas y preguntas frecuentes en hora pico | Reserva y responde | Mesas ocupadas |
| **Talleres** | Turnos de service y estado | Agenda y responde estado | Capacidad utilizada |
| **Call centers** | Picos y horario nocturno | Cubre overflow y nivel 1 | Costo por llamada |
| **Seguros y finanzas** | Calificación y agendamiento | Filtra y agenda con compliance | Citas con asesor |
| **RRHH** | Screening inicial | Entrevista y agenda | Tiempo del reclutador |

**Orden de ataque:**

1. **Escuelas de idiomas** — evidencia directa, comprador identificable, demo natural.
2. **Clínicas** — dolor medible y presupuesto; cuidado regulatorio.
3. **Inmobiliarias** — alto valor por lead y venta rápida.
4. **Servicios para el hogar** — retorno directo y ciclo corto.
5. **Gimnasios** — ingreso mensual recurrente y bajo riesgo.

---

## 8. Alcance del MVP

**Incluido**

- Conversación de voz en vivo desde el navegador.
- Interrupciones: el usuario habla y el agente se detiene.
- Persona configurable: nombre, rol, voz, idioma y objetivo.
- Acciones: consultar disponibilidad, reservar, responder con conocimiento y derivar.
- Transcript, resumen y métricas por sesión.
- Dos demos con la misma base: tutor de inglés y recepcionista.
- Límites de duración y costo por sesión.

**Fuera del MVP**

- Telefonía real (fase 2).
- Avatar realista (fase 2, opcional).
- Multiusuario por cliente y facturación.
- Integraciones profundas con sistemas del cliente.
- Entrenamiento de modelos propios.
- Apps móviles.

**Principio de alcance:**

> Si una funcionalidad no mejora la conversación, la latencia o la demostración de valor, va para después.

---

## 9. Cómo se siente una conversación

### Tutor de inglés

| Turno | Quién | Qué dice |
|---|---|---|
| 1 | Agente | "Hi! I'm Alex. We're going to have a short conversation about travel. Ready?" |
| 2 | Alumno | "Yes, but I'm a little nervous." |
| 3 | Agente | "That's normal. We'll go slow. Tell me about the last trip you took." |
| 4 | Alumno | "I go to Bariloche last year with my family." |
| 5 | Agente | "Nice! Small correction: 'I went to Bariloche last year.' What did you like most?" |
| 6 | Alumno | "Wait, what does 'trip' mean?" |
| 7 | Agente | "A trip is a journey, when you travel somewhere. Like your Bariloche trip." |

Cierre: resumen con tres correcciones, cinco palabras nuevas y un puntaje. El profesor recibe el reporte.

### Recepcionista de clínica

| Turno | Quién | Qué dice |
|---|---|---|
| 1 | Agente | "Clínica San Martín, buenas tardes. ¿En qué puedo ayudarte?" |
| 2 | Paciente | "Quiero un turno con el doctor Pérez." |
| 3 | Agente | "Claro. ¿Tenés obra social?" |
| 4 | Paciente | "Sí, OSDE." |
| 5 | Agente | "Perfecto. El doctor Pérez tiene lugar el martes a las 10 o el jueves a las 16. ¿Cuál preferís?" |
| 6 | Paciente | "El jueves." |
| 7 | Agente | "Listo, jueves 16 con el doctor Pérez. Te va a llegar un recordatorio. ¿Algo más?" |

Si el paciente pide algo clínico o el agente no entiende, deriva con un resumen.

---

## 10. Qué tiene que cumplir

- **Latencia:** primer audio p50 < 800 ms y p95 < 1.2 s en conexión estable.
- **Interrupciones:** el agente se detiene en menos de 250 ms.
- **Calidad:** 85% de éxito en conversaciones guionadas.
- **Costo:** menos de USD 0.20 por minuto de conversación.
- **Privacidad:** sin grabación de audio por defecto; retención configurable y borrado por sesión.
- **Idiomas:** español rioplatense e inglés.
- **Disponibilidad:** 99.5% para el demo público.
- **Independencia:** poder cambiar de proveedor sin rehacer el producto.

---

## 11. Métricas de éxito

| Métrica | Definición | Objetivo MVP |
|---|---|---|
| Time to first audio | Desde que el usuario termina de hablar hasta el primer audio del agente | p50 < 800 ms |
| Interruption recovery | Tiempo en detenerse y retomar tras una interrupción | < 250 ms para detenerse |
| Task completion | Reserva confirmada o clase completada | > 80% |
| Containment | Conversaciones resueltas sin humano | > 60% |
| Cost per minute | Costo variable total | < USD 0.20 |
| Eval pass rate | Aserciones aprobadas | > 85% |

Métricas de negocio: sesiones atendidas, turnos agendados por semana, leads calificados, minutos de práctica por alumno, retención a 30 días y costo por conversación vs. humano.

---

## 12. Modelo de negocio

> Todos los precios son **hipótesis a validar** con pilotos. No son una promesa.

| Etapa | Qué incluye | Precio hipotético |
|---|---|---|
| **Demo** | Link o número con un escenario | Gratis |
| **Piloto** | 2 semanas, un escenario, una integración, métricas | USD 500–1.500 |
| **Producción** | Número real, agenda o CRM, soporte | Setup USD 1.000–3.000 + USD 300–800/mes + uso |
| **Uso** | Minutos de conversación | USD 0.40–0.80/min |
| **White-label** | Agencia revende con su marca | USD 500–1.500/mes |

**Objetivo de unit economics:**

```
Precio por minuto           USD 0.50–0.80
Costo variable por minuto   USD 0.10–0.20
Margen bruto                > 60%
```

---

## 13. Go-to-market

**Beachhead: escuelas de idiomas**

- **Comprador:** director académico o dueño.
- **Pitch:** "Tus alumnos practican speaking 24/7 y vos recibís un reporte de progreso. No reemplaza al profesor: lo multiplica."
- **Objeción:** "La IA va a decir barbaridades." → Evaluaciones, límites y revisión del reporte.
- **Objeción:** "Los alumnos quieren hablar con personas." → El agente es práctica adicional, no reemplazo.
- **Prueba:** minutos de práctica y retención a 30 días.

**Después:** clínicas (turnos y no-shows), inmobiliarias (leads calificados), servicios para el hogar (trabajos fuera de horario) y gimnasios (reservas y retención).

**Canal:** demo pública, video de 90 segundos, contacto directo a 20 escuelas y 20 clínicas, LinkedIn con el caso de estudio y alianzas con agencias que ya venden automatización.

---

## 14. Riesgos

| Riesgo | Impacto | Mitigación |
|---|---|---|
| Latencia alta | El usuario abandona | Medir desde el día uno, respuestas cortas, operar cerca del usuario |
| Costo por minuto alto | Margen negativo | Límites por sesión y control del costo por minuto |
| Alucinación | Daño de marca | Acciones obligatorias para datos del negocio y evaluaciones |
| Ruido y acentos | Mala experiencia | Pruebas por sector y push-to-talk de respaldo |
| Regulación (salud) | Bloqueo comercial | No diagnóstico, consentimiento y retención mínima |
| Caída del proveedor | Sesión interrumpida | Continuidad, reintento y mensaje claro |
| Dependencia de un proveedor | Costo y lock-in | Independencia como requisito de producto |
| Avatar costoso | Mala economía | Avatar fuera del camino crítico |
| Expectativa equivocada | Churn | Demo con el escenario real y límites explícitos |

---

## 15. Fases

| Fase | Entregable |
|---|---|
| **0. Idea** | Este documento |
| **1. Núcleo web** | Conversación, interrupciones, persona, transcript |
| **2. Acciones** | Agenda, conocimiento, derivación, administración |
| **3. Teléfono** | Número entrante, transferencia, métricas |
| **4. Verticales** | Tutor, recepcionista, inmobiliaria, servicios |

---

## 16. Preguntas abiertas de producto

1. ¿El beachhead es escuela de idiomas o clínica? La evidencia directa favorece a la escuela; la clínica tiene más presupuesto pero más fricción regulatoria.
2. ¿El avatar entra en el MVP o en fase 2? Hipótesis: fase 2, fuera del camino crítico.
3. ¿El precio por minuto se valida con escuelas? Hacer tres entrevistas antes de publicar la oferta.
4. ¿Se ofrece white-label desde el inicio o después de tres clientes directos?
5. ¿Cuál es la métrica de éxito que el colegio acepta como prueba de valor: minutos de práctica, retención o reporte del profesor?
6. ¿Qué nivel de personalización por cliente es necesario para el primer piloto?

---

## 17. Lo que todavía no está definido

La tecnología, el lenguaje de programación, la arquitectura, los proveedores y la infraestructura **no están decididos**. Se documentan y se eligen después de leer y validar esta idea.
