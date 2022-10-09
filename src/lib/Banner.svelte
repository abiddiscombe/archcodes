<!-- src/lib/Banner.svelte -->
<script>

    async function fetchMetadata() {
        const response = await fetch('https://directus.archiebiddiscombe.net/items/personalWebsite')
        const responseJson = await response.json()
        // note: currently only returns banner data
        return responseJson.data[0]
    }

    let bannerData = fetchMetadata()

</script>

<style>
    section {
        margin: 0;
        padding: 0;

        color: #222222;
        background: rgb(255, 208, 97);
    }

    section > p {
        margin: 10px;
        padding: 0;
		font-size: 0.9em;
		font-weight: 400;
        font-family: -apple-system, BlinkMacSystemFont, avenir next, avenir, segoe ui, helvetica neue, helvetica, Cantarell, Ubuntu, roboto, noto, arial, sans-serif;
    }
</style>

<!-- scaffold -->

<section>
    {#await bannerData}
        <div></div>
    {:then bannerData}
        {#if bannerData.enabled}
            <p>{bannerData.content}</p>
        {/if}
    {/await}
</section>

