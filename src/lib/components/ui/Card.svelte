<script lang="ts">
  import Title from "./CardTitle.svelte";
</script>

<div class="px-4 py-3 rounded-md bg-gray-900 space-y-2">
  <slot Title={Title} />
  <slot name="content" />
    {#if $$slots.action}
        <slot name="action"/>
    {/if}
</div>
