<template>
    <div>
        {{title}}

        <li v-for="(item, index) in items" :key="index">
            {{item}}
        </li>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            required: true, //obrigatorio
            type: String, //tipo de dado
            default: '' //Valor default
        },
        items: {
            required: true,
            type: Array,
            default: ''
        }
    },
    data() {
        return {

        }
    }
}
</script>

<style scoped>

</style>

