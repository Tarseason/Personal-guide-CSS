# Personal-guide-CSS
Este repositório serve como um guia pessoal de CSS, onde organizo e compartilho o meu aprendizado sobre os fundamentos e conceitos essenciais dessa linguagem de estilo. Este repositório está em constante evolução, aprendendo e aplicando novos conceitos. Sinta-se à vontade para acompanhar o progresso ou contribuir com sugestões! 

## Adicionando CSS Inline a Elementos HTML
Existem 3 maneiras principais de adicionar CSS a uma pagina HTML. A primeira delas eh utilizando o estilo inline. Este método consiste em adicionar o atributo ``style`` diretamente em um elemento HTML, permitindo que voce defina as propriedades CSS desejadas para aquele elemento especifico.
Por exemplo, para estilizar uma seção, podemos adicionar o atributo style a tag ``<section>``.
Dentro deste atributo, eh possível definir varias declarações CSS, onde cada declaração eh composta por uma propriedade e seu valor. No caso do fundo da seção, utilizamos a propriedade ``backgound`` e atribuímos um valor, como uma cor ou uma imagem.

Exemplo de CSS inline para definir um fundo vermelho:
```html
<section style="background: #ff0000">
```

No exemplo acima, a cor de fundo da seção foi definida utilizando um código hexadecimal ``#ff0000`` que resulta a cor vermelha.
Embora o uso de inline seja simples, nao é recomendado para uso em projetos maiores onde sera necessário manter atualizado, uma vez que é adicionado manualmente em cada elemento suas propriedades e valores de estilo.