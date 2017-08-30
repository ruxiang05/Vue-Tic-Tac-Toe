<template>
    <div id="app">
        <div id="details">
            <h1>Tic Tac Toe</h1>
        </div>
        <board></board>
    </div>
</template>

<script>
    import Board from "./components/Board.vue";
    export default {
        name: 'app',
        components: {
            'board': Board
        },
        data () {
            return {
                matched: 0,
                wins: {
                    O: 0,
                    X: 0
                }
            }
        }
    }
</script>

<style>
    body {
        background-color: #fff;
        color: #fff;
        font-family: 'Dosis', Helvetica, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        margin: 0px;
    }
    #app {
        margin: 0 auto;
        max-width: 720px;
        color: #34495e;
    }

    h1 {
        text-transform: uppercase;
        font-weight: bold;
        font-size: 3em;
    }

    .restart {
        background-color: #e74c3c;
        color: #fff;
        border: 0px;
        border-bottom-left-radius: 10px;
        border-bottom-right-radius: 10px;
        font-family: 'Dosis', Helvetica, sans-serif;
        font-size: 1.4em;
        font-weight: bold;
        margin: 0px;
        padding: 15px;
        width: 100%;
    }

    .restart:hover {
        background-color: #c0392b;
        cursor: pointer;
    }

    .scoreBoard h2 {
        margin: 0px;
    }

    scoreBoard span {
        float: right;
        font-size: 1.5em;
        font-weight: bold;
        margin-left: 20px;
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
