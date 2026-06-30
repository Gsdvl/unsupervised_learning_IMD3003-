# Identificacao de Transacoes Fraudulentas com Aprendizado Não Supervisionado

Projeto da disciplina **IMD3003 - Aprendizado de Maquina Não Supervisionado**.

O objetivo do notebook e analisar transacoes de cartao de credito e aplicar tecnicas de aprendizado nao supervisionado, incluindo limpeza dos dados, analise exploratoria, escalonamento e reducao de dimensionalidade com PCA.

## Link Para Apresenação

[Apresentação de slides](https://canva.link/omj81v6ea0b6uid)

## Base de Dados

A base utilizada esta disponivel no Hugging Face:

https://huggingface.co/datasets/pointe77/credit-card-transaction

O notebook espera que o arquivo CSV original esteja salvo em:

```text
data/credit_card_transaction_train.csv
```

O arquivo `data/dados_limpos.csv` e gerado automaticamente pelo notebook apos a etapa de limpeza.

## Como Preparar o Projeto

1. Clone ou baixe este repositorio.

2. Crie a pasta `data` na raiz do projeto, caso ela ainda nao exista:

```bash
mkdir data
```

3. Acesse o dataset no Hugging Face:

```text
https://huggingface.co/datasets/pointe77/credit-card-transaction
```

4. Faca o download do arquivo CSV de treino.

5. Salve o arquivo dentro da pasta `data` com este nome:

```text
credit_card_transaction_train.csv
```

Ao final, a estrutura esperada deve ficar assim:

```text
unsupervised_learning_IMD3003-/
|-- data/
|   `-- credit_card_transaction_train.csv
|-- notebook.ipynb
|-- README.md
`-- .gitignore
```

## Dependencias

O notebook utiliza principalmente:

- pandas
- numpy
- matplotlib
- scikit-learn

As dependencias tambem sao instaladas dentro do proprio notebook. Se preferir instalar antes de executar, use:

```bash
pip install pandas numpy matplotlib scikit-learn
```

## Como Rodar o Notebook

1. Abra o projeto no VS Code, Jupyter Notebook, JupyterLab ou Google Colab.

2. Abra o arquivo:

```text
notebook.ipynb
```

3. Execute as celulas na ordem.

4. A primeira etapa faz a limpeza do arquivo:

```text
data/credit_card_transaction_train.csv
```

e gera o arquivo tratado:

```text
data/dados_limpos.csv
```

5. Depois disso, as proximas etapas usam `dados_limpos.csv` para analise, escalonamento e reducao de dimensionalidade.

## Etapas do Notebook

1. Importacao das bibliotecas.
2. Limpeza e normalizacao dos dados.
3. Salvamento da base limpa em `data/dados_limpos.csv`.
4. Carregamento e inspecao do DataFrame.
5. Analise de informacoes gerais, valores faltantes e valores unicos.
6. Escalonamento das variaveis numericas.
7. Aplicacao do PCA.
8. Grafico de variancia explicada acumulada.
9. Visualizacoes 2D e 3D dos dados reduzidos.

## Observacoes

A pasta `data` esta ignorada pelo Git para evitar o envio de arquivos grandes ao repositorio.

Por isso, cada pessoa que for executar o projeto precisa baixar o CSV manualmente e salvar no caminho indicado.
