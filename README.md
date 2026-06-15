# Artificial Intelligence of Things (AIoT) | Capstone

## Automated Counting Station
**Sistem Verifikasi Kuantitas Part Mikro Menggunakan Density Map Estimation dan Sensor Fusion Berbasis Edge Computing**  
**AI-based Density Map Estimation and Sensor Fusion for IQC Part Verification**

## Project Domain
Our **Automated Counting Station** is built to automate Incoming Quality Control (IQC) verification for micro parts (such as screws and gears) inside sealed transparent plastic packaging. The solution combines **Artificial Intelligence (Density Map Estimation)** and **Sensor Fusion (weight counting)** on **Edge Computing**. This approach avoids manual unsealing while improving accuracy, hygiene, and operational efficiency.

## Meet Our Team "Why-Fi"
- **Hardware & Sensor Engineer:** Jonathan Arya Priguna
- **Hardware & Sensor Engineer:** Achmad Fiky Akbar
- **System Integration Engineer:** Nabillah Septianisa Nur Azizah
- **Business & System Analyst:** Annisa Kayla Jasmine
- **Machine Learning Engineer:** Athar Iftikhar Akhsan
- **Machine Learning Engineer:** Arsa Maulana Adhyasta

## Problem Statements
1. Traditional verification of micro parts (< 3 grams) requires operators to open sealed transparent plastics manually, reducing hygiene standards and increasing repackaging workload.
2. Manual counting is highly prone to human error, with around **±3% discrepancy** between actual quantity and vendor data, potentially causing production line stoppages.
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
System architecture and flowchart assets are being finalized and will be published soon.

## Demo and Evaluation
- **Demo:** Real-time verification of sealed plastic bags containing overlapping screws. The system captures images, generates a density heatmap, reads live weight, and displays final **OK/NG** status and discrepancy logs on the dashboard.  
  **Demo link:** _Coming soon._

- **Dashboard Access:**
  Access credentials are managed internally. Please contact the project team or refer to internal documentation for authorized account access.

- **Evaluation Results:**
  - Tested on **119 varied test packages** and real-time inference scenarios.
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
Behind-the-scenes team photos and testing footage will be published after final media curation.
