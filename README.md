# Cidades e Estados do Brasil

Código criado em JavaScript para retornar as Cidades e Estados brasileiros.

Códigos disponíveis para JavaScript (vanilla) e jQuery.

Abaixo segue as principais funcionalidades do script.

----------

# Funcionalidade para Estados: 

> **Dados:**

> - Retorno dos Estados através do Nome ou da Sigla;
> - Marcar o Estado no campo de SELECT do HTML;


OBS: O retorno é impresso em um SELECT.


Por padrão, usando o método .states(), exemplo:

```javascript
document.getElementById("select").states();
```

Resultado final:
```html
<option value="BA">Bahia</option>
```

----------

Usando a opção **true** no *text*, o nome do Estado será retornado em **sigla**, exemplo:

```javascript
document.getElementById("select").states({
	text: true
});
```

Resultado final:
```html
<option value="BA">Bahia</option>
```

----------

Usando a opção **true** no *value*, o nome do Estado será retornado em **extenso**, exemplo:

```javascript
document.getElementById("select").states({
	value: true
});
```

Resultado final:
```html
<option value="BA">Bahia</option>
```

----------

A combinação do *value* e do *text* podem variar o retorno no SELECT, exemplo:

```javascript
document.getElementById("select").states({
	value: true,
	text: true
});
```

Resultado final:
```html
<option value="Bahia">BA</option>
```

----------

Existe a possibilidade de marcar o Estado como padrão usando o *current*, exemplo:

```javascript
document.getElementById("select").states({
	current: "BA"
});
```

Resultado final:
```html
<option selected="selected" value="Bahia">BA</option>
```
A variação dessa opção pode ser usada como no exemplo abaixo:
```javascript
document.getElementById("select").states({
	current: "Bahia" // BA, ba, Bahia, BAHIA, bahia
});
```

----------

Outra opcão de retorno pode ser usando **states.Array()** fora do objeto SELECT do HTML. Segue exemplo no console:

```javascript
var retorno = states.Array();
console.log(retorno);
```

----------

# Funcionalidade para Cidades: 

> **Dados:**

> - Retorno das Cidades através da Sigla;
> - Marcar a Cidade no campo de SELECT do HTML;


Por padrão, usando o método .city(), exemplo:

```javascript
document.getElementById("select").city();
```

Resultado final é um lista de cidades:
```html
<option value="Salvador">Salvador</option>
```

----------

Usando as siglas dos Estados *states*, você pode retornar as cidades, exemplo:

```javascript
document.getElementById("select").states({
	states: "BA"
});
```

Resultado final:
```html
<option value="Salvador">Salvador</option>
```

----------

Para marcar uma cidade, ou usar ela como padrão use o nome da cidade (com acento se tiver) no *current*:

```javascript
document.getElementById("select").states({
	states: "BA",
    current: "Eunápolis"
});
```

Resultado final:
```html
<option selected="selected" value="Eunápolis">Eunápolis</option>
```

----------

Outra opcão de retorno pode ser usando **city.Array()** (só retorna as cidades do Estado) fora do objeto SELECT do HTML. Segue exemplo no console:

```javascript
var retorno = city.Array({states: "BA"}); // BA ou ba
console.log(retorno);
```
