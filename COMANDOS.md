# 🎮 COMANDOS - Sistema Gojo

> *Comandos básicos para interactuar con el agente personal*

---

## 📚 **Comandos de Conocimiento**

### **Diario de Aprendizaje**
```bash
diario hoy [lo que aprendiste]
# Ejemplo: diario hoy aprendí Python loops, inversión ETFs

# Formato automático:
## YYYY-MM-DD
### 🧠 Qué aprendí hoy
- [punto 1]
- [punto 2]
### 💡 Insight principal
[reflexión]
### 🎯 Para aplicar mañana
- [acción]
```

**Destino**: Google Doc "Diario de Aprendizaje"
**Conexión necesaria**: Google Docs

---

## 📅 **Comandos de Planificación**

### **Plan Semanal**
```bash
plan semanal [objetivos]
# Ejemplo: plan semanal estudiar Python 10h, gym 3 días

# Output:
1. Google Doc "Plan Semanal [fecha]"
2. Eventos Calendar
3. Recordatorios Telegram
```

**Destino**: Google Docs + Calendar + Telegram
**Conexiones**: Google Docs, Calendar, Telegram

### **Ver Plan Actual**
```bash
plan semanal ver
# Muestra el plan de esta semana
```

---

## 🏋️ **Comandos de Entrenamiento**

### **Rutina del Día**
```bash
entrenamiento hoy
# Muestra la rutina programada para hoy

entrenamiento progreso
# Progresión fuerza semana actual
```

### **Registrar Entrenamiento**
```bash
entrenamiento completado [notas]
# Ejemplo: entrenamiento completado press 40kg 4x10
```

---

## 💰 **Comandos Financieros**

### **Estado Financiero**
```bash
finanzas estado
# Resumen deuda + ahorro

finanzas registro gasto [cantidad] [categoría]
# Ejemplo: finanzas registro gasto弈 15 comida
```

### **Pago Registrado**
```bash
deuda pagada [cantidad]
# Actualiza progreso deuda
```

---

## 📊 **Comandos de Seguimiento**

### **Progreso Semanal**
```bash
progreso semanal
# Métricas fuerza + finanzas + hábitos
```

### **Checklist Diario**
```bash
checklist hoy
# Muestra checklist del día

checklist completado [item]
# Marca item como completado
```

---

## 🔧 **Comandos del Sistema**

### **Estado del Agente**
```bash
estado sistema
# Cron jobs activos + conexiones

estado skills
# Skills implementadas
```

### **Ayuda**
```bash
ayuda
# Lista todos los comandos

ayuda [tema]
# Ejemplo: ayuda finanzas
```

---

## 🎯 **Flujos de Trabajo Típicos**

### **Mañana (8:15)**
```bash
# Desayuno automático recordatorio
# Checklist: desayuno completado
```

### **Tarde (17:00)**
```bash
entrenamiento hoy
# Ver rutina
entrenamiento completado
# Registrar
```

### **Noche (21:00)**
```bash
checklist mañana
# Preparar día siguiente
diario hoy [aprendizaje]
# Registrar conocimiento
```

### **Domingo (20:00)**
```bash
progreso semanal
# Revisión completa
plan semanal [objetivos]
# Plan siguiente semana
```

---

## 📱 **Sistema de Recordatorios**

### **Automatizados**
```
21:00 - Checklist día siguiente
8:15 - Recordatorio desayuno
17:00 - Recordatorio entrenamiento (L/M/V)
Dom 20:00 - Revisión semanal
```

### **Manuales**
```bash
recordatorio [mensaje] [hora]
# Ejemplo: recordatorio llamar a Juan 16:30
```

---

## ⚙️ **Configuración del Sistema**

### **Archivos Base**
```
AGENTS.md    # Identidad Gojo
USER.md      # Contexto personal
MEMORY.md    # Preferencias y objetivos
SOUL.md      # Filosofía y valores
TOOLS.md     # Setup específico
```

### **Skills Implementadas**
```
1. diario-aprendizaje/    # Diario conocimiento
2. plan-semanal/          # Planificación semanal
3. [en desarrollo]
```

---

## 🚀 **Quick Start**

### **Día 1**
```bash
# Mañana
diario hoy primeros pasos sistema

# Tarde
entrenamiento hoy
entrenamiento completado

# Noche
checklist mañana
```

### **Semana 1**
```bash
# Lunes
plan semanal [tus objetivos]

# Diario
diario hoy [aprendizaje]

# Domingo
progreso semanal
```

---

## ❓ **Preguntas Frecuentes**

### **¿Dónde se guardan los datos?**
```
- Google Docs: Documentos estructurados
- Google Calendar: Eventos y recordatorios
- Telegram: Checklists y alertas
- Memoria local: Preferencias y progreso
```

### **¿Qué datos son privados?**
```
- USER.md: Contexto personal
- MEMORY.md: Objetivos específicos
- Documentos Google: Tienen tus permisos
- Nunca se sube a GitHub
```

### **¿Puedo añadir mis propias skills?**
```
Sí, siguiendo:
1. Crear carpeta skill/
2. SKILL.md con documentación
3. Probar con ejemplos
4. Integrar en sistema
```

---

## 🔗 **Recursos**

- **GitHub**: https://github.com/theazec34/Mi-Agente-Gojo-Satoru
- **Skills Design**: skills_design.md
- **Plan Maestro**: plan_maestro.md
- **Ejemplos**: ejemplo_*.md

---

## 🏆 **Filosofía de Comandos**

> *"Los comandos no son órdenes, son atajos hacia tu mejor versión. No los ejecutas tú, los ejecuta el sistema que construiste para liberarte."*

**Menos es más**:
- 1 comando = 1 acción clara
- Automatización > repetición
- Sistema > fuerza de voluntad
- Progreso > perfección

---

> *Sistema Gojo - Porque el dominio es un verbo, no un sustantivo*