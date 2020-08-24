<template>
    <div class="container">
        <table>
            <thead>
            <tr>
                <th>Id</th>
                <th>Name</th>
                <th>Age</th>
                <th>Phone</th>
            </tr>
            </thead>
            <tr v-bind:key="todo.id" v-for="todo in userData">
                <td> {{ todo.id }} </td>
                <td> {{ todo.name }} </td>
                <td> {{ todo.age }} </td>
                <td> {{ todo.phone }} </td>
            </tr>
        </table>
    </div>
</template>

<script>
    export default {
        name: 'Table load',
        data() {
            return {
                userData: []
            }
        },
        props: {},
        methods: {
            loadData: function () {
                fetch("data.json")
                    .then(response => response.json())
                    .then(data => (this.userData = data));
            }
        },
        mounted() {
            this.loadData();
        },
    }
</script>

<style scoped>
    h3 {
        margin: 40px 0 0;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
</style>
