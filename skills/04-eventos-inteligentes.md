# Skill: Eventos de Calendar Inteligentes

## 🎯 ¿Qué hace esta skill?
Interpreta descripciones en lenguaje natural y crea eventos en Google Calendar con todos los detalles inferidos automáticamente (fecha, hora, duración, recordatorios).

## 📥 ¿Qué input necesita el agente?
**Input del usuario**: Descripción en lenguaje natural:
- "sesión de estudio el jueves por la tarde, dos horas"
- "reunión con equipo mañana a las 11, 1 hora"
- "entrenamiento extra el viernes a las 18"

**Conocimiento previo**:
- Tu zona horaria (Europe/Madrid)
- Horarios laborales típicos (9:00-15:00)
- Preferencias de duración (default: 1h)
- Tipos de eventos recurrentes
- Recordatorios preferidos (default: 10min antes)

## 📤 ¿Cómo es un buen output?
**Formato**: Evento de Google Calendar con:
- Título descriptivo inferido
- Fecha/hora correctas (de "jueves por la tarde")
- Duración adecuada (de "dos horas")
- Recordatorios configurados
- Descripción clara con contexto
- Color categoría apropiado

**Destino**: Tu Google Calendar principal
**Validación**: Evento creado visible en calendario con parámetros correctos

## ⚙️ Implementación Técnica

### Procesamiento de lenguaje natural
**Entradas soportadas**:
- Días relativos: hoy, mañana, pasado mañana
- Días de semana: lunes, martes...
- Momentos del día: mañana, tarde, noche
- Duración: minutos, horas, "un rato"
- Recordatorios: "con recordatorio", "avísame antes"

**Inferencias por defecto**:
- "por la tarde" → 16:00
- "por la mañana" → 10:00  
- "por la noche" → 20:00
- Sin hora especificada → próxima hora disponible

### Conexiones necesarias
- Google Calendar (ya activa)

### Flujo de ejecución
1. Parsear descripción natural
2. Inferir fecha/hora
3. Determinar duración
4. Crear título apropiado
5. Configurar recordatorios
6. Crear evento en Calendar
7. Confirmar con detalles

### Ejemplos de parsing
```
"estudio jueves tarde 2h" → 
  Día: próximo jueves
  Hora: 16:00
  Duración: 2 horas
  Título: "Sesión de estudio"

"reunión equipo mañana 11" →
  Día: mañana
  Hora: 11:00
  Duración: 1 hora
  Título: "Reunión equipo"
```

## 🔧 Ejemplo de uso
```bash
# Comando simple
evento "sesión de estudio el jueves por la tarde, dos horas"

# Respuesta esperada:
✅ EVENTO CREADO: "Sesión de estudio"
📅 Jueves 26 Jun 2026, 16:00-18:00
🔔 Recordatorio: 10 min antes
📝 Calendar: https://calendar.google.com/...
```

## 🧪 Validación de éxito
- ✅ Evento visible en Google Calendar
- ✅ Fecha/hora correctas según descripción
- ✅ Duración configurada apropiadamente
- ✅ Recordatorios activados
- ✅ Título descriptivo y útil

## 🔄 Integración con sistema
- **Plan semanal**: Eventos recurrentes integrados
- **MEMORY.md**: Aprende preferencias de horarios
- **Telegram**: Confirmación inmediata
- **Google Docs**: Exportación de agenda semanal

## ⚡ Características avanzadas
- **Conflictos**: Detecta solapamientos y sugiere alternativas
- **Recurrencia**: "todos los lunes a las 10"
- **Ubicación**: "en la oficina" → añade ubicación
- **Invitar**: "con Juan y María" → añade invitados
- **Etiquetas**: "estudio", "reunión", "entrenamiento"

---

**🧠 Procesamiento NLP**:
- Análisis de intención: estudio/reunión/entrenamiento
- Extracción entidades: fechas, horas, duraciones
- Resolución ambigüedades: "mañana" = día siguiente vs mañana temprano
- Fallback inteligente: valores por defecto contextuales

**📅 Inferencias temporales**:
```
"próxima semana" → Lunes semana siguiente
"fin de mes" → Último día del mes
"a medio día" → 12:00
"tarde temprano" → 15:00
```

**🎯 Casos de uso**:
- Programación rápida sin apps
- Recordatorios contextuales
- Agenda compartida automática
- Conflict detection proactivo

---

> *Skill 4/6 - Eventos Inteligentes*
> *Estado: ✅ Implementada | Conexiones: Google Calendar*