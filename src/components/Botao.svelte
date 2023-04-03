<script lang="ts">

    
   export let texto:string = '';
   export let triplo:boolean = false;
   export let duplo:boolean = false;
   export let operacao:boolean = false;
   export let destaque:boolean = false;
   export let onClick:(valor:string) => void =()=>{} 


   

</script>
<!--
<button class={`botao ${triplo ? 'triplo': ''}`}>
-->
<button 
    on:click={()=>onClick(texto)}
    class="botao" class:triplo class:duplo class:operacao class:destaque>
    {texto}
</button>

<style>
    .botao {
        margin: 0;
        border: solid 1px var(--cor-fundo);
        color: tomato;
        flex-basis: 25%;
    }
    .triplo{
        flex-basis: 75%;
    }.duplo{
        flex-basis: 50%;
    }
    .operacao {
        background-color: orange;
        color: white;
    }
    .destaque {
        background-color: blue;
        color: white;
    }
</style>