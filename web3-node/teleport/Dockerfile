FROM python:3.11-slim

# Install LoRa/BLE stack
RUN apt-get update && apt-get install -y \
    lorawan-scanner \
    bluez \
    libbluetooth-dev

COPY ble_scanner.py /app/

ENTRYPOINT ["python", "/app/ble_scanner.py", "--hotspots", "colombo_centre,galle_face"]
