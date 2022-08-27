<script>
  export let character
</script>

<div>
  <div>
    <h1>{character.name}</h1>
    <img src={character.image} class="img-character">
    <h2>{character.house}</h2>
  </div>
  <hr>
  <div>
    <p>{character.spacies}</p>
    <p>{character.gender}</p>
    <p>{character.dateOfBirth}</p>
    <p>{character.patronus}</p>
  </div>
</div>