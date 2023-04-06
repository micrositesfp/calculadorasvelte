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
        font-size: 0.90rem;
    }.s-10 {
        font-size: 0.910rem;
    }.s-11 {
        font-size: 0.911rem;
    }
    .s-12 {
        font-size: 0.912rem;
    }
    .s-13 {
        font-size: 0.913rem;
    }
    .s-14 {
        font-size: 0.914rem;
    }
    .s-15 {
        font-size: 0.915rem;
    }
    .s-16 {
        font-size: 0.916rem;
    }
    .s-17 {
        font-size: 0.917rem;
    }
    .s-18 {
        font-size: 0.918rem;
    }
    .s-19 {
        font-size: 0.919rem;
    }
    .s-20 {
        font-size: 0.92rem;
    }
    .pequena{
        font-size: 0.916rem;
    }
</style>