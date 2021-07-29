<template>
    <div class="pagination" v-if="total > 1">

        <nuxt-link :to="{name: 'archives', query: {page: current-1}}" v-if="current > 1"><i
            class="fas fa-angle-left"></i>
        </nuxt-link>

        <span class="page-number">第 {{ current }} 页，共 {{ last }} 页</span>

        <nuxt-link :to="{name: 'archives', query: {page: current+1}}" v-if="current !== last">
            <i class="fas fa-angle-right"></i>
        </nuxt-link>
    </div>
</template>

<script>
export default {
    name: "pagination",
    props: {
        total: {
            type: Number,
        },
        size: {
            type: Number,
            default: 20
        },
        current: {
            type: Number,
            default: 1
        }
    },
    computed: {
        last () {
            return Math.ceil(this.total / this.size)
        }
    }
}
</script>

<style scoped>

</style>
