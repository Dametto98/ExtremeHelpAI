# ExtremeHelp Classificador de Desastres com Visão Computacional

Este projeto é o protótipo funcional (MVP) do componente de Inteligência Artificial para o aplicativo ExtremeHelp. [cite_start]O objetivo é utilizar Visão Computacional para classificar imagens de diferentes cenários de desastres (enchentes, incêndios, etc.), a fim de gerar alertas mais precisos e otimizar os esforços de ajuda humanitária.

## 🛠️ Tecnologias Utilizadas
- Python 3.11
- [cite_start]TensorFlow  Keras 
- Pillow (PIL)
- Numpy
- Matplotlib
- Ambiente Google Colab (recomendado)

## 🚀 Configuração e Execução (Passo a Passo)

O método recomendado para execução é utilizando o Google Colab, que já possui as bibliotecas necessárias e oferece poder computacional gratuito (GPU).

### Passo 1 Preparar o Projeto
1.  Faça o download deste repositório.
2.  Você precisará do arquivo `ExtremeHelp.ipynb` e do dataset compactado `meu_dataset_desastres.zip`.

### Passo 2 Executar no Google Colab
1.  Acesse o [Google Colab](httpscolab.research.google.com).
2.  Faça o upload do notebook `ExtremeHelp.ipynb`.
3.  No menu à esquerda, clique no ícone de pasta 📁 e, em seguida, no ícone Fazer upload 📤. Selecione o arquivo `meu_dataset_desastres.zip`.
4.  Execute as células em ordem A maneira mais fácil é ir ao menu Ambiente de execução e clicar em Executar tudo.

O notebook está programado para seguir a seguinte lógica automaticamente
- Descompactar os dados A primeira célula de código (`!unzip`) irá extrair as imagens.
- Limpeza de Dados A célula seguinte irá verificar e remover automaticamente qualquer imagem corrompida ou truncada para garantir a integridade do treinamento.
- Treinamento do Modelo O modelo de Rede Neural Convolucional (CNN) será construído e treinado com os dados limpos.
- Avaliação Ao final, serão exibidos gráficos de acurácia, perda e uma matriz de confusão para avaliar a performance do modelo.

### Passo 3 Testando uma Nova Imagem
A última célula do notebook contém uma função para carregar uma nova imagem e usar o modelo treinado para prever a qual classe de desastre ela pertence. Você pode alterar o caminho da imagem para testar com seus próprios exemplos.