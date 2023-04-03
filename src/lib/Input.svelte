<script lang="ts">
    export let name:string = "hello";
</script>

<div class="Input">
    <input type="text" bind:value={name}>
    <p>Hello {name}!</p>
</div>