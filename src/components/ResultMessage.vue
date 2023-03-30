<template>
    <div class="container">

        <h4  class="text-center">{{ message }}</h4>
        
    </div>
</template>

<script>
    import {store} from '../store.js';
    export default {
        name: 'ResultMessage',
        data() {
            return {
                store
            }
        },
        computed: {
            message() {
                return `Ci sono ${this.store.charactersList.length} risultati`;
            }
        }
    }
</script>

<style lang="scss">

</style>