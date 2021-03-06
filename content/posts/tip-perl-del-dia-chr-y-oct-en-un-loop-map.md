---
title: "Tip Perl del día: chr y oct en un loop map"
date: 2007-10-22 06:50:03
tag:
---
<p>La función `map` de Perl es muy poderosa. O como diría entre cuates, *mucho muy* poderosa. Básicamente lo que hace es evaluar en un bloque, cada uno de los elementos de una lista.

El día de hoy, en uno de los blogs que <a href="http://raquelhernandez.net/" target="_blank">mi chava</a> y yo (y otra bola de nacos por ahí de quienes estamos al pendiente) solemos visitar a menudo (porque es muy pendejo y nos gusta reírnos de vez en cuando), la escritora publicó <a href="http://plaqueta.blogspot.com/2007/10/ceros-y-unos-todo-bajo-control.html" target="_blank">un post</a> con cadenas en binario (típico entre personas que quieren parecer interesantes usando truquitos que siempre han existido). Como buen chismoso que soy, me di a la tarea de descifrar aquella maraña, pues suponía era un mensaje oculto. Como el resultado de dicha cadena es irrelevante aquí, crearé otra diferente que servirá para ejemplificar el tip del día.
</p>

    my $string = "10100001 01001000 01101111 01101100 01100001 00101100 00100000 01110011 01101111 01111001 00100000 01110101 01101110 00100000 01101101 01100101 01101110 01110011 01100001 01101010 01100101 00100000 01101111 01100011 01110101 01101100 01110100 01101111 00100000 01100101 01101110 00100000 01100011 01100101 01110010 01101111 01110011 00100000 01111001 00100000 01110101 01101110 01101111 01110011 00100001";


Ahora, con un poco de magia de `map`, podríamos iterar en cada uno de esos octales. Nos ayudaremos de split, para que haga la chamba:

    map {
        print chr oct "0b".$_;
    } split /\s/, $string;

A `map`, le pasamos un arreglo. ¿Qué arreglo? El producido por split, que nos devuelve uno, precisamente, a partir de la cadena `$string` y el delimitador para separar cada uno de los elementos es `/\s/`, whitespace. Ya obtenido el arreglo, es pasado a `map` que toma cada uno de los elementos, les agrega el prefijo `0b`, para que Perl entienda que la cadena pasada es en realidad un dato binario. Luego `oct` toma esa cadena y la interpreta como una cadena octal y le pasa a `chr` el valor correspondiente. Éste último toma ese valor, representado por el número obtenido por `oct` y lo traduce a su caracter correspondiente en ASCII o Unicode. Ese valor, finalmente, se lo pasa a `print` que lo imprime en pantalla, desde luego :-)

Le queda de tarea al lector descifrar lo que `$string` contenía. ;-) Próximo tip, relacionado con `map`: Divirtiéndonos con grep.
