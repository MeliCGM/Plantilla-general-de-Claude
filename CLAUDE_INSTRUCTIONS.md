# 🤖 Instrucciones para AI Assistant - Adaptive Optimizer

## Contexto
Este proyecto utiliza **Adaptive Optimizer**, un sistema de 3 componentes para gestión inteligente de workflows.

## 🎯 Cuándo y Cómo Usar

### 1. Loop Detector - Prevenir Repeticiones
**Usar antes de:**
- Reinstalar paquetes
- Reintentar operaciones fallidas
- Ejecutar comandos ya ejecutados

**Comando:** `ao loop check "ACCION" --context "INFO"`

### 2. Context Manager - Memoria del Proyecto
**Usar para:**
- Trackear fase actual del proyecto
- Documentar cambios con rationale
- Registrar decisiones técnicas
- Mapear dependencias

**Comandos principales:**
- `ao context PROYECTO phase "FASE"`
- `ao context PROYECTO change "COMPONENTE" "CAMBIO" --reason "POR_QUE"`
- `ao context PROYECTO summary`

### 3. Resource Optimizer - Planificación
**Usar para:**
- Planificar múltiples operaciones
- Optimizar orden de ejecución
- Validar dependencias

**Comandos principales:**
- `ao optimize add TIPO "TARGET" --priority NIVEL`
- `ao optimize plan`
- `ao optimize validate`

## 🔄 Workflow Estándar
```bash
# 1. Iniciar trabajo
ao context PROYECTO phase "desarrollo"

# 2. Antes de cada acción
ao loop check "ACCION"

# 3. Documentar cambios
ao context PROYECTO change "COMPONENTE" "CAMBIO" --reason "POR_QUE"

# 4. Revisar estado
ao context PROYECTO summary
```

## 🚨 Reglas Críticas
1. Nunca repetir acción 3+ veces sin cambiar enfoque
2. Documentar siempre el "por qué"
3. Mapear dependencias explícitamente
4. Consultar estado antes de continuar

## 📍 Estado se guarda en
- Windows: `%TEMP%\`
- Linux/Mac: `/tmp/`

Ver más: `README.md`, `ao --help`
