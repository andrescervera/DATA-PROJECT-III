## Características del Dataset

Las características del conjunto de datos se pueden clasificar en variables categóricas, binarias y continuas, cada una describiendo diferentes aspectos de la salud cardiovascular de los pacientes.

### Variables Continuas
- `age`: Edad del paciente en años.
- `trestbps`: Presión arterial en reposo (en mm Hg al ingreso en el hospital).
- `chol`: Colesterol sérico en mg/dl.
- `thalach`: Frecuencia cardíaca máxima alcanzada en reposo.
- `oldpeak`: Depresión del ST inducida por el ejercicio en relación con el reposo, medida en milímetros (mm).

### Variables Categóricas
- `cp`: Tipo de dolor de pecho:
  - 1: Angina típica
  - 2: Angina atípica
  - 3: Dolor no-anginoso
  - 4: Asintomático
- `restecg`: Resultados electrocardiográficos en reposo:
  - 0: Normal
  - 1: Anormalidad de la onda ST-T
  - 2: Hipertrofia ventricular izquierda
- `slope`: La pendiente del segmento ST en ejercicio máximo:
  - 1: Pendiente ascendente
  - 2: Plano
  - 3: Pendiente descendente
- `ca`: Número de vasos mayores (0-3) coloreados por fluoroscopia.
- `thal`: Resultados de la prueba de talio:
  - 3: Normal
  - 6: Defecto fijo
  - 7: Defecto reversible

### Variables Binarias
- `sex`: Sexo del paciente:
  - 0: Mujer
  - 1: Hombre
- `fbs`: Dolor provocado por el esfuerzo:
  - 0: No
  - 1: Sí
- `exang`: Angina inducida por el ejercicio:
  - 0: No
  - 1: Sí

### Variable Objetivo
- `label`: Grado de enfermedad cardíaca presente en el paciente (0-4), donde 0 indica ausencia de enfermedad.
