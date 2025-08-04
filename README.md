# 🔐 Key Fob Security Analysis

## 📌 Overview
This project focuses on **analyzing wireless key fob security** using **captured RF signals**.  
It includes **replay attack analysis**, **rolling code detection**, **bitstream decoding**, and **signal/data analysis** using the **Pearson correlation coefficient**.  

The workflow is designed for **controlled security research and academic purposes** only.

> ⚠️ **Disclaimer:** Use only on devices you own or have explicit permission to test. Unauthorized use may be illegal in your country.

---

## 📂 Project Structure
📦 keyfob-security-analysis
┣ 📜 README.md # Project documentation
┣ 📂 Data # Captured and processed signal data
┃ ┣ original_signal.iq
┃ ┣ replayed_signal.iq
┃ ┗ processed_packets.csv
┣ 📜 replay_attack_analysis.py # Analyze replayed vs. original signals
┣ 📜 rolling_code_identification.py # Detect rolling codes & decode bitstream
┣ 📜 signal_data_analysis.py # General signal and packet statistics
┣ 📜 pearson_coefficient.py # Calculate Pearson correlation between signals
┣ 📜 requirements.txt # Python dependencies
┗ 📂 results # Output graphs and analysis results
┣ replay_comparison.png
┣ rolling_code_graph.png
┗ pearson_heatmap.png

---

## ⚙️ Requirements
- **Python 3.8+**
- RTL-SDR / HackRF or other SDR hardware (for signal capture)
- Libraries:
pip install numpy scipy matplotlib pandas bitstring seaborn
🚀 How to Run
1️⃣ Replay Attack Analysis
Compare original and replayed key fob signals.
python replay_attack_analysis.py --original Data/original_signal.iq --replay Data/replayed_signal.iq --output results/replay_comparison.png
2️⃣ Rolling Code Identification & Bitstream Decoding
Detect rolling codes and extract decoded bitstream.
python rolling_code_identification.py --input Data/processed_packets.csv --output results/rolling_code_graph.png
3️⃣ Signal & Data Analysis
General statistics and visualization.
python signal_data_analysis.py --input Data/processed_packets.csv --output results/signal_stats.txt
4️⃣ Pearson Coefficient Analysis
Compute correlation between original and replayed signals.
python pearson_coefficient.py --original Data/original_signal.iq --replay Data/replayed_signal.iq --output results/pearson_heatmap.png

📊 Methodology
Signal Capture – Use SDR hardware to record .iq files.

Replay Attack Analysis – Compare replayed signals against original captures.

Rolling Code Identification – Find changing code segments between transmissions.

Bitstream Decoding – Convert RF captures into binary streams.

Pearson Correlation – Quantify similarity between original and replayed signals.

Visualization – Create plots for presentation & reporting.

| Replay Analysis                    | Rolling Code Visualization          | Pearson Correlation              |
| ---------------------------------- | ----------------------------------- | -------------------------------- |
| ![](results/replay_comparison.png) | ![](results/rolling_code_graph.png) | ![](results/pearson_heatmap.png) |

📜 Legal & Ethical Notice
Educational and research use only.

Testing without authorization is illegal.

Comply with local RF and cybersecurity laws.

👨‍💻 Author
Akshat Pal
[🔗 GitHub Profile](https://github.com/akshat4703) | akshat4703@gmail.com
