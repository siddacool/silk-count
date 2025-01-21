<script lang="ts">
  import GlobalContainer from '$lib/components/GlobalContainer';
  import type { SvelteComponentProps } from '$lib/types/svelte-component';

  const { children }: SvelteComponentProps = $props();
</script>

<GlobalContainer />

<div>
  {#if children}
    {@render children()}
  {/if}
</div>
