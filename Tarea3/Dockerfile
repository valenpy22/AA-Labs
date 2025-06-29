# Utilizamos la imagen base de PyTorch con soporte para CUDA (si tienes GPU) o CPU
FROM pytorch/pytorch:latest

# Instalamos las dependencias necesarias (como Jupyter)
RUN pip install --upgrade pip && \
    pip install jupyter notebook torch torchvision matplotlib numpy

# Definimos el directorio de trabajo en el contenedor
WORKDIR /workspace

# Exponemos el puerto de Jupyter Notebook
EXPOSE 8888

# Comando para iniciar Jupyter Notebook
CMD ["jupyter", "notebook", "--ip='0.0.0.0'", "--port=8888", "--no-browser", "--allow-root"]
