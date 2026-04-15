# Problema do Caixeiro Viajante (TSP) - Heurísticas de Inserção - Grupo G

Este projeto implementa soluções para o **Traveling Salesperson Problem (TSP)** utilizando as heurísticas de **Nearest Insertion** (Inserção Mais Próxima) e **Smallest Insertion** (Inserção do Menor Aumento). A estrutura de dados principal é uma **Lista Ligada Circular**.

## O Problema
O objetivo do TSP é encontrar a rota mais curta que visite um conjunto de pontos exatamente uma vez e retorne à origem. Como encontrar a solução ótima é computacionalmente exaustivo (NP-Difícil), utilizamos heurísticas para encontrar boas soluções em tempo viável.

## Heurísticas Implementadas

### 1. Nearest Insertion (Inserção Mais Próxima)
* **Lógica:** Para cada novo ponto `P`, o algoritmo percorre a rota atual e identifica o ponto `V` (Vencedor) que está geograficamente mais próximo de `P`.
* **Inserção:** O novo ponto `P` é inserido na lista imediatamente após o ponto `V`.

### 2. Smallest Insertion (Inserção do Menor Aumento)
* **Lógica:** O algoritmo avalia todos os pares de pontos conectados (arestas) na rota atual (ex: entre `A` e `B`).
* **Cálculo:** Ele calcula o quanto a distância total aumentaria se um ponto `P` fosse inserido entre eles: `Aumento = dist(A, P) + dist(P, B) - dist(A, B)`.
* **Inserção:** O ponto é inserido no local que gerar o menor aumento na distância total.

---

## Como Executar

### Pré-requisitos
* Java JDK.

### 1. Compilação
Abra o terminal na pasta raiz do projeto e execute:
```
javac src/*.java
```

### 2. Execução
Abra o terminal na pasta raiz e execute:
````
java -cp src Main dados/usa13509.txt
````

### 3. Visualização
Não implementada por problemas no TSPVisualizer do repositório original da T290*

## Resultados Esperados

### 1. Nearest Insertion
````
java -cp src Main dados/usa13509.txt
Instancia TSP carregada:
- dimensoes: 1000 x 600  
- numero de pontos: 13509

Nearest insertion: tamanho = 13509, comprimento = 77449.9794
````

### 2. Smallest Insertion
````
java -cp Main dados/usa13509.txt
Instancia TSP carregada:
- dimensoes: 1000x600
- numero de pontos: 13509

Smallest insertion: tamanho = 13509, comprimento = 45074.7769
````

## Vídeo Explicativo
https://drive.google.com/file/d/1ptr_wIQ5FCPhCs-PaSBOH4XWRDvyIQfC/view?usp=drivesdk
