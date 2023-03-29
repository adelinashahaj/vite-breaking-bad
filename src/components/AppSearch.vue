<template>

    <div class="container my-5">
        <div class="row ">
            <div class="col-auto">
                <select id="race" name="race" class="btn">
            <option value="Dragon">Dragon</option>
            <option value="Alien">Alien</option>
        </select>
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


<style lang="scss" scoped>
.btn{
    background-color: white;
}

</style>