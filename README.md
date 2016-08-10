# Cidades e Estados do Brasil

Código criado em JavaScript para retornar as Cidades e Estados brasileiros.
Abaixo segue as principais funcionalidades do script.


### Funcionalidade para Estados: 

 * Retorno dos Estados através do Nome ou da Sigla;
 * Marcar o Estado no campo de SELECT do HTML;


OBS: O retorno é impresso em um SELECT.

##

Por padrão, usando o método .states(), exemplo:

```javascript
document.getElementById("select").states();
```

Resultado final:
```html
<option value="BA">Bahia</option>
```

##

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

##


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

##

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

##

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

##

Outra opcão de retorno pode ser usando **states.Array()** fora do objeto SELECT do HTML. Segue exemplo no console:

```javascript
var retorno = states.Array();
console.log(retorno);
```

##


### Funcionalidade para Cidades: 

 * Retorno dos Estados através do Nome ou da Sigla;
 * Marcar o Estado no campo de SELECT do HTML;
