# FlexBox
Repositório com o intuito de esclarecer as funcionalidades de algumas propriedades do flexbox, a melhor ocasião para usá-las e como usar  detalhando a fundo com minhas próprias palavras e ilustrações

![banner](https://user-images.githubusercontent.com/78706060/201412957-75ca7fb1-6537-4a53-abe1-4a4cc4c9f6dc.png)

# Perguntas Básicas
De início com o manunseamento do FlexBox é necessário que de ante mão faça às seguintes perguntas:

- Quem são os elementos que eu quero alinhar?
- Quem é o pai desses elementos?

Com a resposta dessas duas perguntas se torna tudo mais fácil, identificando os elementos que deseja alinhar e como alinhar, o que resta pro dev
é só saber qual propriedade que usar em cima do elemento pai

# Propriedades

Dando início a primeira propriedade do css "display:flex" que necessariamente precisamos dela para utilizar às demais, ela por padrão já alinha os 
elementos um ao lado do outro, em uma linha(row) só.

<table>
  <tr>
    <td>flex-end: a borda da margem cruzada dos itens é colocada na linha cruzada</td>
  </tr>
  <tr>
    <td>center: os itens são centralizados no eixo cruzado</td>
  </tr>
  <tr>
    <td>baseline: os itens são alinhados como suas linhas de base se alinham</td>
  </tr>
  <tr>
    <td>stretch( padrão ): esticar para preencher o contêiner (ainda respeita min-width/max-width)</td>
  </tr>
</table>

![alignitens](https://user-images.githubusercontent.com/78706060/201414911-e8dd64f5-30d4-4e01-898c-3b116e7c4faa.png)

## Justify-content
 Justifica os elementos de acordo com o eixo X
 
<table>
  <tr>
    <td>flex-start( padrão ): os itens são empacotados em direção à linha de partida</td>
  </tr>
  <tr>
    <td>flex-end: os itens são embalados em direção à linha final</td>
  </tr>
  <tr>
    <td>center: os itens são centralizados ao longo da linha</td>
  </tr>
  <tr>
    <td>space-between: os itens são distribuídos uniformemente na linha; primeiro item está na linha inicial, último item na linha final</td>
  </tr>
  <tr>
    <td>space-around: os itens são distribuídos uniformemente na linha com espaço igual ao redor deles</td>
  </tr>
  <tr>
    <td>space-evenly: os itens são distribuídos de forma que o espaçamento entre quaisquer dois assuntos de alinhamento adjacentes, antes 
	do primeiro assunto de alinhamento e após o último assunto de alinhamento, seja o mesmo</td>
  </tr>
</table>
 
![justifycontent](https://user-images.githubusercontent.com/78706060/201414117-ed5f3636-5115-437c-a565-ca036533eb61.png)

OBS: É claro champs, tem que ver tudo uma questão da hierarquia das tags, o padding da tag pai juntamente com o margin:0 auto;
OBS: A diferenciação entre o beetwen e o around é que o beetwen coloca espaço entre os elemento enquanto o around coloca esse 
espaço de sobra em volta dos elementos


## Demais propriedades 

- Flex-direction: Muda a direção dos elementos, ou seja, o que estava para row(linha) agora está para collumn(coluna)
    - flex-wrap: Acompanhado do flex-direction, ele vai dizer se o elemento deve quebrar caso o elemento tenha passado o 
	      tamanho do elemento pai.
    - flex-flow: Que é a junção dessas duas propriedades, ele vai já definir a mudança no direcionamento e caso queira 
              ter essa quebra

- Flex-order: Muda a ordem dos elementos no html

- Flex-grow: Fala pro elemento crescer de acordo com o espaço que ficou disponível gerado pelo elemento pai

- Flex-shrink: O contrário do flex-grow, ele diminui quando o espaço vai diminuindo

## FlexBox Responsivo
 O mediaquery é responsável por dizer qual comportamento os elementos html vão possuir quando chegar naquele tamanho de
tela em pixel, dessa forma, posicionando da melhor forma os elementos caso esteja em um determinado tamanho de tela.

- Se tratando de flexbox responsivo... Quando mudamos a sua direção com o "flex-direction", mudando para coluna, o align-itens
e o justify-content trocam de eixos, o que estava no eixo X vai para o eixo Y e vice versa.

- Quando também se coloca um height:auto ele se vira pra calcular o tamanho do bloco de acordo até onde os seus elementos filhos vão 

- Basicamente pro mobile tiramos do row e vamos pro colum, e com essa transição saber como e qual propriedade usar

# Considerações finais
Sempre analisando como os elementos pais se comportam, margins... paddings... e outras coisas

Para uma boa organização do código é necessário que esteja muito bem organizado em tag's semânticas e classes bem intuitivas, pra isso é necessário também 
ter uma boa base em HTML

https://css-tricks.com/snippets/css/a-guide-to-flexbox/

FAZER DIVERSOS EXERCÍCIOS, MAIS MUITO, MAIS MUITO, MAIS MUITOS MESMO

dablet: site que dá pra treinar alguma das proprieades do flex-box
