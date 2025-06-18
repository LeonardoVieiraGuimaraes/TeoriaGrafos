# README

## Projeto: Teoria dos Grafos - Algoritmos e Visualizações

Este projeto reúne exemplos práticos de algoritmos clássicos de grafos, como busca em largura (BFS), busca em profundidade (DFS), Dijkstra, Floyd-Warshall, Prim e Kruskal, com visualizações passo a passo e tabelas de roteamento. O objetivo é facilitar o aprendizado e a aplicação desses conceitos em problemas reais de conectividade, redes, logística e otimização.

---

## Bibliotecas Utilizadas

- **networkx**: Manipulação e análise de grafos.
- **matplotlib**: Visualização gráfica dos grafos e tabelas.
- **pandas**: Criação e exibição de tabelas de dados.
- **markdown** e **pdfkit** (opcional): Para converter textos em Markdown para PDF.

---

## Como Instalar

1. **Crie um ambiente virtual (opcional, mas recomendado):**
   ```bash
   python -m venv .venv
   # Ative o ambiente:
   # No Windows:
   .venv\Scripts\activate
   # No Linux/Mac:
   source .venv/bin/activate
   ```

2. **Instale as bibliotecas necessárias:**
   ```bash
   pip install networkx matplotlib pandas
   ```
   Se for usar conversão para PDF:
   ```bash
   pip install markdown pdfkit
   ```
   Para PDF, também é necessário instalar o [wkhtmltopdf](https://wkhtmltopdf.org/downloads.html) no seu sistema.

3. **Instale o Jupyter Notebook:**
   ```bash
   pip install notebook
   ```

---

## Como Usar no Jupyter Notebook

1. **Inicie o Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
2. Abra o arquivo desejado (`.ipynb`) e execute as células para ver os algoritmos em ação, as visualizações e as tabelas.

---

## Usando no Google Colab

Se preferir, você pode rodar os notebooks diretamente no [Google Colab](https://colab.research.google.com/):

- Faça upload do arquivo `.ipynb` para o Colab.
- Execute as células normalmente (as bibliotecas `networkx`, `matplotlib` e `pandas` já vêm instaladas no Colab).
- Para instalar bibliotecas extras, use:
  ```python
  !pip install markdown pdfkit
  ```
  E para PDF:
  ```python
  !apt-get install wkhtmltopdf
  ```

---

## Observações

- Para exportar notebooks para PDF ou HTML, use o menu do Jupyter ou comandos como:
  ```bash
  jupyter nbconvert --to pdf seu_arquivo.ipynb
  jupyter nbconvert --to html seu_arquivo.ipynb
  ```
- Se encontrar erros de exportação para PDF, instale o LaTeX (MikTeX no Windows ou texlive no Linux).


