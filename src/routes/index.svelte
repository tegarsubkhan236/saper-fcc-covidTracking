<script context="module">
    import requests from "../data/request.js";
    export async function preload() {
        try {
            const usStats = await requests.usStats();

            return { usStats };
        } catch (e) {}
    }
</script>

<script>
    import CovidChart from "../components/CovidChart.svelte";
    import CovidStat from "../components/CovidStat.svelte";
    import TableContainer from "../components/TableContainer.svelte";

    export let usStats;
    console.log(usStats, "usStats");
</script>

<svelte:head>
    <title>Covid 19 Tracker</title>
</svelte:head>

<div class="section header">
    <div class="container">
        <h1>Covid-19 The World</h1>
    </div>
</div>

<CovidStat />
<CovidChart />
<TableContainer />
