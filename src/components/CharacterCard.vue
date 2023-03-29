<template>
<div class="character text-center">
        <img class='img-fluid ' :src="image" :alt="name"/>
        <h3>{{ name }}</h3>
        <h5>{{ race }}</h5>
        
    </div>
</template>

<script>
export default{
    name: 'CharacterCard',
      props: {
            image: String,
            name: String,
            race: String,
            
        }
}

</script>

<style>

</style>