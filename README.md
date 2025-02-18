# Aula Introdutória de Teoria dos Grafos

## Objetivo
Esta aula tem como objetivo introduzir os conceitos básicos da Teoria dos Grafos e demonstrar uma aplicação prática através da implementação do algoritmo de Busca em Largura (BFS) em Python.

## Conteúdo
1. **Introdução à Teoria dos Grafos**
   - Definição de grafos, vértices e arestas.
   - Aplicações da Teoria dos Grafos em diversas áreas.

2. **Estudo de Caso: Implementação do Algoritmo BFS**
   - Objetivo: Implementar o algoritmo de Busca em Largura (BFS) para encontrar o caminho mais curto em um grafo não ponderado.
   - Ferramentas e Bibliotecas:
     - Python
     - NetworkX
     - Jupyter Notebook
     - Google Colab

## Passos para Implementação

### 1. Instalação das Bibliotecas
No Jupyter Notebook ou Google Colab, execute o seguinte comando para instalar a biblioteca NetworkX:
```python
!pip install networkx



## 2. Criação do Grafo Utilize a biblioteca NetworkX para criar e visualizar o grafo:

import networkx as nx
import matplotlib.pyplot as plt

# Criação do grafo
G = nx.Graph()

# Adicionando nós e arestas
G.add_edges_from([(1, 2), (1, 3), (2, 4), (3, 4), (4, 5)])

# Desenhando o grafo
nx.draw(G, with_labels=True)
plt.show()

GitHub Copilot
README.md
2. Criação do Grafo
Utilize a biblioteca NetworkX para criar e visualizar o grafo:

3. Implementação do Algoritmo BFS
Implemente o algoritmo de Busca em Largura (BFS) para percorrer o grafo:

from collections import deque

def bfs(graph, start):
    visited = set()
    queue = deque([start])
    path = []

    while queue:
        vertex = queue.popleft()
        if vertex not in visited:
            visited.add(vertex)
            path.append(vertex)
            queue.extend(set(graph[vertex]) - visited)
    return path

# Executando o BFS
bfs_path = bfs(G, 1)
print("Caminho BFS:", bfs_path)