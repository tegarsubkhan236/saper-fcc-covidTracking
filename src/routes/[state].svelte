<script context="module">
    export async function preload(page) {
        return { state: page.params["state"] };
    }
</script>

<script>
    import CovidChart from "../components/CovidChart.svelte";
    import CovidStat from "../components/CovidStat.svelte";
    export let state;
</script>

<CovidStat />
<CovidChart />
<h1>{state}</h1>
