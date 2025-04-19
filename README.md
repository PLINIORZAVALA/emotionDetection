## Resultados del Entrenamiento - Modelo CNN Emociones

### Configuración:
- **Épocas completadas:** 5/5
- **Batch Size:** 32
- **Learning Rate:** 1e-4  
- **Steps por época:** 106
- **Hardware:** GPU (tiempos variables)

### Resumen de Métricas:
| Métrica          | Mejor Valor | Peor Valor | Época Mejor |
|------------------|-------------|------------|-------------|
| Train Accuracy   | 28.12%      | 3.12%      | 4           |
| Val Accuracy     | 26.11%      | 18.85%     | 4           |
| Train Loss       | 2.3540      | 3.1051     | 5           |
| Val Loss         | 1.9813      | 2.0284     | 3           |

### Detalle por Época:
| Época | Train Acc | Train Loss | Val Acc  | Val Loss  | Tiempo  |
|-------|-----------|------------|----------|-----------|---------|
| 1     | 11.93%    | 2.8533     | 18.95%   | 2.0284    | 4m 36s  |
| 2     | 3.12%     | 3.1051     | 18.85%   | 2.0280    | 1m 7s   |
| 3     | 15.84%    | 2.5553     | 25.91%   | 1.9813    | 4m 32s  |
| 4     | 28.12%    | 2.3917     | 26.11%   | 1.9820    | 56s     |
| 5     | 18.34%    | 2.3540     | -        | -         | ~2s     |

⚠️ **Advertencias:**
1. Falta de datos en época 2 (verificar generador)
2. Tiempos de época inconsistentes (4m → 56s → 2s)
3. Val_Accuracy estancada ~26% (posible sobreajuste)

📈 **Recomendaciones:**
```python
# Corrección para warning:
train_generator = train_datagen.flow_from_directory(...).repeat()

# Mejorar augmentations:
ImageDataGenerator(
    rotation_range=30,
    width_shift_range=0.2,
    zoom_range=0.2,
    horizontal_flip=True
)


