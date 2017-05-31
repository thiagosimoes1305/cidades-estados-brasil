# Cidades e Estados do Brasil

Código criado em JavaScript (sem uso de library) para retornar as Cidades e Estados brasileiros.
Abaixo segue as principais funcionalidades do script.

----------

### Funcionalidades: 

> **Estados:**

> - [Retorno de todos os Estados](https://github.com/tedktedk/cidades-estados-brasil/blob/master/README.md#retornando-os-estados);
> - [Marcar o Estado na lista](https://github.com/tedktedk/cidades-estados-brasil/blob/master/README.md#marcando-um-estado-na-lista);
> - [Escolha do texto option padrão, exemplo: "Selecione um Estado"](https://github.com/tedktedk/cidades-estados-brasil/blob/master/README.md#escolha-do-texto-option-padrão-selecione-um-estado);
> - [Alternar os nomes dos Estados por sigla ou por extenso](https://github.com/tedktedk/cidades-estados-brasil/blob/master/README.md#alternar-os-nomes-dos-estados-por-sigla-ou-por-extenso).
> - [Por padrão o retorno é em um SELECT mas pode ser alterado através dos argumentos](https://github.com/tedktedk/cidades-estados-brasil/blob/master/README.md#por-padrão-o-retorno-é-em-um-select-mas-pode-ser-alterado-através-dos-argumentos);

----------

> **Cidades:**

> - Retorno de todas as Cidades de um Estado;
> - Escolha do texto option padrão, exemplo: "Selecione uma Cidade";
> - Alterar o padrão de retorno através de argumentos;
> - OBS: Não tem a opção de "Marcar uma Cidade" devido aos problemas de acentos e espaços (serão corrigidos na próxima versão);

----------

> **Retornando a cidade Cidades de acordo com o Estado selecionado:**

> - Usando o Estado para retornar as Cidades;

----------

----------

#### **Retornando os Estados:**

*Através do **elementID** você coloca o ID do SELECT*.
```javascript
new statesCitiesBR({
	states: {
		elementID: "selects_estado"
	}
});
```

Resultado final: [https://jsfiddle.net/ted_k/41axqrc4/](https://jsfiddle.net/ted_k/41axqrc4/)

----------

#### **Marcando um Estado na lista:**

*Através do **current** você adiciona a SIGLA do Estado*.
```javascript
new statesCitiesBR({
	states: {
		elementID: "selects_estado",
		current: "BA"
	}
});
```

Resultado final: [https://jsfiddle.net/ted_k/b5vdy8fq/](https://jsfiddle.net/ted_k/b5vdy8fq/)

----------

#### **Escolha do texto option padrão "Selecione um Estado":**

*Através do **defaultOption**, adicione um Texto padrão*.
```javascript
new statesCitiesBR({
	states: {
		elementID: "selects_estado",
		defaultOption: "Selecione um Estado"
	}
});
```

Resultado final: [https://jsfiddle.net/ted_k/bu0L3yhv/1/](https://jsfiddle.net/ted_k/bu0L3yhv/1/)

----------

#### **Alternar os nomes dos Estados por sigla ou por extenso:**

*Através do **initial** com valor "true", você alterna por Sigla ou Extenso*.
```javascript
new statesCitiesBR({
	states: {
		elementID: "selects_estado",
		initial: true
	}
});
```

Resultado final: [https://jsfiddle.net/ted_k/uh98tbjf/](https://jsfiddle.net/ted_k/uh98tbjf/)

----------

#### **Por padrão o retorno é em um SELECT mas pode ser alterado através dos argumentos:**

*Através dos **arguments**, você pode inserir outro elemento, no caso foi usado uma LISTA.*
```javascript
new statesCitiesBR({
	states: {
		elementID: "lista_estado",
		arguments: {
			before: "<li>",
			after: "</li>",
		}
	}
});
```
*Lembre-se também de alterar o elemento HTML que receberá o retorno.*
Resultado final: [https://jsfiddle.net/ted_k/1yqc6wzh/](https://jsfiddle.net/ted_k/1yqc6wzh/)

#### **Outros argumentos:**

*O **defaultOption**, também pode ser usado dentro do arguments.*
```javascript
new statesCitiesBR({
	states: {
		elementID: "lista_estado",
		arguments: {
			before: "<li>",
			after: "</li>",
			defaultOption: "Selecione um Estado"
		}
	}
});
```
Resultado final: [https://jsfiddle.net/ted_k/2aL90f8e/](https://jsfiddle.net/ted_k/2aL90f8e/)


----------

----------


#### **Retorno de todas as Cidades de um Estado:**

*É necessário o uso do **state** para retorno das Cidades*.
```javascript
new statesCitiesBR({
	cities: {
		elementID: "selects_cidades",
		state: "BA"
	}
});
```
Resultado final: [https://jsfiddle.net/ted_k/5v0kfsr0/](https://jsfiddle.net/ted_k/5v0kfsr0/)

----------

#### **Alterar o padrão de retorno através de argumentos:**

*Através dos **arguments**, você pode inserir outro elemento, no caso foi usado uma LISTA.*
```javascript
new statesCitiesBR({
	cities: {
		elementID: "lista_cidades",
		state: "BA",
		arguments: {
			before: "<li>",
			after: "</li>",
			defaultOption: "Selecione uma Cidade"
		}
	}
});
```
*O **defaultOption**, também pode ser usado dentro do arguments.*

Resultado final: [https://jsfiddle.net/ted_k/r4532rfp/](https://jsfiddle.net/ted_k/r4532rfp/)


----------

----------


#### **Usando o Estado para retornar as Cidades:**

*No parâmetro "state", do objeto **cities** é só colocar a string "auto", que irá sincronizar direto com o estado selecionado acima. É necessário o uso do **state** em conjunto com a **cities** *.
```javascript
new statesCitiesBR({
	states: {
		elementID: "lista_estados",
		defaultOption: "Selecione um Estado"
	},
	cities: {
		elementID: "lista_cidades",
		state: "auto",
		defaultOption: "Selecione uma Cidade"
	}
});
```
Resultado final: [https://jsfiddle.net/ted_k/5vqnmLad/](https://jsfiddle.net/ted_k/5vqnmLad/)

----------

* **OBS:** Para usar em uma LISTA é necessário usar os objetos separados e só funcionará com o "states" usando pouco de javascript para restagar o valor de um atributo, o "data-uf". *

Resultado final: [https://jsfiddle.net/ted_k/d492hcje/](https://jsfiddle.net/ted_k/d492hcje/)