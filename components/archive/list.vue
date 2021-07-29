<template>
    <div id="archive">
        <ul class="post-list">
            <li class="post-year"><h2>2021</h2></li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>

            <li class="post-year"><h2>2020</h2></li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>

            <li class="post-year"><h2>2019</h2></li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>
            <li class="post-item">
                <div class="meta">
                    <time datetime="2021-10-10T16:49:32.000Z">2021-10-10</time>
                </div>
                <span>
                    <nuxt-link :to="{name: 'archive-id', params: {id: 1}}">测试文章</nuxt-link>
                </span>
            </li>
        </ul>

        <Pagination :total="100" :size="9" :current="parseInt(current)"/>
    </div>

</template>

<script>
import Pagination from "~/components/pagination"

export default {
    name: "archive-list",
    components: { Pagination },
    data () {
        return {
            current: this.$route.query.page || 1
        }
    },
    watch: {
        '$route.query.page' (value) {
            this.current = value
        }
    }
}
</script>

<style scoped>

</style>
