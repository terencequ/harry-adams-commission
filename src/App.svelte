

<script lang="ts">
  import {Router} from "svelte-navigator";
  import Navigation from "./components/Navigation.svelte"
  import Routes from "./components/Routes.svelte";
</script>

<Router>
  <Navigation/>
  <Routes/>
</Router>

<!-- Global styling -->
<style global lang="scss">
  @import "spacing";
  @import "color";

  /** MAIN LAYOUT */
  body {
    text-align: center;
    color: $text-color;
    background-color: $background-color;
    margin: 0;
  }

  /** TYPOGRAPHY */
  * {
    font-family: 'Comic Sans MS', sans-serif;
  }
  h1 {
    font-size: 3em;
    font-weight: bold;
    margin-bottom: $default-spacing * 4;
  }
  h2 {
    font-size: 2em;
    font-weight: normal;
    margin-bottom: $default-spacing * 2;
  }
  h3 {
    font-size: 1.5em;
    font-weight: bold;
    margin-bottom: $default-spacing;
  }
  h4 {
    font-size: 1.2em;
    font-weight: bold;
    margin-bottom: $default-spacing;
  }
  p {
    font-family: 'Roboto', sans-serif;
    font-size: 1.05em;
    line-height: 1.5em;
  }
  .subtitle {
    font-size: 1.2em;
    font-weight: normal;
  }

  /** IMAGES */
  .defaultImage {
    width: 250px;
  }

  /** LINK HOVER */
  a, a > span {
    font-family: 'Comic Sans MS', sans-serif;
    position: relative;
    color: inherit;
    text-decoration: none;
    line-height: 24px;
    &:before, &:after {
      content: '';
      position: absolute;
      transition: transform .2s ease;
    }
  }

  .hover-effect {
    padding-top: $default-spacing;
    padding-bottom: $default-spacing;
    &:before {
      left: 0;
      bottom: 0;
      width: 100%;
      height: 2px;
      background: $text-color;
      transform: scaleX(0);
    }
    &:hover:before {
      transform: scaleX(1);
    }
  }

  /** MAIN */
  .main {
    margin: auto;
    padding: $default-spacing * 5;
    width: 600px;
    max-width: 90%;
    text-align: left;
    display: flex;
    flex-direction: column;
    background-color: $emphasized-background-color;
  }
</style>
