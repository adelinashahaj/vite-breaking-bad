<template>

    <div class="container my-5">
        <div class="row ">
            <div class="col-auto">
        <select  v-model="store.select" @change="$emit('doSelect')">
            <option value="">All</option>
            <option value="Noble Knight">Noble Knight</option>
            <option value="Alien">Alien</option>
            <option value="Melodious">Melodious</option>
            <option value="Archfiend">Archfiend</option>
            <option value="Elemental HERO">Elemental HERO</option>
            <option value="Umi">Umi</option>
            <option value="ABC">ABC</option>
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

.col-auto {
    padding: 29px 0px;
}

</style>