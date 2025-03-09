# Aula Introdutória de Teoria dos Grafos

## Objetivo
Esta aula tem como objetivo introduzir os conceitos básicos da Teoria dos Grafos e demonstrar uma aplicação prática através da implementação de grafos e digrafos em Python usando a biblioteca NetworkX.

## Conteúdo
1. **Conceitos de Grafos e Digrafos**
2. **Modelagem de Aplicações Usando Grafos**
3. **Caminhos, Ciclos e Árvores**
4. **Grafos Rotulados nos Vértices e nas Arestas**
5. **Definição de Árvores**

### 1. Conceitos de Grafos e Digrafos

#### Grafos
Um grafo é uma estrutura matemática usada para modelar relações entre objetos. Ele é composto por:
- **Vértices (ou nós)**: Representam os objetos.
- **Arestas (ou arcos)**: Representam as conexões entre os objetos.

Por exemplo, em uma rede social, os vértices podem representar pessoas e as arestas podem representar amizades entre elas.

#### Digrafos
Um digrafo (ou grafo direcionado) é um tipo de grafo onde as arestas têm uma direção. Isso significa que cada aresta vai de um vértice a outro específico. Por exemplo, em uma rede de seguidores no Twitter, uma aresta direcionada pode representar que uma pessoa segue outra.

### 2. Modelagem de Aplicações Usando Grafos

Grafos são usados para modelar uma ampla variedade de problemas do mundo real. Aqui estão alguns exemplos:

- **Redes de Computadores**: Modelagem de conexões entre computadores.
- **Redes Sociais**: Modelagem de interações entre pessoas.
- **Mapas de Estradas**: Modelagem de rotas e interseções.
- **Biologia Computacional**: Modelagem de interações entre proteínas ou genes.

### 3. Caminhos, Ciclos e Árvores

#### Caminhos
Um caminho em um grafo é uma sequência de vértices conectados por arestas. Por exemplo, em um mapa de estradas, um caminho pode representar a rota de uma cidade a outra.

#### Ciclos
Um ciclo é um caminho que começa e termina no mesmo vértice. Por exemplo, em uma rede de transporte público, um ciclo pode representar uma rota circular.

#### Árvores
Uma árvore é um grafo acíclico conectado. Em uma árvore, qualquer dois vértices são conectados por exatamente um caminho. Árvores são usadas em muitas áreas da ciência da computação, como estruturas de dados e algoritmos.

### 4. Grafos Rotulados nos Vértices e nas Arestas

Grafos rotulados são grafos onde os vértices e/ou arestas possuem rótulos (informações adicionais). Por exemplo, em um mapa de estradas, os vértices podem ser rotulados com os nomes das cidades e as arestas podem ser rotuladas com as distâncias entre as cidades.

### 5. Definição de Árvores

Uma árvore é um grafo acíclico conectado. Em uma árvore, qualquer dois vértices são conectados por exatamente um caminho. Árvores são usadas em muitas áreas da ciência da computação, como estruturas de dados e algoritmos.

## Implementação Usando NetworkX

Vamos criar exemplos de cada um desses conceitos usando a biblioteca NetworkX em Python.

### Instalação da Biblioteca NetworkX

```python
!pip install networkx

import networkx as nx
import matplotlib.pyplot as plt

# Criação de um grafo
G = nx.Graph()

# Adicionando nós
G.add_nodes_from(["A", "B", "C", "D", "E"])

# Adicionando arestas
G.add_edges_from([("A", "B"), ("A", "C"), ("B", "D"), ("C", "D"), ("D", "E")])

# Desenhando o grafo
plt.figure(figsize=(8, 6))
nx.draw(G, with_labels=True, node_size=700, node_color="lightblue", font_size=12, font_weight="bold")
plt.show()

# Criação de um digrafo
DG = nx.DiGraph()

# Adicionando nós
DG.add_nodes_from(["A", "B", "C", "D", "E"])

# Adicionando arestas direcionadas
DG.add_edges_from([("A", "B"), ("A", "C"), ("B", "D"), ("C", "D"), ("D", "E")])

# Desenhando o digrafo
plt.figure(figsize=(8, 6))
nx.draw(DG, with_labels=True, node_size=700, node_color="lightgreen", font_size=12, font_weight="bold", arrows=True)
plt.show()

# Criação de uma árvore
T = nx.Graph()

# Adicionando nós
T.add_nodes_from(["A", "B", "C", "D", "E"])

# Adicionando arestas
T.add_edges_from([("A", "B"), ("A", "C"), ("B", "D"), ("B", "E")])

# Desenhando a árvore
plt.figure(figsize=(8, 6))
nx.draw(T, with_labels=True, node_size=700, node_color="lightcoral", font_size=12, font_weight="bold")
plt.show()