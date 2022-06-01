<script lang="ts">
    import { Link } from "svelte-navigator";
</script>

<main>
    <ul>
        <li>
            <Link class="hover-effect" to="/">HOME</Link>
        </li>
        <li>
            <Link class="hover-effect" to="forum">FORUM</Link>
        </li>
        <li>
            <Link class="hover-effect" to="compound-interest-calculator">COMPOUND INTEREST CALCULATOR</Link>
        </li>
        <li>
            <Link class="hover-effect" to="harry-quest">HARRY QUEST</Link>
        </li>
        <li>
            <Link class="hover-effect" to="about">ABOUT</Link>
        </li>
    </ul>
</main>

<style lang="scss">
    @import "../spacing";
    @import "../color";

    ul {
      background-color: $emphasized-background-color;
      list-style: none;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: row;
      padding: 0;
      width: 100%;
      height: 50px;
      margin: 0 0 $default-spacing * 10;
    }
    li {
      margin: 0 $default-spacing * 8;
    }
</style>
