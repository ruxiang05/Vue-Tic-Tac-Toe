<template>
    <td class="cell">
        {{ mark }}
    </td>
</template>

<script>
    export default {
        props: ['name'],
        data () {
            return {
                //enables the player to place a mark
                frozen: false,
                //holds either X or O to be displayed in td
                mark: ''
            }
        }
    }
</script>

<style>

</style>
