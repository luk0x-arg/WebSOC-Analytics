# SOC Level 2 · Forensic Security Analyzer 🛡️

Una aplicación web de alta precisión diseñada para analistas de SOC (Security Operations Center) y equipos de Blue Team. Permite importar registros de seguridad masivos (`.xlsx` o `.csv`), filtrar ruido operativo, clasificar automáticamente amenazas mediante un motor analítico heurístico y generar **informes profesionales en PDF** (tanto técnicos como ejecutivos adaptados para clientes o directivos) potenciados por inteligencia artificial local vía **Ollama**.

---

## 🚀 Características Principales

* **Motor Forense Automatizado:** Procesa registros corporativos clasificándolos por severidad (**High, Medium, Low, Normal**) y causa raíz (Fuerza Bruta, PowerShell malicioso, Inyecciones SQL, Phishing).
* **Filtrado Inteligente de Ruido:** Separa la actividad rutinaria de la infraestructura de los incidentes reales de seguridad.
* **Informes Profesionales en PDF (Estándar Tier-1):**
  * **Informe Técnico:** Diseñado para analistas e ingenieros, detallando taxonomía de ataques, métricas estrictas y un registro completo de evidencias forenses sin cortes de paginación.
  * **Informe Ejecutivo (C-Level):** Redactado 100% en lenguaje de negocios y gobernanza de riesgos, ideal para directores y clientes no técnicos.
* **Soporte Multi-Cliente Dinámico:** Adaptación automática del nombre de la organización a partir del archivo importado o personalizable desde la interfaz.
* **Integración con IA Local (Ollama):** Generación de dictámenes periciales basados exclusivamente en la evidencia disponible mediante modelos locales (ej. `qwen3:4b`).

---

## 🛠️ Stack Tecnológico

* **Frontend:** HTML5, Tailwind CSS, JavaScript ES6+.
* **Gráficos y Visualización:** Chart.js, Lucide Icons.
* **Procesamiento de Datos:** SheetJS (`xlsx.full.min.js`) para lectura local de archivos Excel y CSV.
* **Generación de Reportes:** `html2pdf.js` (basado en html2canvas y jsPDF).
* **Motor LLM:** Ollama (API local `http://localhost:11434`).

---

## ⚙️ Requisitos Previos

Para aprovechar al máximo las capacidades de análisis con inteligencia artificial, asegúrate de tener instalado y ejecutándose [Ollama](https://ollama.com/) en tu entorno local:

1. Instalar Ollama.
2. Descargar un modelo compatible (por ejemplo, el configurado por defecto en la app):
   ```bash
   ollama pull qwen3:4b