<template>
    <div class="article-category">
        <i class="fas fa-archive" style="margin-left: 8px"></i>
        <nuxt-link class="category-link" :to="{name: 'category-id', params: {id: 1}}">随笔</nuxt-link>
    </div>
</template>

<script>
export default {
    name: "archive-category",
    props: {
        archive: {
            type: Object,
            default: () => {
            }
        }
    }
}
</script>

<style scoped>

</style>
