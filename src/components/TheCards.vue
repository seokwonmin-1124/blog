<template>
    <div v-for="(item, i) in categories" v-show="show[i]" :key="i">
        <div class="box">
            <p>
                <span class="title">{{ item }}</span>
                <span class="tag is-light">programming</span>
                <span class="tag is-light">{{ item }}</span>
            </p>
            <p class="innerP">{{ msg[i] }}</p>
        </div>
    </div>
</template>

<script>
import data from './json/data'

    export default {
        name: 'TheCards',
        data() {
            return {
                categories: data.categories,
                show : data.show,
                msg : data.msg
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>