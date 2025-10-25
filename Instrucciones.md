
# 📘 Análisis de Ventas por Ciudad con Copilot

Este documento describe el proceso completo seguido con Copilot para construir el análisis de ventas por ciudad en Jupyter Notebook, incluyendo instrucciones, decisiones técnicas y correcciones aplicadas durante la ejecución.

---

## 🎯 Objetivo

Analizar el rendimiento comercial por ciudad a partir de archivos Excel, generando métricas clave como:

- Total vendido por ciudad
- Número de transacciones por ciudad
- Ticket promedio por ciudad

Además, se exportan los resultados y se generan visualizaciones para facilitar la interpretación.

---

## 📁 Archivos de entrada

Ubicados en:

/Users/macos/Downloads/BASE DE DATOS/


Archivos utilizados:

- `Clientes.xlsx`
- `Ventas.xlsx`
- `Detalle_ventas.xlsx`

---

## 🧠 Flujo de trabajo con Copilot

1. **Inicio del análisis:**
   - Se definió el objetivo y se propuso una solución en Python con `pandas`, `matplotlib` y `seaborn`.

2. **Ejecución inicial:**
   - Se intentó ejecutar el script desde la terminal con `/usr/local/bin/python3`, lo que generó errores de importación.

3. **Corrección de entorno:**
   - Se identificó que `pandas` estaba instalado en Anaconda.
   - Se corrigió la ejecución usando el Python de Anaconda:
     ```bash
     /opt/anaconda3/bin/python "ruta/del/script.py"
     ```

4. **Transición a Jupyter Notebook:**
   - Se ejecutó `jupyter notebook` desde la terminal.
   - Se creó un nuevo notebook en la carpeta del proyecto.

5. **Desarrollo modular:**
   - Copilot generó funciones para:
     - Limpieza de datos
     - Unificación de tablas
     - Cálculo de métricas
     - Visualización
     - Exportación

6. **Exportación de resultados:**
   - Se generaron los siguientes archivos en `/Users/macos/Downloads/BASE DE DATOS/salidas/`:
     - `metricas_ventas_por_ciudad.xlsx`
     - `total_vendido_por_ciudad.png`
     - `ticket_promedio_por_ciudad.png`
     - `transacciones_por_ciudad.png`

---

## 🛠️ Correcciones aplicadas

### 1. `ModuleNotFoundError: No module named 'pandas'`

**Causa:** El script se ejecutaba con el Python del sistema, donde no estaba instalado `pandas`.

**Solución:**
- Verificar instalación:
  ```bash
  pip install pandas

### 2. NameError: name 'agrupado' is not defined
Causa: Se intentó graficar sin haber ejecutado la celda que define la variable agrupado.

Solución:

Ejecutar primero la celda que contiene:

python
agrupado = detalle_ciudad.groupby('ciudad').agg(...)

### 3. FutureWarning de Seaborn sobre palette sin hue
Causa: Seaborn advirtió que el uso de palette sin hue será obsoleto en futuras versiones.

Solución:

Se actualizó el código de los gráficos:

python
sns.barplot(data=agrupado, x='ciudad', y='total_vendido', hue='ciudad', palette='viridis', legend=False)

### 4. Rutas incorrectas (/mnt/data/)
Causa: El código inicial usaba una ruta genérica que no coincidía con la ubicación real de los archivos.

Solución:

Se corrigió la ruta base:

python
base = "/Users/macos/Downloads/BASE DE DATOS/"