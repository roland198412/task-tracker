<template>
    <div class="card">
        <div class="card-content">
            <div class="content">
               <ul v-if="hasTasks">
                   <li v-for="(task, index) in tasks" :key="index" class="has-text-left">
                       {{ task }}
                   </li>
               </ul>
                <div v-else>
                    No tasks available
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "TaskList",
    props: {
        tasks: {
            type: Array,
            required: true
        },
    },
    computed: {
        hasTasks() {
            return this.tasks.length > 0;
        }
    },
}
</script>

<style scoped>

</style>