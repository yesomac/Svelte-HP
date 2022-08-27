<script>
  import Character from './lib/Character.svelte'
  import CharacterData from './lib/CharacterData.svelte'

  let characters = []
  let page = 1

  async function loadCharacter(){
    const response = await fetch('http://hp-api.herokuapp.com/api/characters')
    const data = await response.json()
    console.log(data)
    characters = data
  }

  loadCharacter()

  function nextPage(){
    page++
    loadCharacter()
  }

  function previousPage(){
    page--
    loadCharacter()
  }
</script>

<h1 class="title">Harry Pother Character</h1>

<div class="container">
  <div class="btns">
    <button class="btn" on:click={previousPage} disabled={page === 1}>Previous</button>
    <button class="btn" on:click={nextPage}>Next</button>
  </div>

  <div class="container grid">
    {#each characters as character}
    <Character character={character}/>
    <!-- <CharacterData character={character}/> -->
  {/each}
  </div>
</div>