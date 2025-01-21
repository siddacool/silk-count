<script lang="ts">
  import Box from '$lib/components/Box.svelte';
  import SilkUpdateTool from '$lib/components/SilkUpdateTool.svelte';
  import Stack from '$lib/components/ui-framework/Layout/Stack/Stack.svelte';
  import StackItem from '$lib/components/ui-framework/Layout/Stack/StackItem.svelte';
  import { useCountStore } from '$lib/stores/count/count.svelte';
</script>

<main>
  <Box>
    <Stack space={2}>
      <StackItem><h1><b>{useCountStore.count}</b> Silks Pending</h1></StackItem>
      <StackItem><SilkUpdateTool /></StackItem>
    </Stack>
  </Box>
</main>

<style lang="scss">
  main {
    height: 100vh;
    width: 100vw;
    overflow-y: auto;
    overflow-x: hidden;
  }

  h1 {
    font-weight: 500;
    text-align: center;
    font-size: 2rem;
  }
</style>
