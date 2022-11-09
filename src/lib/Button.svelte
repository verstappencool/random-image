<script>
	export let choices;
	export let changeChoice;
</script>

<div class="buttons">
	{#each choices as choice}
		<button on:click={changeChoice(choice.name)}>{choice.emotion}{choice.name}</button>
	{/each}
</div>

<style>
  .buttons {
    display: flex;
    justify-content: center;
    align-items: center;
    column-gap: 10px;
    margin: 1.5rem;
    padding-bottom: 10px;
  }

</style>

<!-- <div class="buttons">
    {#each choices as choice}
      <button on:click={() => {
        selected = choice;
        changeImage();
      }}>{choice}</button>
    {/each}
  
     -->

<!-- <div class="buttons">
      {#each choices as choice}
        <button on:click={changeChoice(choice)}>{choice}</button>
      {/each}
    </div> -->
