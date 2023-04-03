<script lang="ts">
    import About from "./lib/About.svelte";
    import ButtonCount from "./lib/ButtonCount.svelte";
    import Input from "./lib/Input.svelte";
    import Person from "./lib/Person.svelte";
    import Photos from "./lib/Photos.svelte";
    import Skills from "./lib/Skills.svelte";
    import Text from "./lib/Text.svelte";
    import type {PersonType} from './types/person'


  let sveltelogo:string = 'https://arepa.s3.amazonaws.com/svelte-logo.png'

  
  const data:PersonType = {
    name: 'Fernando',
    lastName: 'Perez',
    age: 25
  }
</script>

<main>
  <img src={sveltelogo} alt="Svelte">
  <h1>Vite + Svelte</h1>
  <About />
  <Text anotherText="Hi from App svelte file"/>
  <Text />
  <Person person={data}/>
  <Skills />
  <Input />
  <Photos />
  <ButtonCount />

  <p class="read-the-docs">
    Click on the Vite and Svelte logos to learn more
  </p>
</main>

<style>
  main img{
    width: 30%;
  }

  :global(body.dark-mode){
    background-color: #222;
    color: aliceblue;
  }
</style>
