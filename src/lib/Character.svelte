<script>
  import CharacterData from './CharacterData.svelte'

  export let character
</script>

<div class="character">
  <h1>{character.name}</h1>

  <img src={character.image} class="img-character">

  <h2>{character.house}</h2>
</div>