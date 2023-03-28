<template>
    <div class="results" :class="{ green: this.type === 0, orange: this.type === 1, red: this.type === 2 }">Reaction time: {{ this.score }}ms <br> {{ this.rank }}</div>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null,
            type: null
        }
    },
    mounted() {
        if (this.score < 250) {
            this.rank = 'LIGHTSPEED'
            this.type = 0
        }else if (this.score < 400) {
            this.rank = 'Rapid reflexes'
            this.type = 1
        }else{
            this.rank = 'As slow as a snail...'
            this.type = 2
        }
    }
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
.green {
    background-color: darkgreen;
    color: whitesmoke;
}
.orange {
    background-color: darkorange;
    color: black;
}
.red {
    background-color: darkred;
    color: whitesmoke;
}
</style>
