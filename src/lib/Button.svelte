<script lang="ts">
    export let count:number;
    export let text:string;
</script>

<button on:click>
    {text}
    {count === 0? '': count}
</button>