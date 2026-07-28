# Visão Computacional

Visão Computacional é a área da IA voltada para extrair informação e significado a partir de imagens e vídeos. Combina técnicas de processamento de imagem com deep learning para resolver tarefas como reconhecimento de objetos, detecção facial e segmentação, sendo essencial em aplicações que vão de carros autônomos a diagnóstico médico por imagem.

## Conceitos principais
- Classificação de imagem: atribuir uma ou mais categorias a uma imagem inteira (ex.: "gato" ou "cachorro").
- Detecção de objetos: localizar e classificar múltiplos objetos em uma imagem, geralmente com caixas delimitadoras (bounding boxes), como em YOLO e Faster R-CNN.
- Segmentação semântica e de instância: classificar cada pixel de uma imagem por categoria (semântica) ou distinguir instâncias individuais do mesmo objeto (instância).
- Redes convolucionais (CNNs): arquitetura fundamental que usa filtros convolucionais para extrair características visuais em diferentes níveis de abstração.
- Vision Transformers (ViT): adaptação da arquitetura Transformer para imagens, tratando patches da imagem como tokens de sequência.
- Data augmentation: técnicas (rotação, corte, mudança de cor) para aumentar artificialmente a diversidade do conjunto de treino e melhorar generalização.
- Transfer learning: uso de modelos pré-treinados em grandes datasets (ImageNet) como ponto de partida para tarefas específicas com menos dados.
- OCR (Optical Character Recognition): extração de texto a partir de imagens ou documentos escaneados.
- Reconhecimento facial: identificação ou verificação de identidade a partir de características faciais, tema sensível do ponto de vista ético e regulatório.

## Na prática
- Frameworks e bibliotecas: OpenCV para processamento clássico de imagem; PyTorch/TensorFlow com modelos como ResNet, YOLO e ViT para deep learning.
- Casos de uso: inspeção de qualidade industrial, veículos autônomos, diagnóstico por imagem médica, controle de acesso por biometria, contagem de pessoas/objetos em vídeo.
- Modelos multimodais recentes (CLIP, GPT-4V) combinam visão e linguagem, permitindo buscar imagens por descrição textual ou gerar legendas automáticas.
- Ferramentas de anotação (Label Studio, CVAT) são usadas para criar datasets rotulados para treino supervisionado.

## Pontos de atenção
- Qualidade e diversidade do dataset de treino impactam diretamente a robustez do modelo a variações de iluminação, ângulo e ambiente.
- Reconhecimento facial e biometria envolvem riscos legais e éticos significativos, exigindo consentimento e conformidade regulatória (ex.: LGPD).
- Modelos de visão podem ser enganados por perturbações adversariais quase imperceptíveis ao olho humano.
- Desempenho em produção pode degradar significativamente se as condições de captura (câmera, resolução, iluminação) diferirem do ambiente de treino.
- Viés de representação em datasets (ex.: sub-representação de certos grupos demográficos) pode gerar desempenho desigual entre populações.
