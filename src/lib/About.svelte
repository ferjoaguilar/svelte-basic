<script lang="ts">
    import type {DarkmodeType} from '../types/darkmode'
    import Button from './Button.svelte';

    let someText:string = `Frontend Developer at Platzi`;
    let count:number = 0;
    let styles:DarkmodeType = {darkmode: false}

    const handleClick = () =>{
        count += 1;
    }

    const handleDarkMode = () =>{
        styles.darkmode =!styles.darkmode;
        window.document.body.classList.toggle("dark-mode")
    }

</script>

<div class="About">

    <!-- Estructure conditional -->
    {#if !styles.darkmode}
        <p>{someText}</p>
    {:else}
        <p><span>Hello dark mode</span></p>
    {/if}
    <Button text="Click" count={count} on:click={handleClick}/>
    <button on:click={handleDarkMode}>{styles.darkmode ? 'Dark mode' : 'Light mode'}</button>
</div>

<style>
    p{
        color: purple;
    }
</style>