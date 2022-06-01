<script>
    import {Route} from "svelte-navigator";
    import Home from "../pages/Home.svelte";
    import Forum from "../pages/Forum.svelte";
    import About from "../pages/About.svelte";
</script>

<main>
    <Route path="/"><Home/></Route>
    <Route path="about"><About/></Route>
    <Route path="forum"><Forum/></Route>
</main>
