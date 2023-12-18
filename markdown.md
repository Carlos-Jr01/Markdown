# Markdown
[Introdução]
## Cabeçalhos
No Markdown existem 6 níveis de cabeçalho e são usados da seguinte forma:  
```
# Título 1  
## Título 2 (menor que o 1)  
### Título 3 (menor que o 2)  
#### Título 4 (menor que o 3)  
##### Título 5 (menor que o 4)  
###### Título 6 (menor que o 5)  
```

## Parágrafos
Para quebrar linha, deve-se inserir dois espaços após o ponto de quebra. Para um espaçamento maior, deve-se inserir dois enters.

## Ênfase
- **Negrito**: inserir dois "*" antes e dois depois da String  
- *Itálico*: inserir apenas um "*" antes e dois depois da String  
- ***Negrito e Itálico***: inserir três "*" antes e dois depois da String  
- ~~Palavra Riscada~~: inserir dois "~" antes e dois depois da String  

## Citação
> Insere-se um ">" antes do parágrafo 

## Linhas Horizontais
* Exemplo 1: Insere-se três "*" ou três "-"
***
* Exemplo 2: Insere-se três "*" ou três "-" separados por espaço
* * *
* Exemplo 3: Insere-se quantos "*" ou "-" quiser desde que seja mais de 3
****************************

## Listas Não Ordenadas
Insere-se um "*" ou "-" ou "+" antes dos itens. Para adicionar subitens, basta dar um tab antes do item. É possível espaçar os itens com enters entre eles.
* Item 1
  * Subitem 1
- Item 2 
  - Subitem 2
+ Item 3
  + Subitem 3

## Listas Ordenadas
Insere-se "1.", "2."... antes dos itens:
1. Item 1
2. Item 2
3. Item 3

O Markdown conta a partir da numeração do primeiro item; portanto, se o usuário numerar desordenado (8. 4. 1...), será exibido a partir do 8:

8. item 8
4. item 4
1. item 1

É possível "ignorar" essa ordenação se o usuário quiser, por exemplo, listar os campeões da Copa do Mundo.  
Utilizando uma `\` antes do "." e dois espaços após o item (para quebrar a linha como visto anteriormente):

1994\. Brasil  
1998\. França  
2002\. Brasil  

## Links
Para transformar texto em links, usa-se:  
[texto do link](url do link "texto alternativo (opcional)")  
O texto alternativo é exibido quando passa o mouse sobre o link.

* Exemplo 1: Acesse o link [clicando aqui](https://www.google.com.br/?hl=pt-BR "Google")

Uma outra forma de utilizar o link é criando uma "variável" e atribuindo a ela como "valor" a URL do link:  
[variável]: url "texto alternativo"   

Assim, usa-se o link da seguinte forma:  
 [texto][variável]

[url]:https://www.google.com.br/?hl=pt-BR "Google"

* Exemplo 2: Acesse o link [clicando aqui][url]

## Imagens
Para adicionar imagens é semelhante ao uso de links, mas com uma exclamação antes:  
![nome da imagem](endereço da imagem)

* Exemplo 1: ![Markdown](markdown-1.jpg)

É possível também utilizar o link criando uma "variável" e atribuindo a ela como "valor" o caminho da imagem:  
[variável]: caminho-da-imagem   

Assim, usa-se a imagem da seguinte forma:  
![nome][variável]

[markdown]: markdown-1.jpg
* Exemplo 2: ![Markdown][markdown]

É possível utilizar imagem com link colocando a imagem onde seria o texto do link, da seguinte forma:  
[![nome da imagem](endereço da imagem)](url do link "texto alternativo (opcional)")

* Exemplo 3: [![Markdown](markdown-1.jpg)](https://www.google.com.br/?hl=pt-BR "Google")

## Tabelas
Usa-se "|" para separar as colunas das tabelas e "-" na segunda linha para a ferramenta identificar que será uma tabela.
Pode-se alinhar cada coluna da forma que preferir:
* À esquerda: adicionando ":-" na linha de identificação
* Ao centro: adicionando ":-:" na linha de identificação
* À direita: adicionando "-:" na linha de identificação

No exemplo a seguir, usaremos o seguinte alinhamento: |:-|:-:|-:|, assim, as colunas serão alinhadas respectivamente à esquerda, centro e direita.
* Exemplo 1:

| Nome    | Idade | Profissão  |
| :---    | :---: | ---------: |
| Roberto | 36    | Scrum      |
| Flavia  | 19    | Estudante  |
| João    | 28    | Desenvolvedor |

## Código
Pequenos trechos de códigos são destacados quando são colocados entre crases
* Exemplo 1: Informe os parâmetros `username` e `password`.  

Quando a crase é um caractere da própria linguagem, o trecho será destacado colocando-o entre crases duplas.
* Exemplo 2: ``const message = `My name is ${name}`;``

Para trabalhar com blocos de código, pode-se utilizar 4 espaços antes do bloco (ou dois tabs), ou, utilizando três crases antes e três crases depois do bloco, que é a forma mais utilizada. Para destacar a sintaxe do código (Syntax Highlighting), basta informar o nome da linguagem após as 3 crases do início.
* Exemplo 3:

```javascript
// login.js

const username = 'pedrohenrique';
const password = 'secret';

login(username, password);
```