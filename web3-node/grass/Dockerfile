FROM ubuntu:24.04

# Install FPGA drivers
RUN apt-get update && apt-get install -y \
    ice40-fpga-driver \
    libgrassproof2025

# Bandwidth scheduler (off-peak optimization)
COPY bandwidth-cron /etc/cron.d/
RUN chmod 0644 /etc/cron.d/bandwidth-cron

ENTRYPOINT ["grass", "--fpga", "aggressive", "--region", "SG"]
