<script lang="ts">
    import type {SkillsType} from '../types/skills'

    let skills:Array<SkillsType> = [
        {id: 1, name: 'HTML'},
        {id: 2, name: 'CSS'},
        {id: 3, name: 'JavaScript'},
        {id: 4, name: 'TypeScript'}
    ]
</script>

<div class="Skills">
    <ul>
        {#each skills as skill, i}
            <li>index: {i} - {skill.name}</li>
        {/each}
    </ul>
</div>

<style>
    .Skills{
        display: flex;
        align-items: center;
        justify-content: center;
    }
    ul{
        margin: 0;
        padding: 0;
        list-style: none;
    }
</style>