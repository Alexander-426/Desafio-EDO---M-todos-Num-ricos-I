# Modelo de Crecimiento Logístico en Huertos Urbanos (EDO de 1.er Orden)

Desafío individual de **Métodos Numéricos**. Modelado matemático de una situación real orientada al bienestar de una comunidad utilizando ecuaciones diferenciales ordinarias de primer orden y su comparación con métodos numéricos (Heun y Runge-Kutta de 4.° orden).

---

## 1. Descripción del Modelo y Contexto

* **Nombre del Desafío:** Modelo de Crecimiento Logístico de Biomasa en Huertos Urbanos Comunitarios.
* **Comunidad Beneficiaria:** Comedor Comunitario y Familias del Sector.
* **Problema Específico:** Predecir con exactitud el volumen total cosechable de hortalizas hidropónicas (en kg) a lo largo del tiempo para asegurar el abastecimiento del comedor comunitario local.
* **Pregunta de Investigación:** *¿Cuánta biomasa vegetal comestible (en kg) tendremos disponible en el huerto tras $t$ semanas y qué tan confiables son las predicciones numéricas frente al crecimiento real?*

### Formulación Matemática
Se utiliza el **Modelo Logístico de Crecimiento**, que contempla recursos limitados (espacio y nutrientes):

* **Ecuación Diferencial Ordinaria (EDO):**
  $$\frac{dy}{dt} = r \cdot y \left(1 - \frac{y}{K}\right)$$
* **Condición Inicial:** $y(0) = 5 \text{ kg}$
* **Parámetros:**
  * Tasa de crecimiento ($r$): $0.4 \text{ semana}^{-1}$
  * Capacidad de carga ($K$): $50 \text{ kg}$ (límite máximo de biomasa)
* **Solución Analítica Exacta:**
  $$y(t) = \frac{K \cdot y_0}{y_0 + (K - y_0)e^{-rt}}$$

---

## 2. Métodos Numéricos Implementados

El proyecto simula la evolución de la EDO mediante dos métodos numéricos con un tamaño de paso ($h$) configurable:
1. **Método de Heun (RK2):** Predictor de Euler y corrector basado en el promedio de pendientes.
2. **Runge-Kutta de 4.° Orden (RK4):** Método de alta precisión que evalúa cuatro pendientes ponderadas por intervalo.

---

## 3. Contenido del Repositorio

* `index.html`: Aplicación web interactiva completa (HTML5, CSS3, JavaScript, Chart.js y KaTeX) que incluye:
  * Simulador interactivo de parámetros en tiempo real.
  * Gráfica comparativa de soluciones (Analítica vs. Heun vs. RK4).
  * Tabla iterativa de resultados con cálculo de errores absolutos.
  * Desglose paso a paso de fórmulas matemáticas con sustituciones numéricas exactas.
  * Botón de exportación de datos a formato CSV.

---

## 4. Instrucciones de Ejecución

Puedes ejecutar este proyecto de dos formas sencillas:

### Opción A: Ejecución Local en el Navegador (Recomendado)
1. Clona este repositorio o descarga el archivo comprimido.
2. Asegúrate de tener el archivo `index.html` en tu equipo.
3. Haz doble clic sobre `index.html` o ábrelo directamente con cualquier navegador web moderno (Google Chrome, Firefox, Edge, Safari). No requiere instalación de servidores ni dependencias adicionales.

### Opción B: Visualización Online (GitHub Pages)
1. Accede a la URL pública desplegada en GitHub Pages: Enlace de la web
2. Modifica los parámetros iniciales directamente en los campos de entrada y haz clic en **"Calcular y Simular"** para actualizar la gráfica y la tabla de errores de forma dinámica.

---

## 5. Autor
* **Estudiante:** Cristian Alexander Quispe Espinal
* **Materia:** Métodos Numéricos
* **Fecha:** 6 de noviembre de 2026
