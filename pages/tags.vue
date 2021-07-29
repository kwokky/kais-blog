<template>
    <article class="post">
        <div class="content">
            <div id="categories">
                <div class="category-list-title">
                </div>
                <div class="category-list">
                    <ul class="category-list">
                        <li class="category-list-item">
                            <nuxt-link class="category-list-link" :to="{name: 'tag-tag', params: {tag: 'docker'}}">#docker
                            </nuxt-link>
                            <span class="category-list-count">1</span>
                        </li>
                    </ul>
                    <ul class="category-list">
                        <li class="category-list-item">
                            <nuxt-link class="category-list-link" :to="{name: 'tag-tag', params: {tag: 'linux'}}">#linux
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
name: "tags"
}
</script>

<style scoped>

</style>
