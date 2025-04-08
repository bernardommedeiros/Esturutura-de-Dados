# Pilha

<br>

## Tipos abstratos de dados (TAD)
<p> Armazena dados qualquer, utilizando o esquema LIFO - Last in, First out. </p>

<br>

- Especificidades do TAD
  - Dados armazenados
  - Operações sobre os dados (metodos)
  - condições de erro associada aos metodos

---
 
 <br>
 
- Principais operações:
  - push(object) - inserção de elemento no topo da pilha
  - object pop() - remove e retorna o último elemento inserido no topo da pilha
  <p>OBS: não podem ser realiadas caso a pilha esteja vazia, causando uma exceção. </p>
- Operações auxiliares:
  - object top() - retorna o elemento situado no topo sem remove-lo
  - integer size() - quantidade de elementos na estrutura
  - boolean isEmpty() - se há ou não elementos na estrutura
 
  <br>
 
### Exceções
<p> Condição de erro, ao tentar remover um elemento de uma pilha vazia, ou tentar alcançar o topo dela </p>

<br>

## Pilhas baseadas em array
<p> Forma simplificada de implementar uma pilha usa array, uma variável mantém o índice do elemento no topo da pilha
  
  <br>
                        
  Exemplo: arrayIndice = -1 <br> array = A(0) B(1) C(2) D(3) 

</p>

<br>

### Pseudocodigo com operações

- Push
  <p> ao limitador do array ser atingido, levanta a exceção EPIlhaCheia - gambiarra, não será utilizada, O(1). </p>
  
```

```

  <p> ao invés disso, será utilizado a integração de um novo array maior, copiando os dados do array anterior, deixa de ser O(1) para O(n), quando o array fica cheio. </p>
  <p> S = A B C <br> A = A B C E . . . . </p>

  
  

## Estrategia incremental - O(n)

<p> incremento fixo após encher o array </p>

## Estrategia de duplicação - O(1)

<p> substituímos o array <b>k = log2 </b>, <b>n</b> vezes </p>


