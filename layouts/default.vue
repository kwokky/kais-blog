<template>
    <div class="max-width mx-auto px3 ltr" style="height: 100%">
        <div class="content index py4">
            <Header/>
            <nuxt/>
            <Footer/>
        </div>
    </div>
</template>

<script>
import Header from "~/components/header"
import Footer from "~/components/footer"

export default {
    name: "default",
    components: { Header, Footer }
}
</script>

<style scoped>

</style>
