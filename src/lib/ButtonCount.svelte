<script lang="ts">
    import {count} from '../store/store'

    const handleClick = () => {
        //Update global value
        count.update(n => n+1)
    }
</script>

<div class="Button">
    <button on:click={handleClick}>
        Click {$count === 0 ? '': $count}
    </button>
</div>

<style>
    button{
        background-color: #f76027;
        color: white;
        border-radius: 4px;
        padding: 0.5rem;
        text-transform: uppercase;
        cursor: pointer;
    }
</style>