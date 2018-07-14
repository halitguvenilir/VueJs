<template>
<div id="app">
    <div class="container">
        <h3>{{ title }}</h3>
        <div class="col-md-12">
            <Character
                v-for="(id, index) in initial_ids"
                :id="id"
                key="index"
            />
        </div>
    </div>
</div>
</template>

<script>
import Character from './components/Character.vue'

export default {
    name: 'app',
    data() {
        return {
            title: 'Hello Darth Vader',
            initial_ids: [1]
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