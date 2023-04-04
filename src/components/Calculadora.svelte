    <script lang="ts">
        import Botao from "./Botao.svelte";
        import Linha from "./Linha.svelte";
        import Tela from "./Tela.svelte";

        let valor = '0';

        
        class Model {
            valor: string
            constructor(valor: string = '0'){

            }
            inc(){
                return new Model(`${parseInt(this.valor)+1}`);
            }
        }

        let obj = new Model();
        function numeroDigitado(numero: string){
            obj = obj.inc();
        }

    </script>

    <div class="calculadora" >
        <Tela valor={valor}></Tela>
            <Linha>
            <Botao destaque triplo={true} texto="CE"></Botao>
            <Botao operacao texto="/"></Botao>
        </Linha>

        <Linha>
            <Botao texto="9" onClick={numeroDigitado}></Botao>
            <Botao texto="8" onClick={numeroDigitado}></Botao>
            <Botao texto="7" onClick={numeroDigitado} ></Botao>
            <Botao operacao texto="*"></Botao>
        </Linha>
        <Linha>
            <Botao texto="6" onClick={numeroDigitado} ></Botao>
            <Botao texto="5" onClick={numeroDigitado} ></Botao>
            <Botao texto="4" onClick={numeroDigitado} ></Botao>
            <Botao operacao texto="+"></Botao>
        </Linha>
        <Linha>
            <Botao texto="3" onClick={numeroDigitado} ></Botao>
            <Botao texto="2" onClick={numeroDigitado} ></Botao>
            <Botao texto="1" onClick={numeroDigitado} ></Botao>
            <Botao operacao texto="-"></Botao>
        </Linha>
        <Linha>
            <Botao duplo={true} texto="0"></Botao>
            <Botao texto=","></Botao>
            <Botao destaque texto="="></Botao>
        </Linha>
        
    </div>

    <style>

        .calculadora {
            background-color: var(--cor-fundo);
            display: flex;
            flex-direction: column;
            height: 220px;
            width: 150px;
            padding: 6px;
            border-radius: 6px;
        }

    </style>