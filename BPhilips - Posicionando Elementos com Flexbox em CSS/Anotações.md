Flex Box CSS

Flexbox é um recurso CSS3 que serve de modelo para desenvolvimento de layouts para websites e aplicações web visando organizar elementos dentro de contêiners de forma flexível conforme sua necessidade.

O que indica que um layout está utilizando CSS Flexbox é definição da propriedade display de um contêiner, o Flex Container, com o valor flex, ou inline-flex. Veja o código a seguir.

Código CSS:

.container {
     display: flex;
}



<u>Propriedades:</u>

- display - A propriedade CSS display específica como elementos HTML devem ser apresentados em relação ao tipo de caixa de renderização.


Com o valor “flex” ou “inline-flex” atribuído a esta propriedade, o contêiner e se torna flexível. Consequentemente seus filhos se tornam Flex Itens.

- flex-direction - Flex-direction é aplicada no contêiner, mas define o fluxo de exibição que os Flex Itens serão dispostos. É esta propriedade que pode mudar o Eixo principal da posição horizontal (Flex Itens aninhados lado a lado em linha) para na vertical (Flex Itens aninhados um abaixo do outro em coluna). Conheça os possíveis valores para esta propriedade:
  - row: Este é o valor padrão, onde os itens são organizados para exibição em forma de linha da esquerda para a direita;
  - row-reverse: Os itens também são organizados em linha, só que em ordem reversa em relação ao valor anterior. Da direita para a esquerda;
  - column: Os itens são organizados em forma de colunas iniciando de cima para baixo;
  - column-reverse: Os itens são organizados em forma de colunas, só que iniciando de baixo para cima.

- Flex-wrap - A propriedade flex-wrap determina se um Flex Container é de linha única ou multilinhas. O que ocorre é que por padrão os Flex Itens tentarão se ajustar dentro de uma linha mesmo que ultrapassem visualmente a largura do elemento pai. O flex-wrap oferece a opção de quebra de linha para que os elementos filhos se ajustem adequadamente. Conheça os possíveis valores para esta propriedade Flexbox:

  - nowrap: Este é o valor padrão. Com ele todos os itens inseridos dentro do Flex Container serão dispostos em uma linha mesmo que ultrapasse a largura do contêiner;

  - wrap: Ocorrerá a quebra de linha se alguns dos itens ultrapassar a largura do Flex Container. Os itens mais à direita serão deslocados para a linha de baixo;

  - wrap-reverse: Também ocorrerá a quebra de linha se alguns dos itens ultrapassar a largura do Flex Container, só que neste caso os itens mais à direita serão deslocados para a linha de cima.



- 
  flex-flow - A propriedade flex-flow é um propriedade de declaração única para escrita das propriedades flex-direction e flex-wrap.


Ao usar as propriedades flex-direction e flex-wrap usualmente a declaração fica da seguinte forma:

.container {
     display: flex;
     flex-direction: row;
     flex-wrap: wrap;
}
Agora a forma abreviada com flex-flow:

.container {
     display: flex;
     flex-flow: row wrap;
}



- Justify-content - Alinhamento dos ítens do container e da distribuição de espaço entre eles.Justify-content é uma propriedade que define o alinhamento dos Flex Itens ao longo do eixo principal do contêiner.
  - flex-start: Esse é o valor padrão. Os Flex Itens são alinhados a partir do <u>início do contêiner</u>;
  - flex-end: Os Flex Itens são alinhados a partir do <u>fim do contêiner</u>;
  - center: Os itens são alinhados ao <u>centro do contêiner</u>;
  - space-between: Cria um alinhamento uniforme entre os Flex Itens com um <u>espaçamento igual entre esses elementos</u>. **O primeiro item é deslocado para o início, e o último é deslocado para o final do contêiner;**
  - space-around: Os Flex Itens também são distribuídos ao longo contêiner, onde é criado um espaçamento ao redor dos elementos. Com isso, o primeiro e o último item possuirão margens e não ficaram grudados as extremidades do contêiner. Visualmente os espaçamentos antes do primeiro e depois do último item são menores que os outros espaçamentos. O que acontece é que os espaçamentos são aplicados no lado esquerdo e direito de cada Flex Item, portanto os espaçamentos que não estão nas extremidades tem tamanho dobrado porque soma o espaçamento a direita do item antecessor e o espaçamento a esquerda do item sucessor.
  - space-evenly: Os Flex Itens também são distribuídos ao longo contêiner, onde também é criado um espaçamento ao redor dos elementos. O que difere do space-around é que os espaçamentos entre os itens e os espaçamentos nas extremidades do contêiner são distribuídos de forma igualitária.




- align-items: Align-items é uma propriedade que define como os Flex Itens serão distribuídos ao longo do eixo transversal do contêiner. Conheça os possíveis valores para esta propriedade:
  - **stretch:** Esse é o valor padrão. Neste caso os Flex Itens serão esticados para preencher toda a dimensão do eixo transversal igualmente;
  - **flex-start:** Desloca os Flex Itens para o início do eixo transversal;
  - **flex-end:** Desloca os Flex Itens para o final do eixo transversal;
  - **center:** Os Flex Itens são centralizados no eixo transversal;
  - **baseline:** Alinha os Flex Itens a partir da base da primeira linha de texto de cada um deles. Na aplicação abaixo você verá um exemplo onde os Flex Itens tem o mesmo tamanho de fonte o que não modifica o posicionamentos das caixas, também terá um exemplo com tamanhos diferentes de fontes e sem alinhando baseline e um terceiro também com tamanhos de fontes diferentes, mas com o alinhamento a partir de base da tipografia o que explicita melhor como funciona o valor baseline e mostra a mudança no posicionamento das caixas.

- align-content: Align-content é uma propriedade que define como as linhas são distribuídas ao longo do eixo transversal do contêiner. Como está propriedade trabalha com a distribuição das linha, ele é a aplicada quando o Flex Container é multilinhas, ou seja, recebe **flex-wrap** com o valor **wrap**. Conheça os possíveis valores para esta propriedade:
  - **stretch:** Este é o valor padrão. As linhas são distribuídas uniformemente ao longo do eixo transversal.
  - **flex-start:** Distribui as linhas a partir do início do eixo transversal;
  - **flex-end:** Distribui as linhas a partir do fim do eixo transversal;
  - **center:** Mantém as linhas no centro do eixo transversal;
  - **space-between:** Cria um espaçamento entre as linhas. Onde a primeira linha é deslocada para o início do eixo transversal, a última é deslocada para o final do eixo transversal;
  - **space-around:** As linhas são uniformemente distribuídos ao longo do eixo transversal, onde é criado um espaçamento ao redor delas. Com isso, a primeira e o última linha possuirão margens e não ficaram grudadas as extremidades do contêiner.



Flex Itens 

- flex-grow: A propriedade flex-grow serve para especificar o fator de crescimento que um Flex Item terá em relação aos outros Flex Itens encontrados em um Flex Container. O valor especificado deve ser um número positivo. Por padrão o valor de flex-grow é 0, ou seja, os Flex Itens não crescem.

- flex-basis: flex-basis define o tamanho inicial que um Flex Item deve ter antes que o espaço ao seu redor seja distribuído por outras propriedades.  Quando o eixo principal for horizontal, esta propriedade define a largura mínima antes que espaço restante seja distribuído, quando for vertical defina e altura mínima. Por padrão seu valor é auto (flex-basis: auto) que quer dizer o tamanho da largura (ou altura) do Flex Item. Caso se para esse Flex Item não for determinado um tamanho de width, e caso o eixo principal for horizontal, ou height, caso vertical, então flex-basis: auto; equivalerá ao tamanho do conteúdo. Além do valor auto, esta propriedade também pode receber valores para dimensões, como pixels e porcentagens.

  **Observação:** Ao utilizar o valor **auto** para flex-basis é possível alterar tamanho de um Flex Item (Largura, caso eixo principal na horizontal e altura, caso eixo principal na vertical) quando conjuntamente usamos **width** e **height**. Mas somente nesta situação. Quando você define um valor diferente de auto qualquer declaração com width e height perde o efeito.

- flex-shrink: é a propriedade que estabelece a capacidade redução ou compressão do tamanho de um item.



**Flex:** Esta é a abreviatura para flex-grow, flex-shrink, flex-basis combinados nesta sequencia. O padrão é flex: 0 1 auto;. O uso da abreviatura é recomendada em vez de definir as propriedades separadamente.

```
.item {
  flex: 0 1 auto;
}
```

A declaração acima faz do flex item inflexível, quando há espaço disponível no contêiner, mas permite encolher quando há espaço insuficiente.

**Order:** O padrão faz com que os Flex Itens aparecem no contêiner na ordem que são inseridos no HTML. Mas essa ordem pode ser alterada através da propriedade **order** sendo que se inicia de uma valor menor para o maior. O valor inicial de order é 0 e também é possível especificar valores negativos.

**align-self:** Esta propriedade permite definir um alinhamento de um único Flex Item dentro de um contêiner sobrescrevendo o que foi definido no align-itens do Flex Container. Conheça os possíveis valores para esta propriedade:

- **auto:** Este é o valor padrão. Com ele declarado o comportamento definido no container por meio do align-items é respeitado.

- **stretch:** Neste caso o item será esticado para preencher toda a dimensão do eixo transversal (largura ou altura) igualmente;

- **flex-start:** Desloca o item para o início do eixo transversal;
- **flex-end:** Desloca o item para o final do eixo transversal;
- **center:** O item é centralizado no eixo transversal;
- **baseline:** Alinha o item a partir da base da primeira linha de texto dos demais itens.





-----------------------------------------------------
Display block - cada item embaixo do outro
diplay flex - lado a lado
padding (1 valor) Margem interna da caixa - 2 valores (em cima e embaixo) (dos dois lados) - 4 valores ()cima - ()lado direito - ()baixo - ()lado esquerdo
border (tamanho borda)px Solid(tipo de borda) cor
max-width () tamanho máximo da largura
max-height () tamamnho máximo da altura
background-color - cor do fundo
margin() - margin externa do ítem
fle-direction:row ordem numerica
flex-direction:row-reverse - ordem reversa na mesma linha
flex-direction: column em colunas
flex-direction: column em colunas reversas
flex-wrap: nowrap em ordem dentro de uma caixa - passando para fora se acabar a caixa
flex-wrap: wrap preenche em ordem a caixa, passando para baixo, com quebra de linha
flex-wrap: preenche a caixa em ordem inversa com quebra de linha
line-height(): altura da linha escrita 
margin-boton: espaço entre os elementos

flex-flow é um atalho para o flex-direction e o wrap (3-flex-flow.html)



[Flexbox CSS - Guia completo de CSS3 - display: flex. (chiefofdesign.com.br)](https://www.chiefofdesign.com.br/css-flexbox/)
