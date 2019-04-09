<template>
    <div>
        <input type="text" v-model="task">
        <button @click="callParent">Adicionar tarefa</button>
        <h2>{{ title }}</h2>

        <ul>
            <li v-for="(item, index) in items" :key="index">
                {{item}}
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    props : ['items', 'title'],
    data() {
        return {
            task: ''
        }
    }, methods: {
        callParent () {
            this.$emit('calledParent', this.task)
        }
    }
}
</script>

<style scoped>

</style>
