# telecomX
# Análisis de Fuga de Clientes en TelecomX

## 📌 Objetivo

Este proyecto tiene como objetivo analizar el comportamiento de los clientes de **TelecomX** con el fin de identificar **patrones de evasión (churn)** y proponer mejoras para reducir la pérdida de clientes.

---

## 🛠 Tecnologías utilizadas

- `pandas` – para el manejo de datos
- `numpy` – para operaciones matemáticas
- `matplotlib.pyplot` – para visualización de datos
- `plotly.express` – para gráficos interactivos

---

## 1️⃣ Introducción

TelecomX presenta una **alta tasa de fuga de clientes**, motivo por el cual solicita un análisis profundo de sus datos. Nuestro objetivo es recopilar, limpiar, transformar y analizar los datos para encontrar patrones de evasión y puntos de mejora en el servicio.

---

## 2️⃣ Limpieza y Tratamiento de Datos

- Se importaron los datos desde un archivo JSON con columnas anidadas.
- Se normalizó el DataFrame y se detectaron incoherencias, las cuales fueron tratadas (valores vacíos, tipos incorrectos).
- Se estandarizaron los nombres de columnas al español para facilitar la lectura.
- Se convirtieron valores categóricos como `"Sí"` / `"No"` a binarios (`1`, `0`).
- Se creó una nueva columna llamada `Cuentas_Diarias`, derivada del valor de cargos mensuales dividido por 30.
- Se manejaron valores faltantes de forma explícita, usando `-1` como código especial cuando fue necesario.

---

## 3️⃣ Análisis Exploratorio de Datos (EDA)

Se calcularon medidas estadísticas como:

- **Media, mediana y desviación estándar** para variables numéricas.
- Distribuciones y porcentajes para variables categóricas y booleanas.

### 🔍 Principales visualizaciones:

- 📊 **Distribución de clientes activos:** Solo ~22% de los clientes están activos actualmente.
- 📉 **Clientes mayores de 65 años:** Aunque son menos, presentan una mayor tasa de churn proporcionalmente.
- 📆 **Duración del contrato:** Clientes con contratos "mes a mes" tienen una mayor tasa de evasión.
- 📡 **Tipo de servicio de internet:** Se identificó alta fuga de clientes que usan **fibra óptica**, lo cual puede indicar problemas en la calidad del servicio.
- 💳 **Método de pago:** El método `Electronic Check` está asociado a una fuga significativamente más alta que otros métodos.

---

## 4️⃣ Conclusiones e Insights

- Los clientes **mayores de 65 años** muestran un patrón de mayor evasión.
- Los **contratos de corto plazo** (mes a mes) tienen una alta correlación con churn.
- A pesar de ser un servicio moderno, **la fibra óptica presenta alta tasa de fuga**.
- El **método de pago `Electronic Check`** es un factor claro de riesgo de fuga.

---

## 5️⃣ Recomendaciones

- 📞 Mejorar el servicio y soporte personalizado para personas mayores.
- 🤝 Ofrecer incentivos para contratos de mayor duración (descuentos, beneficios).
- ⚙️ Auditar y optimizar la calidad del servicio de fibra óptica.
- 💰 Mejorar la experiencia de pago para quienes usan `Electronic Check` y promover métodos alternativos.

---

## 📂 Estructura de archivos

- `TelecomX_Data.json` – fuente de datos original
- `notebook.ipynb` – proceso de análisis, limpieza y visualización
- `descarga.png` a `newplot (5).png` – gráficos generados en el análisis
- `README.md` – este archivo

---

## 📌 Estado del proyecto

✅ **Finalizado** – listo para presentar o aplicar a modelos predictivos en futuras etapas.
