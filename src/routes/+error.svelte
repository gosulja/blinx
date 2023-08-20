<script>
    import Button from "../components/Button.svelte";
</script>

<main>
    <div class="centered-content">
        <h1>404 Error, how did this happen... 🙄</h1>
        <Button text="BACK" icon="undo" on_click={()=>{
            window.location.href = "/";
        }}/>
    </div>
</main>

<style>
    .centered-content {
        display: flex;
        flex-direction: column;
        align-items: center; /* Center horizontally */
        justify-content: center; /* Center vertically */
        height: 95vh; /* Set the height to viewport height */
    }

    main {
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: "Inter", sans-serif;
    }

    h1 {
        color: aliceblue;
    }
</style>
