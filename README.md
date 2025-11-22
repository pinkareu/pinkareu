# AI Support for Field Observation of Pollinators (Capstone)

Energy- and storage-efficient Raspberry Pi + AI-accelerator camera that saves images only when pollinators are detected.

Goals
- Reduce energy and storage for long-term ecological camera monitoring.
- Run lightweight object detection on embedded hardware and persist only relevant frames.

Key features
- YOLO-based detector optimized for edge inference.
- Raspberry Pi + Sony IMX500 camera sensor; supports Edge TPU/Movidius accelerators.
- On-device logic to save images when detections exceed a confidence threshold.
- Scripts to train, convert, and deploy models (see /models and /edge).

Quickstart
1. git clone https://github.com/pinkareu/pinkareu.git
2. Install dependencies: pip install -r models/requirements.txt && pip install -r edge/requirements.txt
3. Convert a trained model (models/convert) and copy model + edge/ to the Pi.
4. Run on the Pi: python3 edge/run_detection.py --model /path/to/model.tflite --conf 0.35 --save-dir /path/to/save

Hardware
- Raspberry Pi (see edge/HARDWARE.md for model specifics)
- Sony IMX500 sensor
- USB/NPU accelerator (e.g., Coral Edge TPU or Intel Movidius)

Contact
Favour Nwanna — https://www.linkedin.com/in/favour-nwanna-96a0321a1/