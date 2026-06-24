# Skill: Notas de Reunión Inteligentes

## 🎯 ¿Qué hace esta skill?
Transforma notas en bruto de una reunión (pasted text) en un documento estructurado con: decisiones tomadas, tareas asignadas, preguntas abiertas y próximos pasos, listo para compartir y ejecutar.

## 📥 ¿Qué input necesita el agente?
**Input del usuario**: Texto crudo pegado del chat:
```
Reunión equipo proyecto IA
Juan: vamos a usar Python para el MVP
María: necesitamos definir arquitectura para viernes
Pedro: yo me encargo de la base de datos
Quedamos en reunirnos el miércoles próximo
Pendiente: decidir herramienta de deployment
```

**Conocimiento previo**:
- Contexto de tus proyectos (AI Engineer training de USER.md)
- Personas con las que trabajas (compañeros, profesores)
- Estilo preferido: claro, con action items destacados
- Formatos útiles para ti (Google Docs, tablas, listas)

## 📤 ¿Cómo es un buen output?
**Formato**: Google Doc estructurado con:
- **📅 Metadatos**: Fecha, participantes, duración
- **✅ Decisiones tomadas**: Qué, quién decidió, cuándo
- **📋 Tareas asignadas**: Quién, qué, deadline
- **❓ Preguntas abiertas**: Qué falta resolver, responsable
- **🚀 Próximos pasos**: Acciones inmediatas, fechas
- **📎 Apéndices**: Notas crudas, referencias, links

**Destino**: Nuevo Google Doc en folder "Reuniones/[Fecha]"
**Validación**: Documento creado con estructura clara que facilita ejecución sin preguntas adicionales

## ⚙️ Implementación Técnica

### Procesamiento de lenguaje natural
**Patrones detectados**:
- Decisiones: "vamos a...", "decidimos...", "acordamos..."
- Tareas: "yo me encargo", "X hará Y", "asignar a..."
- Fechas: "para viernes", "el miércoles próximo", "en 2 semanas"
- Preguntas: "pendiente:", "falta decidir", "por resolver"
- Acciones: "reunirnos", "enviar", "revisar"

**Clasificación automática**:
1. Segmentar por participante/línea
2. Identificar tipo de contenido (decisión/tarea/pregunta)
3. Extraer entidades (personas, fechas, acciones)
4. Estructurar en categorías
5. Inferir relaciones (tarea → responsable → deadline)

### Conexiones necesarias
- Google Docs (ya activa)
- Google Drive (para organización)

### Flujo de ejecución
1. Recibir texto crudo
2. Parsear y clasificar contenido
3. Extraer metadatos (participantes, fechas)
4. Crear estructura de documento
5. Generar Google Doc con formato
6. Compartir con participantes (opcional)
7. Crear tareas en Calendar (opcional)
8. Confirmar con resumen ejecutivo

### Estructura del documento
```
# Reunión: [Título] - [Fecha]

## 👥 Participantes
- Juan (presente)
- María (presente) 
- Pedro (presente)

## ⏱️ Duración
Inicio: HH:MM | Fin: HH:MM | Total: X minutos

## ✅ DECISIONES TOMADAS
| Decisión | Quién | Cuándo |
|----------|-------|--------|
| Usar Python para MVP | Equipo | Inmediato |
| Definir arquitectura | María | Viernes |

## 📋 TAREAS ASIGNADAS
| Tarea | Responsable | Deadline | Estado |
|-------|-------------|----------|--------|
| Base de datos | Pedro | Miércoles | Pendiente |
| Documentación | Juan | Lunes | Pendiente |

## ❓ PREGUNTAS ABIERTAS
1. **Herramienta deployment** (Equipo) - Decidir para jueves
2. **Presupuesto infra** (María) - Confirmar con dirección

## 🚀 PRÓXIMOS PASOS
1. Reunión seguimiento: Miércoles HH:MM
2. Enviar resumen: Hoy EOD
3. Revisar arquitectura: Viernes AM

## 📎 NOTAS CRUDAS
[texto original pegado]
```

## 🔧 Ejemplo de uso
```bash
# Pegar notas después del comando
notas reunion
[paste text here]

# Output:
✅ DOCUMENTO CREADO: "Reunión equipo IA - 2026-06-24"
📄 Google Doc: [link]
📋 3 decisiones, 4 tareas, 2 preguntas identificadas
⏰ Tareas añadidas a Calendar automáticamente
```

## 🧪 Validación de éxito
- ✅ Documento Google creado en folder correcto
- ✅ Estructura clara y fácil de seguir
- ✅ Todas las decisiones/tareas extraídas
- ✅ Fechas y responsables identificados correctamente
- ✅ Acciones ejecutables sin interpretación adicional
- ✅ Tiempo de procesamiento < 30 segundos

## 🔄 Integración con sistema
- **Google Calendar**: Crea eventos para próximas reuniones
- **Gmail**: Envía resumen a participantes
- **MEMORY.md**: Aprende nombres y proyectos recurrentes
- **GitHub**: Crea issues de tareas técnicas
- **Telegram**: Envía resumen ejecutivo inmediato

---

**🧠 Procesamiento NLP avanzado**:
- **Segmentación**: Identifica participantes y sus contribuciones
- **Clasificación**: Decisión vs tarea vs pregunta vs acción
- **Extracción entidades**: Personas, fechas, acciones específicas
- **Relación**: Tarea → Responsable → Deadline

**📊 Métricas de calidad**:
- **Tasa extracción**: % puntos crudos correctamente clasificados
- **Tasa acción**: % tareas con responsable+deadline claros
- **Tiempo proceso**: Segundos desde paste hasta documento
- **Reducción follow-ups**: Menos preguntas de clarificación

**🎯 Casos de uso**:
- Reuniones equipo proyectos
- Clases/tutorías académicas
- Planificación personal
- Brainstorming sessions

---

> *Skill 6/6 - Notas de Reunión*
> *Estado: ✅ Implementada | Conexiones: Google Docs + Calendar*