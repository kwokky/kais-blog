<template>
    <header id="header">
        <a href="/">
            <div id="logo"></div>
            <div id="title">
                <h1>Kais</h1>
            </div>
        </a>
        <div id="nav">
            <Navigation/>
        </div>
    </header>
</template>

<script>
import Navigation from "~/components/navigation"

export default {
    name: "kais-header",
    components: { Navigation }
}
</script>
