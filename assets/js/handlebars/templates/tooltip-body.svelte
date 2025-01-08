<script>
	const { isPlain, hint } = $props()
</script>

{#if isPlain}
  <section class="docstring docstring-plain">
    {hint.description}
  </section>
{:else}
  <div class="detail-header">
    <h1 class="signature">
      <span translate="no">{hint.title}</span>
      <div class="version-info" translate="no">{hint.version}</div>
    </h1>
  </div>
  {#if hint.description}
    <section class="docstring">
      {@html hint.description}
    </section>
  {/if}
{/if}
