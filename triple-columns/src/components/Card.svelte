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
        position: fixed;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        box-shadow: 5px 5px 5px rgba(0, 0, 0, 0.25);
    }
</style>
