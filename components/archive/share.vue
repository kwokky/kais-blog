<template>
    <ul>
        <li v-for="platform of platforms">
            <a class="icon" :href="platform.url"><i :class="['fab', platform.iconClass]"></i></a>
        </li>
    </ul>
</template>

<script>
export default {
    name: "archive-share",
    props: {
        archive: {
            type: Object,
            default: () => {
            }
        }
    },
    data () {
        return {
            platforms: [
                {
                    iconClass: 'fa-facebook',
                    url: 'http://www.facebook.com/sharer.php?u=:link'
                }, {
                    iconClass: 'fa-twitter',
                    url: 'http://www.linkedin.com/shareArticle?url=:link&title=:title'
                }, {
                    iconClass: 'fa-linkedin',
                    url: 'https://pinterest.com/pin/create/bookmarklet/?url=:link&is_video=false&description=:title'
                }, {
                    iconClass: 'fa-weibo',
                    url: 'http://service.weibo.com/share/share.php?url=:link&title=:title'
                }
            ]
        }
    },
    mounted () {
        this.platforms = this.platforms.map(platform => {
            return {
                ...platform,
                url: platform.url
                    .replace(':title', this.archive?.title || '')
                    .replace(':link', this.archive?.link || '')
                    .replace(':pic', this.archive?.pic || '')
            }
        })
    }
}
</script>

<style scoped>

</style>
