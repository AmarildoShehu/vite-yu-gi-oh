<script>
export default {
    name: 'Pokemon Card',
    props: {
        pokemon: Object
    }
}
</script>

<template>
    <div class="card p-3 text-center">
        <div class="border ">
            <div class="card-img-top ">
                <img :src="pokemon.imageUrl" :alt="pokemon.name" class="img-fluid rounded-circle">
            </div>
            <div class="body-card">
                <h5 class="card-title"> <span>{{ pokemon.number }}</span>. {{ pokemon.name }}</h5>
                <p class="">{{ pokemon.type1 }} {{ pokemon.type2 }}</p>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.body-card {
    height: 100px;
}

img {
    padding: 5px;
    margin-top: 1rem;
    margin-bottom: 1rem;
    border: 2px solid;
    width: 120px;
    height: 100px;
}
</style>