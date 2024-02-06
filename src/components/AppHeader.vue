<script>
export default {
    name: 'AppHeader',
    data: () => ({
        typeInput: ''
    }),
    props: {
        types: Array
    },
    emits: ['select-type']
}
</script>

<template>
    <div class="">
        <div class=" container d-flex pt-5 justify-content-between">
            <h1 class="text-white text-center">Pokedex</h1>
            <select @click="$emit('select-type', typeInput)" v-model="typeInput" name="types" id="select-type">
                <option selected disabled value="">Select a type</option>
                <option v-for="(type, i) in types" :key="i" :value="type">{{ type }}</option>
            </select>
        </div>
    </div>
</template>


<style lang="scss" scoped>
div {
    background-color: #B71B1B;
}
</style>