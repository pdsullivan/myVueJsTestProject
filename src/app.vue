<template>
    <div class="container">
        <input class="form-control" type="text" v-model="text" />
        <div class="primary">
            Hello {{ text }}!
        </div>
        <br>
        <div class="" v-for="todo in todos" >
            <button class="btn btn-primary" v-on:click="reverseMessage(todo)">
                {{ todo.text }}
            </button>
            <br><br>
        </div>
    </div>

</template>

<script>
    export default {
        replace: false,
        data() {
            return {
                text: 'vue',
                todos: [
                    { text: 'Learn JavaScript' },
                    { text: 'Learn Vue' },
                    { text: 'Build something awesome' }
                ]
            }
        },
        methods: {
            reverseMessage: function (todo) {
                this.text = todo.text // this.text.split('').reverse().join('')
            }
        }
    }
</script>
