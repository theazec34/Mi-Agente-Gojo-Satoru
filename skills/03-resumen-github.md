# Skill: Resumen Diario de GitHub

## 🎯 ¿Qué hace esta skill?
Genera un briefing diario de tu actividad en GitHub (issues abiertos, commits recientes, PRs pendientes) y te lo envía por Telegram con recomendaciones accionables.

## 📥 ¿Qué input necesita el agente?
**Trigger manual**: "resumen github"
**Trigger automático**: Se puede configurar como cron job diario
**Conocimiento previo**:
- Tu cuenta GitHub: theazec34 (de USER.md)
- Repositorios relevantes para AI Engineer training
- Métricas que te importan (commits, issues resueltos, PRs)

## 📤 ¿Cómo es un buen output?
**Formato**: Mensaje estructurado en Telegram:
```
📊 RESUMEN GITHUB - [Fecha]

🔴 ISSUES ABIERTOS (3)
• [repo] #ID: Título (assignee)
• ...

✅ COMMITS HOY (5)
• [repo] Hash corto: Mensaje commit
• ...

🔶 PRs PENDIENTES (2)
• [repo] #ID: Título (reviewers)
• ...

🎯 RECOMENDACIONES
1. Revisar issue #X (crítico)
2. Mergear PR #Y (listo)
3. Completar tarea Z
```

**Destino**: Telegram directo a ti (chat_id: 8761483620)
**Validación**: Mensaje recibido con datos actualizados y útiles

## ⚙️ Implementación Técnica

### Conexiones necesarias
- GitHub (ya activa)
- Telegram (ya activa)

### Flujo de ejecución
1. Fetch issues abiertos asignados a ti
2. Fetch commits últimos 24 horas
3. Fetch PRs pendientes de review
4. Procesar y priorizar
5. Formatear mensaje Telegram
6. Enviar con recomendaciones

### Parámetros configurables
- Repositorios a monitorear (default: todos)
- Frecuencia (default: manual)
- Nivel de detalle (default: medio)
- Alertas críticas (issues bloqueantes)

## 🔧 Ejemplo de uso
```bash
# Trigger manual
resumen github

# Respuesta esperada en Telegram:
📊 RESUMEN GITHUB - 2026-06-24
🔴 ISSUES: 1 crítico en Mi-Agente-Gojo-Satoru
✅ COMMITS: 6 hoy (skills implementadas)
🎯 ACCIÓN: Revisar PR #1
```

## 🧪 Validación de éxito
- ✅ Mensaje Telegram recibido
- ✅ Información actualizada (últimas 24h)
- ✅ Issues/PRs correctamente listados
- ✅ Recomendaciones accionables
- ✅ Sin errores en fetch de datos

## 🔄 Integración con sistema
- **MEMORY.md**: Guarda métricas semanales
- **Google Docs**: Puede exportar resumen semanal
- **Cron jobs**: Configurable diario/semanal
- **Alertas**: Issues críticos notificación inmediata

---

**📊 Métricas clave**:
- Issues abiertos/resueltos
- Commits por día/semana
- PRs pendientes/revisados
- Tiempo respuesta issues

**🔄 Flujo de trabajo**:
```
GitHub Activity → Daily Fetch → Process → Telegram → Action Items
```

**🎯 Casos de uso**:
- Revisiones diarias de progreso
- Identificación de bloqueos
- Seguimiento de proyectos
- Recordatorios de tareas pendientes

---

> *Skill 3/6 - Resumen GitHub*
> *Estado: ✅ Implementada | Conexiones: GitHub + Telegram*