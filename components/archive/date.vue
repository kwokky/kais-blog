<template>
    <div class="postdate">
        <time datetime="2016-11-01T08:35:18.000Z">2016-11-01</time>
    </div>
</template>

<script>
export default {
    name: "archive-date",
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
