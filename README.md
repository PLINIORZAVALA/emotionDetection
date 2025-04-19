## Resultados del Entrenamiento - Modelo CNN Emociones (20 épocas)

### Configuración:
- **Learning Rate:** 1e-4  
- **Steps por época:** 106
- **Hardware:** GPU (tiempos variables entre 55s-321s/época)

### Resumen de Métricas:
| Métrica          | Mejor Valor | Peor Valor | Época Mejor |
|------------------|-------------|------------|-------------|
| Train Accuracy   | 50.00%      | 12.46%     | 20          |
| Val Accuracy     | 59.27%      | 19.66%     | 20          |
| Train Loss       | 1.4232      | 2.7276     | 20          |
| Val Loss         | 1.3328      | 2.0284     | 20          |

### Detalle por Época (Selección Clave):
| Época | Train Acc | Train Loss | Val Acc  | Val Loss  | Tiempo  |
|-------|-----------|------------|----------|-----------|---------|
| 1     | 12.46%    | 2.7276     | 20.16%   | 2.0246    | 4m 1s   |
| 5     | 16.94%    | 2.3659     | 37.20%   | 1.9298    | 4m 20s  |
| 10    | 25.00%    | 2.0879     | 39.01%   | 1.7882    | 57s     |
| 15    | 33.23%    | 1.8235     | 50.00%   | 1.5501    | 3m 36s  |
| 20    | **50.00%**| **1.4232** | **59.27%**| **1.3328**| 1m 24s  |

✅ **Tendencias Positivas:**
1. Mejora consistente en val_accuracy (+39.11% total)
2. Reducción estable de loss (train -47.8%, val -34.2%)
3. Últimas 5 épocas con ganancia de +9.98% val_accuracy

⚠️ **Alertas Técnicas:**
1. Tiempos variables (¿problemas de carga/memoria?)
2. Época 14 con accuracy anómala (12.5% train)
3. Val_accuracy aún tiene margen de mejora (~60%)
