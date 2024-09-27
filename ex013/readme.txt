Aprendendo sobre os métodos siblings, next e prev [jQuery] - Curso de jQuery - Aula 13



<div>
    <span>
        <h3>
            Bernardo Gama
        </h3>
            <p>
                Curso de JQuere
            </o>
            <h2>
                Selectors irmãos
            </h2>
            <p>
                Siblings
            </p>
        </span>
    </div>


perseba que existe pais filhos e irmão. irmão são os que estão na mesma linha, sendo que os outros estão em linhas diferentes.

para que se estrubua a as mesma caracteristicas dos irmão é nessesario atrimuir os sequintes parametros, unsado a função siblings():

$('h3').siblings().css({'border':'1px solid red'})

voce tambem pode tatrimuir a um irmão espesifico dentre os irmãos, basta incorporar na função:

$('h3').siblings('p').css({'border':'1px solid red'})


já o next(), aponda para seu proximo irmão na lista.


já o prev(), "previa" é referente ao irmão da anterir:

$('h3').prev().css({'border':'1px solid red'})


já o prevAll(), "todos previa" pega todos irmãos anteriores.

$('h3').prevAll().css({'border':'1px solid red'})

já o nextAll(), "todos proximo" pega todos irmãos posteriores.

$('h3').nextAll().css({'border':'1px solid red'})

já o prevUntil('h3'), "previa até" pega todos os elementos previos até determindado elementos.

já o nextUntil('h3'), "proximo até" pega todos os elementos a posteriore até determindado elementos.
