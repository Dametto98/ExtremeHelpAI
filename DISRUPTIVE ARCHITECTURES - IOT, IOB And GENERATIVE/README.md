# ExtremeHelp: Classificador de Desastres com Visão Computacional

Este projeto é o protótipo funcional (MVP) do componente de Inteligência Artificial para o aplicativo ExtremeHelp. O objetivo é utilizar Visão Computacional para classificar imagens de diferentes cenários de desastres (enchentes, incêndios, etc.), a fim de gerar alertas mais precisos e otimizar os esforços de ajuda humanitária.

## 🛠️ Tecnologias Utilizadas
- **Python 3.11**
- **TensorFlow / Keras**
- **Pillow (PIL)**
- **Numpy**
- **Matplotlib**
- **Ambiente:** Google Colab (recomendado)

## 🚀 Configuração e Execução (Passo a Passo)

O método recomendado para execução é utilizando o **Google Colab**, que já possui as bibliotecas necessárias e oferece poder computacional gratuito (GPU).

### **Passo 1: Download e Preparação do Dataset**

1.  **Faça o Download:** Baixe o dataset de imagens a partir do seguinte link no Kaggle:
    * **Link:** [Disaster Images Dataset](https://www.kaggle.com/datasets/brsdincer/disaster-images-dataset)

2.  **Organize os Arquivos:** Após baixar e descompactar, você precisará organizar as imagens na seguinte estrutura de pastas. Crie uma pasta principal chamada `meu_dataset_desastres`.
    * **Estrutura Final Necessária:**
        ```
        meu_dataset_desastres/
        ├── train/
        │   ├── Damaged_Infrastructure/
        │   ├── Fire_Disaster/
        │   └── Human_Damage/
        │   └── Land_Disaster/
        │   └── Non_Damage/
        │   └── Water_Disaster/
        └── validation/
        │   ├── Damaged_Infrastructure/
        │   ├── Fire_Disaster/
        │   └── Human_Damage/
        │   └── Land_Disaster/
        │   └── Non_Damage/
        │   └── Water_Disaster/
        ```
    * **Importante:**
        * Cuidado com as subpastas! Traga-as para o nível indicado.
        * Divida as imagens de cada classe, colocando aproximadamente 80% em `train` e 20% em `validation`.
        * Garanta que não existam subpastas extras dentro das pastas de cada classe (ex: `train/Fire_Disaster/subpasta_extra`). As imagens devem estar diretamente dentro de `train/Fire_Disaster/`.

3.  **Compacte o Projeto:** Após organizar a pasta `meu_dataset_desastres`, compacte-a em um único arquivo chamado `meu_dataset_desastres.zip`.

### **Passo 2: Execução no Google Colab**

1.  Abra o notebook `ExtremeHelp.ipynb` no Google Colab.
2.  No menu à esquerda, clique no ícone de pasta 📁 e, em seguida, no ícone **"Fazer upload"** 📤. Selecione o arquivo `meu_dataset_desastres.zip` que você acabou de criar.
3.  Execute as células em ordem. A maneira mais fácil é ir ao menu **"Ambiente de execução"** e clicar em **"Executar tudo"**.

O notebook está programado para:
- **Descompactar os dados**: A primeira célula de código (`!unzip`) irá extrair as imagens.
- **Limpeza de Dados**: Uma célula de verificação irá remover automaticamente qualquer imagem corrompida.
- **Treinamento e Avaliação**: O modelo será treinado e, ao final, serão exibidos os resultados de performance.

### **Passo 3: Testando uma Nova Imagem**
A última célula do notebook contém uma função para carregar uma nova imagem e usar o modelo treinado para prever a qual classe de desastre ela pertence. Você pode alterar o caminho da imagem para testar com seus próprios exemplos.
