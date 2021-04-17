# A cascata (cascading)

A escolha do browser de qual regra aplicar, caso haja muitas regras para o mesmo elemento.

* seu estilo é lido de cima para baixo.

É levado em consideração 3 fatores

1. Origem do estilo
2. Especificidade
3. Importância

### Origem do estilo

inline > tag style > tag link

### Especificidade

é um cálculo matemático, onde, cada tipo de seletor e origem do estilo, possuem valores a serem considerados.

0. Universal selector, combinators e negation pseudo-class (:not()) 
* {
	color: green;
}
1. Element Type selector e pseudo-elements (::before, ::after)
h1 {
	color: red;
}
10. Classes e attribute selectors ([type-"radio])  
in html
<h1 class="title">Título </h1>
in CSS
.title {
	color:red;
}
100. ID selector
in html
<h1 class="title" id="my-title">Título </h1>
in CSS
#my-title {
	color: gray;
}
1000. Inline
in html
<h1 class="title" id="my-title" style="color: orange">Título </h1>

### A regra !important

* cuidado, evite o uso
* não é considerado uma boa prática
* quebra o fluxo natural da cascata

rouba a força de tudo, as vezes é necessario, quando voce não conseguir sobreescrever, se você esta usando seu proprio css não use, caso voce esteja usando a biblioteca de alguem e não consiga substituir utilizar
