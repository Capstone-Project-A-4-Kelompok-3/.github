# Artificial Intelligence of Things (AIoT) | Capstone

## Automated Counting Station
**Sistem Verifikasi Kuantitas Part Mikro Menggunakan Density Map Estimation dan Sensor Fusion Berbasis Edge Computing**  
**AI-based Density Map Estimation and Sensor Fusion for IQC Part Verification**

## Project Domain
Our **Automated Counting Station** is built to automate Incoming Quality Control (IQC) verification for micro parts (such as screws and gears) inside sealed transparent plastic packaging. By combining **Artificial Intelligence (Density Map Estimation)** and **Sensor Fusion (weight counting)** on **Edge Computing**, the system avoids manual unsealing while improving accuracy, hygiene, and operational efficiency.

## Meet Our Team "Why-Fi"
- **Hardware & Sensor Engineer:** JONATHAN ARYA PRIGUNA (235150301111015)
- **Hardware & Sensor Engineer:** ACHMAD FIKY AKBAR (235150301111043)
- **System Integration Engineer:** NABILLAH SEPTIANISA NUR A (235051707111002)
- **Business & System Analyst:** ANNISA KAYLA JASMINE (235150407111004)
- **Machine Learning Engineer:** ATHAR IFTIKHAR AKHSAN (235150200111010)
- **Machine Learning Engineer:** ARSA MAULANA ADHYASTA (235150201111030)

## Problem Statements
1. Traditional verification of micro parts (< 3 grams) requires operators to open sealed transparent plastics manually, reducing hygiene standards and increasing repackaging workload.
2. Manual counting is highly prone to human error, with around **±3% discrepancy** between actual quantity and vendor data, potentially causing production stop-lines.
3. There is no integrated digital documentation system for real-time inspection evidence, making historical tracking, audits, and vendor claim processes (Return Delivery Order/R1) difficult.

## Goals
1. Develop an AI model to estimate heavily overlapping micro-part counts through plastic packaging with low **Mean Absolute Error (MAE)**.
2. Integrate visual estimation with load-cell data (sensor fusion) to cross-validate results and reduce error margins versus manual methods.
3. Deploy a secure standalone edge station with synchronized dashboard for real-time **OK/NG** status and automated logs for internal and vendor monitoring.

## Solution Statements
1. Implement **Density Map Estimation (DME)** using Gaussian Heatmaps to handle severe overlap where conventional object detection (e.g., YOLO) struggles.
2. Build a **Decision Matrix** that compares AI prediction and physical weight against tolerance limits to output **Accept (OK)** or **Reject (NG)**.
3. Use **Edge PC** for local AI inference (< 3 seconds), aligned with factory data privacy requirements.
4. Integrate **SQLite (local)** and **Supabase (cloud)** to support a React-based analytics dashboard.

## Prerequisites – Component Preparation
### Hardware Powerhouse
- **Edge PC / Laptop** with NVIDIA RTX GPU for local inference.
- **Web Camera (1080p)** for image capture.
- **Load Cell (HX711)** for precision weight measurement.
- **Diffuse Lighting System** to reduce glare/reflection on transparent plastics.

### Software & Platforms
- **Python & OpenCV** for camera streaming and preprocessing.
- **PyTorch** for training/inference with MobileNetV2-based DME.
- **Albumentations** for robust augmentation (glare and lighting variation handling).
- **SQLite & Supabase** for local/cloud logging and synchronization.
- **React & Tailwind CSS** for interactive QC analytics dashboard.

## Schematic
> _[Gambar Arsitektur Sistem, Flowchart Edge PC & Dashboard]_

## Demo and Evaluation
- **Demo:** Real-time verification of sealed plastic bags containing overlapping screws. The system captures images, generates a density heatmap, reads live weight, and displays final **OK/NG** status and discrepancy logs on the dashboard.  
  **Demo link:** _(Insert Google Drive / YouTube URL)_

- **Dashboard Access:**
  > _Example account formats only (replace with authorized internal credentials)._
  - `admin@example.com`
  - `vendor1@example.com`
  - `vendor2@example.com`

- **Evaluation Results:**
  - Tested on **119 varied datasets** and real-time inference scenarios.
  - **AI Visual Counting Accuracy:** MAE of ~**4.73** for severely overlapped objects.
  - **Processing Speed:** < **3 seconds** per package.
  - **Hardware Stability:** Weight signal noise reduced with **Exponential Moving Average (EMA)** filtering.
  - **Data Synchronization:** **100% success rate** for local logging and NG alert cloud sync.

## Conclusion
This project delivers an **Edge Computing-based Automated Counting Station** that transforms IQC workflows. By replacing bounding-box counting with **Density Map Estimation**, the system handles extreme overlap and plastic glare more reliably. Combined with precision load-cell validation, it achieves fast and accurate verification without sacrificing factory data privacy. Local edge processing plus cloud analytics provides transparent audit trails for management and vendors, reducing discrepancy risk and preventing production disruptions.

## Contact Us
- **Our GitHub:** https://github.com/Capstone-Project-A-4-Kelompok-3
- **Our LinkedIn:**
  - [Jonathan Arya Priguna](https://www.linkedin.com/in/jonathan-arya-priguna)
  - [Achmad Fiky Akbar](https://www.linkedin.com/in/achmad-fiky-akbar)
  - [Nabillah Septianisa Nur Azizah](https://www.linkedin.com/in/nabillah-septianisa-nur-azizah)
  - [Annisa Kayla Jasmine](https://www.linkedin.com/in/annisa-kayla-jasmine)
  - [Athar Iftikhar Akhsan](https://www.linkedin.com/in/athar-iftikhar-akhsan)
  - [Arsa Maulana Adhyasta](https://www.linkedin.com/in/arsa-maulana-adhyasta)

## Behind the Lens
> _[Foto-foto Behind The Scenes Tim "Why-Fi" saat merakit Inspection Box, melabeli dataset, dan saat uji coba]_
