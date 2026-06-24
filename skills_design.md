# Skills Design - Alfredo

Análisis detallado de las 6 skills solicitadas para Gojo.

---

## 1. Diario de Aprendizaje Diario

### ¿Qué hace esta skill?
Añade entradas estructuradas al diario personal de conocimiento en Google Docs con formato consistente y fecha automática.

### ¿Qué input necesita el agente?
**Input del usuario**: Lista de puntos aprendidos (ej: "aprendí sobre machine learning, practiqué Python")
**Conocimiento previo (de AGENTS.md/USER.md/MEMORY.md)**:
- Alfredo está en formación de AI Engineer
- Intereses: programación, finanzas, fitness
- Estilo de comunicación directo y práctico
- Documento base: "Diario de Aprendizaje - Alfredo" (ya creado)

### ¿Cómo es un buen output?
**Formato**: Markdown estructurado con:
```
## [YYYY-MM-DD]
### 🧠 Qué aprendí hoy
- Punto 1
- Punto 2
### 💡 Insight principal
[reflexión]
### 🎯 Para aplicar mañana
- Acción 1
```
**Destino**: Google Doc "Diario de Aprendizaje - Alfredo"
**Validación**: Verificar que la entrada aparece en el documento con fecha correcta y formato estructurado.

---

## 2. Plan de Semana

### ¿Qué hace esta skill?
Crea un plan semanal priorizado en Google Docs y genera eventos clave en Google Calendar.

### ¿Qué input necesita el agente?
**Input del usuario**: Lista de objetivos y compromisos (ej: "estudiar Python 3h, reunión equipo miércoles, entrenar 4 días")
**Conocimiento previo**:
- Prioridades de Alfredo: carrera, finanzas, salud, relaciones, aprendizaje
- Preferencia por planes accionables y prácticos
- Horarios típicos (de USER.md se podría inferir rutina)

### ¿Cómo es un buen output?
**Formato**: Documento estructurado con:
- Objetivos semanales
- Desglose diario (Lunes-Viernes)
- Bloque de tiempo para cada actividad
- Métricas de éxito
**Destino**:
1. Google Doc "Plan Semanal [fecha]" 
2. Eventos en Google Calendar con recordatorios
**Validación**: Documento creado + eventos visibles en Calendar con horarios correctos.

---

## 3. Notas de Reunión

### ¿Qué hace esta skill?
Transforma notas en bruto de reuniones en decisiones formateadas, tareas y preguntas abiertas.

### ¿Qué input necesita el agente?
**Input del usuario**: Texto crudo de notas de reunión (pegar en chat)
**Conocimiento previo**:
- Contexto de proyectos de Alfredo (AI Engineer training)
- Estilo preferido: claro, con acción items

### ¿Cómo es un buen output?
**Formato**: Documento estructurado con:
- **Decisiones tomadas** (qué, quién, cuándo)
- **Tareas asignadas** (quién, qué, deadline)
- **Preguntas abiertas** (qué falta resolver)
- **Próximos pasos**
**Destino**: Google Drive (nuevo doc por reunión)
**Validación**: Archivo creado en Drive con estructura clara y elementos accionables.

---

## 4. Eventos de Calendar Inteligentes

### ¿Qué hace esta skill?
Interpreta descripciones en lenguaje natural para crear eventos en Google Calendar con todos los detalles.

### ¿Qué input necesita el agente?
**Input del usuario**: Descripción natural (ej: "sesión de estudio el jueves por la tarde, dos horas, con recordatorio")
**Conocimiento previo**:
- Preferencias de Alfredo (tiempos de trabajo típicos)
- Zona horaria (UTC, pero podría ajustar)
- Tipos de eventos recurrentes

### ¿Cómo es un buen output?
**Formato**: Evento de Calendar con:
- Título descriptivo
- Fecha/hora correctas (inferidas de "jueves por la tarde")
- Duración adecuada (2 horas)
- Recordatorios configurados
- Descripción clara
**Destino**: Google Calendar de Alfredo
**Validación**: Evento creado con parámetros correctos, visible en calendario.

---

## 5. Borradores de Gmail con Tu Voz

### ¿Qué hace esta skill?
Crea correos electrónicos en Gmail con el estilo de escritura, tono y firma habitual de Alfredo.

### ¿Qué input necesita el agente?
**Input del usuario**: Puntos clave del correo (para, asunto, puntos a cubrir)
**Conocimiento previo (de USER.md/MEMORY.md)**:
- Estilo de comunicación de Alfredo: directo, práctico
- Tipo de correos que envía (profesionales, personales)
- Firma habitual (si se documenta en memoria)
- Relaciones clave (Ester, compañeros de estudio)

### ¿Cómo es un buen output?
**Formato**: Correo de Gmail con:
- Saludo apropiado
- Estructura clara y directa
- Puntos cubiertos completamente
- Firma consistente
- Tonó profesional pero amigable
**Destino**: Borrador en Gmail (listo para revisión mínima)
**Validación**: Borrador creado que refleja el estilo de Alfredo y necesita pocas correcciones.

---

## 6. Resumen Diario de GitHub

### ¿Qué hace esta skill?
Genera un briefing diario de actividad en GitHub (issues abiertos, commits recientes) y lo envía por Telegram.

### ¿Qué input necesita el agente?
**Input del usuario**: Trigger "resumen github" (o automático diario)
**Conocimiento previo**:
- Repositorios de Alfredo (theazec34)
- Progreso de AI Engineer training
- Métricas que le importan (commits, issues resueltos)

### ¿Cómo es un buen output?
**Formato**: Mensaje de Telegram con:
- Issues abiertos (número, títulos)
- Commits del día (resumen)
- PRs pendientes de revisión
- Recomendaciones de acción
**Destino**: Telegram de Alfredo
**Validación**: Mensaje recibido con información actualizada y útil.

---

## Prioridad de Implementación

1. **Diario de Aprendizaje** ✅ (ya implementada)
2. **Plan de Semana** ✅ (implementada y probada)
3. **Resumen GitHub** (rápido - usa conexión existente)
4. **Eventos Inteligentes** (Calendar solo)
5. **Borradores Gmail** (requiere análisis de estilo)
6. **Notas de Reunión** (más compleja - procesamiento NLP)

**Estado actual**: 
- Conexiones activas: Google Docs, Google Calendar, Gmail, GitHub
- Skills implementadas: 2/6
- Plan maestro activo: 8 semanas
- Sistema de seguimiento: Configurando

---

## Implementación Real

### **Diario de Aprendizaje**
- Documento: https://docs.google.com/document/d/1gNOSnFTOD1FYyEjNVepbxTQY1Oi0dQogeaEqO-ovIcI/edit
- Comando: `diario hoy [aprendizaje]`

### **Plan Semanal**
- Documento maestro: https://docs.google.com/document/d/1AFfgABulBy3YL-fUS-Osp9MZaSB11mh-_NBkRMNPEE0/edit
- Calendario: 6 eventos recurrentes configurados
- Comando: `plan semanal ver`

### **Entrenamiento**
- Progresión 8 semanas detallada
- Timing nutricional estratégico
- Checklists diarios

---

## Configuración de Seguimiento

### **Telegram (Diario)**
- 21:00: Checklist día siguiente
- 8:15: Recordatorio desayuno
- 17:00: Recordatorio entrenamiento
- 22:00: Resumen diario

### **Automático (Semanal)**
- Domingo 20:00: Revisión completa
- Ajuste de plan basado en progreso
- Actualización documentos automática

---

*Última actualización: 2026-06-24*
*Por Gojo - El agente más fuerte*