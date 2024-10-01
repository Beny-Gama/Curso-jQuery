imagine que vc que adicionar um elemento a sua aplicação, basta usar a funnção append():

        $('#btnAdicionar').click(()=>{
            $('#caixa').append('<div class="subcaixa"> </div>')
        })

Podemos por exepo adicinar cores diferentes a essa aplicação:

        let r,g,b
        $('#btnAdicionar').click(()=>{
            r=Math.floor(Math.random()*255)
            g=Math.floor(Math.random()*255)
            b=Math.floor(Math.random()*255)
            $('#caixa').append('<div class="subcaixa" style="background-color: rgb('+r+','+g+','+b+')"  > </div>')
        })

podemos adiciona mais de uma vez usando um loop for():

        let r,g,b
        $('#btnAdicionar5').click(()=>{
            for(let i = 0; i < 5; i++){
                r=Math.floor(Math.random()*255)
                g=Math.floor(Math.random()*255)
                b=Math.floor(Math.random()*255)
                $('#caixa').append('<div class="subcaixa" style="background-color: rgb('+r+','+g+','+b+')"  > </div>')
            }
        })


Tambem é possivel adiconar as modificação, e depois indereçar onde vc quer usar, com a função appendTo():

                $('<div class="subcaixa" style="background-color: rgb('+r+','+g+','+b+')"  > </div>').appendTo($('#caixa'))

Qunado vc usa as append() e appendTo(). Eles adicionam um nomo elemento ao final da extrutura.

Porem se guisermos adiconar no começo da estrutura é so usar as funções Prepend() e PrependTo():

        let r,g,b
        let num=0
        $('#btnAdicionar').click(()=>{
            r=Math.floor(Math.random()*255)
            g=Math.floor(Math.random()*255)
            b=Math.floor(Math.random()*255)
            $('#caixa').prepend('<div class="subcaixa" style="background-color: rgb('+r+','+g+','+b+')">'+num+'</div>')
            num++
        })

        $('#btnAdicionar5').click(()=>{
            for(let i = 0; i < 5; i++){
                r=Math.floor(Math.random()*255)
                g=Math.floor(Math.random()*255)
                b=Math.floor(Math.random()*255)
                // $('<div class="subcaixa" style="background-color: rgb('+r+','+g+','+b+')">'+num+'</div>').prependTo($('#caixa'))
                $('<div class="subcaixa" style="background-color: rgb('+r+','+g+','+b+')"></div>').prependTo($('#caixa')).text(num)
                num++
            }
        })
