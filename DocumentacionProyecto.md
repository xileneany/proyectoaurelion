# Análisis de ventas por ciudad

## Tema
Optimización de la estrategia comercial mediante el análisis de ventas por ciudad. El objetivo es identificar zonas con alto y bajo rendimiento para tomar decisiones informadas que impulsen los ingresos.

---

## ❗ Problema
Actualmente no contamos con una visión clara sobre qué ciudades generan más ingresos y cuáles tienen bajo rendimiento comercial. Esta falta de información limita la capacidad de rediseñar estrategias específicas para mejorar las ventas en zonas menos activas.

---

## ✅ Solución propuesta

Utilizaremos Python y pandas para realizar un análisis de ventas por ciudad, siguiendo estos pasos:

1. **Unificación de datos**  
   - Integrar los archivos `Clientes.xlsx`, `Ventas.xlsx` y `Detalle_ventas.xlsx`.
   - Relacionar cada venta con la ciudad del cliente.

2. **Cálculo del total vendido por ciudad**  
   - Agrupar las ventas por ciudad.
   - Sumar el importe total por cada una.

3. **Generación de ranking de ciudades**  
   - Ordenar las ciudades según el volumen de ventas.
   - Identificar las más y menos rentables.

## (opcional)
4. **Visualización de resultados**  
   - Crear gráficos con `matplotlib` o `seaborn` para facilitar la interpretación.
   - Destacar oportunidades de mejora en ciudades con bajo rendimiento.

---

## 🎯 Resultado esperado

- Un reporte claro con el ranking de ventas por ciudad.
- Identificación de zonas con potencial de crecimiento.
- Base para rediseñar campañas, promociones o estrategias logísticas.