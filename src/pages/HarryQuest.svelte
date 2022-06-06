<script>
    import {onMount} from "svelte";

    function injectScript(src) {
        return new Promise((resolve, reject) => {
            const id = "harry-quest-game-script";

            // Clean up old script by refreshing the whole page
            const oldScript = document.getElementById(id);
            if (oldScript) {
                console.log("hard refreshing page");
                location.reload();
            }

            // Create new script
            const script = document.createElement('script');
            script.src = src;
            script.id = id;
            script.addEventListener('load', resolve);
            script.addEventListener('error', e => reject(e.error));
            document.head.appendChild(script);
        });
    }

    async function startGameAsync(){
        await injectScript('/games/harry-quest-game/game.js')
            .then(() => {
                console.log('Harry Quest JS script loaded!');
            }).catch(error => {
            console.error(error);
        });
    }

    onMount(async () => {
        await startGameAsync();
    });
</script>

<main>
    <h1>Harry Quest</h1>
    <canvas id="canvas" width="276" height="414"></canvas>
</main>

<style>
    #canvas {
        background-color: #be8172;
        border: 2px solid black;
        display: block;
        margin: auto;
    }
</style>
