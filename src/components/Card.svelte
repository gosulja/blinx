<script>
    import { onMount } from "svelte";

    import Seperator from "./Seperator.svelte";
    import Button from "./Button.svelte";
    import LabelIcon from "./LabelIcon.svelte";

    /**
	 * @type {string}
	 */
     export let title;
     /**
	 * @type {string}
	 */
      export let description;

</script>

<main class="card-container">
    <div class="card">
        <div class="card-content">
            <div class="card-header">
                <span class="card-title">{title}</span>
                <!-- svelte-ignore a11y-img-redundant-alt -->
                <img class="card-pfp" src="pfp.png" alt="My profile picture">
            </div>
            <div class="card-divider-container">
                <div class="card-divider"></div>
            </div>
            <p class="card-description">
                {description}
            </p>
            <div class="card-icons">
                <i class="devicon-lua-plain-wordmark colored"></i>
                <i class="devicon-cplusplus-plain colored"></i>      
                <i class="devicon-javascript-plain colored"></i>
                <i class="devicon-typescript-plain colored"></i>
                <i class="devicon-svelte-plain colored"></i>
                <i class="devicon-nextjs-original colored"></i>
                <i class="devicon-vuejs-plain colored"></i>
            </div>
            <div class="card-divider-container">
                <div class="card-divider"></div>
            </div>
            <div class="card-link">
                <a href="https://discordapp.com/users/797222948800954460" class="card-link-a">Contact me via Discord</a>
            </div>
        </div>
    </div>

    <!-- <Button text="PROJECTS" icon="arrow_downward" on_click={()=>{
        window.scrollTo({
            top: 712,
            left: 0,
            behavior: 'smooth'
        });
    }}/> -->
</main> 

<style>
    .card-container {
        display: flex;
        flex-direction: column;
        gap: 50px;
        justify-content: center;
        align-items: center; /* Vertically center the cards */
        margin-top: 7em;
        margin-bottom: 7em;
    }

    .card {
        display: flex;
        border-radius: 12px;
        height: 450px;
        width: 300px;
        background: rgb(40, 40, 40);
    }

    .card-content {
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        align-items: center; /* Vertically center the content */
        width: 100%;
        padding: 20px;
    }

    .card-header {
        color: rgb(255, 255, 255);
        font-size: 26px;
        font-weight: 700;
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 10px;
    }

    .card-description {
        color: rgb(201, 201, 201);
        font-weight: 400;
        text-align: center;
        font-size: 18px;
        margin-top: 15px;
        display: flex;
        align-items: center;
        justify-content: center;
        padding-bottom: 25px;
        justify-items: flex-end;
    }

    .card-link {
        margin-top: 5px;
        padding: 13px 40px;
        border-radius: 6px;
        background-color: #007bff;
        color: white;
        cursor: pointer;
        transition: background-color 0.3s;;
    }

    .card-link-a {
        color: white;
        font-weight: 500;
        text-decoration: none;
    }

    .card-link:hover {
        background-color: #0056b3;
    }

    .card-divider-container {
        width: 115%;
        padding-top: 10px;
        padding-bottom: 10px;
    }

    .card-divider {
        background: rgb(50, 50, 50);
        height: 1px;
    }

    .card-icons {
        padding-top: 10px;
        padding-bottom: 10px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: aliceblue;
        flex-wrap: wrap;
        max-width: 400px; 
        margin: 0 auto; 
    }

    i {
        font-size: 40px;
        margin-right: 15px;
        margin-bottom: 10px;
    }

    .card-pfp {
        border-radius: 5em;
        margin-left: 25px;
        width: 50px;
        height: 50px;
    }
</style>
