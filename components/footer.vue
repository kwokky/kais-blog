<template>
    <footer id="footer">
        <div class="footer-left">
            Copyright © 2021 Kais
        </div>
        <div class="footer-right">
            <nav>
                <Navigation/>
            </nav>
        </div>
    </footer>
</template>

<script>
import Navigation from "~/components/navigation"

export default {
    name: "bolg-footer",
    components: { Navigation }
}
</script>

<style scoped>

</style>
