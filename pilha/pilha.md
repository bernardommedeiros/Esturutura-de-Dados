# Pilha

<br>

## Tipos abstratos de dados (TAD)
<p> Armazena dados qualquer, utilizando o esquema LIFO - Last in, First out. </p>

<br>

- Especificidades do TAD:
  - Dados armazenados
  - Operações sobre os dados (metodos)
  - Condições de erro associada aos metodos

<br>

- Exemplo: TAD que modela um controle de estoque
    - Dados:
      - pedidos de compra e venda
    - Operações:
      - comprar(produto)
      - vender(produto)
      - cancelar(pedido)
    - Condições de erro:
      - Comprar/vender produto inexistente
      - Cancelar pedido inexistente

---
 
 <br>
 
- Principais operações:
  - push(object) - inserção de elemento no topo da pilha
  - object pop() - remove e retorna o último elemento inserido na pilha
- Operações auxiliares:
  - object top() - retorna o elemento situado no topo sem removê-lo
  - integer size() - retorna a quantidade de elementos armazenados na estrutura
  - boolean isEmpty() - se há ou não elementos na estrutura

<p>OBS: operações POP e TOP não podem ser realizadas caso a pilha esteja vazia, causando uma exceção - EPilhaVazia. </p>
  <br>
 
### Exceções
<p> Condição de erro, ao tentar remover um elemento de uma pilha vazia, ou tentar alcançar o topo dela </p>

<br>

## Pilhas baseadas em array
<p> Forma simplificada de implementar uma pilha usa arrays, uma variável mantém o índice do elemento no topo da pilha
  
  <br>
                        
  Exemplo: 
  - Push
  <p> ao limitador do array ser atingido, levanta a exceção EPIlhaCheia - gambiarra, não será utilizada, O(1). </p>
  
```
  Algoritmo size()
    return t + 1

  Algoritmo pop()
    if (isEmpty())
      throw EPilhaVazia
    else
      t <- t -1
      return S[t+1]
```

</p>

<br>

### Pseudocodigo com operações

- Push
  <p> ao limitador do array ser atingido, levanta a exceção EPIlhaCheia - gambiarra, não será utilizada, O(1). </p>
  
```
  Algoritmo push(o)
    if (t = S.lenght - 1)
      throw EPilhaCheia
    else
      t <- t + 1
      S[t] <- 0
```

  <p> ao invés disso, será utilizado a integração de um novo array maior, copiando os dados do array anterior, deixa de ser O(1) para O(n), quando o array fica cheio. </p>
  <p> S = A B C <br> A = A B C E . . . . </p>


### Desempenho
<p>Seja <b>n</b> o número de elementos na pilha, o espaço utilizado é O(n) e as operações tem tempo de execução O(1)</p>
  
### Limitações
<p> Tamanho do array pré-definido e imutável, caso haja a adição de um novo elemento após esse limite ser atingido causa uma exceção </p>

## Estrategia incremental - O(n)

<p> incremento fixo após encher o array </p>

## Estrategia de duplicação - O(1)

<p> substituímos o array <b>k = log2 </b>, <b>n</b> vezes </p>














