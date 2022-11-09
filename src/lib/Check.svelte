<script>
  export let isSfw;
  export let onClick;
</script>

<div>
  <!-- <input type="checkbox" bind:checked={isSfw} /> -->
  <button on:click={onClick()}>{isSfw ? 'SFW' : 'SFW'}</button>
  {#if isSfw}
    <span>Safe For Work</span>
  {:else}
    <span>Not Safe For Work</span>
  {/if}
</div>
