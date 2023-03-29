<template>

    <div class="container my-5">
        <div class="row ">
            <div class="col-auto">
                <input type="text" class="form-control" placeholder="Search character" v-model="store.search" >
            </div>
            
        </div>
    </div>

</template>


<script>
    import { store } from '../store.js';
    export default {
        name: 'AppSearch',
        data() {
            return {
                store
            }
        }
    }
</script>


<style>
</style>