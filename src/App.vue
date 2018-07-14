<template>
<div id="app">
    <div class="title">
        <h3>{{ title }}</h3>
        <button class="btn btn-primary" @click="fetchCharacter">Test Fetch Character</button>
    </div>
</div>
</template>

<script>
export default {
    name: 'app',
    data() {
        return {
            title: 'Hello Darth Vader'
        }
    },
    methods: {
        fetchCharacter() {
            fetch('https://swapi.co/api/people', {
                method: 'GET'
            })
            .then(response => response.json())
            .then(json => console.log(json))
        }
    }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
</style>