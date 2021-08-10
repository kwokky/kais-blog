<template>
    <section id="search">
        <form>
            <input type="text" class="search-input" id="search-input" placeholder="Show your keyword">
        </form>
        <div id="search-result">
            <ul class="search-result-list">
                <li>
                    <a href="/hexo-theme-cactus/default/hello-world/" class="search-result-title">hello world</a>
                    <p class="search-result">Welcome to <em class="search-keyword">hello</em>! This is your very first
                        post. Check documentation for more
                        info. If you get any pro...
                    </p>
                </li>
            </ul>
        </div>
        <p class="search-no-result">抱歉，没有搜索到结果。</p>
    </section>
</template>

<script>
export default {
    name: "search"
}
</script>

<style scoped>

</style>
