<template>
    <ArchiveList/>
</template>

<script>
import ArchiveList from "~/components/archive/list"

export default {
    name: "tag_tag",
    components: { ArchiveList },
    async asyncData ({ params }) {
        return {
            tag: params.tag
        }
    }
}
</script>

<style scoped>

</style>
