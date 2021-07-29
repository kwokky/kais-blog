<template>
    <article class="post">
        <header>
            <h1 class="posttitle">Categories</h1>
            <div class="meta">
                <span class="author"><span>Kais</span></span>

                <ArchiveDate/>
                <ArchiveCategory/>
                <ArchiveTag/>
            </div>
        </header>
        <div class="content">
            {{ 'sdf'.repeat(1000) }}
        </div>
    </article>
</template>

<script>
import ArchiveTag from "~/components/archive/tag"
import ArchiveCategory from "~/components/archive/category"
import ArchiveDate from "~/components/archive/date"

export default {
    name: "archive-id",
    components: { ArchiveDate, ArchiveCategory, ArchiveTag },
    layout: 'archive'
}
</script>

<style scoped>

</style>
