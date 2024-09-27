Podemos animar nosso CSS com a função animate():

por ex, essa function almenta o btn_almentar dos elemtos.

<button id="btn_almentar" style="width: 200px; height: 200px;">Almentar</button>

    $('#btn_almentar').click(
            function(){
                $('#caixa').animate({width:'500px',height:'500px'})
            }
        )


Da maneira que foi escrita em cima a animação sera feita de uma so vez. no enstado tambem é possivel adcionar ordem nessas animações ecrevendo dessa forma:

    $('#btn_diminuir').click(
            function(){
                $('#caixa').animate({width:'200px'}).animate({height:'200px'})
            }
        )


tambem é possivel é possivel contrar propriedades desses animações. ex diração. O primero grupo de chaces esta o argumento. já o sequndo é referente ao tempo de duração {duration:x} onde: 1000 = 1 segundo:

    $('#btn_almentar').click(
        function(){
            $('#caixa').animate({width:'500px',height:'500px'},{duration:3000})
        }
    )

    $('#btn_diminuir').click(
            function(){
                $('#caixa').animate({width:'200px'},{duration:200}).animate({height:'200px'},{duration:3000})
            }
        )

Tambem é possivel esecutar funções call back:


