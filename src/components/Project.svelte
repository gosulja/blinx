<script>
    import Seperator from "./Seperator.svelte";
    import Button from "./Button.svelte";
    import Image from "./Image.svelte";

    /**
	 * @type {any[]}
	 */
    let projects = [];
  
    async function loadData() {
      try {
        const response = await fetch('projects.json');
        const data = await response.json();
        projects = Object.values(data.projects);
      } catch (error) {
        console.error('Error fetching data:', error);
      }
    }

    import { onMount } from "svelte";

    onMount(loadData);
</script>  

<main>
    {#each projects as project}
        <div class="project-container">
            <h1>{project.name}</h1>
            <div class="divider"></div>
            <p>{project.description}</p>

            <div class="image-container">
                {#each project.images as image}
                    <Image src={image} />
                {/each}
            </div>
            
            <div class="button-container">
                {#each project.links as link}
                    {#if link.name == "BACK TO TOP"}
                        <Button text={link.name} icon="arrow_upward" on_click={() => {
                            window.scrollTo({
                                top: 0,
                                left: 0,
                                behavior: 'smooth'
                            });
                        }}/>
                    {:else}
                        <Button text={link.name} icon="open_in_new" on_click={() => {
                            window.location.href = link.link;

                            return false;
                        }}/>
                    {/if}
                {/each}
            </div>
        </div>

        <Seperator />
    {/each}
</main>

<style>
    main {
        padding: 1em;
    }

    h1 {
        color: #fafafa;
        font-weight: 300;
        font-size: 30px;
        text-align: center; /* Center align the heading on mobile */
        margin-bottom: 15px; /* Add margin for separation on mobile */
    }

    p {
        color: #7b7b7b;
        font-size: 18px;
        font-weight: 300;
        text-align: justify; /* Justify text for better readability on mobile */
        margin-bottom: 10px; /* Add margin for separation on mobile */
    }

    .project-container {
        background: rgb(24, 24, 24);
        border-radius: 12px;
        padding: 10px;
        margin-top: 10px;
    }

    .divider {
        width: 100%;
        height: 2px;
        background-color: rgb(51, 51, 51);
        margin: 10px 0;
    }

    .button-container {
        display: flex;
        flex-direction: row; /* Stack buttons vertically on mobile */
        align-items: center; /* Center align buttons on mobile */
        gap: 10px;
        margin-top: 10px;
    }

    .image-container {
        display: flex;
        flex-wrap: nowrap; /* Prevent wrapping of images */
        justify-content: flex-start;
        align-items: center;
        margin-top: 10px;
        overflow-x: auto;
        padding: 5px;
        background-color: transparent;
        border-radius: 8px;
    }

    .image-container::-webkit-scrollbar {
        width: 5px;
    }

    .image-container::-webkit-scrollbar-thumb {
        background: rgb(120, 120, 120);
        border-radius: 20px;
    }

    .image-container::-webkit-scrollbar-thumb:hover {
        background: rgb(140, 140, 140);
    }
</style>

