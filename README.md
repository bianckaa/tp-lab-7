# Laboratorio 9 — MM3014 Teoría de Probabilidades
**Biancka Raxón (24960) · Lázaro Díaz (24713)**

Simulación del proceso de llenado del álbum Panini del Mundial FIFA 2026 mediante técnicas de Monte Carlo.

---

## Descripción

El álbum consta de **980 estampas** distintas. Cada sobre contiene **7 estampas** (todas distintas dentro del mismo sobre). Se asume distribución uniforme e independiente entre sobres.

---

## Archivos

| Archivo | Descripción |
|---|---|
| `lab9-24960-24713.ipynb` | Notebook con todas las simulaciones de la Etapa 5 (álbum real N = 980) |
| `Lab9_Etapa5.pdf` | Informe con resultados, gráficas y reflexiones de la Etapa 5 |
| `README.md` | Este archivo |


## Etapa 5 — Álbum real (N = 980)

Parámetros: N = 980, S = 7, R = 1,000, semilla 2026.

Se usan menos repeticiones porque cada simulación es ~10× más costosa que con N = 100.

### Preguntas simuladas

| # | Pregunta | Temática |
|---|---|---|
| P1 | ¿Cuántos sobres y cuánto cuesta completar el álbum? Comparar con valor teórico. | Sobres esperados |
| P2 | ¿Cuál es la probabilidad de completarlo con Q 10,000 y con Q 15,000? | Presupuesto fijo |
| P3 | ¿Cuántas cajas se necesitan? ¿Conviene vs sobres sueltos? | Cajas vs sueltos |
| P4 | ¿Cómo varía el ahorro en función de K ∈ {2,3,4,5,6,8,10}? ¿Cuándo deja de ser significativo el ahorro marginal? | Intercambio de repetidas |
| P5 | ¿Cuántos sobres se necesitan para alcanzar el 90 % y 95 % del álbum? ¿Qué costo concentra el último tramo? | Escenarios extremos |

### Resultados principales

| Métrica | Valor |
|---|---|
| E[sobres] sin intercambio | 1,045 |
| Costo esperado sin intercambio | Q 9,931 |
| Prob. completar con Q 10,000 | 60.6 % |
| Prob. completar con Q 15,000 | 98.7 % |
| E[cajas] necesarias | 10.6 |
| E[sobres] con K = 2 / 4 / 10 | 194 / 258 / 356 |
| Ahorro con K = 2 / 4 / 10 | Q 8,087 / Q 7,477 / Q 6,546 |
| E[sobres] al 90 % del álbum | 321 |
| E[sobres] al 95 % del álbum | 417 |
| Costo del tramo 95 % → 100 % | Q 5,971 (60 % del total) |

---

## Cómo ejecutar

El notebook está diseñado para Google Colab. Abrirlo y ejecutar todas las celdas en orden — no requiere instalar nada adicional (numpy y matplotlib vienen incluidos).

```python
# Semilla usada en todas las simulaciones
np.random.seed(2026)
```

Para correr localmente:

```bash
pip install numpy matplotlib jupyter
jupyter notebook lab9-24960-24713.ipynb
```
