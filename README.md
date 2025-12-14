# 📞 Proyecto Final – Identificación de Operadores Ineficientes

## 📌 Descripción General
El proyecto analiza información realista sobre llamadas telefónicas gestionadas por operadores a través de un sistema virtual (CallMeMaybe). El objetivo es identificar operadores ineficientes y validar, mediante análisis estadístico, si el **tiempo promedio de espera** es un indicador confiable de ineficiencia operativa.

La base de datos contiene más de **53,000 registros de llamadas** (entrantes, salientes e internas), con información sobre duración, espera, pérdidas de llamadas y operadores involucrados.

---

## 🎯 Objetivos del Proyecto

✔ Realizar análisis exploratorio para comprender comportamientos y patrones de llamadas  
✔ Identificar operadores ineficientes mediante métricas clave  
✔ Confirmar estadísticamente si el tiempo de espera es un indicador válido  
✔ Proponer métricas y criterios para monitorear desempeño operativo  

---

## 🗂️ Estructura de Archivos del Proyecto

| Archivo | Descripción |
|---------|-------------|
| `Proyecto_Final_Telecom.ipynb` | Notebook principal con análisis, visualizaciones y prueba estadística |
| `telecom_dataset_new.csv` | Datos de llamadas (call logs) |
| `telecom_clients.csv` | Información de operadores y planes tarifarios |
| `CA.pem` | Certificado SSL usado para conexión a base de datos |
| `README.md` | Documentación general del proyecto |

---

## 📊 Principales Hallazgos

| Métrica clave | Operadores Eficientes | Operadores Muy Ineficaces |
|---------------|------------------------|----------------------------|
| Tiempo de espera promedio | 30.46 s | 997.48 s |
| Mediana (50%) | 25.78 s | 814.00 s |
| Llamadas perdidas promedio | Baja | Alta |
| Variabilidad | Estable | Muy dispersa |

---

## 🧪 Prueba Estadística Realizada

### Hipótesis:
- **H₀:** El tiempo de espera promedio es igual entre operadores eficientes e ineficientes  
- **H₁:** El tiempo de espera promedio es mayor en operadores ineficientes (unilateral)

📌 **Prueba utilizada:** Mann-Whitney U (no paramétrica)  
📉 **Resultado:**  
- U-Statistic = 0.00  
- p-value = 0.00000  

✔ Como **p-value < 0.05**, se **rechaza H₀**  
👉 El tiempo de espera **sí es un indicador confiable de ineficiencia operativa**

---

## 📎 Métricas Recomendadas para Monitoreo

| Métrica | Umbral de alerta | Interpretación |
|---------|------------------|----------------|
| Avg_waiting_time | > 200 s | Posible ineficiencia |
| Missed_call_rate | > 40% | Mal desempeño | 
| Total_calls | < 20 llamadas mensuales | Baja productividad |
| Internal_call_rate | < 5% | Bajo uso del sistema interno |

---

## 🚀 Propuestas para la Empresa

✔ Crear ranking mensual de operadores según desempeño  
✔ Implementar alertas automáticas con Python / Power BI  
✔ Diseñar tablero en Tableau para seguimiento operativo  
✔ Ofrecer capacitación específica a operadores ineficientes  

---

## 🛠️ Tecnologías Utilizadas

| Tipo | Herramientas |
|------|--------------|
| Lenguaje | Python |
| Librerías | pandas, numpy, matplotlib, scipy, seaborn |
| Entorno | VS Code, Jupyter Notebook |
| Análisis estadístico | Mann-Whitney U |
| Visualización | Histogramas, pie charts, líneas temporales |

---

## 📚 Fuentes Documentales

El documento “Fuentes_documentales.pdf” incluye referencias utilizadas durante el proyecto:
- Documentación de pandas, scipy, matplotlib  
- Artículos académicos sobre Mann-Whitney  
- Guías de análisis de eficiencia operativa  
- Buenas prácticas para uso de KPIs  

---

## 📎 Presentación Final

📄 Versión PDF con visualizaciones, hallazgos y conclusiones.  
(Se agregará aquí un enlace una vez generada)

---

## ✨ Autor
**Ronin**  
Analista de Datos Jr. – Proyecto Final Bootcamp  
Noviembre 2025
