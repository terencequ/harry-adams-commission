<script>
    import {Route} from "svelte-navigator";
    import Home from "../pages/Home.svelte";
    import Forum from "../pages/Forum.svelte";
    import About from "../pages/About.svelte";
    import CompoundInterestCalculator from "../pages/CompoundInterestCalculator.svelte";
    import HarryQuest from "../pages/HarryQuest.svelte";
</script>

<main>
    <Route path="/"><Home/></Route>
    <Route path="about"><About/></Route>
    <Route path="compound-interest-calculator"><CompoundInterestCalculator/></Route>
    <Route path="harry-quest"><HarryQuest/></Route>
    <Route path="forum"><Forum/></Route>
</main>
