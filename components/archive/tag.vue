<template>
    <div class="article-tag">
        <i class="fas fa-tag" style="margin-left: 8px"></i>
        <nuxt-link class="tag-link" :to="{name: 'tag-tag', params: {tag: 'markdown'}}">markdown</nuxt-link>
        <nuxt-link class="tag-link" :to="{name: 'tag-tag', params: {tag: 'php'}}">php</nuxt-link>
    </div>
</template>

<script>
export default {
    name: "archive-tag",
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
