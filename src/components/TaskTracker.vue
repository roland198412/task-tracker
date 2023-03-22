<template>
    <section>
        <task-create @add-task="addTask"></task-create>
        <task-list :tasks="tasks"></task-list>
    </section>
</template>

<script>
import TaskList from '@/components/TaskList.vue';
import TaskCreate from '@/components/TaskCreate.vue';

export default {
    name: "TaskTracker",
    components: {
        TaskCreate,
        TaskList,
    },
    data() {
        return {
            tasks: []
        }
    },
    methods: {
        addTask(task) {
            this.tasks.push(task)
        }
    },
}
</script>

<style scoped>

</style>