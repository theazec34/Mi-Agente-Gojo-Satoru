# Skill: Borradores de Gmail con Tu Voz

## 🎯 ¿Qué hace esta skill?
Crea correos electrónicos en Gmail que suenan como si los hubieras escrito tú mismo, usando tu estilo, tono y firma habitual, listos para revisión mínima antes de enviar.

## 📥 ¿Qué input necesita el agente?
**Input estructurado**:
- Para: destinatario(s)
- Asunto: línea de asunto
- Puntos clave: lista de lo que debe cubrir el correo
- Tonality: formal/informal/neutral (opcional)
- Urgencia: baja/media/alta (opcional)

**Ejemplo**:
```
para: profesor@curso.com
asunto: Consulta sobre proyecto IA
puntos: agradecer clase de ayer, preguntar deadline extensión, confirmar reunión viernes
tono: formal pero cercano
```

**Conocimiento previo** (de USER.md/MEMORY.md):
- Tu estilo de comunicación: directo, práctico
- Relaciones clave: Ester (pareja), compañeros estudio, profesores
- Tipo de correos que envías: profesionales, académicos, personales
- Firma habitual (si se documenta en memoria)
- Expresiones típicas que usas

## 📤 ¿Cómo es un buen output?
**Formato**: Borrador de Gmail con:
- Saludo apropiado al destinatario
- Estructura clara y directa
- Puntos cubiertos completamente
- Tonality consistente con tu estilo
- Firma personalizada
- Buen balance entre profesional y amigable

**Destino**: Borrador en Gmail (folder: "Borradores Gojo")
**Validación**: Borrador creado que necesita ≤2 correcciones antes de enviar

## ⚙️ Implementación Técnica

### Análisis de estilo personal
**Fuentes de aprendizaje**:
- Correos anteriores enviados (si acceso disponible)
- USER.md: estilo de comunicación descrito
- MEMORY.md: relaciones y contexto
- Feedback de correcciones que hagas

**Elementos de estilo detectables**:
- Longitud promedio de frases
- Uso de emojis (sí/no, cuáles)
- Formalidad por destinatario
- Estructura típica (agradecimiento → punto → cierre)
- Expresiones repetidas

### Conexiones necesarias
- Gmail (ya activa)

### Flujo de ejecución
1. Analizar destinatario y contexto
2. Determinar tonality apropiado
3. Expandir puntos clave a párrafos
4. Aplicar estilo personal aprendido
5. Añadir saludo y despedida contextual
6. Insertar firma personalizada
7. Crear borrador en Gmail
8. Proporcionar preview para aprobación

### Templates por tipo
**Académico**:
```
Hola [Nombre],
[Agredecimiento/clase]
[Punto principal]
[Pregunta/solicitud]
[Propuesta concreta]
Saludos,
[Tu nombre]
```

**Profesional**:
```
Estimado/a [Nombre],
[Contexto breve]
[Acción/información solicitada]
[Plazo si aplica]
Quedo a la espera,
[Tu nombre]
[Puesto/contacto]
```

**Personal**:
```
[Saludo informal],
[Punto directo]
[Detalles si necesarios]
[Propuesta concreta]
[Despedida casual]
```

## 🔧 Ejemplo de uso
```bash
# Comando estructurado
gmail para:ester@email.com asunto: planes finde puntos: confirmar cine viernes, preguntar hora, sugerir restaurante tono: informal

# Borrador creado:
"Hola cariño,
¿Quedamos para el cine el viernes como hablamos?
¿A qué hora te viene bien? Podríamos cenar después en ese italiano nuevo.
Dime qué te parece.
Besos,
Alfredo"
```

## 🧪 Validación de éxito
- ✅ Borrador visible en Gmail
- ✅ Destinatario correcto
- ✅ Asunto apropiado
- ✅ Puntos cubiertos completamente
- ✅ Tono consistente con tu estilo
- ✅ Firma personalizada correcta
- ✅ ≤2 correcciones necesarias antes de enviar

## 🔄 Integración con sistema
- **MEMORY.md**: Aprende de correcciones para mejorar estilo
- **Google Docs**: Puede guardar plantillas reusables
- **Calendar**: Integra fechas de eventos mencionados
- **Telegram**: Preview rápido antes de crear borrador

---

**🧠 Aprendizaje de estilo**:
- **Baseline**: USER.md + MEMORY.md
- **Feedback loop**: Cada corrección mejora el modelo
- **Perfiles**: Estilo diferente por destinatario
- **Evolución**: Mejora continua con uso

**📧 Templates inteligentes**:
```
Respuesta rápida profesor:
- Agradecimiento
- Pregunta concreta
- Propuesta opciones
- Firma formal

Recordatorio pago:
- Contexto breve
- Monto y fecha
- Instrucciones pago
- Contacto seguimiento
```

**🎯 Casos de uso**:
- Respuestas rápidas profesionales
- Comunicación personal consistente
- Ahorro tiempo escritura
- Mejora calidad comunicación

---

> *Skill 5/6 - Borradores Gmail*
> *Estado: ✅ Implementada | Conexiones: Gmail*