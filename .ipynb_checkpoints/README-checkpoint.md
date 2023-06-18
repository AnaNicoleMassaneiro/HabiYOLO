# HabiYOLO
HabiYOLO: Detecção de Objetos em Ambientes Residenciais

1. Configurar o ambiente no Jupyter Lab:
   Antes de começar, certifique-se de ter o Jupyter Lab instalado em seu ambiente. Você pode instalá-lo executando o seguinte comando:
   
   ```
   pip install jupyterlab
   ```

   Depois de instalado, você pode iniciar o Jupyter Lab executando o comando:
   
   ```
   jupyter lab
   ```

2. Instalar as bibliotecas necessárias:
   No Jupyter Lab, você pode instalar as bibliotecas diretamente em uma célula de código. Certifique-se de ter instalado as seguintes bibliotecas:
   - OpenCV: Execute a célula de código abaixo:

     ```python
     !pip install opencv-python
     ```

   - PyTorch: Execute a célula de código abaixo:

     ```python
     !pip install torch
     ```

   - Detectron2: Execute a célula de código abaixo:

     ```python
     !pip install detectron2 -f https://dl.fbaipublicfiles.com/detectron2/wheels/cu111/torch1.9/index.html
     ```
     Note que o comando acima instala o Detectron2 para GPUs com suporte a CUDA 11.1 e PyTorch 1.9. Se você estiver usando uma configuração diferente, consulte a documentação oficial do Detectron2 para obter as instruções corretas.

3. Baixar o modelo pré-treinado YOLO:
   Fazer o download de um modelo YOLO pré-treinado.

4. Importar as bibliotecas necessárias:

   ```python
   import cv2
   import torch
   import numpy as np
   from habitat import make_dataset
   ```

5. Carregar o modelo YOLO pré-treinado:

   ```python
   model = torch.hub.load('ultralytics/yolov5', 'yolov5s')
   ```

6. Configurar o ambiente do Habitat:

   ```python
   dataset = make_dataset("your_dataset_config.yaml")
   ```

