<template>
    <div>
        <QuestionListComponent></QuestionListComponent>
    </div>
</template>

<script>
    // @ is an alias to /src
    import QuestionListComponent from '@/components/QuestionListComponent.vue'
    export default {
        name: "Questions",
        components: {
            QuestionListComponent
        }
    }
</script>

<style scoped>

</style>