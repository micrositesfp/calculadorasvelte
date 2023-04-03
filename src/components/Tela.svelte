<script lang="ts">
    export let valor: string = ''
    $: tamanhoFonte = valor.length > 20 ? 'pequena': `s-${valor.length}`
</script>

<div class={`tela ${tamanhoFonte}`}>
<span>{valor}</span>
</div>

<!-- flex:1; faz o flexbox oculpar o espaço restante na tela -->
<style>
    .tela{
        display: flex;
        flex: 1;
        align-items: center;
        justify-content: flex-end;
        padding: 3px;
        overflow: hidden;
        font-size: 1.5rem;
        background-color: aliceblue;
        border-radius: 3px;
        margin-bottom: 5px;
    }
    .s-9 {
        font-size: 1.8rem;
    }.s-10 {
        font-size: 1.1rem;
    }.s-11 {
        font-size: 1.2rem;
    }
    .s-12 {
        font-size: 1.6rem;
    }
    .s-13 {
        font-size: 1.5rem;
    }
    .s-14 {
        font-size: 1.4rem;
    }
    .s-15 {
        font-size: 1.3rem;
    }
    .s-16 {
        font-size: 1.2rem;
    }
    .s-17 {
        font-size: 0.82rem;
    }
    .s-18 {
        font-size: 0.76rem;
    }
    .s-19 {
        font-size: 0.74rem;
    }
    .s-20 {
        font-size: 0.72rem;
    }
    .pequena{
        font-size: 1rem;
    }
</style>