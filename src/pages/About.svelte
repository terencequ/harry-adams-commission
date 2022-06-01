<script lang="ts">
    import harry2 from "../assets/harry2.jpg";

    const copypastaRickAndMorty = "Harry Adams";
    const copypastaRickAndMorty2 = "Hazamysta";
    const copypastaTheoreticalPhysics = "alcoholism";
    const copypastaViewer = "consumer";
    const copypastaRick = "Harry";
    const copypastaPersonalPhilosophySource = "being unoriginal";
    const copypastaLife = "LIFE";
    const copypastaCatchphrase = "I'll drink to that";
    const copypastaCrypticReference = "Jeremy 985's epic streams and videos";
    const copypastaDanHarmon = "Harry";
    const copypastaTelevisionScreens = "eyeballs";

</script>

<main>
    <h1>About</h1>
    <div class="main">
        <h3>To be fair...</h3>
        <img class="aboutImage" src="{harry2}" alt="Harry 2" />
        <p>
            ...you have to have a very high IQ to understand <b>{copypastaRickAndMorty}</b>.
            The humour is extremely subtle, and without a solid grasp of <b>{copypastaTheoreticalPhysics}</b> most of the jokes will go over a typical <b>{copypastaViewer}</b>'s head.
            There's also <b>{copypastaRick}</b>'s nihilistic outlook, which is deftly woven into his characterisation- his personal philosophy draws heavily from <b>{copypastaPersonalPhilosophySource}</b>, for instance.
            The fans understand this stuff; they have the intellectual capacity to truly appreciate the depths of these jokes, to realise that they're not just funny- they say something deep about <b>{copypastaLife}</b>.
            As a consequence people who dislike <b>{copypastaRickAndMorty2}</b> truly ARE idiots- of course they wouldn't appreciate, for instance, the humour in <b>{copypastaRick}</b>'s existential catchphrase "<b>{copypastaCatchphrase}</b>,"
            which itself is a cryptic reference to <b>{copypastaCrypticReference}</b>.
            I'm smirking right now just imagining one of those addlepated simpletons scratching their heads in confusion as <b>{copypastaDanHarmon}</b>'s genius wit unfolds itself on their <b>{copypastaTelevisionScreens}</b>.
            What fools.. how I pity them. 😂
        </p>
        <p>
            And yes, by the way, i DO have a <b>{copypastaRickAndMorty2}</b> tattoo. And no, you cannot see it.
            It's for the ladies' eyes only- and even then they have to demonstrate that they're within 5 IQ points of my own (preferably lower) beforehand.

        </p>
        <h3>Nothin personnel kid 😎</h3>
    </div>

</main>

<style lang="scss">
    @import "../color";
    @import "../spacing";

    .main{
        margin: auto;
        padding: $default-spacing * 5;
        width: 600px;
        max-width: 90%;
        text-align: left;
        display: flex;
        flex-direction: column;
        background-color: $emphasized-background-color;
        h1, h3{
            text-align: center;
          margin-bottom: $default-spacing * 5;
        }
        .aboutImage {
            align-self: center;
            width: 250px;
        }
        p{
            text-indent: 1em;
        }
    }
</style>
