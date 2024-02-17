<script lang='ts'>
  import Sidebar from '$lib/components/ui/Sidebar.svelte';
    import '../app.css'
</script>

<div class='flex border mx-auto w-full max-w-6xl '>
    <Sidebar/>
    <slot/>
</div>
