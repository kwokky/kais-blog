<template>
    <div class="max-width mx-auto px3 ltr" style="height: 100%">
        <div class="content index py4">
            <ArchiveHeader/>
            <nuxt/>
            <Footer/>
        </div>
    </div>
</template>

<script>
import Footer from "~/components/footer"
import ArchiveHeader from "~/components/archive-header"

export default {
    name: "archive",
    components: { ArchiveHeader, Footer }
}
</script>

<style scoped>

</style>
