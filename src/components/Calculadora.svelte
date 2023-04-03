    <script lang="ts">
        import Botao from "./Botao.svelte";
        import Linha from "./Linha.svelte";
        import Tela from "./Tela.svelte";
    </script>

    <div class="calculadora" >
        <Tela valor={'111111111111111111012345678910'}></Tela>
            <Linha>
            <Botao destaque triplo={true} texto="CE"></Botao>
            <Botao operacao texto="/"></Botao>
        </Linha>

        <Linha>
            <Botao texto="9"></Botao>
            <Botao texto="8"></Botao>
            <Botao texto="7"></Botao>
            <Botao operacao texto="*"></Botao>
        </Linha>
        <Linha>
            <Botao texto="6"></Botao>
            <Botao texto="5"></Botao>
            <Botao texto="4"></Botao>
            <Botao operacao texto="+"></Botao>
        </Linha>
        <Linha>
            <Botao texto="3"></Botao>
            <Botao texto="2"></Botao>
            <Botao texto="1"></Botao>
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