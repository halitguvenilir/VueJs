<template>
<div id="app">
    <div class="title">
        <h3>{{ title }}</h3>
        <h4>{{ user }}</h4>
    </div>
</div>
</template>

<script>
export default {
    name: 'app',
    data() {
        return {
            title: 'Hello Darth Vader',
            user: 'Halit GÜVENİLİR'
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

.title {
    display: flex;
    justify-content: space-between;
    color: red;
    background: #000;
    padding: 10px;
}
</style>