<script>
    import Item from "./Item.svelte";
    export let data;
</script>

<div id="card">
    {#each data as item}
        <Item data={item} />
    {/each}
</div>

<style>
    #card {
        border-radius: 10px;
        overflow: hidden;
        display: flex;
    }
</style>
