<template>
    <div ref="header-post" id="header-post">
        <a id="menu-icon" href="javascript:" @click="expand = !expand" :class="{active: expand}"><i
            class="fas fa-bars fa-lg"></i></a>
        <a id="menu-icon-tablet" :class="{active: expand}"><i class="fas fa-bars fa-lg"></i></a>
        <a id="top-icon-tablet" href="#"><i class="fas fa-chevron-up fa-lg"></i></a>

        <span id="menu" :style="{visibility: expand ? 'visible' : 'hidden'}">
            <span id="nav" v-show="showNav"><Navigation/></span>
            <br/>
            <div id="actions">
                <ul>
                    <li>
                        <nuxt-link class="icon" :to="{name: 'archive-id', params: {id: 1}}">
                            <i class="fas fa-chevron-left" @mouseover="$set(textCtl, 'prev', true)"
                               @mouseout="$set(textCtl, 'prev', false)"></i>
                        </nuxt-link>
                    </li>
                    <li>
                        <nuxt-link class="icon" :to="{name: 'archive-id', params: {id: 2}}">
                            <i class="fas fa-chevron-right" @mouseover="$set(textCtl, 'next', true)"
                               @mouseout="$set(textCtl, 'next', false)"></i>
                        </nuxt-link>
                    </li>
                    <li>
                        <a class="icon" href="javascript:" @click="goTop">
                            <i class="fas fa-chevron-up" @mouseover="$set(textCtl, 'top', true)"
                               @mouseout="$set(textCtl, 'top', false)"></i></a>
                    </li>
                    <li>
                        <a class="icon" href="#">
                            <i class="fas fa-share-alt" @mouseover="$set(textCtl, 'share', true)"
                               @mouseout="$set(textCtl, 'share', false)" @click="share = !share"></i>
                        </a>
                    </li>
                </ul>

                <span class="info" v-show="textCtl.prev">Previous post</span>
                <span class="info" v-show="textCtl.next">Next post</span>
                <span class="info" v-show="textCtl.top">Back to top</span>
                <span class="info" v-show="textCtl.share">share post</span>
            </div>
            <br/>

            <div id="share" v-show="share">
                <ArchiveShare/>
            </div>

            <div id="toc">
                <ArchiveToc/>
            </div>
        </span>
    </div>
</template>

<script>
import ArchiveShare from "~/components/archive/share"
import ArchiveToc from "~/components/archive/toc"
import Navigation from "~/components/navigation"

export default {
    name: "archive-header",
    components: { Navigation, ArchiveToc, ArchiveShare },
    data () {
        return {
            expand: true,
            textCtl: { prev: false, next: false, top: false, share: false },
            showNav: true,
            share: false
        }
    },
    mounted () {
        window.addEventListener('scroll', this.scrollHandle)
        this.$on('hook:beforeDestroy', () => window.removeEventListener('scroll', this.scrollHandle))
    },
    methods: {
        goTop () {
            const scroll = document.documentElement.scrollTop || document.body.scrollTop
            if (scroll > 0) {
                window.requestAnimationFrame(this.goTop)
                window.scrollTo(0, scroll - (scroll / 5))
            }
        },
        scrollHandle () {
            const scroll = document.documentElement.scrollTop || document.body.scrollTop
            this.showNav = top < 30
        }
    }
}
</script>

<style scoped>

</style>
