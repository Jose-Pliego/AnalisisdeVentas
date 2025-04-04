# Análisis de Ventas y Predicción para una Compañía de Productos de Consumo

## Introducción

### Contexto del Proyecto
Este proyecto se centra en analizar el rendimiento histórico de ventas de una compañía de productos de consumo e implementar modelos predictivos para estimar ventas futuras. El objetivo es identificar patrones, outliers y segmentos clave que permitan optimizar estrategias comerciales y operativas.

### Relevancia del Análisis
- **Toma de decisiones estratégicas**: Los insights obtenidos ayudan a la empresa a gestionar inventarios, planificar campañas de marketing y asignar recursos eficientemente.
- **Identificación de oportunidades**: Detectar regiones, categorías y segmentos con alto potencial o problemas permite acciones focalizadas.
- **Pronóstico preciso**: Las predicciones de ventas facilitan la planificación financiera y operativa a corto y mediano plazo.

### Herramientas Utilizadas
- **Lenguajes**: Python (pandas, matplotlib, seaborn, scikit-learn, pmdarima), SQL.
- **Visualización**: PowerBI (para dashboards interactivos).
- **Metodologías**: Análisis exploratorio de datos (EDA), clustering (K-Means), modelos de series temporales (ARIMA).

---

## Datos Utilizados
Se integraron múltiples fuentes de datos:
- **Tablas de dimensión**: `DIM_CALENDAR`, `DIM_CATEGORY`, `DIM_PRODUCT`, `DIM_SEGMENT`.
- **Tabla de hechos**: `FACT_SALES` (ventas unitarias y en valor por fecha, región y producto).
- **Variables clave**: 
  - `total_unit_sales`: Unidades vendidas.
  - `total_value_sales`: Valor monetario de ventas.
  - Atributos como `category`, `region`, `segment`, y `brand`.

---

## Técnicas Aplicadas
1. **Limpieza y Transformación de Datos**:
   - Eliminación de valores nulos y duplicados.
   - Unificación de tablas mediante merges (e.g., ventas con categorías y segmentos).
   - Estandarización de formatos (fechas, nombres de columnas).

2. **Análisis Exploratorio (EDA)**:
   - Distribuciones de ventas (histogramas y boxplots).
   - Tendencia temporal de ventas totales y por categoría/región/segmento.
   - Detección de outliers usando el rango intercuartílico (IQR).

3. **Clustering con K-Means**:
   - Segmentación de productos basada en ventas promedio semanales y valor total.
   - Identificación de 5 clusters con comportamientos diferenciados.

4. **Pronóstico de Ventas (ARIMA)**:
   - Modelado estacional para predecir ventas de productos destacados (Vanish y Lysol).
   - Validación con métricas como MAE y MAPE.

---

## Conclusiones y Hallazgos Clave
### 1. Distribución de Ventas
- **Outliers significativos**: 
  - La categoría "BLEACH" registró outliers de hasta **504 unidades** y **$12,236** en ventas.
  - La región "SCANNING MEXICO" mostró los mayores picos, sugiriendo oportunidades de expansión.
- **Segmentos destacados**: "BAR" y "LIQUID & GEL" presentaron ventas consistentemente altas.

### 2. Tendencias Temporales
- **Estacionalidad**: Picos en diciembre debido a campañas navideñas (ventas aumentaron un 50% en Vanish).
- **Crecimiento anual**: Tendencia ascendente del 15-20% en ventas unitarias desde 2022.

### 3. Clustering
- **Cluster 3**: Productos con alto valor de ventas y estabilidad semanal (priorizar en estrategias de retención).
- **Cluster 1**: Productos con baja rotación pero alto margen (oportunidad para promociones).

### 4. Predicciones
- **Modelos ARIMA** lograron un **MAPE < 8%** en pruebas, indicando alta precisión.
  - **Vanish**: Pronóstico de **2,200 unidades** para enero 2024.
  - **Lysol**: Crecimiento estimado del **12%** en el último trimestre de 2023.

---

## Recomendaciones Estratégicas
- **Optimizar inventario** en regiones con alta variabilidad (ej: TOTAL AUTOS AREA 2).
- **Reforzar campañas** en segmentos como "BLEACH" durante temporadas pico.
- **Incrementar producción** de productos en Cluster 3 para aprovechar su estabilidad.

---

## Resultados
![image](https://github.com/user-attachments/assets/2e1377ac-619e-45ca-b490-7a7da71d76ba)
![image](https://github.com/user-attachments/assets/ae880b00-ea62-42ef-8f51-d84484d085ac)
![image](https://github.com/user-attachments/assets/92cdc253-f6c2-4ea7-ad0b-80cc7087822f)
![image](https://github.com/user-attachments/assets/a8785ea4-670c-4378-b36a-429842300ee5)
![image](https://github.com/user-attachments/assets/faad6128-385b-4ce3-8901-02b6602c4e7a)
![image](https://github.com/user-attachments/assets/694e74aa-da8b-4d16-bc94-2e9c79905f36)
![image](https://github.com/user-attachments/assets/e5b9e347-023f-43f2-b8b5-518421a14112)
![image](https://github.com/user-attachments/assets/408232b8-741e-48e0-bbdd-8861b45fa9b8)
![image](https://github.com/user-attachments/assets/3b3de09a-ad77-434c-ac53-45ef923122bd)
![image](https://github.com/user-attachments/assets/4fff8e31-85fb-42d7-81b8-f673a8298930)
