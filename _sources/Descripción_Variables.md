# Descripción de Variables

A continuación se describen las variables presentes en el dataset `diabetic_data.csv`, organizadas por categorías:

---

## 🔐 Variables de Identificación

| Variable       | Tipo       | Descripción |
|----------------|------------|-------------|
| `encounter_id` | Numérica   | Identificador único del encuentro hospitalario (visita). |
| `patient_nbr`  | Numérica   | Identificador único del paciente. |

---

## 👤 Datos Demográficos y de Ingreso

| Variable               | Tipo        | Descripción |
|------------------------|-------------|-------------|
| `race`                 | Categórica  | Raza del paciente. Valores: Caucasian, Asian, African American, Hispanic, Other. |
| `gender`               | Categórica  | Género del paciente. Valores: male, female, unknown/invalid. |
| `age`                  | Categórica  | Edad agrupada en intervalos de 10 años (ej. [50-60)). |
| `weight`               | Numérica/Categórica | Peso del paciente (en libras). Muchos valores faltantes. |
| `admission_type_id`    | Categórica (codificada) | Tipo de admisión (1=Emergency, 2=Urgent, 3=Elective, etc.). |
| `discharge_disposition_id` | Categórica (codificada) | Disposición al alta. Indica el destino del paciente al ser dado de alta. |
| `admission_source_id`  | Categórica (codificada) | Fuente de admisión (referencia médica, urgencias, etc.). |
| `time_in_hospital`     | Numérica    | Días de estancia en el hospital. |

---

## 🔬 Pruebas y Procedimientos

| Variable             | Tipo     | Descripción |
|----------------------|----------|-------------|
| `num_lab_procedures` | Numérica | Número de pruebas de laboratorio realizadas. |
| `num_procedures`     | Numérica | Número de procedimientos distintos realizados (excluye laboratorios). |
| `num_medications`    | Numérica | Número de medicamentos diferentes administrados. |
| `number_outpatient`  | Numérica | Número de visitas ambulatorias previas. |
| `number_emergency`   | Numérica | Número de visitas a urgencias previas. |
| `number_inpatient`   | Numérica | Número de ingresos hospitalarios previos. |
| `number_diagnoses`   | Numérica | Número de diagnósticos registrados. |

---

## 🏥 Diagnósticos Principales

| Variable | Tipo     | Descripción |
|----------|----------|-------------|
| `diag_1` | Categórica | Diagnóstico principal (código ICD9, 3 dígitos). |
| `diag_2` | Categórica | Diagnóstico secundario. |
| `diag_3` | Categórica | Diagnóstico adicional. |

---

## 💉 Resultados de Laboratorio

| Variable       | Tipo       | Descripción |
|----------------|------------|-------------|
| `max_glu_serum`| Categórica | Resultado máximo de glucosa en suero. Valores: >200, >300, normal, none. |
| `A1Cresult`    | Categórica | Resultado de hemoglobina A1C. Valores: >8, >7, normal, none. |

---

## 💊 Medicamentos Administrados

Cada una de las siguientes variables indica si el medicamento fue administrado y si hubo cambio de dosis.  
**Valores posibles:** `up`, `down`, `steady`, `no`.

**Variables:**

`metformin`, `repaglinide`, `nateglinide`, `chlorpropamide`, `glimepiride`, `acetohexamide`, `glipizide`, `glyburide`, `tolbutamide`, `pioglitazone`, `rosiglitazone`, `acarbose`, `miglitol`, `troglitazone`, `tolazamide`, `examide`, `citoglipton`, `insulin`, `glyburide-metformin`, `glipizide-metformin`, `glimepiride-pioglitazone`, `metformin-rosiglitazone`, `metformin-pioglitazone`

---

## ⚙️ Control del Tratamiento

| Variable      | Tipo       | Descripción |
|---------------|------------|-------------|
| `change`      | Categórica | Indica si hubo algún cambio en los medicamentos para la diabetes durante la estancia (`change`, `no change`). |
| `diabetesMed` | Categórica | Indica si se prescribió algún medicamento para la diabetes (`yes`, `no`). |

---

## 🎯 Variable Objetivo

| Variable     | Tipo       | Descripción |
|--------------|------------|-------------|
| `readmitted` | Categórica | Indica si el paciente fue readmitido y cuándo. Valores: `<30`, `>30`, `No`. |
