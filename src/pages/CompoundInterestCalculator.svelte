<script lang="ts">
    import {createEventDispatcher} from "svelte";

    let loanAmountInDollars: number | undefined = undefined;
    let interestRate: number | undefined = undefined;
    let numberOfTimesPerYear: number | undefined = undefined;
    let years: number | undefined = undefined;

    let result: string = "";

    const dispatch = createEventDispatcher();

    function save() {
        getResult();
        dispatch('done-editing');
    }

    function getResult(): string{
        try {
            const resultNum = ((loanAmountInDollars * (1 + interestRate/numberOfTimesPerYear)**(numberOfTimesPerYear * years)) - loanAmountInDollars);
            if(isNaN(resultNum)){
                result = "Imbecile. Your inputs suck."
            } else {
                result = `The total interest accrued is: \$${resultNum}`;
            }
        } catch (e) {
            return e;
        }
    }
</script>

<main>
    <h1>Compound Interest Calculator</h1>
    <div class="main">
        <em>The formula for this code was kindly supplied by YouTuber <a class="hover-effect" href="https://www.youtube.com/channel/UCP-e7t39xWBpIfZhKzvyc3w" target="_blank">Coxit Fabam</a>.</em>
        <div class="formField">
            <label for="loanAmountInDollars">Please enter the loan amount in dollars:</label>
            <input type="number" id="loanAmountInDollars" bind:value="{loanAmountInDollars}" minlength="0"/>
        </div>
        <div class="formField">
            <label for="interestRate">Please enter the interest rate as a decimal:</label>
            <input type="number" id="interestRate" bind:value="{interestRate}" minlength="0"/>
        </div>
        <div class="formField">
            <label for="numberOfTimesPerYear">Please enter the number of times interest is applied per year:</label>
            <input type="number" id="numberOfTimesPerYear" bind:value="{numberOfTimesPerYear}" minlength="0"/>
        </div>
        <div class="formField">
            <label for="years">Please enter the length of the loan in years:</label>
            <input type="number" id="years" bind:value="{years}" minlength="0"/>
        </div>

        <div class="formField">
            <button on:click="{() => save()}">Save</button>
        </div>

        <div class="result">
            <h3>{result}</h3>
        </div>
    </div>

</main>

<style lang="scss">
    @import "../color";
    @import "../spacing";

    .main {
      em {
        margin-bottom: $default-spacing * 6;
      }
      .formField {
        display: flex;
        justify-content: space-between;
        margin-bottom: 1em;
        text-align: right;
        button {
          margin-top: $default-spacing * 2;
          width: 100%;
          height: 30px;
        }
        label {
            text-align: left;
        }
        input {
          width: 100px;
        }
      }
      .result {
        text-align: center;
      }
    }
</style>
