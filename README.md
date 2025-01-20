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


### Estilos Adicionais e Fontes
O objetivo principal é melhorar o visual do site ajustando como fontes, cores, espaçamentos e aplicando estilos únicos para diferentes seções.

### Personalização de Fontes e Cores
**Alterando a Cor do Texto**
 1. Use a propriedade ``color`` para definir a cor do texto.
 2.  Exemplo:
 ```CSS
 h1 {
	 color: white;
}
```

**Alterando a Familia de Fontes**
1. Use a propriedade ``font-family`` para alterar a fonte.
2.  Opções:
	-  **Fontes padrão**: ``serif``, ``sans-serif``, ``monospace``.
	-  **Fontes Personalizadas** 
		- Utilize Google Fonts para importar novas fontes.
		- Exemplo  com Google Fonts:
			1. Adicione o link de importação no HTML
			``` html
			
			<link href="https://fonts.googleapis.com/css2?family=Anton&display=swap" rel="stylesheet">
```
			2. Aplique a font no CSS:
			```css
			h1 {
				font-family: 'Anton', sans-serif;
			}
```

### Estilização por seção 
para aplicar estilos únicos a diferentes seções, utilize seletores específicos:
1. Identifique as seções por **tags**, **classes**, ou **IDs**.
	Exemplo:
	``` css
	// exemplo por classes
	.header-sectrion {
		background: #ff0000;
		color: white;
	}
	.content-section {
		background: #008000;
		color: black;
	}
```

Cada seção tera um estilo único sem compartilhamento de propriedades.

### Utilizando o Google Fonts
1. Acesse o [Google Fonts](https://fonts.google.com)
2.  Escolha uma fonte desejada (ex: "Anton").
3. Copie o link de importação fornecido
4. Integre no HTML e utilize no CSS
```html
<head> 
	<link href="https://fonts.googleapis.com/css2?family=Anton&display=swap" rel="stylesheet">
</head>
```

### Considerando Espacamento

1. Ajuste espaçamento dentro e ao redor dos elementos com:
	- ``padding``: espaçamento interno
	- ``margin``: espaçamento externo.
2. Exemplo:
```css
.header-section {
	padding: 20px;
	margin: 0;
}
```

A personalização de fontes e cores melhora a estica do site.
O uso de estilos únicos para cada seção aumenta a flexibilidade do design.
Ferramentas como Google Fonts facilitam a importação de fontes personalizadas para qualquer projeto


### Regras de Especificidade
1. **Ordem de Prioridade**
	- **Estilos inline**: maior prioridade.
	- **Seletores de ID**: alta prioridade.
	- **Classes, pseudo-classes e seletores de atributos**: prioridade intermediaria. 
	- **Tags e pseudo-elementos**: menor prioridade
	- **Seletor universal (``*``)**: prioridade baixa
	
2. **Ordem de Arquivo**
	 - Em seletores com a mesma especificidade, o estilo **definido por ultimo no CSS** tem prioridade

3. **Herança e valores Padrão**
	- Propriedades herdáveis (como ``font-family`` e ``color``) podem ser sobrescritas por seletores mais específicos.
	- Estilos padrão do navegador tem a menos prioridade.

#### Boas Praticas
1. **Evite Estilos Inline**
	- Use estilos inline apenas em casos específicos, pois eles possuem a maior prioridade e podem dificultar a manutenção.

2. **Organize o CSS**
	- Coloque seletores menos específicos no inicio e aumente a especificidade gradualmente

3. **Compreenda a Cascata**
	- Combine seletor de tags, classes e IDs de forma estratégica para evitar conflitos desnecessários.

Exemplo:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Especificidade</title>
    <style>
        h1 {
            color: white; 
        }
        .title {
            color: green;
        }
    </style>
</head>
<body>
    <h1 class="title">Título Muito Específico</h1>
</body>
</html>

```

O texto sera exibido em **verde**, pois ``.title`` (classe) tem maior especificidade do que ``h1`` (tag).


A especificidade é um conceito fundamental para evitar conflitos e garantir que os estilos corretos sejam aplicados. O uso estratégico de seletores no CSS simplifica o desenvolvimento e a manutenção de projetos de projetos web.


## Herança no CSS
Certas propriedades, como ``font-family`` e ``color``, sao automaticamente herdados dos elementos pais e para os filhos. Propriedades nao herdáveis podem ser explicitamente aplicadas ao filhos com ``inherit``

### Como configurar
- Estilize elementos globais, como o ``<body>``, para aplicar herança a todos os elementos da pagina
Exemplo:
```css
body {
	font-family: 'Montserrat', sans-serif;]
	color: #333;
}
```

### Hierarquia de Herança
A heranca sempre tem **baixa especificidade**, aparecendo abaixo de seletores diretos e padrões do navegador. Elementos filhos só herdam propriedades de pais diretos ou indiretos.

#### Especificidade no Contexto de Herança
1. **Seletores Diretos Sobrescrevem Herança**
- Estilos aplicados diretamente a um elemento tem prioridade sobre herança
Exemplo:
```css
h1 {
	font-family: 'Anton', sans-serif; //Sobrescreve a heranca
}
```

#### Boas Práticas

1. **Configuração Global``
	- Defina fontes e cores padrão no ``<body>`` para consistência e eficiência
2. **Evite Uso Excessivo de Herança**
	 - Para estilos específicos, use seletores diretos.
3. **Compreenda as Limitações**
	 - Propriedades nao herdáveis (como ``margin`` e ``padding``) devem ser definidas diretamente.

A herança é  uma ferramenta poderosa para aplicar estilos globais de maneira eficiente, especialmente para textos. No entanto, é  essencial compreender como ela interage com a especificidade para evitar conflitos e garantir que os estilos desejados sejam aplicado corretamente.