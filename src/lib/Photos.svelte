<script lang="ts">
    import {onMount} from 'svelte'

    let photos = [];

    onMount(async () => {
        console.log("Initializing")
        const response = await fetch('https://jsonplaceholder.typicode.com/photos?_limit=20');
        const data = await response.json();
        photos = data;
    })
</script>

<div class="Photos">
    {#each photos as photo,i}
        <figure>
            <img src={photo.thumbnailUrl} alt={photo.title}>
            <figcaption>{photo.title}</figcaption>
        </figure>
        {:else}
        <p>Loading...</p>
    {/each}
</div>