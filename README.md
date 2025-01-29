# 🌧️ Predicción de Lluvia en Australia: Análisis Meteorológico

## 📊 Proyecto de Minería de Datos
### Análisis y Modelado Predictivo de Precipitaciones

**Desarrollado por:**
- 👨‍💻 Italo Brignardello
- 👨‍💻 Patricio Quintanilla

**Detalles Académicos**
- 📚 Asignatura: Minería de Datos
- 📅 Fecha: Enero 2025
- 🎓 DuocUC

**Alcance del Proyecto**
- 🗺️ Cobertura: 49 ubicaciones en Australia
- 📈 Dataset: 142,193 registros
- ⏰ Período: 2007-2017
- 🎯 Objetivo: Predicción precisa de eventos de lluvia

**Tecnologías Utilizadas**
- 🐍 Python
- 📊 Scikit-learn
- 📈 Pandas
- 🎨 Seaborn
- 🔮 Random Forest

> Proyecto enfocado en el análisis y predicción de patrones meteorológicos en Australia utilizando técnicas avanzadas de minería de datos


# Configuración de Tipos de Datos del Dataset

## Variables Temporales
| Variable | Descripción |
|----------|-------------|
| 📅 Fecha | Formato datetime para análisis temporal |

## Variables Categóricas
| Variable | Descripción |
|----------|-------------|
| 📍 Ubicacion | Localidades de medición |
| 🌪️ DirRafaga | Dirección del viento en ráfagas |
| 🧭 Dir9am/Dir3pm | Dirección del viento a las 9am y 3pm |
| 🌧️ LluviaHoy/LluviaMan | Registro de lluvia (actual y predicción) |

## Variables Numéricas (float64)
| Variable | Descripción |
|----------|-------------|
| 🌡️ Temperatura | TempMin, TempMax, Temp9am, Temp3pm |
| 💧 Precipitaciones | Lluvia, RISK_MM |
| 💨 Viento | VelRafaga, Vel9am, Vel3pm |
| 💦 Humedad | Hum9am, Hum3pm |
| 🌪️ Presión | Pres9am, Pres3pm |
| ☁️ Nubosidad | Nub9am, Nub3pm |
| ☀️ Sol | Horas de sol |
| 💧 Evaporacion | Nivel de evaporación |


# 1. COMPRENSIÓN DEL NEGOCIO 🎯

## 🎯 Objetivo
> Analizar patrones climáticos en Australia para predecir lluvia con precisión utilizando técnicas de machine learning.

## 🌏 Contexto
### Datos Meteorológicos
- Múltiples ubicaciones australianas
- Fuente: Oficina de Meteorología de la Commonwealth
- Variables climáticas detalladas
- Series temporales extensas

## 🔍 Alcance
### Predicción de Lluvia
- Variables de entrada:
  - Temperatura
  - Humedad
  - Presión
  - Dirección del viento
  - Velocidad del viento
  - Nubosidad
  
### Resultados Esperados
- Modelo predictivo de lluvia
- Análisis de patrones climáticos
- Identificación de variables clave
- Dashboard interactivo

## 💡 Valor del Proyecto
- Mejora en la predicción meteorológica
- Apoyo a la toma de decisiones agrícolas
- Prevención de riesgos climáticos
- Optimización de recursos hídricos


# 2. COMPRENSIÓN DE LOS DATOS 📊

## 📑 Descripción del Dataset

### 📌 Características Principales
- Conjunto de datos meteorológicos de Australia
- Mediciones diarias de variables climáticas
- Registros históricos de múltiples estaciones meteorológicas

### 🗺️ Cobertura Geográfica
- Extensión territorial: 7.741.220 km²
- Costa: 36.735 km
- Principales estados y territorios monitoreados

### 📈 Variables Registradas
#### Mediciones Diarias
- 🌡️ Temperaturas (mínima, máxima, 9am, 3pm)
- 💨 Viento (dirección, velocidad, ráfagas)
- 💧 Precipitaciones y evaporación
- ☁️ Nubosidad
- 💦 Humedad
- 🌪️ Presión atmosférica

#### Variables Objetivo
- 🎯 LluviaMan: Predicción de lluvia (Sí/No)
- 📏 RISK_MM: Cantidad de lluvia esperada

### ⏰ Temporalidad
- Mediciones en diferentes momentos del día
- Registros matutinos (9am)
- Registros vespertinos (3pm)


# 📊 Información Detallada del Dataset

## 📈 Estadísticas Generales

| Métrica | Valor |
|---------|-------|
| 📝 Total de Registros | 142,193 |
| 📅 Fecha Inicial | 2007-11-01 |
| 📅 Fecha Final | 2017-06-25 |
| 📍 Ubicaciones Monitoreadas | 49 |

## ⏳ Cobertura Temporal
- **Duración**: ~10 años
- **Frecuencia**: Registros diarios
- **Estaciones**: Incluye múltiples ciclos estacionales completos

## 🗺️ Cobertura Espacial
- **Distribución**: 49 estaciones meteorológicas
- **Representatividad**: Múltiples zonas climáticas de Australia
- **Alcance**: Principales centros urbanos y rurales

## 💫 Valor del Dataset
- Base sólida para análisis de tendencias
- Suficientes datos para entrenamiento de modelos
- Cobertura geográfica significativa


# 3. PREPARACIÓN DE DATOS

## Análisis de Valores Nulos


# 📊 Análisis de Valores Nulos en el Dataset

## ✨ Variables Sin Valores Nulos (0%)
- 📅 Fecha
- 📍 Ubicacion
- 📏 RISK_MM
- 🌧️ LluviaMan

## 🟢 Variables con Pocos Valores Nulos (<3%)
| Variable | % Nulos |
|----------|---------|
| 🌡️ TempMin | 0.45% |
| 🌡️ TempMax | 0.23% |
| 💧 Lluvia | 0.99% |
| 💨 Vel9am | 0.95% |
| 💨 Vel3pm | 1.85% |
| 💦 Hum9am | 1.25% |
| 💦 Hum3pm | 2.54% |
| 🌡️ Temp9am | 0.64% |
| 🌡️ Temp3pm | 1.92% |
| 🌧️ LluviaHoy | 0.99% |

## 🟡 Variables con Valores Nulos Moderados (3-10%)
| Variable | % Nulos |
|----------|---------|
| 🌪️ DirRafaga | 6.56% |
| 💨 VelRafaga | 6.52% |
| 🧭 Dir9am | 7.04% |
| 🧭 Dir3pm | 2.66% |
| ⏲️ Pres9am | 9.86% |
| ⏲️ Pres3pm | 9.83% |

## 🔴 Variables con Muchos Valores Nulos (>30%)
| Variable | % Nulos |
|----------|---------|
| 💧 Evaporacion | 42.79% |
| ☀️ Sol | 47.69% |
| ☁️ Nub9am | 37.74% |
| ☁️ Nub3pm | 40.15% |


# 🧹 Estado del Dataset Post-Limpieza

## ✅ Variables Completamente Limpias (0 nulos)
- 📅 Variables Temporales
  - Fecha

- 📊 Mediciones Principales
  - TempMin, TempMax
  - Lluvia, Evaporacion
  - Sol, VelRafaga
  - Vel9am, Vel3pm
  - Hum9am, Hum3pm
  - Pres9am, Pres3pm
  - Nub9am, Nub3pm
  - Temp9am, Temp3pm
  - RISK_MM, LluviaMan

## ⚠️ Variables con Valores Nulos Restantes
| Variable | Nulos Restantes |
|----------|----------------|
| 🧭 Dir9am | 10,013 |
| 🌪️ DirRafaga | 9,330 |
| 🧭 Dir3pm | 3,778 |
| 🌧️ LluviaHoy | 1,406 |

## 💡 Observaciones
- Las variables direccionales mantienen algunos valores nulos
- La mayoría de las variables numéricas están completas
- Dataset significativamente más limpio y listo para análisis


# 4. ANÁLISIS EXPLORATORIO Y MODELADO

## Análisis por Ubicación


# 🏆 Top 5 Ubicaciones Destacadas

## 1. 🌡️ Katherine
- Temperatura máxima más alta: 34.77°C
- Días con lluvia: 265
- Porcentaje días lluviosos: 17.00%

## 2. 🌴 Darwin
- Temperatura máxima: 32.54°C
- Días con lluvia: 852
- Porcentaje días lluviosos: 26.69%

## 3. 🏜️ Uluru
- Temperatura máxima: 30.39°C
- Días con lluvia: 116
- **Menor porcentaje de días lluviosos**: 7.63%

## 4. 🌊 Portland
- Temperatura máxima: 18.06°C
- Días con lluvia: 1,095
- **Mayor porcentaje de días lluviosos**: 36.55%

## 5. 🌺 Cairns
- Temperatura máxima: 29.54°C
- Días con lluvia: 950
- Alto porcentaje días lluviosos: 31.79%

> Estas ubicaciones representan los extremos climáticos más significativos de Australia


# Visualización 1: Distribución de temperaturas por mes


# 📊 Análisis de Temperaturas Máximas por Mes

## 🌡️ Meses Más Significativos

### 1. Enero (Mes 1)
- Pico de verano australiano
- Temperaturas más altas del año
- Mayor variabilidad térmica

### 2. Julio (Mes 7)
- Pleno invierno austral
- Temperaturas más bajas registradas
- Menor dispersión en los datos

### 3. Diciembre (Mes 12)
- Inicio del verano
- Tendencia ascendente marcada
- Alta variabilidad térmica

### 4. Abril (Mes 4)
- Transición otoñal
- Punto de inflexión temperatura
- Variabilidad moderada

### 5. Octubre (Mes 10)
- Primavera avanzada
- Incremento térmico notable
- Preparación para verano

# Visualización 2: Lluvia por ubicación

# 🌧️ Top 5 Ubicaciones con Mayor Precipitación

## 1. 🌊 Cairns
- Ubicación tropical
- Mayor promedio de lluvia
- Clima húmedo constante

## 2. 🌿 Darwin
- Ciudad norteña
- Altas precipitaciones
- Patrón monzónico

## 3. 🌳 Coffs Harbour
- Costa este
- Precipitaciones frecuentes
- Clima subtropical

## 4. 🌲 Wollongong
- Región costera
- Lluvias consistentes
- Influencia oceánica

## 5. 🌺 Gold Coast
- Destino turístico
- Precipitaciones significativas
- Clima subtropical húmedo

> Estas ubicaciones representan las zonas más lluviosas de Australia, principalmente en regiones costeras y tropicales.


# Visualización 3: Correlaciones

# 📊 Correlaciones Más Significativas

## 🔵 Correlaciones Positivas Fuertes
1. Temp3pm ↔️ TempMax (0.98)
   - Temperatura máxima altamente relacionada con temperatura vespertina
   
2. Temp9am ↔️ TempMin (0.92)
   - Temperatura mínima vinculada a temperatura matutina

## 🔴 Correlaciones Negativas Fuertes
3. Temp3pm ↔️ Hum3pm (-0.85)
   - Relación inversa entre temperatura y humedad vespertina
   
4. TempMax ↔️ Hum3pm (-0.82)
   - Mayor temperatura máxima indica menor humedad

## 🟣 Correlaciones Moderadas
5. Pres9am ↔️ Pres3pm (0.79)
   - Presión atmosférica mantiene consistencia durante el día

> Estas correlaciones revelan patrones climáticos clave para el modelo predictivo


# Análisis de patrones

# 📊 Patrones Climáticos Identificados

## 🌡️ Relación Temperatura-Lluvia
- Correlación: -0.07
- Indica una correlación negativa débil
- La temperatura tiene baja influencia directa en precipitaciones

## 💧 Análisis de Precipitaciones
### Promedio Diario
- 2.35 mm de lluvia
- Refleja un clima moderadamente seco
- Típico del territorio australiano

### Frecuencia de Lluvia
- 31,877 días con precipitaciones registradas
- Representa eventos de lluvia significativos
- Base sólida para análisis predictivo

## 💡 Insights Clave
- La lluvia en Australia es relativamente independiente de la temperatura
- Patrón de precipitaciones consistente con clima árido/semiárido
- Datos robustos para modelado predictivo

> Estos patrones son fundamentales para el desarrollo de modelos de predicción meteorológica


# 5. MODELADO PREDICTIVO

# 📊 Especificaciones del Dataset de Entrenamiento

## 🎯 Dimensiones del Dataset
| Conjunto | Registros |
|----------|-----------|
| Entrenamiento | 113,754 |
| Prueba | 28,439 |
| **Total** | 142,193 |

## 📈 Variables Seleccionadas
### Temperatura
- 🌡️ TempMin: Temperatura mínima
- 🌡️ TempMax: Temperatura máxima

### Precipitación
- 💧 Lluvia: Nivel de precipitación

### Viento
- 💨 VelRafaga: Velocidad de ráfagas

### Humedad
- 💦 Hum9am: Humedad matutina
- 💦 Hum3pm: Humedad vespertina

## 💫 Características
- Dataset balanceado 80/20
- Variables críticas seleccionadas
- Cobertura temporal significativa
- Métricas meteorológicas clave

> Dataset robusto para entrenamiento de modelos predictivos


# 6. EVALUACIÓN DEL MODELO

# 📊 Reporte de Clasificación del Modelo

## 🎯 Métricas por Clase

### Clase 0 (Sin Lluvia)
| Métrica | Valor |
|---------|-------|
| Precisión | 86% |
| Recall | 94% |
| F1-Score | 90% |
| Muestras | 22,098 |

### Clase 1 (Con Lluvia)
| Métrica | Valor |
|---------|-------|
| Precisión | 70% |
| Recall | 47% |
| F1-Score | 57% |
| Muestras | 6,341 |

## 📈 Métricas Globales
| Tipo | Precisión | Recall | F1-Score | Muestras |
|------|-----------|---------|----------|-----------|
| Accuracy | 84% | - | - | 28,439 |
| Macro Avg | 78% | 71% | 73% | 28,439 |
| Weighted Avg | 83% | 84% | 83% | 28,439 |

## 💡 Insights Clave
- Excelente predicción de días sin lluvia (90% F1-Score)
- Desempeño moderado en predicción de lluvia (57% F1-Score)
- Precisión global del modelo: 84%
- Dataset desbalanceado: más días sin lluvia

> El modelo muestra un rendimiento sólido, especialmente en la predicción de días secos


# Importancia de características

# 7. IMPLEMENTACIÓN Y EJEMPLO

# 🔍 Insights y Recomendaciones

## 🌡️ Patrones Estacionales
### Temperatura
- Variaciones mensuales significativas identificadas
- Picos en verano austral (diciembre-febrero)
- Valores mínimos en invierno (junio-agosto)

### Precipitaciones
- Patrones específicos por región
- Mayor frecuencia en zonas costeras
- Variabilidad según ubicación geográfica

## 📊 Variables Críticas
| Variable | Importancia | Interpretación |
|----------|-------------|----------------|
| 💧 Hum3pm | 0.284115 | Humedad vespertina dominante |
| 🌡️ TempMin | 0.166691 | Temperatura mínima significativa |
| 🌡️ TempMax | 0.164121 | Máximas impactan predicción |
| 💦 Hum9am | 0.141403 | Humedad matutina relevante |
| 💨 VelRafaga | 0.127310 | Viento factor considerable |
| 🌧️ Lluvia | 0.116360 | Precipitación histórica |

## 💡 Recomendaciones Clave
### Monitoreo Prioritario
- Enfoque en humedad vespertina
- Seguimiento de temperaturas extremas
- Control de patrones de viento

### Consideraciones Geográficas
- Adaptar modelos por región
- Evaluar microclimas locales
- Ajustar predicciones por ubicación

### Sistema de Alertas
- Implementar alertas tempranas
- Basado en probabilidades
- Actualización en tiempo real

> Este análisis proporciona una base sólida para mejorar la precisión en la predicción de lluvia
