<script>
    import Project from "../components/Project.svelte";
    import Seperator from "../components/Seperator.svelte";
    import Card from "../components/Card.svelte";
    import Divider from "../components/Divider.svelte";
</script>

<main>
    <Card title="hi, i'm blinx" description="i program in lua, c++, js and ts. i'm also learning svelte, next.js and vue.js. i love to design and program uis / uxs" />

    <Seperator />

    <Divider />

    <Seperator />

    <Seperator />

    <h1>Projects</h1>

    <Seperator />

    <Project />
</main>

<style>
    /* global styles */

    h1 {
        color: rgb(255, 255, 255);
        font-size: 3em;
        text-align: center;
        width: 100%;
    }
</style>
