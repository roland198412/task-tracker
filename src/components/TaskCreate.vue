<template>
    <div class="columns">
        <div class="column">
            <input class="input" type="text" placeholder="Enter task name" v-model="task">
        </div>
        <div class="column">
            <button class="button is-link is-pulled-left" @click="addTask">Add Task</button>
        </div>
    </div>
</template>

<script>
export default {
    name: "TaskCreate",
    data() {
        return {
            task: ''
        }
    },
    methods: {
        addTask() {
            this.$emit('add-task', this.task);
            this.task = '';
        }
    },
}
</script>

<style scoped>

</style>