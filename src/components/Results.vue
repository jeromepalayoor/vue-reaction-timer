<template>
    <div class="results">Score: {{ this.score }}ms</div>
</template>

<script>
export default {
    props: ['score'],
};
</script>

<style>
.results {
    width: 400px;
    border-radius: 20px;
    background-color: gold;
    color: black;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
}
</style>
