<template>
    <div>
        lorem ipsum
        {{ products }}
    </div>
</template>

<script>
    export default {
        computed: {
            products() {
                return this.$store.getters.getProductId(this.$route.params.id)
            }
        }
    }
</script>

<style scoped>

</style>