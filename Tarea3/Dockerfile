# Utilizamos la imagen base de PyTorch con soporte para CUDA (si tienes GPU) o CPU
FROM pytorch/pytorch:latest

# Instalamos git y las dependencias necesarias (como Jupyter, las versiones compatibles de torch y CLIP)
RUN apt-get update && \
    apt-get install -y git && \
    pip install --upgrade pip && \
    pip install jupyter notebook torch==2.6.0 torchvision==0.21.0 matplotlib numpy && \
    pip install git+https://github.com/openai/CLIP.git  # Installing CLIP from GitHub

# Definimos el directorio de trabajo en el contenedor
WORKDIR /workspace

# Exponemos el puerto de Jupyter Notebook
EXPOSE 8888

# Comando para iniciar Jupyter Notebook
CMD ["jupyter", "notebook", "--ip='0.0.0.0'", "--port=8888", "--no-browser", "--allow-root"]
