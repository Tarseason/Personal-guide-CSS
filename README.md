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


Alternativas ao inline
Estilo na seção <head>
Definir Estilos Internos
Use a tag style na seção <head> do documento HTML.
Escreva as regras CSS entre as tags <style>...</style>
Exemplo:
	<head>
		<style>
			section {
				background: #ff0000;
			}
		</style>
	</head>
Funcionamento
a regra CSS sera aplicada a todas as tags <section> na pagina
Vantagens
Reutilização do código
manutenção simplificada.
Folha de Estilo Externa
Criar um Arquivo CSS:
Crie um arquivo com a extensão .css (ex : main.css || home.css)
Escreva as regras CSS diretamente no arquivo, sem usar tags <style>
Exemplo (main.css)
	section {
		background: #ff000;
	}
Linkar o Arquivo no HTML:
Adicionando a tag <link> na seção <head> para conectar o arquivo CSS
Exemplo:
<head>
	<link rel="stylesheet" href="main.css">
</head>
Vantagens
Separação clara entre HTML e CSS
Reutilização em varias paginas
melhor performace (cache do navegador).
Comparação de Métodos
Método	Vatagens	Desvantagens
Estilo Inline	Simplicidade em elementos únicos	Difícil de manter e reutilizar
Estilo interno	Codigo centraliizado em um local no HTML	Nao reutilizavel entre paginas
Folha de estilo externa	Reutilização em varias paginas; separação clara entre HTML e CSS; melhor performance com cache.	
Recomendação nao poderia ser outra, sempre que possível utilize folhas de estilos externas para melhorar a organização, escalabilidade e performance do projeto.