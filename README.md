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
