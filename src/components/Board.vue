<template>
    <table class="grid">
        <tr>
            <cell name="1"></cell>
            <cell name="2"></cell>
            <cell name="3"></cell>
        </tr>
        <tr>
            <cell name="4"></cell>
            <cell name="5"></cell>
            <cell name="6"></cell>
        </tr>
        <tr>
            <cell name="7"></cell>
            <cell name="8"></cell>
            <cell name="9"></cell>
        </tr>
    </table>
</template>

<script>
    import Cell from "./Cell.vue";
    export default {
        components: {
            'cell': Cell
        },
        data () {
            return {
                //can be O or X
                activePlayer: 'O',
                //maintains the status of the game: turn or win or draw
                gameStatus: 'turn',
                gameStatusMessage: `O's turn`,
                /* status color is used as background color in the status background
                   it can hold the name of either of the following CSS classes
                   statusTurn(default) is yellow for a turn
                   statusWin is green for a wins
                   statusDraw is purple for a draw */
                gameStatusColor: 'statusTurn',
                //no. of moves played by both players in a single game(max = 9)
                moves: 0,
                //stored the placement of X and O in cells by their cell number
                cells: {
                    1: '', 2: '', 3: '',
                    4: '', 5: '', 6: '',
                    7: '', 8: '', 9: ''
                },
                //contains all (8) possible winning conditions
                winConditions: [
                    [1,2,3],[4,5,6],[7,8,9], //rows
                    [1,4,7],[2,5,8],[3,6,9], //columns
                    [1,5,9],[3,5,7] //diagonals
                ]
            }
        }
    }
</script>

<style>

</style>
