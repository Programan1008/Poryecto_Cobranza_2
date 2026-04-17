# 🏦 Análisis de Contactabilidad y Eficiencia Operacional en Gestión de Cobranza

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=flat&logo=pandas)
![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E?style=flat&logo=scikit-learn)
![Status](https://img.shields.io/badge/Estado-Activo-4CAF50?style=flat)

> **Caso de Negocio Simulado** orientado al rol de **Analista de Procesos Jr. —**, simulando el proceso operativo real de un departamento de Cobranza bancaria en Chile.

---

## 🎯 Problema de Negocio

| | |
|---|---|
| **Área** | Dpto. de Cobranza — Mejora Continua y Procesos |
| **Problema** | Baja contactabilidad, gestiones ineficientes y recursos mal asignados sin segmentación |
| **Metodología** | EDA → KPIs → Detección cuellos de botella → Segmentación → ML → Plan de mejora |
| **Enfoque** | Proceso · Datos · Indicadores · Mejora Continua · Python |

---

## 🗂️ Estructura del Repositorio

```
cobranza-eficiencia-operacional/
│
├── 📓 Contactabilidad_Eficiencia_Operacional.ipynb  ← Notebook principal
├── 📄 operacional_cobranza.csv                      ← Dataset (3.000 gestiones)
├── 📄 lista_campana_prioritaria.csv                 ← Output: Top 200 prioritarios
└── 📋 README.md
```

---

## 📁 Dataset — Variables Clave

| Variable | Descripción |
|---|---|
| `gestion_id` | ID único de la gestión |
| `fecha` / `mes` | Fecha de la gestión |
| `gestor_id` | Ejecutivo que realizó la gestión (25 gestores) |
| `tipo_cliente` | dependiente / independiente / jubilado / microempresario |
| `producto` | Tipo de crédito |
| `deuda` / `dias_mora` | Monto y antigüedad de la deuda |
| `estado_cuenta` | vigente / castigado / prejuridico / juridico |
| `franja_horaria` | mañana / tarde / noche |
| `canal` | teléfono / whatsapp / email / visita / carta notarial |
| `intentos_previos` | N° de intentos sin contacto anteriores |
| `contactado` | 0/1 — ¿Se logró contactar? |
| `resultado_contacto` | promesa_pago / convenio_acordado / no_contesta / etc. |
| `pago_realizado` | 0/1 — Variable objetivo ML |
| `promesa_cumplida` | 0/1 — Seguimiento de compromisos |
| `tiempo_gestion_min` | Duración de la gestión en minutos |

---

## 📊 Contenido del Notebook (12 secciones)

| Sección | Descripción |
|---|---|
| 1. Setup | Librerías, paleta corporativa |
| 2. Carga y exploración | Calidad del dato, tipos, estructura |
| 3. KPIs operacionales | Tablero ejecutivo completo |
| 4. EDA distribuciones | Perfil del cliente y la cartera |
| 5. Análisis contactabilidad | Por franja, canal, producto, heatmap |
| 6. Cuellos de botella | Resultado gestiones, intentos fallidos, evolución mensual |
| 7. Segmentación eficiencia | Matriz 2×2 contactabilidad × recuperación |
| 8. Desempeño gestores | Ranking, score global, scatter performance |
| 9. Modelo ML | LR, DT, RF, GBM — predicción de pago |
| 10. Visualizacion y Evaluación Modelos ML | ROC, confusion matrix, feature importance |
| 11. Scoring y priorización | Top 200 clientes prioritarios exportados |
| 12. Plan de mejora | AS-IS → TO-BE + KPIs objetivo |

---

## 🤖 Resultados ML

| Modelo | AUC-ROC | Accuracy | F1 |
|---|---|---|---|
| Logistic Regression | ~0.79 | ~0.73 | ~0.72 |
| Decision Tree | ~0.77 | ~0.74 | ~0.74 |
| **Gradient Boosting** | **~0.84** | **~0.78** | **~0.78** |
| Random Forest | ~0.83 | ~0.77 | ~0.77 |

**Variables más importantes:** `dias_mora`, `score_riesgo`, `contactado`, `ratio_deuda_ingreso`, `franja_horaria`

---

## 🔄 Plan AS-IS → TO-BE

| AS-IS | TO-BE |
|---|---|
| Contacto sin segmentación horaria | Priorizar franja tarde |
| Canal único | Multi-canal por perfil de cliente |
| Mora indiferenciada | Alerta automática mora 0-30 días |
| Sin seguimiento promesas | Alerta vencimiento de promesas |
| Sin scoring | Score ML diario — top 200 al inicio del turno |

---

## 🛠️ Stack

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn` · `Jupyter`

---

## 🚀 Cómo ejecutar

```bash
git clone https://github.com/Programan1008/Poryecto_Cobranza_2.git
cd cobranza-eficiencia-operacional
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook Contactabilidad_Eficiencia_Operacional.ipynb
```

---
## 👤 Autor

**Cristopher Jiménez Escobar** — Analista de Procesos Jr.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Perfil-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/www.linkedin.com/in/programan1008)
[![GitHub](https://img.shields.io/badge/GitHub-Portafolio-181717?style=flat&logo=github)](https://github.com/https://github.com/Programan1008)
