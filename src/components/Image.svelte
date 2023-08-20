<script>
    /**
	 * @type {string}
	 */
     export let src;
</script>

<main>
    <!-- svelte-ignore a11y-img-redundant-alt -->
    <img class="project-image" src={src} alt="A project showcase image"/>
</main>

<style>
    .project-image {
        border-radius: 6px;
        width: auto;
        height: 300px;
        margin-right: 20px;
    }
</style>