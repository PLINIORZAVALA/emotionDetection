## Resultados del Entrenamiento - Modelo CNN Emociones (20 épocas)

### Configuración:
- **Batch Size:** 32
- **Learning Rate:** 1e-4  
- **Steps por época:** 106
- **Hardware:** GPU (tiempos variables entre 55s-321s/época)

### 📌 Resumen de Progreso:
| Métrica          | Inicio (Época 1) | Mejor Resultado (Época 20) | Mejora |
|------------------|------------------|----------------------------|--------|
| Train Accuracy   | 12.46%           | 50.00%                     | +37.54%|
| Val Accuracy     | 20.16%           | 59.27%                     | +39.11%|
| Train Loss       | 2.7276           | 1.4232                     | -47.8% |
| Val Loss         | 2.0246           | 1.3328                     | -34.2% |

### 🔍 Análisis por Fases:
1. **Fase Inicial (Épocas 1-5)**:
   - Val_Accuracy saltó de 20.16% → 37.20% (+17.04%)
   - Primer indicio de aprendizaje efectivo

2. **Fase Intermedia (Épocas 6-12)**:
   - Estancamiento en ~38-45% val_accuracy
   - Posible necesidad de ajuste de LR

3. **Fase Final (Épocas 13-20)**:
   - Crecimiento acelerado (49.29% → 59.27%)
   - Máxima eficiencia en últimas 5 épocas

### 📊 Detalle por Época:
| Época | Train Acc | Train Loss | Val Acc  | Val Loss  | Tiempo  | Hito Importante               |
|-------|-----------|------------|----------|-----------|---------|--------------------------------|
| 1     | 12.46%    | 2.7276     | 20.16%   | 2.0246    | 241s    | Baseline                       |
| 5     | 16.94%    | 2.3659     | 37.20%   | 1.9298    | 260s    | Primer salto importante        |
| 10    | 25.00%    | 2.0879     | 39.01%   | 1.7882    | 57s     | Estancamiento temporal         |
| 15    | 33.23%    | 1.8235     | 50.00%   | 1.5501    | 216s    | Rompe barrera del 50%          |
| 20    | **50.00%**| **1.4232** | **59.27%**| **1.3328**| 84s     | **Mejor desempeño**            |

