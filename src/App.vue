<template>
    <div id="app">
        <h4 class="bg-primary text-white text-center p-2">
            TO DO List
        </h4>
        <div class="container-fluid p-4">
            <div class="row">
                <div class="col font-weight-bold">Task</div>
                <div class="col-2 font-weight-bold">Done</div>
            </div>
            <div class="row" v-for="t in tasks" v-bind:key="t.action">
                <div class="col">{{t.action}}</div>
                <div class="col-2">
                    <input type="checkbox" v-model="t.done" class="form-check-input" title="是否完成">
                    {{t.done}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import HelloWorld from './components/HelloWorld.vue'

    export default {
        name: 'app',
        components: {
            HelloWorld
        },
        data() {
            return {
                name: "Adam",
                tasks: [{action: "abc", done: false},
                    {action: "zsc", done: false},
                    {action: "liata", done: true},
                    {action: "zhang", done: false}]
            }
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
