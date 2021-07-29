<template>
    <article class="post">
        <div class="content">
            <div id="categories">
                <div class="category-list-title">
                </div>
                <div class="category-list">
                    <ul class="category-list">
                        <li class="category-list-item">
                            <nuxt-link class="category-list-link" :to="{name: 'categories-id', params: {id: 1}}">随笔
                            </nuxt-link>
                            <span class="category-list-count">1</span>
                        </li>
                    </ul>
                    <ul class="category-list">
                        <li class="category-list-item">
                            <nuxt-link class="category-list-link" :to="{name: 'categories-id', params: {id: 2}}">感想
                            </nuxt-link>
                            <span class="category-list-count">20</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </article>
</template>

<script>
export default {
    name: "categories"
}
</script>

<style scoped>

</style>
