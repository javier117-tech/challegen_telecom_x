# 📉 Análisis de Evasión de Clientes

## 🎯 Objetivo
Identificar las categorías y variables que influyen en la evasión de los clientes.

## ❓ Problema
¿Por qué la empresa presenta una alta tasa de cancelación y pérdida de clientes?

---

## 🧹 Limpieza y Tratamiento de Datos

- Se importaron las bibliotecas `pandas` y `requests` para el tratamiento de datos y las peticiones HTTP.
- Se cargaron los datos desde un archivo JSON mediante una petición `GET`, y se convirtieron a formato `DataFrame`.
- Se normalizaron los datos para facilitar el análisis.
- Se revisaron valores nulos, valores únicos y duplicados.
- Se limpiaron los valores vacíos y se convirtieron tipos de datos (por ejemplo, `account.Charges.Total` a `float`).
- Se creó una nueva columna llamada **cuentas diarias** y se eliminó la última fila.
- Se visualizó el `DataFrame` final para confirmar que los datos estaban listos para el análisis.

---

## 📊 Análisis Exploratorio de Datos

Se utilizaron herramientas de visualización como `plotly.express` para comprender mejor los patrones de cancelación:

### 1. **Género**
- Hombres y mujeres presentan tasas de cancelación similares.
- ✅ El género **no es un factor determinante**.

### 2. **Edad (SeniorCitizen)**
- Mayores de 65 años presentan mayor tasa de evasión.
- 🔍 La edad influye en la cancelación.

### 3. **Antigüedad (tenure)**
- A mayor duración del contrato, menor tasa de cancelación.
- 🕓 Clientes nuevos cancelan más.

### 4. **Tipo de contrato**
- Contratos mensuales → mayor evasión.
- Contratos a 2 años → menor evasión.
- 💡 Fomentar contratos de largo plazo.

### 5. **Cargos mensuales (`account.Charges.Monthly`)**
- Clientes que cancelan tienden a pagar más.
- 📉 Costo puede influir, pero no es el único factor.

### 6. **Servicio telefónico (`phone.PhoneService`)**
- Menor cancelación entre quienes tienen el servicio.
  
### 7. **Tipo de internet (`internet.InternetService`)**
- Fibra óptica → mayor tasa de evasión.
- Sin internet → menor tasa de cancelación.

### 8. **Servicio de StreamingTV**
- Usuarios con este servicio cancelan más.

---

## ✅ Conclusiones

- El género **no influye significativamente** en la evasión.
- Clientes **mayores de 65 años**, con **contratos mensuales** y **menor antigüedad** tienden a cancelar más.
- Muchos clientes cancelan incluso con **tarifas bajas**, lo que sugiere que **la percepción de valor** y **la experiencia inicial** son más relevantes que el costo.
- Servicios como **fibra óptica** y **StreamingTV** están asociados a tasas más altas de cancelación, lo cual puede deberse a la calidad del servicio, expectativas no cumplidas o fuerte competencia.

---

## 💡 Recomendaciones

- Fomentar contratos a largo plazo (anuales o bienales).
- Mejorar la experiencia del cliente en los primeros meses.
- Analizar la calidad y satisfacción de servicios como fibra óptica y StreamingTV.
- Desarrollar estrategias de retención personalizadas según el perfil del cliente.

---

📁 Proyecto desarrollado en Google Colab utilizando Python y bibliotecas de análisis de datos.
