## Home

## Welcome to R.E.F.R.E.S.H

### Revolutionizing Formula 1 Driver Safety and Performance

#### 
R.E.F.R.E.S.H (Racing Equipment for Fluid Regulation and Enhanced Sweat Handling) is an innovative wearable glove system designed to improve the safety and efficiency of Formula 1 drivers. By integrating advanced sensor technology, real-time health monitoring, and efficient cooling mechanisms, this project addresses the unique challenges of high-performance racing.

## About the Project

### Background

#### 
Formula 1 drivers endure extreme physical and environmental stress during races, often experiencing dehydration, overheating, and cognitive fatigue. These conditions compromise their performance and safety.
R.E.F.R.E.S.H tackles these challenges with:
- Real-time monitoring of hydration, pulse, and SpO₂ levels.
- Dynamic cooling systems for temperature regulation.
- Reliable data transmission using LoRa technology for remote health management.

### Our Goal

####
Our project has the following objectives:

- Hydration Monitoring: Provide real-time feedback on hydration levels using GSR data, processed through a machine learning model.
- Vital Sign Tracking: Monitor heart rate and oxygen saturation with precision.
- Dynamic Cooling: Automatically adjust cooling intensity based on hydration levels.
- Reliable Communication: Ensure seamless data transmission using LoRa and a backup ESP32 system.

## Design

### Hardware Requirements Specification (HRS)

#### 
The hardware requirements focus on modularity, precision, and performance. Key specifications include:
- Microcontroller: ATmega328PB for sensor integration and control logic.
- Sensors:
    - MAX30102 Pulse Oximeter for SpO₂ and heart rate.
    - Grove GSR Sensor for hydration monitoring.
- Cooling System: PWM-controlled DC fan for temperature regulation.
- Communication Modules:
    - LoRa for long-range data transmission.
    - ESP32 for Wi-Fi-based backup communication.

### HRS Results

####
- The ATmega328PB successfully integrated with all sensors.
- The cooling system dynamically adjusted fan speeds by designing a PCB with MOSFETs and resistors.
- LoRa modules reliably transmitted data over medium distances under controlled conditions.

### Software Requirements Specification (SRS)

####
The software design supports data acquisition, real-time processing, and machine learning integration. Key specifications include:
- Data Acquisition: Use ADC for GSR data and I2C for pulse oximeter readings.
- Data Processing: ML model analyzes GSR data to determine hydration levels.
- Control Logic: Dynamic PWM adjustments for fan speed.
- Data Transmission: LoRa handles primary communication; ESP32 serves as a backup.

### SRS Results

####
- GSR data updated hydration levels every second.
- The ML model achieved 100% accuracy in classifying hydration levels.
- LoRa communication showed minimal latency over tested distances.

### Flow Diagram
####
*Add the flow diagram here with a small explanation

## Testing and Challenges

####
- LoRa Communication Issues: Inconsistent data transmission at longer ranges. Mitigated by using ESP32 as a backup.
- Sensor Calibration: Debugging static readings from the MAX pulse oximeter.
- Fan Control Heat Issues: Addressing heat dissipation issues in the cooling system’s MOSFET component.

## Results

### Performance Metrics

####
- Hydration Monitoring: GSR sensor classified hydration levels into Normal, Medium, and High categories with ML model accuracy of 100%.
- Cooling Effectiveness: Cooling response times improved with dynamic fan control based on GSR thresholds.
- Data Transmission: The backup ESP32 + Blynk communication system ensured reliable data logging.

## Conclusion

####
The REFRESH glove showcases a breakthrough in wearable technology for high-performance athletes. It combines precision monitoring, intelligent cooling, and robust communication, providing a holistic solution for Formula 1 drivers. Future work includes refining LoRa for better range and integrating additional biometric sensors.

## Media

### Video

####
Embed a demo video showcasing the glove’s features and functionality.

### Gallery

####
Upload images of the prototype, system architecture, and testing process.

## Team

### Meet the Creators

####
1. Chirag Satapathy
2. Sanskriti Binani
3. Megha Mistry

## Acknowledgments

####
We extend our gratitude to the University of Pennsylvania's ESE 5190 faculty and mentors for their guidance and support.
