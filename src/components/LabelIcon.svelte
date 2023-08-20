<script>
	export let text, icon;
</script>

<span class="content"> {text} <span class="material-symbols-outlined"> {icon} </span> </span>

<style>
	span.material-symbols-outlined {
        color: rgb(210, 210, 210);
        margin-left: 10px;
    }

    .content {
        display: flex;
        align-items: center;
        padding: 10px 8px;
        color: rgb(210, 210, 210);
        font-weight: 500;
        font-size: 16px;
        font-family: "Inter", sans-serif;
        background-color: transparent;
        cursor: crosshair;
        transition: color 0.3s, transform 0.2s;
    }

    .content:hover {
        color: rgb(255, 255, 255);
    }
</style>