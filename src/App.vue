<template>
<div id="app">
    <div class="container">
        <h3>{{ title }}</h3>
        <Character/>
    </div>
</div>
</template>

<script>
import Character from './components/Character.vue'

export default {
    name: 'app',
    data() {
        return {
            title: 'Hello Darth Vader'
        }
    },
    components: {
        Character
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