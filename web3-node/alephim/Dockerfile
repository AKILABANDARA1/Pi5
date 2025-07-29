FROM alephim/rpi5-inference:2025.8

# Coral TPU dependencies
RUN curl https://py.tpu/install.sh | bash

# 4-bit quantized model (pre-downloaded)
COPY --from=quantizer /phi2-4b-gguf /models/

CMD ["serve", "--accelerator", "coral", "--quant", "gguf-4bit", "--geo", "eu-central"]
