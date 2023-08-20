<script>
    /**
	 * @type {string}
	 */
     export let text;
    /**
	 * @type {any}
	 */
     export let on_click;
    /**
     * @type {string} 
     */
     export let icon;
</script>

<main>
    <button on:click={on_click}>
        <span class="button-content">
            {text}
            <span class="material-symbols-outlined">
                {icon}
            </span>
        </span>
    </button>
</main>

<style>
    .button-content {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 5px 8px;
    }

    span.material-symbols-outlined {
        color: rgb(230, 230, 230);
        margin-left: 10px;
    }

    button {
        display: flex;
        align-items: center;
        padding: 10px 8px;
        border: none;
        border-radius: 8px;
        color: rgb(230, 230, 230);
        font-weight: 500;
        font-size: 16px;
        font-family: "Inter", sans-serif;
        background-color: rgb(40, 40, 40);
        cursor: pointer;
        transition: background-color 0.3s, transform 0.2s;
    }

    button:hover {
        background-color: rgb(60, 60, 60);
    }

    button:active {
        background-color: rgb(20, 20, 20);
        transform: translateY(2px);
    }
</style>
