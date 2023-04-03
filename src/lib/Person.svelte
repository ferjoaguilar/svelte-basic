<script lang="ts">
    import type {PersonType} from '../types/person'
    export let person:PersonType;
</script>

<div class="Person">
    <p>{person.name} {person.lastName} {person.age}</p>
</div>