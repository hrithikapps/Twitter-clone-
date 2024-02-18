<script lang="ts">
  import Card from "./Card.svelte";
  import Title from "./CardTitle.svelte";
  import Searchbar from "./Searchbar.svelte";
  import { Button } from "$lib/components/ui/button";
</script>

<div class="px-5 flex-[0.6] hidden md:inline-block border py-2 space-y-4">
  <Searchbar />
  <Card let:Title>
    <Title>Subscribe to Premium</Title>
    <p slot="content">This is the content slot</p>
    <Button slot="action">Premium</Button>
  </Card>

  <Card let:Title>
    <Title>trends for you</Title>
    <div slot="content">
      {#each { length: 20 } as _}
        <div class="space-y-1 cursor-pointer rounded py-2 hover:bg-gray-800">
          <div class="flex gap-1 capitalize items-center text-xs text-gray-500">
            <p>Music</p>
            <p>Trending</p>
          </div>
          <p class="font-bold text-sm capitalize">hrithik</p>
          <p class="text-xs text-gray-500">22k</p>
        </div>
      {/each}
    </div>
  </Card>
</div>
